<script>
	import Button from "./../atoms/Button.svelte";
	import Selector from "./../atoms/Selector.svelte";
	import { europeNumbers } from "./../../scripts.js";
	import DescriptionText from "./../atoms/DescriptionText.svelte";
	export let pizza = {
		img: "",
		title: "",
		price: 0,
		description: "",
	};
	export let i = 0;
	export let popUp = false;
	export let onClick = () => console.log("click");
</script>

<div class={popUp ? "show" : "hide"} id="pizza-info-{i}">
	<div class="modal rounded-2xl h-96 grid grid-cols-2 ">
		<div class="h-full   grid justify-items-center ">
			<img
				class=" m-auto align-baseline inline-block h-80 rounded-full"
				src={pizza.img}
				alt=""
			/>
		</div>
		<div class="h-full bg-gradient-to-r from-gray-200  via-white rounded-r-2xl">
			<button on:click={onClick} class="float-right m-4 ">X</button>
			<div class="mt-10 ml-10">
				<h1 class=" font-serif text-4xl">
					{pizza.title}
				</h1>
				<h2 class="text-red-600 text-2xl font-mono">
					{europeNumbers(pizza.price)}€
				</h2>
			</div>

			<div class=" m-10">
				<div class="inline-block mr-4">
					<Selector />
				</div>
				<div class="inline-block">
					<Button>¡Hornear!</Button>
				</div>

				<div class="mt-5">
					<DescriptionText>{pizza.description}</DescriptionText>
				</div>
			</div>
		</div>
	</div>
</div>






<style>
	.hide {
		display: none;
	}

	.show {
		position: fixed;
		background-color: rgba(0, 0, 0, 0.6);
		z-index: 1;
		padding-top: 100%;
		left: 0;
		top: 0;
		width: 100%;
		height: 100%;
	}
	.modal {
		transition: opacity 0.25s ease;
		background: #fefefe;
		position: absolute;
		left: 15%;
		top: 15%;
		width: 56em;
	}
</style>
