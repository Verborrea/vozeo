<script>
	import desktop from '$lib/assets/grafo.webp';
	import mobile from '$lib/assets/mobile.webp';
</script>

<article id="how" class="flex flex-col gap-12 py-12 md:py-32">
	<div class="px-6">
		<h1 class="mw text-center text-5xl">¿cómo lo hacemos?</h1>
	</div>
	<picture>
		<source srcset={mobile} media="(max-width: 768px)" />
		<source srcset={desktop} media="(min-width: 769px)" />
		<img src={desktop} alt="Método vozeo" class="w-full" />
	</picture>
</article>
