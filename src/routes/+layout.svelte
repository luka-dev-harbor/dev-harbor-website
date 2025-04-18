<script>
    import Header from "$lib/components/Header.svelte";
    import "../app.css";
</script>

<Header></Header>

<div class="page-wrapper">
    <div class="page-content">
        <slot />
    </div>
</div>

<style>
    .page-wrapper {
        display: flex;
        justify-content: center;

        .page-content {
            margin-top: 100px;
            min-height: calc(100vh - 100px);
            max-width: 2000px;
        }
    }
</style>