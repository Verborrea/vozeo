<script>
	import hero from '$lib/assets/metodo/hero.avif';
	import heroMobile from '$lib/assets/metodo/hero-mobile.avif';
	import Adquisicion from './Adquisicion.svelte';
	import Nutricion from './Nutricion.svelte';
	import Auto from './Auto.svelte';
	import Fullfillment from './Fullfillment.svelte';
</script>

<svelte:head>
	<title>Nuestra Metodología | Vozeo</title>
	<meta
		name="description"
		content="Automatizamos tu proceso comercial con Paid Media, Estrategia, WhatsApp y CRM. Más leads, menos esfuerzo, todo medible."
	/>
</svelte:head>

<main class="mt-21.5 md:mt-23">
	<article id="guiamos" class="bg-blue px-6 py-12 md:py-32">
		<div class="mw flex flex-col gap-6 md:gap-12">
			<h1 class="text-center text-4xl text-yellow md:text-6xl">¿cómo opera el sistema?</h1>
			<picture>
				<source srcset={heroMobile} media="(max-width: 768px)" />
				<source srcset={hero} media="(min-width: 769px)" />
				<img src={hero} alt="Diagrama del método" class="w-full" />
			</picture>
		</div>
	</article>
	<Adquisicion />
	<Nutricion />
	<Auto />
	<Fullfillment />
</main>
