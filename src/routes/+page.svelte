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
	<Generate />
	<Download />
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
		gap: 15px;
		margin-top: 5%;
	}
</style>
