<script>
    import Badge from "$lib/components/Badge.svelte";
    import WhiteCard from "$lib/components/WhiteCard.svelte";
    import HeroGradientWave from "$lib/components/HeroGradientWave.svelte";
    import CleanLineTransition from "$lib/components/CleanLineTransition.svelte";
    import CurvedTransition from "$lib/components/CurvedTransition.svelte";

    let formStatus = $state('idle'); // 'idle' | 'submitting' | 'success' | 'error'

    async function handleSubmit(event) {
        event.preventDefault();
        formStatus = 'submitting';

        const form = event.target;
        const formData = new FormData(form);
        const data = Object.fromEntries(formData.entries());

        try {
            const response = await fetch('https://submit-form.com/oJlrklgSo', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                    'Accept': 'application/json'
                },
                body: JSON.stringify(data)
            });

            if (response.ok) {
                formStatus = 'success';
                form.reset();
            } else {
                formStatus = 'error';
            }
        } catch (error) {
            formStatus = 'error';
        }
    }
</script>

<svelte:head>
    <title>Dev Harbor - Custom Web Development</title>
    <meta name="description" content="Dev Harbor builds custom web applications, mobile apps, and enterprise software. Belgrade-based development team specializing in modern, scalable solutions." />

    <!-- Open Graph -->
    <meta property="og:type" content="website" />
    <meta property="og:title" content="Dev Harbor - Custom Web Development" />
    <meta property="og:description" content="Dev Harbor builds custom web applications, mobile apps, and enterprise software. Belgrade-based development team specializing in modern, scalable solutions." />
    <meta property="og:image" content="https://dev-harbor.com/og-image.png" />
    <meta property="og:url" content="https://dev-harbor.com/" />
    <meta property="og:site_name" content="Dev Harbor" />

    <!-- Twitter Card -->
    <meta name="twitter:card" content="summary_large_image" />
    <meta name="twitter:title" content="Dev Harbor - Custom Web Development" />
    <meta name="twitter:description" content="Dev Harbor builds custom web applications, mobile apps, and enterprise software." />
    <meta name="twitter:image" content="https://dev-harbor.com/og-image.png" />

    <link rel="canonical" href="https://dev-harbor.com/" />

    <!-- JSON-LD Structured Data -->
    {@html `<script type="application/ld+json">
    {
        "@context": "https://schema.org",
        "@type": "Organization",
        "name": "Dev Harbor",
        "legalName": "Dev Harbor d.o.o.",
        "url": "https://dev-harbor.com",
        "logo": "https://dev-harbor.com/logo.svg",
        "description": "Custom software development company specializing in web applications, mobile apps, and enterprise solutions.",
        "address": {
            "@type": "PostalAddress",
            "addressLocality": "Belgrade",
            "addressCountry": "RS"
        },
        "founder": {
            "@type": "Person",
            "name": "Luka Stanisic"
        },
        "contactPoint": {
            "@type": "ContactPoint",
            "email": "office@dev-harbor.com",
            "contactType": "sales"
        },
        "areaServed": "Worldwide",
        "serviceType": ["Web Development", "Mobile App Development", "Custom Software Development", "IT Consulting"]
    }
    </script>`}
</svelte:head>

