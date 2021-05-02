<script lang="typescript">
	export let onClick = () => console.log("click");
</script>

<button
	on:click="{onClick}"
	class=" hover:bg-purple-400 active:bg-green-700 text-white rounded-sm font-sans font-semibold bg-red-500 hover:border-gray-500 px-4 py-2 rounded-lg"

	><slot /></button
>
