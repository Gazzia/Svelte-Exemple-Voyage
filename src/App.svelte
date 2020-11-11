<script>
	import Button from "./modules/Bouton.svelte";
	import Voyage from "./modules/Voyage.svelte";
	import {voyages} from "./voyages.js";

	let voyageActuel = false;

	function voyager() {
		//sélectionne un voyage au hasard et l'affecte à la variable voyageActuel
		voyageActuel = voyages[Math.floor(Math.random() * voyages.length)];
	}
</script>

<style>
	main {
		text-align: center;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}

	h1 {
		color: #93593c;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 900;
		margin: 0;
		font-family: "Poppins", sans-serif;
	}
</style>

<main>
	<h1>Aventurier !</h1>
	<p>Quelle sera votre prochaine destination ?</p>
	<p>Actuellement :</p>
	{#if !voyageActuel}
		<span>Vous êtes tranquillement chez vous, dans la douceur du foyer..</span>
	{:else}
		<Voyage {...voyageActuel} />
	{/if}
	<Button on:click={voyager}>Prendre l'avion ✈</Button>
</main>
