<script>
	// @ts-nocheck

	import html2canvas from 'html2canvas';

	let handleClick = () => {
		console.log('hello');

		const element = document.querySelector('#text');
		const scale = 4; // Increase scale value for higher quality

		setTimeout(() => {
			html2canvas(element, { scale }).then((canvas) => {
				const dataURL = canvas.toDataURL('image/png');
				const link = document.createElement('a');
				link.href = dataURL;
				link.download = `${element.innerText}.png`;
				link.click();
			});
		}, 500);
	};
</script>

<button id="download" on:click={handleClick}>Download</button>

<style>
	#download {
		background-color: darkred;
		color: whitesmoke;
		width: fit-content;
		height: fit-content;
		padding: 15px;
		border: solid;
		border-color: darkred;
		border-radius: 10px;
		font-size: 1em;
		display: none;
	}
	#download:hover {
		cursor: pointer;
		background-color: whitesmoke;
		color: darkred;
	}
</style>
