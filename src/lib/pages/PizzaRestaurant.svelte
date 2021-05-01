<script lang="typescript">
	import Bar from "./../atoms/Bar.svelte";
	import Header from "./../organisms/Header.svelte";
	import PizzaGrid from "./../organisms/PizzaGrid.svelte";
	const titular = {
		headline: "Pizzería Diavole",
		title: "El hogar de la pizza más cremosa y picante",
		img: "/static/diablo.png",
	};
</script>

<main class="lg:pb-4 xl:pb-80 pb-9">
	<Bar position="top" color="red" />
	<Header {titular}>
		<p>
			Que aburrimiento comer siempre la misma pizza fría todos los días. <br /> ¿Por
			qué no te atreves a probar una de nuestras pizzas? pero Shhh! sólo comparte
			el secreto con comensales de confianza.
		</p>
	</Header>
	<PizzaGrid />
	<Bar position="bottom" color="green" />
</main>

<style>

main {
	background: url(/static/foodpatterns.svg);
	background-repeat: repeat;
	background-size: 12rem;
	height: 100%;
	}

</style>
