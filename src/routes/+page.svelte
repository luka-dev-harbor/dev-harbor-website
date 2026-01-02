<script>
    import Badge from "$lib/components/Badge.svelte";
    import WhiteCard from "$lib/components/WhiteCard.svelte";
    import HeroGradientWave from "$lib/components/HeroGradientWave.svelte";
    import CleanLineTransition from "$lib/components/CleanLineTransition.svelte";
    import CurvedTransition from "$lib/components/CurvedTransition.svelte";
</script>

<svelte:head>
    <title>Dev Harbor — Custom Web Development</title>
    <meta name="description" content="We craft modern, fast, and beautiful websites for your business." />
    <meta property="og:title" content="Dev Harbor — Custom Web Development" />
    <meta property="og:description" content="We craft modern, fast, and beautiful websites for your business." />
    <meta property="og:image" content="/og-image.png" />
    <link rel="canonical" href="https://dev-harbor.com/" />
</svelte:head>

<div class="page-content">

    <!------------------------->
    <!-- HERO HEADER + IMAGE -->
    <!------------------------->
    <div class="hero-section">
        <div class="hero-content">
            <h1>Built in harbor.</h1>
            <h1>Ready for open waters.</h1>
            <div class="hero-subtitle">
                <p>At Dev Harbor, we build custom software that's more than just code.</p>
                <p>It's the foundation for your journey.</p>
            </div>
            <button class="btn btn-primary">Get started</button>
        </div>
        <img src="/hero-image.svg" class="hero-image" alt="Hero">
    </div>

    <!-- WAVE -->
    <HeroGradientWave></HeroGradientWave>

    <!--------------->
    <!-- BLACK BOX -->
    <!--------------->
    <div class="black-box">
        <div class="content-wrapper">

            <!------------->
            <!-- CLIENTS -->
            <!------------->
            <div class="clients-section">
                <Badge text={'TRUSTED BY'}></Badge>
                <img src="/clients.svg" class="clients-logos" alt="Clients">
            </div>

            <!----------------->
            <!-- CORE VALUES -->
            <!----------------->
            <div class="values-section">
                <Badge text={'VALUES'}></Badge>
                <h1>Core Values</h1>
            </div>
            <div class="values-cards">
                <WhiteCard iconClass="iris-scan" isLeft={true} headerText="User Experience" bodyText="We create beautiful & clean apps that people enjoy using daily"></WhiteCard>
                <WhiteCard iconClass="code" isLeft={false} headerText="Tailor-Made Solutions" bodyText="We are developing software specifically for every individual requirement"></WhiteCard>
                <WhiteCard iconClass="magic" isLeft={true} headerText="Simplicity" bodyText="We always strive to find and implement the simplest solution for any given problem"></WhiteCard>
                <WhiteCard iconClass="subtract" isLeft={false} headerText="Scalable Design" bodyText="We build every application with stable growth and future improvements in mind"></WhiteCard>
                <WhiteCard iconClass="dashboard-dots" isLeft={true} headerText="Performance" bodyText="We take great measures to ensure all our applications are blazing fast"></WhiteCard>
                <WhiteCard iconClass="mobile-dev-mode" isLeft={false} headerText="Responsive design" bodyText="We design all our apps to work perfectly with laptops, tablets and smart phones"></WhiteCard>
            </div>

        </div>
    </div>

    <!-- CLEAN LINE TRANSITION -->
    <CleanLineTransition></CleanLineTransition>

    <!-------------------------------->
    <!-- CUSTOM SOFTWARE DEVELOPMENT -->
    <!-------------------------------->
    <div class="white-section">
        <div class="content-wrapper">
            <div class="row align-items-center">
                <div class="col-12 col-lg-6 order-2 order-lg-1">
                    <h2>Custom software development</h2>
                    <p>Our team specializes in building tailor-made software solutions that perfectly align with your business goals. From concept to deployment, we handle every aspect of the development process with precision and expertise.</p>
                    <p>Whether you need a web application, mobile app, or enterprise system, we deliver high-quality code that scales with your business.</p>
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
    <div class="white-section">
        <div class="content-wrapper">
            <div class="row align-items-center">
                <div class="col-12 col-lg-6">
                    <img src="/full-scope.svg" alt="Full Scope of Work">
                </div>
                <div class="col-12 col-lg-6">
                    <h2>Full scope of work</h2>
                    <p>We provide end-to-end solutions covering every phase of your project lifecycle. From initial consultation and planning to design, development, testing, and ongoing maintenance.</p>
                    <p>Our comprehensive approach ensures seamless integration and optimal performance across all aspects of your digital ecosystem.</p>
                </div>
            </div>
        </div>
    </div>

    <!--------------------------->
    <!-- MODERNIZING LEGACY TECH -->
    <!--------------------------->
    <div class="white-section">
        <div class="content-wrapper">
            <div class="row align-items-center">
                <div class="col-12 col-lg-6 order-2 order-lg-1">
                    <h2>Modernizing legacy tech</h2>
                    <p>Transform your outdated systems into modern, efficient solutions. We help businesses migrate from legacy technologies to cutting-edge platforms without disrupting operations.</p>
                    <p>Our modernization approach improves performance, security, and maintainability while preserving your valuable business logic and data.</p>
                </div>
                <div class="col-12 col-lg-6 order-1 order-lg-2">
                    <img src="/modernize.svg" alt="Modernizing Legacy Tech">
                </div>
            </div>
        </div>
    </div>

    <!-- CURVED TRANSITION -->
    <CurvedTransition></CurvedTransition>

    <!------------->
    <!-- EXPERTISE -->
    <!------------->
    <div class="black-box">
        <div class="content-wrapper">
            <h1>Expertise</h1>
            <div class="expertise-grid">
                <div class="expertise-card">
                    <div class="icon-circle">
                        <span class="icon code"></span>
                    </div>
                    <h3>Web Apps</h3>
                    <p>Modern, responsive web applications built with cutting-edge technologies and best practices.</p>
                </div>
                <div class="expertise-card">
                    <div class="icon-circle">
                        <span class="icon mobile-dev-mode"></span>
                    </div>
                    <h3>Native Mobile</h3>
                    <p>Native and cross-platform mobile applications designed for optimal performance and user experience.</p>
                </div>
                <div class="expertise-card">
                    <div class="icon-circle">
                        <span class="icon dashboard-dots"></span>
                    </div>
                    <h3>Consulting</h3>
                    <p>Strategic technology consulting to help you make informed decisions about your digital transformation.</p>
                </div>
            </div>

            <!--------------->
            <!-- TECHNOLOGIES -->
            <!--------------->
            <div class="technologies-section">
                <div class="tech-grid">
                    <img src="/logo-js.svg" class="tech-logo" alt="JavaScript">
                    <img src="/logo-ts.svg" class="tech-logo" alt="TypeScript">
                    <img src="/logo-svelte.svg" class="tech-logo" alt="Svelte">
                    <img src="/logo-angular.svg" class="tech-logo" alt="Angular">
                    <img src="/logo-node.svg" class="tech-logo" alt="Node.js">
                    <img src="/logo-net.svg" class="tech-logo" alt=".NET">
                    <img src="/logo-pg.svg" class="tech-logo" alt="PostgreSQL">
                    <img src="/logo-docker.svg" class="tech-logo" alt="Docker">
                    <img src="/logo-azure.svg" class="tech-logo" alt="Azure">
                    <img src="/logo-gcloud.svg" class="tech-logo" alt="Google Cloud">
                    <img src="/logo-swift.svg" class="tech-logo" alt="Swift">
                    <img src="/logo-bootstrap.svg" class="tech-logo" alt="Bootstrap">
                </div>
            </div>

            <!---------------------------->
            <!-- BASIC CONTRACT OPTIONS -->
            <!---------------------------->
            <div class="pricing-section">
                <h1>Basic Contract Options</h1>
                <div class="pricing-grid">
                    <div class="pricing-card">
                        <div class="pricing-icon">
                            <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                                <line x1="12" y1="1" x2="12" y2="23"></line>
                                <path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"></path>
                            </svg>
                        </div>
                        <h3>Fixed Price</h3>
                        <p>Perfect for well-defined projects with clear requirements and scope.</p>
                        <ul>
                            <li>Defined scope and timeline</li>
                            <li>Predictable costs</li>
                            <li>Milestone-based delivery</li>
                            <li>Quality assurance included</li>
                        </ul>
                    </div>
                    <div class="pricing-card">
                        <div class="pricing-icon">
                            <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                                <circle cx="12" cy="12" r="10"></circle>
                                <polyline points="12 6 12 12 16 14"></polyline>
                            </svg>
                        </div>
                        <h3>Time & Materials</h3>
                        <p>Ideal for evolving projects that require adaptability and iterative development.</p>
                        <ul>
                            <li>Agile methodology</li>
                            <li>Regular sprint reviews</li>
                            <li>Flexible scope adjustments</li>
                            <li>Continuous feedback integration</li>
                        </ul>
                    </div>
                    <div class="pricing-card">
                        <div class="pricing-icon">
                            <svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                                <path d="M20 21v-2a4 4 0 0 0-4-4H8a4 4 0 0 0-4 4v2"></path>
                                <circle cx="12" cy="7" r="4"></circle>
                            </svg>
                        </div>
                        <h3>Dedicated Dev</h3>
                        <p>For clients who have their own design and project management but need development expertise.</p>
                        <ul>
                            <li>Pure development focus</li>
                            <li>Work with your existing team</li>
                            <li>Technical implementation only</li>
                            <li>Code review and optimization</li>
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
    <div class="contact-section">
        <div class="content-wrapper">
            <div class="contact-grid">
                <div class="contact-info">
                    <Badge text={'CONTACT US'}></Badge>
                    <h2>Contact Us</h2>
                    <p class="contact-item">
                        <strong>Address:</strong><br>
                        123 Harbor Street<br>
                        Tech Bay, CA 94102
                    </p>
                    <p class="contact-item">
                        <strong>Phone:</strong><br>
                        +1 (555) 123-4567
                    </p>
                    <p class="contact-item">
                        <strong>Email:</strong><br>
                        hello@dev-harbor.com
                    </p>
                </div>
                <form class="contact-form">
                    <input type="text" class="form-control" placeholder="Your Name" required>
                    <input type="email" class="form-control" placeholder="Your Email" required>
                    <textarea class="form-control" rows="5" placeholder="Your Message" required></textarea>
                    <button type="submit" class="btn btn-primary">Send</button>
                </form>
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
    .hero-section {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        padding: 70px 20px 60px;

        .hero-content {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        h1 {
            font-size: 3.5rem;
            font-weight: 400;
            line-height: 1.1;
            letter-spacing: -0.03em;
            margin-bottom: 0;
        }

        .hero-subtitle {
            margin: 2rem auto 0;

            p {
                font-size: 1rem;
                color: #666;
                line-height: 1.6;
                margin-bottom: 0.15rem;
            }
        }

        .btn-primary {
            margin-top: 2rem;
        }

        .hero-image {
            display: block;
            width: 100%;
            max-width: 950px;
            margin: 30px auto 0;
            margin-bottom: -100px;
            position: relative;
            z-index: 1;
        }
    }

    /* Black Box Section */
    .black-box {
        padding: 60px 0 80px;
        text-align: center;

        h1 {
            font-size: 2.5rem;
            font-weight: 500;
            margin-bottom: 2.5rem;
            margin-top: 0.5rem;
            letter-spacing: -0.02em;
        }

        .clients-section {
            display: flex;
            flex-direction: column;
            align-items: center;
            margin-bottom: 4rem;
        }

        .clients-logos {
            width: 100%;
            max-width: 900px;
            margin: 1.5rem auto 0;
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
            max-width: 800px;
            margin: 0 auto;
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

        h2 {
            font-size: 2.25rem;
            font-weight: 600;
            margin-bottom: 1.25rem;
            line-height: 1.2;
            letter-spacing: -0.02em;
        }

        p {
            font-size: 0.95rem;
            line-height: 1.7;
            margin-bottom: 1rem;
            color: #555;
            max-width: 420px;
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

        .icon-circle {
            width: 70px;
            height: 70px;
            background-color: #fff;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0 auto 1.25rem;
            box-shadow: 0 2px 8px rgba(255, 255, 255, 0.06);

            .icon {
                width: 32px;
                height: 32px;
                background-size: 32px !important;
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
            max-width: 250px;
            margin: 0 auto;
        }
    }

    /* Technologies */
    .technologies-section {
        margin-top: 3rem;
        padding: 2rem 0;

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(6, 1fr);
            gap: 2rem 1.5rem;
            max-width: 720px;
            margin: 0 auto;
            align-items: center;
            justify-items: center;
        }

        .tech-logo {
            max-width: 60px;
            max-height: 40px;
            opacity: 0.85;
            transition: opacity 0.3s, transform 0.2s;

            &:hover {
                opacity: 1;
                transform: scale(1.05);
            }
        }
    }

    /* Pricing */
    .pricing-section {
        margin-top: 4rem;
        padding: 0 1.5rem;

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
                margin-bottom: 1.25rem;

                svg {
                    color: #000;
                    width: 28px;
                    height: 28px;
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
        margin: 2rem 0;

        p {
            font-family: 'Georgia', serif;
            font-style: italic;
            font-size: 1.5rem;
            color: #888;
            font-weight: 400;
            line-height: 1.4;
            max-width: 500px;
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

        h2 {
            font-size: 2.25rem;
            font-weight: 600;
            margin-bottom: 2rem;
            margin-top: 1rem;
            line-height: 1.2;
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
        }
    }

    /* Responsive: Large screens (768px+) */
    @media (min-width: 768px) {
        .hero-section {
            padding: 70px 20px 80px;

            h1 {
                font-size: 4.5rem;
            }

            .hero-subtitle p {
                font-size: 1.1rem;
            }

            .hero-image {
                max-width: 1500px;
                margin-top: 40px;
                margin-bottom: -185px;
            }
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

        .expertise-grid {
            grid-template-columns: repeat(2, 1fr);
        }

        .pricing-section .pricing-grid {
            grid-template-columns: repeat(2, 1fr);
        }

        .technologies-section .tech-grid {
            grid-template-columns: repeat(4, 1fr);
        }

        .contact-section .contact-grid {
            grid-template-columns: 1fr;
            gap: 2rem;
        }
    }

    /* Responsive: Mobile (max 767px) */
    @media (max-width: 767px) {
        .hero-section {
            padding: 70px 20px 35px;

            h1 {
                font-size: 2.5rem;
            }

            .hero-subtitle {
                max-width: 90%;

                p {
                    font-size: 0.9rem;
                }
            }
        }

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

        .pricing-section .pricing-grid {
            grid-template-columns: 1fr;
            max-width: 400px;
            margin: 0 auto;
        }

        .technologies-section .tech-grid {
            grid-template-columns: repeat(3, 1fr);
        }

        .technologies-section .tech-logo {
            max-width: 50px;
            max-height: 34px;
        }

        .quote-section {
            padding: 2rem 0;

            p {
                font-size: 1.15rem;
            }
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
        .hero-section {
            padding: 60px 20px 30px;

            h1 {
                font-size: 2rem;
            }

            .hero-subtitle p {
                font-size: 0.85rem;
            }
        }

        .technologies-section .tech-grid {
            grid-template-columns: repeat(2, 1fr);
        }
    }
</style>