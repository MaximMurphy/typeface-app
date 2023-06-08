<script>
	// @ts-nocheck

	let handleClick = () => {
		const newElement = document.querySelector('#text');
		const containerElement = document.querySelector('#container');

		document.querySelector('#text').style.display = 'block';
		document.querySelector('#download').style.display = 'flex';
		containerElement.parentNode.insertBefore(newElement, containerElement.nextSibling);
	};
</script>

<button id="generate" on:click={handleClick}>Generate</button>

<style>
	button {
		background-color: red;
		color: whitesmoke;
		width: fit-content;
		height: fit-content;
		padding: 15px;
		border: solid;
		border-color: red;
		border-radius: 10px;
		font-size: 1em;
	}
	button:hover {
		cursor: pointer;
		background-color: whitesmoke;
		color: red;
	}
	/* For desktop: */
	@media only screen and (min-width: 768px) {
		button {
			margin-left: 25px;
		}
	}
</style>
