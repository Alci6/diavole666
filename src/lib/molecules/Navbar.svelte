<script>
	import Button from "./../atoms/Button.svelte";
</script>

<nav class="p-3 ">
	<div class="table-cell align-middle " title="Home">
		<img src="img/diavole.svg" alt="Diavole Logo" />
	</div>
	<div class="table-cell align-middle  w-10/12 text-right  selectDisable ">
		<a
			class="hover:underline text-white text-md"
			href="#information"
			title="más información"
		>
			¿En que consiste?
		</a>
		<a href="#formulario">
			<Button href="#formulario" type={"nav-btn"}>¡Apúntate!</Button>
		</a>
	</div>
</nav>

<style>
	nav {
		display: table;
		width: 100%;
	}
</style>
