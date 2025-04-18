<script>
    import Badge from "$lib/components/Badge.svelte";
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
    <div class="page-title">
        <h1 class="text-center px-3 mb-0">Built in harbor.</h1>
        <h1 class="text-center px-3">Ready for open waters.</h1>
    </div>

    <h6 class="text-muted text-center px-3 mb-0 mt-3">At Dev Harbor, we build custom software that’s more than just code.</h6>
    <h6 class="text-muted text-center px-3">It’s the foundation for your journey.</h6>

    <div class="text-center mt-4">
        <button class="btn btn-primary">Get started</button>
    </div>

    <img src="/hero-image.svg" class="hero-image" alt="Hero image">

    <div class="black-box">
        <div class="text-center">
            <Badge text={'TRUSTED BY COMPANIES WORLDWIDE'}></Badge>
        </div>
        <img src="/clients.svg" class="hero-image mb-3" alt="Clients">

        <div class="text-center mb-2">
            <Badge text={'VALUES'}></Badge>
        </div>
        <h1 class="text-center">Core Values</h1>
    </div>
</div>

<style>
    @media (min-width: 768px) {
        .page-title h1 {
            font-size: 50px;
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
        }
    }
    .hero-image {
        width: 100%;
        height: auto;
    }
</style>