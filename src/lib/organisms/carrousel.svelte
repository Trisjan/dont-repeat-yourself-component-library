<script>
    export let carrouselTitle
    export let data
</script>

<section class="component">
    <h1>{carrouselTitle}</h1>
    <section class="carousel">
        
    </section>
</section>

<style>
    
    .component {
        max-width: 80%;
        display: flex;
        flex-direction: column;
        margin: 0 1rem;
    }

    section .carousel {
        display: flex;
        flex-direction: row;
        overflow-x: scroll;
        overflow-y: hidden;
        scroll-snap-type: x mandatory;
        scroll-behavior: smooth;
        height: 50%;
    }

    @media (max-width: 1000px) {
        .component {
            max-width: 90%;
        }
    }

    @media (max-width: 600px) {
        .component {
            max-width: 100%;
        }
}
</style>