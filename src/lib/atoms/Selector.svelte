<script>
	export let number = 1;

	const sum = () => (number < 9 ? (number += 1) : (number = 9));
	const sub = () => (number > 1 ? (number -= 1) : (number = 1));
</script>

<button on:click={sub} class="rounded-l-lg p-2 bg-white">-</button>
<input class="w-10 p-2 text-center bg-white" type="number" bind:value={number} />
<button on:click={sum} class="rounded-r-lg p-2 bg-white">+</button>

<style>
	/* Chrome, Safari, Edge, Opera */
	input::-webkit-outer-spin-button,
	input::-webkit-inner-spin-button {
		-webkit-appearance: none;
		margin: 0;
	}

	/* Firefox */
	input[type="number"] {
		-moz-appearance: textfield;
	}
</style>
