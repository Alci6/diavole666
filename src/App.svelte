<script lang="typescript">
	import PizzaRestaurant from "./lib/pages/PZ_Home.svelte";
	import Dreams from "./lib/pages/Dreams.svelte"	
	import {dungeonAccess} from "./stores/enterDungeon.ts"
</script>

{#if $dungeonAccess}
	<Dreams/>
	{:else}
<PizzaRestaurant />
{/if}
