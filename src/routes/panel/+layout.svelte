<nav>
	<a href="/panel/players">Players</a>
	<a href="/panel/teams">Teams</a>
</nav>
<div>
	<slot />
</div>

<style>
	nav {
		height: 100%;
		position: fixed;
		width: 250px;
        left: 0;
	}
	div {
		margin-left: 250px;
	}
</style>
