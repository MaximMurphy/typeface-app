<script>
	let handleClick = () => {
		console.log('hello');
	};
</script>

<button on:click={handleClick}>Generate</button>

<style>
	button {
		background-color: red;
		color: whitesmoke;
		width: fit-content;
		height: fit-content;
		padding: 15px;
		border: solid;
		border-color: whitesmoke;
		border-radius: 10px;
		font-size: 1em;
	}
	button:hover {
		cursor: pointer;
		opacity: 70%;
	}
	/* For desktop: */
	@media only screen and (min-width: 768px) {
		button {
			width: 10%;
			font-size: 1em;
		}
	}
</style>
