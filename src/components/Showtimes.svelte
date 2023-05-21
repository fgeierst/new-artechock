<script>
	export let showtimes;
</script>

<ul class="times">
	{#each Object.entries(showtimes) as [day, times]}
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