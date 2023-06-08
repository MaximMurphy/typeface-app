<script>
	// @ts-nocheck

	const getRandomColor = () => {
		const letters = '0123456789ABCDEF';
		let color = '#';
		for (let i = 0; i < 6; i++) {
			color += letters[Math.floor(Math.random() * 16)];
		}
		return color;
	};

	const addRandomColorsToWords = (words) => {
		let formattedText = '';

		for (let i = 0; i < words.length; i++) {
			const word = words[i];
			const color = getRandomColor();
			formattedText += `<span style="color: ${color}">${word}</span> `;
		}

		return formattedText;
	};

	const handleClick = () => {
		const textElement = document.querySelector('#text');
		const containerElement = document.querySelector('#container');

		const inputText = document.querySelector('#input').value;
		const formattedText = addRandomColorsToWords(inputText.split(' '));

		textElement.innerHTML = formattedText.trim();
		textElement.style.display = 'block';
		document.querySelector('#download').style.display = 'flex';

		containerElement.parentNode.insertBefore(textElement, containerElement.nextSibling);
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
