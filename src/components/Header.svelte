<script>
	import { page } from '$app/stores';
	let items = [
		{
			href: '/',
			title: 'Cinemas'
		},
		{
			href: '/movies',
			title: 'Movies'
		},
	]
</script>

<header>
	<a class="page-title" href="/">Munich Movie Showtimes</a>

	<nav>
		{#each items as { href, title } }
			<a {href} aria-current={$page.url.pathname === href ? 'page' : undefined}>{title}</a>
		{/each}
	</nav>

</header>

<style>
	.page-title {
		display: block;
		font-size: 2em;
		margin-block-start: 0.67em;
		margin-block-end: 0.67em;
		text-decoration: none;
	}

	nav {
		display: flex;
		gap: .2em;
		font-size: 2em;
	}

	a {
		text-decoration: none;
		border: 2px solid;
		border-color: transparent;
		padding: 0 .2em;
	}

	[aria-current='page'] {
		border-color: black;
	}
</style>
