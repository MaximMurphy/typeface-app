<script>
	let text = '';
</script>

<form action=""><input id="input" placeholder="Enter text here.." bind:value={text} /></form>
{@html text}

<style>
	form {
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	input {
		width: 30%;
		height: 100px;
		text-align: start;
		margin: 50px 0px 50px 0px;
		padding: 5px;
		font-size: 2em;
	}
	input:focus {
		outline: none;
		border-color: red;
	}
</style>
