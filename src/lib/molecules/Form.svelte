<script>
	import Button from './../atoms/Button.svelte';
	import Input from './../atoms/Input.svelte';
	import { v4 as uuidv4 } from 'uuid';
	import Toast from "./../atoms/Toast.svelte"; 
	import {db} from "./../../firebase.js"; 

	export let title = "Te ayudamos a hacer realidad tus fantasías"

	let userDataObject = { id: '', email: '', postalCode: '', time: "" };
	let { id, email, postalCode, time } = userDataObject;
	const timeElapsed = Date.now();
	const today = new Date(timeElapsed);

let showToast = false;  

	const changeToast = () => {
		showToast = !showToast;
		setTimeout(() => (showToast = !showToast), 2000);
	};

	let onClick = () => {
		id = uuidv4();
		time =  today.toUTCString();  
		if(email){
		db.collection("leads").doc(id).set({id, email, postalCode, time})
		
		changeToast(); 
		email = '';
		postalCode = ''; 

		}
	};


	export let placeholderEmail = "siddhartha@gmail.com"; 

	export let placeholderPostalCode = "28008"; 
</script>
<style>
	.maxwd{
			max-width: 26rem;
	}

	.roboto {
		font-family: Roboto;
	}

	.roboto-bold {
		font-family: Roboto-Bold;
	}
</style>
<section>
		<div class="bg-white md:m-10 m-1 p-9 max-w-md rounded-2xl shadow selectDisable">
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
				<Button {onClick} type={'orange-btn'}>Únete</Button>
			</div>
		</div>
</section>
	<Toast {showToast} >Información Recibida</Toast> 

