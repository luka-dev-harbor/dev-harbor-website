<script>
    import Header from "$lib/components/Header.svelte";
    import "../app.css";
</script>

<Header></Header>

<div class="page-content">
    <slot />
</div>

<style>
    .page-content {
        margin-top: 100px;
        padding: 40px 80px;
        min-height: calc(100vh - 100px);
    }
</style>