<script>
    import {Button} from '$lib/index'
    export let bookUrl
    export let bookTitle
    export let bookAuthor
    export let bookInleverdatum
    export let bookUitleendatum
    export let buttonText
</script>

<article>
    <img src="{bookUrl}" alt="foto van {bookTitle}" loading="lazy">
    <section class="info">
        <p class="p__title">{bookTitle}</p>
        <p>{bookAuthor}</p>
        <section class="s__date">
            <section>
                <p class="p__title">Uitleendatum:</p>
                <p>{bookUitleendatum}</p>
            </section>
            <section>
                <p class="p__title">Inleverdatum:</p>
                <p>{bookInleverdatum}</p>
            </section>
        </section>
        <Button buttonText="verlengen" />
    </section>
</article>

<style>

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

    article img {
        object-fit: cover;
        height: 50%;
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

    .info  {
        display: flex;
        flex-direction: column;
    }

    .info button {
        justify-content: space-between;

    }

    @media (max-width: 1000px) {

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