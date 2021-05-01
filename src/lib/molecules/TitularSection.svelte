<script lang="typescript">
	export let titular = {
		headline: "Transactions",
		title: "A better way to send money",
		img: "/static/diablo.png", 
	};

</script>

<div class="py-12 bg-white ">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="lg:text-center md:text-center">
			<h2
				class="text-center text-base text-red-600 font-serif tracking-wide uppercase"
			>
				<img class="w-8 inline" src="{titular.img}" alt="">

				{titular.headline}

				<img  class="w-8 inline" src= "/static/diablo.png" alt=""> 
			</h2>
			<p
				class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl"
			>
				{titular.title}
			</p>
			<p class="mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto md:mx-auto">
				<slot/>
			</p>
		</div>
	</div>
</div>
