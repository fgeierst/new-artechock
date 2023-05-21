<script>
	import Showtimes from '../../components/Showtimes.svelte';
	import { cinemas, movies } from '../../lib/data.js';	

</script>

<h1 class="visually-hidden">Movies</h1>

{#each $movies as movie}
	<h2>{movie.title}</h2>
	<ul>
		{#each movie.cinemas as cinema}
			<li>
				<h3>{cinema.name}</h3>
				<Showtimes showtimes={cinema.times} />
			</li>
		{/each}
	</ul>
{/each}

<style>
	h3 {
		margin: .5rem 0;
	}
	ul {
		list-style: none;
		margin: 0;
	}
</style>