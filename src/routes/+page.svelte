<script>
	import Cinema from '../components/Cinema.svelte';
	import Info from '../components/Info.svelte';
	import { data } from '../lib/data.js';

</script>

<h1>Munich Movie Showtimes</h1>

<Info icon="⚠️">Note this is a prototype with mockup data, visit <a href="https://www.artechock.de/">artechock.de</a> to see the real movie showtimes.</Info>

<div class="cinema-list">
	{#each data[0].cinemas as cinema}
		<Cinema {cinema} />
	{/each}
</div>

<style>
	
</style>