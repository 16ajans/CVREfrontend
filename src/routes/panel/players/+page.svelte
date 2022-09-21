<script>
	import PlayerMod from '$lib/PlayerMod.svelte';
</script>

<h1>Welcome to the player section of the captain panel!</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<aside>
	<PlayerMod />
</aside>

<style>
	aside {
		position: fixed;
		right: 0;
		width: 250px;
	}
</style>
