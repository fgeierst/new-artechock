<script>
	import Info from '../components/Info.svelte';
	import Header from '../components/Header.svelte';
	import './styles.css';
</script>

<div class="app">
	<Info />

	<Header />

	<main>
		<slot />
	</main>

</div>

