<script lang="ts">
	import Player from './Player.svelte';

	const players = [
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
</script>

<style>
	main {
		text-align: center;
		padding: 1em;
		margin: 0 auto;
	}
</style>

<main>
	{#each players as player}
		<Player name={player.name} score={player.score} />
	{/each}
</main>