<script>
    
</script>

<section>

    <!-- DESKTOP -->
    <details class="desktop">
        <summary> Hulp nodig? </summary>
        <summary> Sluit chat </summary>
        
        <div class="chat">
            
            <h3>Vragen over je betalingen?</h3>  
            
            <div class="conversation">
                <article class="received">
                    <p>Hoi! Ik ben de chatbot van oba.nl. Waar kan ik je mee helpen?</p>
                </article>
                <article class="sent">
                    <p>Hoe kan ik het tegoed van mijn pas opwaarderen?</p>
                </article>
                <article class="received">
                    <p>Hoi! Ik ben de chatbot van oba.nl. Waar kan ik je mee helpen?</p>
                </article>
                <article class="sent">
                    <p>Hoe kan ik het tegoed van mijn pas opwaarderen?</p>
                </article>
            </div>
            
            <div>
                <input type="text" placeholder="Typ hier je vraag">
                <button type="button">
                    <img src="src/lib/assets/send.svg" height="24" width="24" alt="stuur bericht" loading="lazy">
                </button>  
            </div>  
            
            
        </div>
        
    </details>

    <!-- MOBILE -->
    <details open class="mobile">
        <summary> Hulp nodig? </summary>
        <summary> Sluit chat </summary>
        
        <div class="chat">
            
            <h3>Vragen over je betalingen?</h3>  
            
            <div class="conversation">
                <article class="received">
                    <p>Hoi! Ik ben de chatbot van oba.nl. Waar kan ik je mee helpen?</p>
                </article>
                <article class="sent">
                    <p>Hoe kan ik het tegoed van mijn pas opwaarderen?</p>
                </article>
                <article class="received">
                    <p>Hoi! Ik ben de chatbot van oba.nl. Waar kan ik je mee helpen?</p>
                </article>
                <article class="sent">
                    <p>Hoe kan ik het tegoed van mijn pas opwaarderen?</p>
                </article>
            </div>
            
            <div>
                <input type="text" placeholder="Typ hier je vraag">
                <button>
                    <img src="src/lib/assets/send.svg" height="24" width="24" alt="stuur bericht" loading="lazy">
                </button>  
            </div>  
            
            
        </div>
        
    </details>


</section>

<style>

    section{
        display: flex;
        flex-direction: column;
        justify-content: space-between;

        width: 33vw;
        height: 75vh;
    }

    .desktop{
        display: none;
    }

    details{
        border: solid black 0.2rem;
        background: #E3E9F9;
    }

    details summary {
        cursor: pointer;
        transition: margin 150ms ease-out;
    }

    details[open] summary {
        margin-bottom: 1rem;
        font-size: 0;
    }

    details[open] h3 {
        margin: -2rem 0 1rem 1rem;
    }
    
    details[open] summary::marker {
        font-size: initial;
    }

    summary{
        user-select: none;
    }

    div{
        display: flex;
        justify-content: space-between;
        padding: 0 1rem 1rem 1rem;
    }

    .chat{
        padding: 0;
        display: block;
    }

    .conversation{
        flex-direction: column;
        font-size: 0.9rem;
    }

    article{
        display: inline-block;
        background: #F5F5F5;
        border-radius: 0.5rem;
        padding: 1rem;
        margin-bottom: 1rem;
    }

    .received{
        max-width: 70vw;
    }

    .sent{
        margin-left: 10vw;
    }

    button{
        border: none;
        background: transparent;
    }

    input{
        border-radius: 0.5rem;
        border: none;
        width: 80vw;
        text-indent: 1rem;
    } 

@media only screen and (max-width: 770px) {

    section{
        width: 100vw;
        height: 100vh;
    }

    .mobile{
        display: block;
    }

    .desktop{
        display: none;
    }
    
    details[open] summary {
        display: none;
    }

    details[open] h3 {
        margin: 1rem 0 1rem 1rem;
    }
}


</style>