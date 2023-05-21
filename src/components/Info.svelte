<script>
	export let icon = 'ℹ️';
</script>

<div class="disclaimer">
	<span>{icon}</span> 
	<p>
		<slot />
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
