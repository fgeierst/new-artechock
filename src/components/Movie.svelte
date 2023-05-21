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
				<span class="time">{time}</span>
			{/each}
		</li>
		{/if}
	{/each}
</ul>

<style>
	h3 {
		margin: 0 0 .5rem 0;
	}

	.times {
		list-style: none;
		padding: 0;
		margin: 0;
		display: flex;
		flex-wrap: wrap;
		gap: .5em 1em;
	}

	.time {
		border: 1px solid;
		border-radius: .3em;
		padding: 0 .2em;
		margin-inline-end: .2em;
	}

</style>