<script>
	export let paysPrefix;
	export let pays;
	export let phrase;
</script>

<style>
	.pays {
		font-weight: bold;
		display: inline;
		color: #93593c;
	}
</style>

<div class="voyage">
	Vous êtes
	{paysPrefix}
	<div class="pays">{pays}</div>, pour
	{phrase}.
</div>
