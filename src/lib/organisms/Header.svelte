<script>
	import TitularSection from "./../molecules/TitularSection.svelte";
	export let titular = {};
</script>

<header class="shadow-xl">
	<TitularSection {titular}>
		<slot />
	</TitularSection>
</header>
