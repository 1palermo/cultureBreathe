<script>
	import Accordion from '$lib/Accordion.svelte';
	import Header from '$lib/components/Home/Header.svelte';
	import Footer from '$lib/components/Home/Footer.svelte';
	import Hero from '$lib/components/Home/Hero.svelte';
	import Features from '$lib/components/Home/Features.svelte';
	import Products from '$lib/components/Home/Products.svelte';
	import Faq from '$lib/components/Home/Faq.svelte';
	const accordions = [1, 2, 3, 4, 5];
</script>

<div class="bg-white">
	<Header/>
	<Hero/>
	<Features/>
	<Products/>
	<Faq/>
	<Footer/>

	<!-- <div class="space-y-2">
		{#each accordions as accordion}
			<Accordion number={accordion} />
		{/each}
	</div> -->
</div>
