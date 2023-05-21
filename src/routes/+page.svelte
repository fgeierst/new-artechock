<script>
	import Cinema from '../components/Cinema.svelte';
	import { data } from '../lib/data.js';

</script>

<h1>Munich Movie Showtimes</h1>

<div class="cinema-list">
	{#each data[0].cinemas as cinema}
		<Cinema {cinema} />
	{/each}
</div>
