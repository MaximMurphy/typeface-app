<script>
	// @ts-nocheck

	let text = '';
	const handleInput = () => {
		document.querySelector('#text').style.display = 'none';
		document.querySelector('#download').style.display = 'none';
	};
</script>

<form action="">
	<input id="input" placeholder="Enter text here..." bind:value={text} on:input={handleInput} />
</form>

<p id="text">{text}</p>

<style>
	#text {
		display: none;
		margin-left: auto;
		margin-right: auto;
		flex-direction: column;
		font-weight: bold;
		text-align: center;
		width: 300px;
		height: 300px;
		font-size: 4.5em;
		border: solid 2px blue;
	}
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
		#text {
			width: 500px;
			height: 500px;
			font-size: 7em;
		}
	}
	input:focus {
		outline: none;
		border-color: red;
	}
</style>
