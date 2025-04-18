<script>
    import Badge from "$lib/components/Badge.svelte";
    import WhiteCard from "$lib/components/WhiteCard.svelte";
    import HeroGradientWave from "$lib/components/HeroGradientWave.svelte";
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
    <div class="page-title">
        <h1 class="text-center px-3 mb-0">Built in harbor.</h1>
        <h1 class="text-center px-3">Ready for open waters.</h1>
    </div>
    <h6 class="text-muted text-center px-3 mb-0 mt-3 mb-1">At Dev Harbor, we build custom software that’s more than just code.</h6>
    <h6 class="text-muted text-center px-3">It’s the foundation for your journey, setting you up to navigate the future with confidence.</h6>
    <div class="text-center mt-4">
        <button class="btn btn-primary">Get started today</button>
    </div>
    <img src="/hero-image.svg" class="hero-image" alt="Hero">

    <!-- WAVE -->
<!--    <HeroGradientWave></HeroGradientWave>-->

    <!--------------->
    <!-- BLACK BOX -->
    <!--------------->
    <div class="black-box d-flex justify-content-center">
        <div class="content-wrapper">

            <!------------->
            <!-- CLIENTS -->
            <!------------->
            <div class="text-center">
                <Badge text={'TRUSTED BY COMPANIES WORLDWIDE'}></Badge>
            </div>
            <img src="/clients.svg" class="hero-image mb-3" alt="Clients">

            <!----------------->
            <!-- CORE VALUES -->
            <!----------------->
            <div class="text-center mb-2">
                <Badge text={'VALUES'}></Badge>
            </div>
            <h1 class="text-center">Core Values</h1>
            <div class="row">
                <WhiteCard iconClass="iris-scan" isLeft={true} headerText="User Experience" bodyText="We create beautiful & clean apps that people enjoy using daily"></WhiteCard>
                <WhiteCard iconClass="code" isLeft={false} headerText="Tailor-Made Solutions" bodyText="We are developing software specifically for every individual requirement"></WhiteCard>
                <WhiteCard iconClass="magic" isLeft={true} headerText="Simplicity" bodyText="We always strive to find and implement the simplest solution for any given problem"></WhiteCard>
                <WhiteCard iconClass="subtract" isLeft={false} headerText="Scalable Design" bodyText="We build every application with stable growth and future improvements in mind"></WhiteCard>
                <WhiteCard iconClass="dashboard-dots" isLeft={true} headerText="Performance" bodyText="We take great measures to ensure all our applications are blazing fast"></WhiteCard>
                <WhiteCard iconClass="mobile-dev-mode" isLeft={false} headerText="Responsive design" bodyText="We design all our apps to work perfectly with laptops, tablets and smart phones"></WhiteCard>
            </div>


        </div>
    </div>
</div>

<style>
    .page-content {
        text-align: center;

        .content-wrapper {
            width: 90%;
            max-width: 1240px;
            padding: 0 40px;
        }
    }
    .btn {
        &.btn-primary {
            background-color: #000;
            border-color: #000;
            padding: 0.75rem 1.5rem;

            &:focus {
                box-shadow: none;
            }
            &:hover {
                background-image: linear-gradient(315deg, #000000 50%, #282828 50%);
            }
        }
    }
    .hero-image {
        width: 100%;
        height: auto;
    }
    .black-box {
        padding-bottom: 100px;
    }

    /* Large screen */
    @media (min-width: 768px) {
        .page-title h1 {
            font-size: 50px;
        }
    }
</style>