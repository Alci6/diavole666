<script>
	import Button from "./../atoms/Button.svelte";
	import Selector from "./../atoms/Selector.svelte";
	import { europeNumbers } from "./../../scripts.ts";
	import DescriptionText from "./../atoms/DescriptionText.svelte";
	import { dungeonAccess } from "./../../stores/enterDungeon.ts";
	export let data = {
		img: "",
		title: "",
		price: 0,
		description: "",
	};

	let {img, title, price, description} = data; 
export let i = 0;
	export let popUp = false;
	export let onClick = () => console.log("click");
	export const dungeonOpen = () =>
		title == "Diavole" ? ($dungeonAccess = true) : "";
</script>

<div class={popUp ? "show" : "hide"} id="pizza-info-{i}">
	<div
		class="modal m-1/2 max-w-md mx-auto bg-white rounded-xl shadow-md overflow-hidden md:max-w-2xl"
	>
		<div class="md:flex">
			<div class="md:flex-shrink-0 flex">
				<img
					class="h-48 w-full self-center object-cover md:w-48 "
					src={img}
					alt="imagen-{i}"
				/>
			</div>
			<div class="p-8 bg-gradient-to-r from-gray-200">
				<button on:click={onClick} class="float-right ">X</button>
				<div class=" tracking-wide text-sm text-red-500 font-semibold">
					{europeNumbers(price)} €
				</div>
				<p
					class="block mt-1 text-2xl leading-tight font-medium text-black font-serif"
				>
					{title}
				</p>

				<div class="my-3">
					<div class="inline-block mr-4">
						<Selector />
					</div>
					<div class="inline-block">
						<Button onClick={dungeonOpen}>¡Hornear!</Button>
					</div>
				</div>
				<p class="mt-2 text-gray-500">
					<DescriptionText>{description}</DescriptionText>
				</p>
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
		left: 0;
		right: 0;
		top: 15%;
		margin: auto;
	}
</style>
