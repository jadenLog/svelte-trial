<script lang="ts">
    export let name: string;
    export let score: number;

    const addScore = () => { score += 1; };
    const subtractScore = () => { score -= 1; };
</script>

<style>
    div {
        border: 1px solid gray;
        margin: 0 auto 10px auto;
        max-width: 600px;
    }
    div:last-child {
        margin-bottom: 0px;
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