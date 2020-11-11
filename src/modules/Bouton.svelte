<script>
</script>

<style>
	.bouton {
		display: flex;
		justify-content: center;
		cursor: pointer;
		color: #725dff;
		font-weight: 600;
		letter-spacing: 0.3px;
		background-color: #dfddef;
		border-radius: 6px;
		padding: 10px 20px;
		width: max-content;
		margin-top: 20px;
		transition: 0.2s;
		user-select: none;
	}
	.bouton:hover {
		background-color: #eeedf8;
	}
	.bouton:active {
		transform: scale(0.9);
	}
</style>

<div class="bouton" on:click>
	<slot />
</div>
