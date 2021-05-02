<script lang="typescript">
	import PizzaRestaurant from "./lib/pages/PizzaRestaurant.svelte";
	import Dreams from "./lib/pages/Dreams.svelte"	
	import {dungeonAccess} from "./stores/enterDungeon.js"
</script>

{#if $dungeonAccess}
	<Dreams/>
	{:else}
<PizzaRestaurant />
{/if}
