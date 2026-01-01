<script lang="ts">
    let {text} = $props();
</script>

<span class="badge">{text}</span>

<style>
    .badge {
        font-family: "Chivo Mono", monospace;
        background-color: #1a1a1a;
        color: #fff;
        font-weight: 500;
        font-size: 10px;
        padding: 0.4rem 0.75rem;
        letter-spacing: 0.1em;
        border-radius: 4px;
        display: inline-block;
        text-transform: uppercase;
        margin-bottom: 1rem;
    }
</style>
