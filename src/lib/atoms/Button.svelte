<script lang="typescript">
	export let onClick = () => console.log("click");
	export let type = ""; 
</script>

<button
	on:click={onClick}
	class=" text-white hover:bg-purple-400 active:bg-green-700 rounded-sm font-sans font-semibold bg-red-500 hover:border-gray-500 px-4 py-2 rounded-lg {type}"
	><slot /></button
>

<style>

	.nav-btn{
	color: white;
	background-color: transparent;

	}

</style>
