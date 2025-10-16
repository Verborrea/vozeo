<!-- <main class="mt-21.5 md:mt-23">
	<article id="guiamos" class="bg-cream px-6 py-12 md:py-32">
		<div class="mw flex flex-col gap-6 md:gap-12">
			<h1 class="text-center text-4xl text-blue md:text-6xl">¿Quiénes somos?</h1>
			<p>
				Somos una agencia performance que combina automatización, estrategia humana y medios pagados
				para construir ecosistemas que atraen, nutren y convierten clientes.
			</p>
			<p>
				En VOZEO convertimos el caos del marketing digital en sistemas predecibles de crecimiento.
			</p>
		</div>
	</article>
</main> -->

<script>
	import { ArrowDown, ArrowUpRight } from 'lucide-svelte';
	import desktop from '$lib/assets/hero.webp';
	import Numbers from './Numbers.svelte';
</script>

<main>
	<article id="hero" class="min-h-[80vh] content-end bg-cream px-6 pt-10 md:min-h-[unset] md:pt-32">
		<div class="mw flex flex-col-reverse justify-between gap-6 py-12 md:flex-row md:items-end">
			<div class="flex max-w-175 flex-col gap-4 sm:gap-6 md:items-start">
				<h1 class="text-5xl text-blue md:text-6xl lg:text-7xl xl:text-8xl">¿Quiénes somos?</h1>
				<div class="space-y-4 text-balance sm:text-lg md:text-xl">
					<p>
						Somos una agencia performance que combina <em>automatización</em>,
						<em>estrategia humana</em> y <em>medios pagados</em>
						para construir ecosistemas que atraen, nutren y convierten clientes.
					</p>
					<p>
						En <strong class="text-blue">VOZEO</strong> convertimos el caos del marketing digital en
						sistemas predecibles de crecimiento.
					</p>
				</div>
				<Numbers />
			</div>
			<!-- <img
			src={desktop}
			alt="Ilustración vectorial alusiva al marketing y la publicidad adaptativa"
			class="hidden w-full md:block md:w-[400px]"
		/> -->
		</div>
	</article>
</main>
