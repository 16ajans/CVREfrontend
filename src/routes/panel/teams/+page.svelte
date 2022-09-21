<script>
	import TeamMod from '$lib/TeamMod.svelte';

    let modMenu;
    let displayMod = false;
    export function toggleMod() {
        if (displayMod) {
            modMenu.style.width = '0';
        } else modMenu.style.width = '250px';
        displayMod = !displayMod;
    }
</script>

<h1>Welcome to the team section of the captain panel!</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<button on:click={toggleMod}>Toggle Mod</button>

<aside bind:this={modMenu}>
	<TeamMod on:hide={toggleMod}/>
</aside>

<style>
	aside {
		position: fixed;
		right: 0;
		height: 100%;
		width: 0;
		z-index: 1;
		top: 0;
		overflow-x: hidden;
		transition: 0.25s;
	}
</style>
