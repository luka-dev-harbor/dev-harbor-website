<script>
    import { onMount } from 'svelte';

    let headerTheme = $state('dark'); // 'dark' = dark text/logo, 'light' = light text/logo

    function closeMenu() {
        const navbar = document.getElementById('main-navbar');
        if (navbar?.classList.contains('show')) {
            navbar.classList.remove('show');
        }
    }

    onMount(() => {
        const sections = document.querySelectorAll('[data-header-theme]');
        if (sections.length === 0) return;

        const headerHeight = 80; // Fixed header height from CSS

        // Find which section is behind the header
        function updateTheme() {
            const sectionsArray = Array.from(sections);
            for (let i = sectionsArray.length - 1; i >= 0; i--) {
                const section = sectionsArray[i];
                const rect = section.getBoundingClientRect();
                // If section's top is above the header bottom, it's behind the header
                if (rect.top <= headerHeight) {
                    headerTheme = section.dataset.headerTheme || 'dark';
                    return;
                }
            }
            // Default to first section's theme
            headerTheme = sectionsArray[0]?.dataset.headerTheme || 'dark';
        }

        const observerOptions = {
            root: null,
            rootMargin: `-${headerHeight}px 0px -${window.innerHeight - headerHeight - 1}px 0px`,
            threshold: 0
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach((entry) => {
                if (entry.isIntersecting) {
                    headerTheme = entry.target.dataset.headerTheme || 'dark';
                } else {
                    // When element exits, recalculate which section is behind header
                    updateTheme();
                }
            });
        }, observerOptions);

        sections.forEach((section) => observer.observe(section));

        return () => observer.disconnect();
    });
</script>

<nav class="navbar fixed-top navbar-expand-md" class:theme-light={headerTheme === 'light'} class:theme-dark={headerTheme === 'dark'}>
    <div class="container-fluid">
        <a class="navbar-brand" href="/">
            <img src="/logo.svg" class="logo" alt="Dev Harbor">
        </a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#main-navbar" aria-controls="main-navbar" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="main-navbar">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                <li class="nav-item">
                    <a class="nav-link active" aria-current="page" href="/" onclick={closeMenu}>Home</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/#pricing" onclick={closeMenu}>Pricing</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/blog" onclick={closeMenu}>Blog</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/#contact" onclick={closeMenu}>Contact</a>
                </li>
            </ul>
        </div>
    </div>
</nav>

<style>
    .navbar {
        height: 80px;
        padding: 20px;
        background-color: rgba(255, 255, 255, 0.8);
        -webkit-backdrop-filter: blur(10px);
        backdrop-filter: blur(10px);
        transition: background-color 0.2s ease;

        .navbar-brand {
            z-index: 5;
        }

        .logo {
            height: 40px;
            width: auto;
            filter: brightness(0);
            transition: filter 0.2s ease;
        }

        .navbar-toggler {
            display: flex;
            justify-content: center;
            align-items: center;
            border: none;

            &:focus {
                box-shadow: none !important;
            }

            .navbar-toggler-icon {
                width: 18px;
                height: 18px;
                background-repeat: no-repeat;
                display: inline-block;
                background-size: 18px;
                transition: background-image 0.3s ease;
            }
        }
    }

    /* DARK THEME - dark logo/text on light backgrounds */
    .navbar.theme-dark {
        background-color: rgba(255, 255, 255, 0.8);
        -webkit-backdrop-filter: blur(10px);
        backdrop-filter: blur(10px);

        .logo {
            filter: brightness(0);
        }

        .navbar-toggler-icon {
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='24' height='24' fill='none' stroke-width='2.5'%3E%3Cpath stroke='%23000' stroke-linecap='round' stroke-linejoin='round' d='M3 6h18M3 12h18M3 18h18'/%3E%3C/svg%3E");
        }

        .nav-link {
            color: #000 !important;
            opacity: 0.6;

            &:hover {
                opacity: 1;
            }
        }
    }

    /* LIGHT THEME - light logo/text on dark backgrounds */
    .navbar.theme-light {
        background-color: rgba(0, 0, 0, 0.3);
        -webkit-backdrop-filter: blur(10px);
        backdrop-filter: blur(10px);

        .logo {
            filter: brightness(0) invert(1);
        }

        .navbar-toggler-icon {
            background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='24' height='24' fill='none' stroke-width='2.5'%3E%3Cpath stroke='%23fff' stroke-linecap='round' stroke-linejoin='round' d='M3 6h18M3 12h18M3 18h18'/%3E%3C/svg%3E");
        }

        .nav-link {
            color: #fff !important;
            opacity: 0.7;

            &:hover {
                opacity: 1;
            }
        }
    }

    /* Desktop: center nav links */
    @media (min-width: 768px) {
        .navbar {
            .navbar-toggler {
                display: none !important;
            }

            .navbar-collapse {
                .navbar-nav {
                    width: calc(100% + 150px);
                    margin-left: -150px;
                    justify-content: center;

                    .nav-item a {
                        padding-left: 1rem;
                        padding-right: 1rem;
                    }
                }
            }
        }
    }

    /* Mobile: dropdown menu styles */
    @media (max-width: 767px) {
        .navbar {
            .navbar-collapse {
                background-color: #fff;
                box-shadow: rgba(0, 0, 0, 0.1) 0px 20px 25px -5px, rgba(0, 0, 0, 0.04) 0px 10px 10px -5px;
                padding: 1rem;
                margin-top: 1rem;
                border-radius: 8px;

                .navbar-nav {
                    .nav-item {
                        padding: 0.5rem 1rem;
                        text-align: center;

                        &:hover {
                            background-color: #f9f9f9;
                        }

                        a {
                            color: #000 !important;
                            opacity: 1 !important;
                        }
                    }
                }
            }
        }
    }
</style>
