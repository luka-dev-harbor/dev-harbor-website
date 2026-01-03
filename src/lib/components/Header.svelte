<script>
</script>

<nav class="navbar fixed-top navbar-expand-md">
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
                    <a class="nav-link active" aria-current="page" href="/">Home</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/#pricing">Pricing</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/blog">Blog</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="/#contact">Contact</a>
                </li>
            </ul>
        </div>
    </div>
</nav>

<style>
    .navbar {
        height: 80px;
        padding: 20px;

        .navbar-brand {
            z-index: 5;
        }

        .logo {
            height: 40px;
            width: auto;
        }
        .navbar-toggler {
            display: flex;
            justify-content: center;
            align-items: center;

            &:focus {
                box-shadow: none !important;
            }
            .navbar-toggler-icon {
                background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='24' height='24' fill='none' stroke-width='3' color='%23000'%3E%3Cpath stroke='%23000' stroke-linecap='round' stroke-linejoin='round' d='M3 5h18M3 12h18M3 19h18'/%3E%3C/svg%3E");
                width: 16px;
                height: 16px;
                background-repeat: no-repeat;
                display: inline-block;
                background-size: 16px;
            }
        }
    }

    /* LARGE MENU STYLE (on larger screens) */
    @media (min-width: 768px) {
        .navbar {
            background-color: rgba(0, 0, 0, 0.2);
            -webkit-backdrop-filter: blur(5px);
            backdrop-filter: blur(5px);
            mix-blend-mode: difference;

            .navbar-toggler {
                display: none !important;
            }
            .navbar-collapse {

                .navbar-nav {
                    width: calc(100% + 150px);
                    margin-left: -150px;
                    justify-content: center;

                    .nav-item {
                        a {
                            color: #fff !important;
                            opacity: 0.6;
                            padding-left: 1rem;
                            padding-right: 1rem;

                            &:hover {
                                opacity: 1;
                            }
                        }
                    }
                }
            }
        }
    }

    /* COLLAPSED MENU STYLE (on smaller screens) */
    @media (max-width: 767px) {
        .navbar {
            .navbar-collapse {
                background-color: #fff;
                box-shadow: rgba(0, 0, 0, 0.1) 0px 20px 25px -5px, rgba(0, 0, 0, 0.04) 0px 10px 10px -5px;
                padding: 1rem;
                margin-top: 1rem;

                .navbar-nav {
                    .nav-item {
                        padding: 0.5rem 1rem;
                        text-align: center;

                        &:hover {
                            background-color: #f9f9f9;
                        }
                        a {
                            color: #000 !important;
                        }
                    }
                }
            }
        }
    }
</style>