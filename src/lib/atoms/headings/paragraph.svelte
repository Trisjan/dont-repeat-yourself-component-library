<script>
    export let inputText
</script>

<p>
    {inputText}
</p>

<style>
    p {
        font-size: calc(var(--font-size) / 1.5);
    }

    @media (min-width: 601px) {
        p {
            font-size: var(--font-size);
        }
    }
</style>