<script lang="typescript">
	export let onClick = () => console.log("click");
</script>

<button
	on:click="{onClick}"
	class="border-2 rounded-sm border-black-500 bg-green-50 hover:border-gray-500 px-4 py-2"
	><slot /></button
>
