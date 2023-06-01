<script>
	// @ts-nocheck

	import html2canvas from 'html2canvas';

	let handleClick = () => {
		console.log('hello');

		const element = document.querySelector('#everything');
		const scale = 2; // Increase scale value for higher quality

		setTimeout(() => {
			html2canvas(element, { scale }).then((canvas) => {
				const dataURL = canvas.toDataURL('image/png');
				const link = document.createElement('a');
				link.href = dataURL;
				link.download = 'screenshot.png';
				link.click();
			});
		}, 500);
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
		border-color: red;
		border-radius: 10px;
		font-size: 1em;
	}
	button:hover {
		cursor: pointer;
		background-color: whitesmoke;
		color: red;
	}
</style>
