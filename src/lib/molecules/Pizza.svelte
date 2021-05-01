<script>
	export let pizza = {
		img: "",
		title: "",
		price: 0,
	};

	export let i = 0;
</script>

<div class="flex items-center bg-red-300 max-w-sm" id="pizza-{i}">
	<img src="{pizza.img} " alt="pizza-{i}" />
	<div>
		<h3 class="inline">{pizza.title}</h3>
		<h3 class="inline">{pizza.price}€</h3>
	</div>
</div>
