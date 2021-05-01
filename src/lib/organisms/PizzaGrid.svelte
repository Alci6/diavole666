<script lang="typescript">
	import Pizza from "../molecules/Pizza.svelte";

	const pizzas = [
		{ img: "/static/pizza-peperonni.png", title: "Peperonni", price: 12.95 },

		{ img: "/static/pizza-diavola.png", title: "Diavola", price: 13.69 },
		{ img: "/static/pizza-carbonara.png", title: "Carbonara", price: 12.95 },
	];
</script>

<div class="mb-7 mt-8">
	<div class=" gap-8 justify-center flex flex-wrap items-center">
		{#each pizzas as pizza, i}
			<Pizza {pizza} {i} />
		{/each}
	</div>
</div>
