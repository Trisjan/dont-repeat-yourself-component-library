<script>
    export let title
</script>
<h2>
    {title}
</h2>

<style>
    h2 {
        font-size: calc(var(--font-scale) * var(--font-scale) * var(--font-scale) * var(--font-scale) * var(--font-scale) * var(--font-size) / 1.5);
    }

    @media (min-width: 601px) {
        h2 {
            font-size: calc(var(--font-scale) * var(--font-scale) * var(--font-scale) * var(--font-scale) * var(--font-scale) * var(--font-scale) * var(--font-size));
        }
    }
</style>