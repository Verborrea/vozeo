<script>
	import { ArrowDown, ArrowUpRight } from 'lucide-svelte';
	import face from '$lib/assets/face.avif';
</script>

<article id="hero" class="relative bg-blue px-6 pt-18 md:pt-36">
	<div class="mw flex justify-between gap-6 py-12 text-white md:items-end">
		<div class="flex max-w-175 flex-col gap-4 sm:gap-6 md:items-start">
			<h1 class="text-5xl md:text-8xl">
				¿Necesitas más <span class="text-yellow">clientes</span>?
			</h1>
			<div class="text-lg text-balance md:text-xl">
				<p>
					Te construimos un sistema de adquisición automatizado que atrae, filtra y califica
					prospectos listos para comprar.
				</p>
				<p class="font-extrabold text-yellow">
					No más anuncios al aire. Solo crecimiento predecible.
				</p>
			</div>
			<a href="/#how" class="btn btn-white group md:text-lg">
				<span>Descubre cómo aquí</span>
				<ArrowUpRight
					class="size-4 transition duration-500 group-hover:rotate-45 md:size-5"
					strokeWidth={3}
				/>
			</a>
		</div>
		<img
			src={face}
			class="hidden w-75 md:block"
			alt="Ilustración de un rostro triste."
			width="300"
		/>
	</div>
	<a
		href="#cards"
		class="translate absolute -bottom-5.5 left-1/2 flex size-11 -translate-x-1/2 items-center justify-center rounded-full bg-yellow text-black"
		aria-label="Conócenos"
		title="Bajar"
	>
		<ArrowDown class="arrow mt-1 animate-bounce" strokeWidth={2.5} />
	</a>
</article>

<style>
	:global(.arrow) {
		animation-duration: 1000ms;
	}
</style>
