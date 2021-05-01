<script lang="typescript">
	import Pizza from "../molecules/Pizza.svelte";

	const pizzas = [
		{
			img: "/static/diablo.png",
			title: "Peperonni",
			price: 13,
		},
		{ img: "/static/diablo.png", title: "Carbonara", price: 13 },
	];
</script>

<div class=" grid grid-rows-2 grid -flow-col gap-4">
	{#each pizzas as pizza, i}
		<Pizza {pizza} {i} />
	{/each}
</div>
