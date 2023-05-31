<script>
	import Generate from '../components/Generate.svelte';
	import Input from '../components/Input.svelte';
	import Footer from '../components/layout/Footer.svelte';
	import Header from '../components/layout/Header.svelte';
</script>

<Header />
<section class="content">
	<Input />
	<Generate />
</section>
<Footer />

<style>
	.content {
		height: 80vh;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		gap: 30px;
		width: 100%;
	}
	/* For desktop: */
	@media only screen and (min-width: 768px) {
		.content {
			height: 90vh;
			gap: 30px;
		}
	}
</style>
