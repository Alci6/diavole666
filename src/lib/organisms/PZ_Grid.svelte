<script lang="typescript">
	import Pizza from "../molecules/Pizza.svelte";
	import { pizzas } from "./../../stores/pizzaStore";
</script>

<div class="mb-7 mt-8">
	<div class=" justify-center flex flex-wrap items-center">
		{#each pizzas as pizza, i}
			<Pizza {pizza} {i} />
		{/each}
	</div>
</div>
