<script lang="ts">
    export let name: string;
    export let score: number;

    const addScore = () => { score += 1; };
    const subtractScore = () => { score -= 1; };
</script>

<style>
    div {
        max-width: 600px;
        margin: 0 auto;
        border: 1px solid gray;
    }
    h1 {
        font-weight: bold;
    }
</style>

<div>
    <h1>{name}</h1>
    <p>{score}</p>
    <button type="button" on:click={addScore}>+</button>
    <button type="button" on:click={subtractScore}>-</button>
</div>