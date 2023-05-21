<script>
	import Cinema from '../components/Cinema.svelte';
	import { data } from '../lib/data.js';

</script>

<h1>Munich Movie Showtimes</h1>
<div class="disclaimer">
	<span>⚠️</span> 
	<p>
		Note this is a prototype with mockup data, visit <a href="https://www.artechock.de/">artechock.de</a> to see the real movie showtimes.
	</p>	
</div>

<div class="cinema-list">
	{#each data[0].cinemas as cinema}
		<Cinema {cinema} />
	{/each}
</div>

<style>
	a {
		color: inherit;
	}
	.disclaimer {
		color: blue;
		border: 3px dashed blue;
		padding: 1rem;
		display: inline-flex;
		gap: .75rem;
		align-items: center;
	}

	.disclaimer span {
		font-size: 150%;
	}

	.disclaimer p {
		margin: 0	;
	}
</style>