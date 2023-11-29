<script>
    export let title;
</script>
<h1>{title}</h1>

<style>
    h1 {
        font-size: calc(var(--font-scale) * var(--font-scale) * var(--font-scale) * var(--font-scale) * var(--font-scale) * var(--font-scale) * var(--font-size) / 1.5);
    }

    @media (min-width: 601px) {
        h1 {
            font-size: calc(var(--font-scale) * var(--font-scale) * var(--font-scale) * var(--font-scale) * var(--font-scale) * var(--font-scale) * var(--font-size));
        }
    }
</style>