<div class="page-content mt-5">

    <!------------------------->
    <!-- HERO HEADER + IMAGE -->
    <!------------------------->
    <div class="hero-section" data-header-theme="dark">
        <div class="page-title">
            <h1>Software,</h1>
            <h1>built as it should be.</h1>
        </div>

        <p class="hero-subtitle">From a team where every detail matters — since 2020.</p>

        <div class="text-center mt-4">
            <a href="/#contact" class="btn btn-primary">Build with us</a>
        </div>

        <img src="/hero-image.svg" class="hero-image mt-5" alt="Hero">

        <!-- WAVE -->
        <div data-header-theme="light">
            <HeroGradientWave></HeroGradientWave>
        </div>
    </div>

    <!--------------->
    <!-- BLACK BOX -->
    <!--------------->
    <div class="black-box" data-header-theme="light">
        <div class="content-wrapper">

            <!------------->
            <!-- CLIENTS -->
            <!------------->
            <div class="clients-section">
                <Badge text={'TRUSTED BY COMPANIES WORLDWIDE'}></Badge>
                <img src="/clients.svg" class="clients-logos" alt="Clients">
            </div>

            <!-------------------->
            <!-- TRACK RECORD -->
            <!-------------------->
            <div class="values-section">
                <Badge text={'TRACK RECORD'}></Badge>
                <h1>Where we've proven ourselves</h1>
            </div>
            <div class="values-cards">
                <WhiteCard iconClass="code" isLeft={true} headerText="Challenging projects" bodyText="We take on the work that makes other teams nervous. And we deliver."></WhiteCard>
                <WhiteCard iconClass="infinity" isLeft={false} headerText="Long-term partnerships" bodyText="Our longest client relationship is 5+ years and counting. We stick around."></WhiteCard>
                <WhiteCard iconClass="rocket" isLeft={true} headerText="Startups" bodyText="We've helped founders go from idea to launch. We know what matters when runway is short and stakes are high."></WhiteCard>
                <WhiteCard iconClass="community" isLeft={false} headerText="Team integration" bodyText="We've embedded with teams across Europe. Direct communication, no layers — just delivery."></WhiteCard>
            </div>

            <!-------------------->
            <!-- HOW WE WORK -->
            <!-------------------->
            <div class="who-section">
                <Badge text={'HOW WE WORK'}></Badge>
                <h1>What to expect</h1>
                <div class="who-grid who-grid--stacked">
                    <div class="who-card">
                        <h3>Clear scope</h3>
                        <p>We define exactly what we're building before we start. Defined deliverables, realistic timelines.</p>
                    </div>
                    <div class="who-card">
                        <h3>Direct access</h3>
                        <p>Your project has one clear point of contact — directly connected to the team building it.</p>
                    </div>
                    <div class="who-card">
                        <h3>Consistent updates</h3>
                        <p>Weekly progress, clear timelines. You always know where things stand.</p>
                    </div>
                    <div class="who-card">
                        <h3>Honest feedback</h3>
                        <p>We speak up when something doesn't make sense. We're partners, not people-pleasers.</p>
                    </div>
                </div>
            </div>

        </div>
    </div>

    <!-- CLEAN LINE TRANSITION -->
    <div data-header-theme="dark">
        <CleanLineTransition></CleanLineTransition>
    </div>

    <!-------------------------------->
    <!-- CUSTOM SOFTWARE DEVELOPMENT -->
    <!-------------------------------->
    <div class="white-section mt-5" data-header-theme="dark">
        <div class="content-wrapper">
            <div class="row align-items-center">
                <div class="col-12 col-lg-6 order-2 order-lg-1">
                    <div class="text-start">
                        <Badge text={'BUILT FROM SCRATCH'}></Badge>
                    </div>
                    <h2>Custom software development</h2>
                    <p>Every business works differently, and your software should reflect that. We handle the full development process - from understanding your needs to building and deploying a solution that fits.</p>
                    <p>Web applications, mobile apps, enterprise systems - we build what you actually need, nothing more, nothing less.</p>
                </div>
                <div class="col-12 col-lg-6 order-1 order-lg-2">
                    <img src="/custom-software.svg" alt="Custom Software Development">
                </div>
            </div>
        </div>
    </div>

    <!---------------------->
    <!-- FULL SCOPE OF WORK -->
    <!---------------------->
    <div class="white-section" data-header-theme="dark">
        <div class="content-wrapper">
            <div class="row align-items-center">
                <div class="col-12 col-lg-6">
                    <img src="/full-scope.svg" alt="Full Scope of Work">
                </div>
                <div class="col-12 col-lg-6">
                    <div class="text-start">
                        <Badge text={'END-TO-END'}></Badge>
                    </div>
                    <h2>Full scope of work</h2>
                    <p>We handle every phase of your project lifecycle - from initial consultation and planning to design, development, testing, and ongoing maintenance.</p>
                    <p>Working with a single team from start to finish means better coordination, clearer communication, and a product that holds together.</p>
                </div>
            </div>
        </div>
    </div>

    <!--------------------------->
    <!-- MODERNIZING LEGACY TECH -->
    <!--------------------------->
    <div class="white-section" data-header-theme="dark">
        <div class="content-wrapper">
            <div class="row align-items-center">
                <div class="col-12 col-lg-6 order-2 order-lg-1">
                    <div class="text-start">
                        <Badge text={'FUTURE'}></Badge>
                    </div>
                    <h2>Modernizing legacy tech</h2>
                    <p>Outdated systems slow you down and become harder to maintain over time. We help you migrate to modern technologies without disrupting your day-to-day operations.</p>
                    <p>Your existing business logic and data stay intact - you get better performance, improved security, and a codebase that's easier to work with going forward.</p>
                </div>
                <div class="col-12 col-lg-6 order-1 order-lg-2">
                    <img src="/modernize.svg" alt="Modernizing Legacy Tech">
                </div>
            </div>
        </div>
    </div>

    <!-- CURVED TRANSITION -->
    <div data-header-theme="light">
        <CurvedTransition></CurvedTransition>
    </div>

    <!------------->
    <!-- EXPERTISE -->
    <!------------->
    <div class="black-box pb-3" data-header-theme="light">
        <div class="content-wrapper">
            <Badge text={'SERVICES'}></Badge>
            <h1>Expertise</h1>
            <div class="expertise-grid">
                <div class="expertise-card">
                    <div class="icon-square">
                        <span class="icon code"></span>
                    </div>
                    <h3>Web Apps</h3>
                    <p>From simple internal tools to complex platforms, we build web applications that fit your business.</p>
                </div>
                <div class="expertise-card">
                    <div class="icon-square">
                        <span class="icon dashboard-dots"></span>
                    </div>
                    <h3>Native Mobile</h3>
                    <p>iOS and Android apps built for performance, usability, and seamless integration with your systems.</p>
                </div>
                <div class="expertise-card">
                    <div class="icon-square">
                        <span class="icon iris-scan"></span>
                    </div>
                    <h3>Consulting</h3>
                    <p>Honest, practical advice to help you plan, prioritize, and avoid common pitfalls.</p>
                </div>
            </div>

            <!--------------->
            <!-- TECHNOLOGIES -->
            <!--------------->
            <div class="technologies-section">
                <!-- Desktop: 8 + 7 -->
                <div class="tech-row desktop-only">
                    <img src="/logo-angular.svg" class="tech-logo logo-tall" alt="Angular">
                    <img src="/logo-svelte.svg" class="tech-logo" alt="Svelte">
                    <img src="/logo-js.svg" class="tech-logo" alt="JavaScript">
                    <img src="/logo-swift.svg" class="tech-logo" alt="Swift">
                    <img src="/logo-pg.svg" class="tech-logo logo-tall" alt="PostgreSQL">
                    <img src="/logo-ngrx.svg" class="tech-logo" alt="NgRx">
                    <img src="/logo-docker.svg" class="tech-logo logo-wide" alt="Docker">
                    <img src="/logo-node.svg" class="tech-logo logo-wide" alt="Node.js">
                </div>
                <div class="tech-row desktop-only">
                    <img src="/logo-azure.svg" class="tech-logo" alt="Azure">
                    <img src="/logo-material.svg" class="tech-logo" alt="Material">
                    <img src="/logo-bootstrap.svg" class="tech-logo" alt="Bootstrap">
                    <img src="/logo-net.svg" class="tech-logo" alt=".NET">
                    <img src="/logo-hugo.svg" class="tech-logo" alt="Hugo">
                    <img src="/logo-ts.svg" class="tech-logo" alt="TypeScript">
                    <img src="/logo-gcloud.svg" class="tech-logo" alt="Google Cloud">
                </div>
                <!-- Mobile: 6 + 5 + 4 -->
                <div class="tech-row mobile-only">
                    <img src="/logo-angular.svg" class="tech-logo" alt="Angular">
                    <img src="/logo-svelte.svg" class="tech-logo" alt="Svelte">
                    <img src="/logo-js.svg" class="tech-logo" alt="JavaScript">
                    <img src="/logo-swift.svg" class="tech-logo" alt="Swift">
                    <img src="/logo-pg.svg" class="tech-logo" alt="PostgreSQL">
                    <img src="/logo-ngrx.svg" class="tech-logo" alt="NgRx">
                </div>
                <div class="tech-row mobile-only">
                    <img src="/logo-docker.svg" class="tech-logo" alt="Docker">
                    <img src="/logo-node.svg" class="tech-logo" alt="Node.js">
                    <img src="/logo-azure.svg" class="tech-logo" alt="Azure">
                    <img src="/logo-material.svg" class="tech-logo" alt="Material">
                    <img src="/logo-bootstrap.svg" class="tech-logo" alt="Bootstrap">
                </div>
                <div class="tech-row mobile-only">
                    <img src="/logo-net.svg" class="tech-logo" alt=".NET">
                    <img src="/logo-hugo.svg" class="tech-logo" alt="Hugo">
                    <img src="/logo-ts.svg" class="tech-logo" alt="TypeScript">
                    <img src="/logo-gcloud.svg" class="tech-logo" alt="Google Cloud">
                </div>
            </div>

            <!---------------------------->
            <!-- BASIC CONTRACT OPTIONS -->
            <!---------------------------->
            <div id="pricing" class="pricing-section">
                <Badge text={'PRICING'}></Badge>
                <h1>Basic Contract Options</h1>
                <div class="pricing-grid">
                    <div class="pricing-card">
                        <div class="pricing-icon">
                            <span class="icon dollar"></span>
                        </div>
                        <h3>Fixed Price</h3>
                        <p>Best for well-defined projects with clear scope and predictable budgets.</p>
                        <ul>
                            <li>Complete scope definition upfront</li>
                            <li>Guaranteed budget certainty</li>
                            <li>Milestone-based delivery</li>
                            <li>Ideal for MVPs and short-term projects</li>
                        </ul>
                    </div>
                    <div class="pricing-card">
                        <div class="pricing-icon">
                            <span class="icon timer"></span>
                        </div>
                        <h3>Time & Materials</h3>
                        <p>Flexible engagement for projects where requirements evolve over time.</p>
                        <ul>
                            <li>Pay only for actual work delivered</li>
                            <li>Adapt scope as priorities shift</li>
                            <li>Sprint-based Agile workflow</li>
                            <li>Full transparency on time spent</li>
                        </ul>
                    </div>
                    <div class="pricing-card">
                        <div class="pricing-icon">
                            <span class="icon user-star"></span>
                        </div>
                        <h3>Dedicated Developer</h3>
                        <p>Extend your team with developers fully committed to your product's success.</p>
                        <ul>
                            <li>Seamless team integration</li>
                            <li>Scale up or down as needed</li>
                            <li>Direct communication & collaboration</li>
                            <li>Long-term partnership model</li>
                        </ul>
                    </div>
                </div>
            </div>

            <!--------->
            <!-- QUOTE -->
            <!--------->
            <div class="quote-section">
                <p>"We are a small team of hand-picked experts."</p>
            </div>

        </div>
    </div>

    <!------------>
    <!-- CONTACT -->
    <!------------>
    <div id="contact" class="contact-section" data-header-theme="dark">
        <div class="content-wrapper">
            <div class="contact-grid">
                <div class="contact-info">
                    <Badge text={'BOOK A MEETING'}></Badge>
                    <h2 class="mt-0">Contact Us</h2>
                    <p class="contact-item">
                        <strong>Email:</strong>
                        office@dev-harbor.com
                    </p>
                    <p class="contact-item">
                        <strong>Location:</strong>
                        Belgrade, Serbia
                    </p>
                    <p class="contact-item">
                        <strong>Company info:</strong>
                        <span class="text-muted">Name:</span> Dev Harbor d.o.o. <br>
                        <span class="text-muted">Founder:</span> Luka Stanisic <br>
                        <span class="text-muted">Company ID:</span> 21797235 <br>
                        <span class="text-muted">VAT No:</span> 113075028 <br>
                    </p>
                </div>
                {#if formStatus === 'success'}
                    <div class="form-success">
                        <h3>Thank you for reaching out!</h3>
                        <p>We've got it from here. Expect to hear from us soon.</p>
                        <div class="text-center mb-5">
                            <img src="/mail-sent.svg" class="mail-sent" alt="Mail sent">
                        </div>
                        <button class="btn btn-outline-dark" onclick={() => formStatus = 'idle'}>Send another message</button>
                    </div>
                {:else}
                    <form class="contact-form" onsubmit={handleSubmit}>
                        <input type="checkbox" name="_honeypot" style="display:none" tabindex="-1" autocomplete="off">
                        <input type="text" name="name" class="form-control" placeholder="Your Name" required disabled={formStatus === 'submitting'}>
                        <input type="email" name="email" class="form-control" placeholder="Your Email" required disabled={formStatus === 'submitting'}>
                        <textarea name="message" class="form-control" rows="7" placeholder="Your Message" required disabled={formStatus === 'submitting'}></textarea>
                        {#if formStatus === 'error'}
                            <p class="form-error">Something went wrong. Please try again.</p>
                        {/if}
                        <button type="submit" class="btn btn-primary" disabled={formStatus === 'submitting'}>
                            {formStatus === 'submitting' ? 'Sending...' : 'Send'}
                        </button>
                    </form>
                {/if}
            </div>
        </div>
    </div>
</div>

<style>
    /* Global */
    .page-content {
        text-align: center;
    }

    .content-wrapper {
        max-width: 1400px;
        margin: 0 auto;
        padding: 0 20px;
    }

    h2 {
        font-size: 2.25rem;
        margin-bottom: 1.25rem;
        line-height: 1.2;
        letter-spacing: -0.02em;
        text-align: left;
    }

    /* Buttons */
    .btn-primary {
        background-color: #000;
        border-color: #000;
        color: #fff;
        padding: 0.85rem 2rem;
        font-weight: 500;
        border-radius: 8px;
        font-size: 0.9rem;
        border: none;
        cursor: pointer;
        transition: background-color 0.2s ease;

        &:focus {
            outline: none;
        }

        &:hover {
            background-color: #222;
        }
    }

    /* Hero Section */
    .page-title h1 {
        font-size: 2.5rem;
        text-align: center;
        padding: 0 1rem;
        margin: 0;
    }

    @media (min-width: 768px) {
        .page-title h1 {
            font-size: 50px;
            padding: 0;
        }
    }

    .hero-subtitle {
        color: #6c757d;
        text-align: center;
        font-size: 1rem;
        max-width: 600px;
        margin: 0 auto 0;
        padding: 0 1.5rem;
        line-height: 1.6;
    }

    @media (max-width: 576px) {
        .hero-subtitle {
            font-size: 0.925rem;
        }
        .page-title h1 {
            padding: 0 2rem;
        }
    }

    .hero-image {
        width: 100%;
        max-width: 2000px;
        height: auto;
    }

    /* Black Box Section */
    .black-box {
        padding: 60px 0 150px;
        text-align: center;

        .clients-section {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-bottom: 4rem;
        }

        .clients-logos {
            width: 100%;
            max-width: 2000px;
        }

        .values-section {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .values-cards {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            max-width: 1000px;
            margin: 0 auto;
        }

        .who-section {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-top: 7rem;

            h1 {
                margin-bottom: 2.25rem;
            }
        }

        .who-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1.25rem;
            max-width: 800px;
            margin: 0 auto;

            &.who-grid--stacked {
                grid-template-columns: 1fr;
                max-width: 1000px;
            }
        }

        .who-card {
            border: 1px solid rgba(255, 255, 255, 0.15);
            border-radius: 12px;
            padding: 1.75rem;
            text-align: left;
            transition: border-color 0.2s, background-color 0.2s;

            &:hover {
                border-color: rgba(255, 255, 255, 0.3);
                background-color: rgba(255, 255, 255, 0.03);
            }

            h3 {
                color: #fff;
                font-size: 1.1rem;
                font-weight: 600;
                margin: 0 0 0.5rem 0;
            }

            p {
                color: #999;
                font-size: 0.875rem;
                line-height: 1.5;
                margin: 0;
            }
        }
    }

    /* White Section */
    .white-section {
        background-color: #fff;
        padding: 70px 0;

        .content-wrapper {
            max-width: 1100px;
            padding: 0 24px;
        }

        p {
            font-size: 0.95rem;
            line-height: 1.7;
            margin-bottom: 1rem;
            color: #555;
            max-width: 420px;
            text-align: left;
        }

        img {
            max-width: 85%;
            max-height: 320px;
            width: auto;
            margin: 20px auto;
            display: block;
        }
    }

    /* Expertise Grid */
    .expertise-grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 1.5rem;
        max-width: 1000px;
        margin: 0 auto 3rem;
    }

    .expertise-card {
        padding: 1.5rem 1rem;
        text-align: center;

        .icon-square {
            width: 100px;
            height: 100px;
            background-color: #fff;
            border-radius: 16px;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0 auto 1.25rem;

            .icon {
                width: 58px;
                height: 58px;
                background-size: 58px !important;
                filter: brightness(0);
            }
        }

        h3 {
            color: #fff;
            font-size: 1.25rem;
            font-weight: 600;
            margin-bottom: 0.75rem;
            letter-spacing: -0.01em;
        }

        p {
            font-size: 0.875rem;
            line-height: 1.5;
            color: #aaa;
            max-width: 185px;
            margin: 0 auto;
        }
    }

    /* Technologies */
    .technologies-section {
        margin-top: 3rem;
        padding: 2rem 0;

        .tech-row {
            display: flex;
            justify-content: center;
            gap: 3rem;
            margin-bottom: 2rem;
            align-items: center;

            &.mobile-only {
                display: none;
            }
        }

        .tech-logo {
            height: 70px;
            width: auto;
            object-fit: contain;
            opacity: 0.85;
            transition: opacity 0.3s, transform 0.2s;

            &:hover {
                opacity: 1;
                transform: scale(1.05);
            }

            &.logo-wide {
                height: 55px;
            }

            &.logo-tall {
                height: 80px;
            }
        }
    }

    /* Pricing */
    .pricing-section {
        margin-top: 4rem;
        padding: 0 1.5rem;

        &#pricing {
            scroll-margin-top: 150px;
        }

        h1 {
            margin-bottom: 2.5rem;
        }

        .pricing-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1.5rem;
            max-width: 1000px;
            margin: 0 auto;
        }

        .pricing-card {
            background-color: #fff;
            border-radius: 12px;
            padding: 2rem 1.5rem;
            height: 100%;
            text-align: center;
            box-shadow: 0 4px 16px rgba(255, 255, 255, 0.06);
            border: 1px solid rgba(255, 255, 255, 0.08);
            transition: transform 0.2s;

            &:hover {
                transform: translateY(-3px);
            }

            .pricing-icon {
                margin-bottom: 0.25rem;

                .icon {
                    width: 58px;
                    height: 58px;
                    background-size: 58px !important;
                }
            }

            h3 {
                color: #000;
                font-size: 1.25rem;
                font-weight: 700;
                margin-bottom: 1rem;
                padding-bottom: 0.85rem;
                border-bottom: 1px solid #e5e5e5;
            }

            p {
                color: #666;
                font-size: 0.85rem;
                margin-bottom: 1.5rem;
                line-height: 1.5;
                min-height: 50px;
            }

            ul {
                list-style: none;
                padding: 0;
                margin: 0;
                text-align: left;

                li {
                    color: #555;
                    padding: 0.6rem 0;
                    font-size: 0.825rem;
                    display: flex;
                    align-items: center;

                    &:before {
                        content: "";
                        width: 16px;
                        height: 16px;
                        background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='16' height='16' viewBox='0 0 24 24' fill='none' stroke='%23000' stroke-width='2'%3E%3Cpolyline points='20 6 9 17 4 12'%3E%3C/polyline%3E%3C/svg%3E");
                        background-repeat: no-repeat;
                        background-size: contain;
                        margin-right: 0.6rem;
                        flex-shrink: 0;
                    }

                    &:not(:last-child) {
                        border-bottom: 1px solid #f0f0f0;
                    }
                }
            }
        }
    }

    /* Quote */
    .quote-section {
        padding: 3rem 0;
        margin: 2.5rem 0 2rem 0;

        p {
            font-family: "Pinyon Script", cursive;
            font-weight: 400;
            font-style: normal;
            font-size: 2.5rem;
            color: #888;
            line-height: 1.4;
            margin: 0 auto;
        }
    }

    /* Contact */
    .contact-section {
        background-color: #fff;
        padding: 80px 0;
        text-align: left;

        .content-wrapper {
            max-width: 1000px;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }

        .contact-item {
            color: #555;
            margin-bottom: 1.5rem;
            line-height: 1.6;
            font-size: 0.9rem;

            strong {
                color: #000;
                font-weight: 600;
                display: block;
                margin-bottom: 0.35rem;
                font-size: 0.95rem;
            }
            .text-muted {
                color: #aaa !important;
            }
        }

        .contact-form {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .form-control {
            border: 1px solid #e0e0e0;
            border-radius: 8px;
            padding: 0.85rem 1rem;
            font-size: 0.9rem;
            transition: border-color 0.2s;
            background-color: #fafafa;
            width: 100%;

            &:focus {
                border-color: #000;
                outline: none;
                background-color: #fff;
            }

            &::placeholder {
                color: #aaa;
            }
        }

        textarea {
            resize: vertical;
            min-height: 120px;
        }

        .btn-primary {
            width: 100%;

            &:disabled {
                background-color: #999;
                cursor: not-allowed;
            }
        }

        .form-success {
            background-color: #f8f9fa;
            border: 1px solid #e0e0e0;
            border-radius: 12px;
            padding: 2.5rem 2rem;
            text-align: center;

            h3 {
                color: #000;
                font-size: 1.5rem;
                margin: 0 0 0.75rem;
            }

            p {
                color: #666;
                font-size: 0.95rem;
                margin: 0 0 1.5rem;
                line-height: 1.5;
            }

            .mail-sent {
                max-width: 150px;
            }

            .btn-outline-dark {
                background-color: transparent;
                border: 1px solid #000;
                color: #000;
                padding: 0.7rem 1.5rem;
                font-size: 0.9rem;
                border-radius: 8px;
                cursor: pointer;
                transition: background-color 0.2s, color 0.2s;

                &:hover {
                    background-color: #000;
                    color: #fff;
                }
            }
        }

        .form-error {
            color: #dc3545;
            font-size: 0.875rem;
            margin: 0;
            text-align: center;
        }
    }

    /* Responsive: Tablets (max 991px) */
    @media (max-width: 991px) {
        .white-section {
            padding: 60px 0;
            text-align: center;

            h2 {
                font-size: 2rem;
            }

            p {
                max-width: none;
            }
        }

        .technologies-section .tech-row {
            gap: 1.5rem;
        }

        .contact-section .contact-grid {
            grid-template-columns: 1fr;
            gap: 2rem;
        }
    }

    /* Responsive: Mobile (max 767px) */
    @media (max-width: 767px) {
        .black-box {
            padding: 50px 0 60px;

            h1 {
                font-size: 2rem;
                margin-bottom: 1.75rem;
                margin-top: 2rem;
            }
        }

        .white-section {
            padding: 50px 0;

            h2 {
                font-size: 1.75rem;
            }
        }

        .expertise-grid {
            grid-template-columns: 1fr;
            max-width: 400px;
        }

        .who-grid {
            grid-template-columns: 1fr;
            max-width: 400px;
        }

        .pricing-section .pricing-grid {
            grid-template-columns: 1fr;
            max-width: 400px;
            margin: 0 auto;
        }

        .technologies-section {
            .tech-row {
                display: none;
                flex-wrap: wrap;
                justify-content: center;
                gap: 1.5rem 1.25rem;
                margin: 0 auto 1.5rem;

                &.desktop-only {
                    display: none;
                }

                &.mobile-only {
                    display: flex;
                }
            }

            .tech-logo {
                width: 48px;
                height: 48px;

                &.logo-tall, &.logo-wide {
                    height: 48px;
                }
            }
        }

        .quote-section {
            padding: 2rem 0;
        }

        .contact-section {
            padding: 60px 0;

            h2 {
                font-size: 2rem;
                margin-bottom: 1.5rem;
            }
        }
    }

    /* Responsive: Small mobile (max 480px) */
    @media (max-width: 480px) {
        .technologies-section {
            .tech-row {
                gap: 1.25rem 1rem;

                &.desktop-only {
                    display: none;
                }

                &.mobile-only {
                    display: flex;
                }
            }

            .tech-logo {
                width: 40px;
                height: 40px;

                &.logo-tall, &.logo-wide {
                    height: 40px;
                }
            }
        }
    }
</style>