

<div class="wrapper">
	<Header></Header>
	<Main></Main>
	<Footer></Footer>
</div>

<script>
	import Header from "./header/Header.svelte";
	import Main from "./main/Main.svelte";
	import Footer from "./footer/Footer.svelte";
</script>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>