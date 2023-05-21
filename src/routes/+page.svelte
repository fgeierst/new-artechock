<script>
	import Cinema from '../components/Cinema.svelte';
	import { cinemas } from '../lib/data.js';

</script>

<h1 class="visually-hidden">Cinemas</h1>


<div class="cinema-list">
	{#each $cinemas as cinema}
		<Cinema {cinema} />
	{/each}
</div>



<style>
	
</style>