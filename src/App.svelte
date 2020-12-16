<script lang="ts">
	import Player from './Player.svelte';

	let players = [
		{
			name: 'Jaden',
			score: 10,
		},
		{
			name: 'Cheonho',
			score: 20,
		},
		{
			name: 'Ian',
			score: 20,
		},
		{
			name: 'Eunji',
			score: 30,
		},
		{
			name: 'Sunmin',
			score: 40,
		},
		{
			name: 'JYP',
			score: 50,
		},
	];

	let newPlayer = {
		name: '',
		score: 0,
	};

	const handleNameChange = (event) => { // TODO: find event type
		newPlayer = {
			...newPlayer,
			name: event.target.value,
		};
	};

	const handleScoreChange = (event) => { // TODO: find event type
		newPlayer = {
			...newPlayer,
			score: event.target.value,
		};
	};

	const handleAddPlayer = () => {
		players = [
			...players,
			newPlayer
		];
		newPlayer = {
			name: '',
			score: 0,
		};
	};
</script>

<style>
	main {
		text-align: center;
		padding: 1em;
		margin: 0 auto;
	}
</style>

<main>
	<input aria-label="name" type="text" placeholder="name" value={newPlayer.name} on:change={handleNameChange}/>
	<input aria-label="score" type="number" placeholder="score" value={newPlayer.score} on:change={handleScoreChange}/>
	<button type="button" on:click={handleAddPlayer}>Add Player</button>
	{#each players as player}
		<Player name={player.name} score={player.score} />
	{/each}
</main>