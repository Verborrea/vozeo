<script>
	import { page } from '$app/state';
	import logo from '$lib/assets/logo.avif';
	import Link from './Link.svelte';
	import { fly } from 'svelte/transition';

	let hidden = $state(false);
	let lastScroll = $state(0);
	let opened = $state(false);

	const links = [
		{ text: 'Inicio', href: '/' },
		{ text: 'La agencia', href: '/' },
		{ text: 'Método', href: '/' },
		{ text: 'Contáctanos', href: '/' }
	];

	function onScroll() {
		const current = window.scrollY;
		const diff = current - lastScroll;

		if (Math.abs(diff) > 30) {
			if (current > lastScroll && current > 50) {
				hidden = true;
			} else {
				hidden = false;
			}
			lastScroll = current;
		}
	}

	function onclick() {
		opened = !opened;
		if (opened) {
			document.documentElement.style.overflow = 'hidden';
			document.body.style.overflow = 'hidden';
		} else {
			document.documentElement.style.overflow = '';
			document.body.style.overflow = '';
		}
	}
</script>

<svelte:window onscroll={onScroll} />

<header
	class="fixed top-0 right-0 left-0 z-20 bg-blue p-6 text-white transition-transform duration-300"
	class:translate-y-[-100%]={hidden}
>
	<div class="mw flex items-center justify-between gap-6">
		<a href="/"> <img src={logo} alt="Logo de Vozeo" width="184" /></a>
		<nav class="hidden items-center gap-8 sm:flex">
			{#each links as link}
				<Link {...link} />
			{/each}
		</nav>
		<button
			type="button"
			class="flex cursor-pointer flex-col gap-1 py-2.5 sm:hidden"
			aria-label="Menú"
			class:opened
			{onclick}
		>
			<div id="bb1" class="h-[4px] w-7 rounded-full bg-white transition"></div>
			<div id="bb2" class="h-[4px] w-7 rounded-full bg-white transition"></div>
			<div id="bb3" class="h-[4px] w-7 rounded-full bg-white transition"></div>
		</button>
	</div>
</header>

{#if opened}
	<nav
		in:fly={{ y: '-100svh', duration: 400, opacity: 1 }}
		out:fly={{ y: '-100svh', duration: 400, opacity: 1, delay: 300 }}
		class="mobile-nav fixed top-0 right-0 left-0 z-15 flex min-h-[100svh] flex-col justify-end gap-6 bg-blue p-5.5 text-white sm:hidden"
	>
		{#each links as link, index}
			<a
				{onclick}
				class="text-3xl font-extrabold"
				href={link.href}
				in:fly|global={{ y: -20, duration: 400, opacity: 0, delay: index * 35 + 250 }}
				out:fly|global={{
					y: -20,
					duration: 200,
					opacity: 0,
					delay: (links.length - index) * 15 + 15
				}}
				aria-current={page.url.pathname === link.href}>{link.text}</a
			>
		{/each}
		<!-- <a
			{onclick}
			in:fly|global={{ y: -20, duration: 400, opacity: 0, delay: links.length * 35 + 250 }}
			out:fly|global={{ y: -20, duration: 200, opacity: 0, delay: 0 }}
			class="rounded-[16px] bg-yellow p-5.5 text-center text-[28px] leading-none font-bold tracking-tighter shadow-none"
			href="/"><div class="w-full">Dona Ya!</div></a
		> -->
	</nav>
{/if}

<style>
	.opened > #bb1 {
		transform: translateY(8px) rotate(-45deg);
	}
	.opened > #bb2 {
		opacity: 0;
		transform: scaleX(1.5);
	}
	.opened > #bb3 {
		transform: translateY(-8px) rotate(45deg);
	}
	.opened > * {
		fill: white;
		transition: all 200ms;
	}
</style>
