<script>
	import Generate from '../components/Generate.svelte';
	import Input from '../components/Input.svelte';
	import Footer from '../components/layout/Footer.svelte';
	import Header from '../components/layout/Header.svelte';
</script>

<Header />
<section class="content" id="main">
	<Input />
	<Generate />
</section>
<Footer />

<style>
	.content {
		width: fit-content;
		height: fit-content;
		padding: 50px;
		display: flex;
		flex-direction: row;
		align-items: center;
		gap: 50px;
		margin-top: 120px;
	}
</style>
