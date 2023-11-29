<script>
      import Navigatie from "../lib/atoms/Navigatie.svelte";
</script>
<Navigatie />
<main>
<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<a href="/Uitleengeschiedenis">Uitleengeschiedenis</a>
</main>
<style>
    main{
		flex: 1;
		display: flex;
		flex-direction: column;
		width: 100%;
		margin: 0 auto;
		box-sizing: border-box;
		margin-top: 9rem;
    position: absolute;
    top: 0;
    top: 0;
    left: 250px;
    height: 100vh;
    width: calc(100% - 250px);
    transition: var(--tran-05);
    padding: 5px;
}
@media (min-width: 68em){
        main{
		margin-left: 15rem;
		margin-top: 9rem;
	} 
}
</style>