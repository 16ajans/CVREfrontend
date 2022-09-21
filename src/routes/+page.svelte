<script>
	const data = {
		'Beat Saber D2': {
			Beatcats: {
				players: ['Δoctusπ', 'Punitive', 'Egg Time'],
				logo: 'https://i.imgur.com/qY5IZ7j.jpeg'
			},
			'Illini Esports': {
				players: ['BoscoStixs', 'Benjo', 'Nelson16'],
				logo: 'https://i.imgur.com/qY5IZ7j.jpeg'
			}
		},
		'Beat Saber D1': {
			'Illini Esports': {
				players: ['BoscoStixs'],
				logo: 'https://i.imgur.com/qY5IZ7j.jpeg'
			}
		}
	};
	const sample = JSON.stringify(data);
</script>

<p>var is {sample}</p>

{#each Object.keys(data) as division}
	<h2>{division}</h2>
	{#each Object.keys(data[division]) as team}
		<h3>{team}</h3>
        <img href={data[division][team].logo} alt='{team} logo'>
        <ul>
        {#each data[division][team].players as player}
        <li>{player}</li>
        {/each}
    </ul>
	{/each}
{/each}
