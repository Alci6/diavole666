<script lang="typescript">
	import Header from "./../organisms/Header.svelte";
	import PizzaGrid from "./../organisms/PizzaGrid.svelte"; 
	const titular = {
		headline: "Pizzería Diavole",
		title: "El hogar de la pizza más cremosa y picante",
		content:
			"Que aburrimiento comer siempre la misma pizza fría de todos los días, por qué no te atreves a probar una de nuestras pizzas, pero Shhh! sólo comparte el secreto con comensales de confianza.",
	img: "/static/diablo.png", 

	};
</script>

<Header {titular} />
<PizzaGrid/>
