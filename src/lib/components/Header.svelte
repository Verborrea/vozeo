<script>
	import logo from '$lib/assets/logo.avif';
	import { onMount } from 'svelte';
	import Link from './Link.svelte';

	let hidden = $state(false);
	let lastScroll = $state(0);

	const onScroll = () => {
		const current = window.scrollY;
		const diff = current - lastScroll;

		// solo actuar si el movimiento supera el threshold
		if (Math.abs(diff) > 30) {
			if (current > lastScroll && current > 50) {
				// scrolling hacia abajo → ocultar
				hidden = true;
			} else {
				// scrolling hacia arriba → mostrar
				hidden = false;
			}
			lastScroll = current;
		}
	};
</script>

<svelte:window onscroll={onScroll} />

<header
	class="fixed top-0 right-0 left-0 z-20 bg-blue p-6 text-white transition-transform duration-300"
	class:translate-y-[-100%]={hidden}
>
	<div class="mw flex items-center justify-between gap-6">
		<a href="/"> <img src={logo} alt="Logo de Vozeo" width="184" /></a>
		<nav class="flex items-center gap-8">
			<Link text="Inicio" href="/" />
			<Link text="La agencia" href="/nosotros" />
			<Link text="Método" href="/metodo" />
			<Link text="Contáctanos" href="/contacto" />
		</nav>
	</div>
</header>
