<script>
	import Download from '../components/Download.svelte';
	import Generate from '../components/Generate.svelte';
	import Input from '../components/Input.svelte';
	import Footer from '../components/layout/Footer.svelte';
	import Header from '../components/layout/Header.svelte';
</script>

<Header />
<section class="content" id="container">
	<Input />
	<div class="btns">
		<Generate />
		<Download />
	</div>
</section>
<Footer />

<style>
	.content {
		width: fit-content;
		height: fit-content;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		padding: 50px;
		gap: 15px;
		margin-top: 7%;
	}
	.btns {
		display: flex;
		flex-direction: row;
		gap: 30px;
	}
	/* For desktop: */
	@media only screen and (min-width: 768px) {
		.content {
			flex-direction: row;
			margin-top: 5%;
		}
		.btns {
			gap: 15px;
		}
	}
</style>
