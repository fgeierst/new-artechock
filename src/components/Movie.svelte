<script>
	import Showtimes from "./Showtimes.svelte";
	export let movie;
</script>

<h3>{movie.title}</h3>

<Showtimes showtimes={movie.times} />


<style>
	h3 {
		margin: 0 0 .5rem 0;
	}

</style>