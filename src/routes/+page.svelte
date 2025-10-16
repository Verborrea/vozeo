<script>
	import Clientes from './Clientes.svelte';
	import Demanda from './Demanda.svelte';
	import Guiemos from './Guiemos.svelte';
	import Hero from './Hero.svelte';
	import How from './How.svelte';
	import Steps from './Steps.svelte';
	import SubFooter from './SubFooter.svelte';
</script>

<svelte:head>
	<title>Vozeo - Agencia Digital de Publicidad y Marketing</title>
	<meta
		name="description"
		content="Automatizamos tu proceso comercial con Paid Media, Estrategia, WhatsApp y CRM. Más leads, menos esfuerzo, todo medible."
	/>
</svelte:head>

<main>
	<Hero />
	<Demanda />
	<Steps />
	<Guiemos />
	<How />
	<Clientes />
	<SubFooter />
</main>
