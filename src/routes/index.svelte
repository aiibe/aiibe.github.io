<script>
	import { title, projects } from '../../raw/site.json';
	import Logo from '$lib/Logo.svelte'
</script>

<svelte:head>
	<title>{title}</title>
</svelte:head>

<nav>
	<div>
		<Logo />
	</div>
</nav>

<div>
	<h2>Projects</h2>
	<ul>
		{#each projects as { name }}
			<li>{name}</li>
		{/each}
	</ul>
</div>
