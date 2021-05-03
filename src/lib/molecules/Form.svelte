<script>
	import Button from "./../atoms/Button.svelte";
	import Input from "./../atoms/Input.svelte";
	import Toast from "./../atoms/Toast.svelte";
	export let title = "Te ayudamos a hacer realidad tus fantasías";
	export let placeholderEmail = "siddhartha@gmail.com";
	export let placeholderPostalCode = "28008";

	let email = "";
	let postalCode = "";
	let showToast = false;
	let onClick = () => console.log("click form"); 
</script>

<section>
	<div
		class="bg-white md:m-10 m-1 p-9 max-w-md rounded-2xl shadow selectDisable"
	>
		<h1 class="roboto-bold selectDisable text-2xl   text-gray-600 ">
			{title}
		</h1>

		<div class="my-3">
			<h4 class=" selectDisable my-1 text-gray-600 ">email</h4>
			<Input bind:value={email} placeholder="{placeholderEmail} " />
		</div>

		<div class="my-4">
			<h4 class="selectDisable my-1 text-gray-600 ">código postal</h4>

			<Input bind:value={postalCode} placeholder="{placeholderPostalCode} " />
		</div>
		<div class="text-right mr-8  roboto">
			<Button {onClick} type={"orange-btn"}>Únete</Button>
		</div>
	</div>
</section>
<Toast {showToast}>Información Recibida</Toast>

<style>
	.roboto {
		font-family: Roboto;
	}

	.roboto-bold {
		font-family: Roboto-Bold;
	}
</style>
