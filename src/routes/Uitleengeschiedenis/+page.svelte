<script>
    import { Card, Navbar, Table, Title, Subtitle, P } from '$lib/index.js';
    export let data;

    // function formatTableData(data) {
    //     data.uitleengeschiedenis1.map((item) => {
    //         return {
    //             uitleendatum: item.uitleendatum,
    //             title: item.title,
    //             author: item.author,
    //             category: item.category
    //         };
    //     });
    // }

    // console.log("Dit is de data: " + formatTableData(data))
</script>
<Navbar/>
<main>
    <section class="page_section carrousel">
        <Title title="Uitleningen"/>
        <P 
            inputText="U kunt hier materialen verlengen voor de gebruiksvriendelijke leenperiode van het materiaal. 
            Deze gaat in op de dag waarop u verlengt. Het is niet zinvol om materialen tweemaal snel achter elkaar te verlengen. 
            Onze medewerkers kunnen de materialen wel voor een langere periode verlengen, bijvoorbeeld als u op vakantie gaat.">
        </P>
        <section class="carrousel_section
        ">
            {#each data.uitleengeschiedenis1 as book}
            <Card
                bookTitle="{book.title}"
                bookAuthor="{book.author}"
                bookUrl="{book.image.url}"
                bookInleverdatum="{book.inleverdatum}"
                bookUitleendatum="{book.uitleendatum}"
            >
            </Card>
            {/each}
            <!-- ------------------------------------------- -->
            <!-- tweede foreach loop vanwege gebrek aan data -->
            <!-- ------------------------------------------- -->
            {#each data.uitleengeschiedenis1 as book}
            <Card
                bookTitle="{book.title}"
                bookAuthor="{book.author}"
                bookUrl="{book.image.url}"
                bookInleverdatum="{book.inleverdatum}"
                bookUitleendatum="{book.uitleendatum}"
                buttonText="verlengen"
            >
            </Card>
            {/each}
        </section>
    </section>

    <section class="page_section">
        <Subtitle title="Uitleengeschiedenis"/>
        <P inputText="Hieronder kunt u de uitleengeschiedenis zien"/>
        <Table 
            tableData={data.uitleengeschiedenis1}>
        </Table>
    </section>
</main>
<style>
    main {
        padding-left: 7rem;
    }

    .page_section {
        max-width: 80%;
        margin: 0 0rem 3rem 1rem;
    }

    .carrousel  {
        display: flex;
        flex-direction: column;
    }

    section .carrousel_section
    {
        display: flex;
        flex-direction: row;
        overflow-x: scroll;
        overflow-y: hidden;
        scroll-snap-type: x mandatory;
        scroll-behavior: smooth;
        height: 50%;
    }

    @media (max-width: 1000px) {
        .page_section
     {
            max-width: 90%;
        }
    }

    @media (max-width: 600px) {
        .page_section
     {
            max-width: 100%;
        }
}
</style>