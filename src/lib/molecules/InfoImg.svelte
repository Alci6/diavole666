<script>
	import Article from "./../atoms/Article.svelte";
	import Ilustration from "./../atoms/Ilustration.svelte";

	export let copyText;
	export let img;
	export let order = "left";
</script>

{#if order == "left"}
	<div class="md:flex flex-row-reverse max-w-4xl mx-auto my-9 ">
		<div class="md:w-10/12 ">
			<Article {copyText} />
		</div>
		<div />
		<div class="md:w-10/12">
			<Ilustration {img} />
		</div>
	</div>
{:else if order == "right"}
	<div class="md:flex max-w-4xl mx-auto my-9 ">
		<div class="md:w-10/12">
			<Article {copyText} />
		</div>
		<div />
		<div class="md:w-10/12">
			<Ilustration {img} />
		</div>
	</div>
{/if}


