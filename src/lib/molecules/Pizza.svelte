<script>
	import Button from "./../atoms/Button.svelte";
	import Modal from "./Modal.svelte";
	import {europeNumbers} from "./../../scripts.ts"; 
	export let pizza = {

		img: "",
		title: "",
		price: 0,
		description: "",
	};

	export let i = 0;

	let popUp = false; 
	let popUpToogle = () => { popUp = !popUp; console.log("popUp clicked")} ; 
</script>

<div class="mx-7 bg-white bg-opacity-75  shadow bg-clip-padding mt-2 text-center  p-8" style="backdrop-filter: blur(2px)" id="pizza-{i}">
	<div class="rounded-full">
		<img   class="h-44 lg:h-50 xl:h-60" src="{pizza.img} " alt="pizza-{i}" />
		
	</div>
	<div class="mb-3">
		<h3 class="font-serif text-3xl ">{pizza.title}</h3>
		<h3 class=" text-red-500 text-1xl">{europeNumbers(pizza.price)}€</h3>
	</div>

	<Button onClick={popUpToogle} >¡Pídeme!</Button>
</div>

<Modal data={pizza} {popUp} onClick={popUpToogle} /> 
