<script>
    export let data
</script>

<section class="component">
    <h1>Uitleningen</h1>
    <section class="carousel">
        {#each data.uitleengeschiedenis1 as book}
            <article>
                <img src="{book.image.url}" alt="foto van {book.title}" loading="lazy">
                <section class="info">
                    <p class="p__title">{book.title}</p>
                    <p>{book.author}</p>
                    <section class="s__date">
                        <section>
                            <p class="p__title">Uitleendatum:</p>
                            <p>{book.uitleendatum}</p>
                        </section>
                        <section>
                            <p class="p__title">Inleverdatum:</p>
                            <p>{book.inleverdatum}</p>
                        </section>
                    </section>
                </section>
            </article>
        {/each}
        <!-- 2de keer data loopen omdat ik niet genoeg dummy data heb om
        de carrousel goed te zien werken -->
        {#each data.uitleengeschiedenis1 as book}
            <article>
                <img src="{book.image.url}" alt="foto van {book.title}" loading="lazy">
                <section class="info" aria-label="information about the book">
                    <p class="p__title">{book.title}</p>
                    <p>{book.author}</p>
                    <section class="s__date" aria-label="important dates">
                        <section>
                            <p class="p__title">Uitleendatum:</p>
                            <p>{book.uitleendatum}</p>
                        </section>
                        <section>
                            <p class="p__title">Inleverdatum:</p>
                            <p>{book.inleverdatum}</p>
                        </section>
                    </section>
                </section>
            </article>
        {/each}
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

    .carousel article:first-child {
        margin-left: auto;
    }

    .carousel article:last-child {
        margin-right: auto;
    }

    article {
        position: relative;
        display: flex;
        flex-direction: column;
        margin: 1rem 3rem 1rem 0;
        width: 12rem;
        padding: 1rem;
        border-radius: 0.5rem;
        background-color: #FFFFFF;
        scroll-snap-align: start;
        transition: 0.3s;
    }
    
    article:hover {
        scale: 103%;
        background-color:red;
        color: #FFFFFF;
    }

    .info > p {
        font-size: 0.9rem;
    }

    .p__title {
        font-weight: bold;
    }

    .s__date section {
        padding: 0 0.5rem 0 0;
    }

    .s__date section > p {
        font-size: 0.75rem;
    }

    .s__date {
        display: flex;
    }

    @media (max-width: 1000px) {
        .component {
            max-width: 90%;
        }

        .info > p {
        font-size: 0.8rem;
        }

        article {
            width: 10rem;
        }

        .s__date section > p {
        font-size: 0.7rem;
        }
    }

    @media (max-width: 600px) {
        .component {
            max-width: 100%;
        }

        article {
            scroll-snap-align: center;
            width: 9rem;
        }

        .s__date {
            flex-direction: column;
        }

        .info > p {
        font-size: 0.75rem;
        }

        .s__date section > p {
        font-size: 0.6rem;
        }
}
</style>