<script lang="ts">
    let {text} = $props();
</script>

<span class="badge">{text}</span>

<style>
    .badge {
        font-family: "Chivo Mono", monospace;
        background-color: #333;
        color: #fff;
        font-weight: 400;
        font-size: 10px;
        padding: 0.5rem 0.75rem;
    }
</style>