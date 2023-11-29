<script>
    import { Chatbot, Navbar } from '$lib/index.js';
    // import logo from '$lib/assets/oba.png';
</script>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>        
    <Navbar />
        <header> 
            <!-- <img src={logo} alt="logo van oba"> -->
            <h1>Betalingen</h1>

            <Chatbot/>

        </header>
        
        <main>

            <section>
            
            <ul>
                <li>SOORT BETALING</li>
                <li>BETAALDATUM</li>
                <li>BEDRAG</li>
                <li>BETALINGSWIJZE</li>
                <li>DETAILS</li>
            </ul>     
            <ul>
                <li>Contributie</li>
                <li>01/08/2023</li>
                <li>€19.99</li>
                <li>PIN</li>
                <li>7394628495</li>
            </ul>
            <ul>
                <li>Betaling uit deposito</li>
                <li>21/07/2023</li>
                <li>€25.00</li>
                <li>PIN</li>
                <li>9749937459</li>
            </ul>
            <ul>
                <li>Boete</li>
                <li>21/07/2023</li>
                <li>€2.75</li>
                <li>Contant</li>
                <li>3845928503</li>
            </ul>
            <ul>
                <li>Inschrijving</li>
                <li>01/06/2023</li>
                <li>€1.00</li>
                <li>PIN</li>
                <li>8648543578</li>
            </ul>
            <ul>
                <li>Verkopen</li>
                <li>01/07/2023</li>
                <li>€2.99</li>
                <li>PIN</li>
                <li>9537905742</li>
            </ul>

            </section>

            <div class="personal-info">

                <article class="depositos">
                    <h2>Deposito's</h2>
                    <p class="p-depositos">Hier kunt u via IDEAL tegoed op uw OBA-pas zetten.</p>
                    <p>Het bedrag hieronder geeft het huidige tegoed op uw pas aan</p>
                    <div class="tegoed">
                        <h3>Leners tegoed</h3>
                        <button>Toevoegen aan deposito</button>
                    </div>
                </article>   

                <article class="tellerstand"> 
                    <h2>Tellerstand abonnement</h2>
                    <p class="p-tellerstand">Hier kunt u zien hoeveel items u nog kunt lenen met uw abonnement.</p>
                        <div class="tegoed">
                            <h3>Beschikbare uitleningen: 8 van de 20</h3>
                        </div>
                </article>
                
                <article class="printtegoed"> 
                    <h2>Printtegoed</h2>
                    <p class="p-printtegoed">Hier kunt u via IDEAL uw printtegoed opwaarderen.</p>
                    <p>Het bedrag hieronder geeft het huidige printtegoed aan.</p>
                    <div class="tegoed">
                        <h3>Printtegoed</h3>
                        <button>Printtegoed opwaarderen</button>
                    </div>
                </article>

                <article class="activiteiten"> 
                    <h2>Activiteiten</h2>
                    <p class="p-activiteiten">Onze klantenservice is bereikbaar op werkdagen van 9.00 tot 17.00 uur.</p>
                        <div class="tegoed">
                            <h3>Beschikbare activiteiten: 7 van de 10</h3>
                        </div>
                </article>

            </div>

                
        </main>

</body>
</html>

<style>
    
    *{ 
        margin: 0;
        font-family: poppins;
    }

    body{
        background: #E4E9F7;
    }

    header{
        display: flex;
        justify-content: space-between;
        margin-left: 17rem;
        margin-top: 1rem;
        padding-right: 1rem;
    }

    main{
        margin-left: 17rem;
        padding-right: 2rem;
    }

    section{
        width: 60rem;
        margin-bottom: 8rem;
        margin-top: -6rem;
    }

    img{
        height: 2rem;
    }

    ul{
        display: flex;
        list-style: none;
    }

    ul:not(:first-of-type){
        background: white;
    }

    ul:nth-last-of-type(5){
        border-top-right-radius: 1rem;
        border-top-left-radius: 1rem;
    }

    ul:last-of-type{
        border-bottom-right-radius: 1rem;
        border-bottom-left-radius: 1rem;
    }

    li{
        padding: 0.5rem 0;
        flex-basis: 100%;
    }

    .personal-info{
        display: grid;
        grid-template-rows: 1fr 1fr;
        grid-template-columns: 1fr 1fr;
        gap: 5rem;
        max-width: 50vw;
    }

    article{
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }

    .tegoed{
        display: flex;
        justify-content: space-between;
    }

    .p-depositos, .p-printtegoed{
        margin: 1rem 0 0 0;
    }

    .p-activiteiten, .p-tellerstand{
        margin: -1rem 0 0 0;
    }

    button{
        background: black;
        color: white;
        border: none;
        padding: 0 1rem;
        cursor: pointer;
    }

    .depositos p:last-of-type, .tellerstand p:last-of-type , .printtegoed p:last-of-type, .activiteiten {
        margin-bottom: 2rem;
    }

</style>