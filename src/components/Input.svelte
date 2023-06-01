<script>
	let text = '';
</script>

<form action=""><input id="input" placeholder="Enter text here..." bind:value={text} /></form>

<style>
	form {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}
	input {
		width: fit-content;
		height: fit-content;
		text-align: start;
		padding: 20px;
		font-size: 1.25em;
		border: solid;
		border-radius: 10px;
		border-color: whitesmoke;
		border-width: thin;
	}
	/* For desktop: */
	@media only screen and (min-width: 768px) {
		input {
			width: 100%;
			font-size: 2em;
		}
	}
	input:focus {
		outline: none;
		border-color: red;
	}
</style>
