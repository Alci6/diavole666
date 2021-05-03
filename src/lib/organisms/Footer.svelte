<script>

	import Form from './../molecules/Form.svelte';

</script>

<style>
	.pattern{
	background-color: black; 
	background-image: url(/img/pattern.svg);
	
	}
		
</style>

<div class="p-2  pattern" id="formulario">
	<div class=" mx-auto max-w-max ">
			<Form placeholderEmail="grey@gmail.com" placeholderPostalCode="28050" title={"¡Apúntate ya a la beta privada!"} />
	</div>		
</div>



