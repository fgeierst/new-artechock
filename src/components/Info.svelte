<script>
	export let icon = '⚠️';
</script>

<div class="disclaimer">
	<span>{icon}</span> 
	<p>
		<slot>Note this is a prototype with mockup data, visit <a href="https://www.artechock.de/">artechock.de</a> to see the real movie showtimes.</slot>
	</p>	
</div>

<style>
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
