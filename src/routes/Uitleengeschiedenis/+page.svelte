<script>
    import Caroussel from "$lib/components/Carrousel.svelte";
    export let data;
</script>

<Caroussel {data} />

<style>
  @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap');

    :root {
        background-color: #E4E9F7;
        font-family: 'Poppins', sans-serif;
    }
</style>