<script>
	export let movie;
</script>

<h3>{movie.title}</h3>

<ul class="times">
	{#each Object.entries(movie.times) as [day, times]}
		<!-- if times not empty -->
		{#if times.length > 0}			
		<li>
			{day.substring(0, 2).toUpperCase()}

			{#each times as time}
				{time} 
			{/each}
		</li>
		{/if}
	{/each}
</ul>

<style>
	h3 {
		margin: 0;
	}
	.times {
		list-style: none;
		padding: 0;
		margin: 0;
		display: flex;
		gap: 1rem;
	}
</style>