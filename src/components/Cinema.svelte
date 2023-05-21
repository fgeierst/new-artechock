<script>
	import Movie from './Movie.svelte';
	export let cinema;
</script>

<h2>{cinema.name}</h2>

<ul class="movies">
	{#each cinema.movies as movie}
		<li>
			<Movie {movie} />
		</li>
	{/each}
</ul>

<style>
	.movies {
		list-style: none;
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}
</style>