<script>
	const data = {
		'Beat Saber D2': {
			Beatcats: {
				players: ['Δoctusπ', 'Punitive', 'Egg Time'],
				logo: 'https://via.placeholder.com/100'
			},
			'Illini Esports': {
				players: ['BoscoStixs', 'Benjo', 'Nelson16'],
				logo: 'https://via.placeholder.com/100'
			}
		},
		'Beat Saber D1': {
			'Illini Esports': {
				players: ['BoscoStixs'],
				logo: 'https://via.placeholder.com/100'
			}
		}
	};

	const divisions = [{}];
	const sample = JSON.stringify(data);
</script>

<p>var is {sample}</p>
<img src="https://via.placeholder.com/100" alt="deeznuts" />

{#each Object.keys(data) as division}
	<h2>{division}</h2>
	<div class="teamFlex">
		{#each Object.keys(data[division]) as team}
			<div class="teamItem">
				<header>
					<h3>{team}</h3>
					<img src={data[division][team].logo} alt="{team} logo" />
				</header>
				<ul>
					{#each data[division][team].players as player}
						<li>{player}</li>
					{/each}
				</ul>
			</div>
		{/each}
	</div>
{/each}

<style>
	.teamFlex,
	.teamItem {
		display: flex;
		flex-direction: row;
	}
</style>
