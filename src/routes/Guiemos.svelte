<script>
	import { ArrowRight } from 'lucide-svelte';
</script>

<article id="guiamos" class="bg-blue px-6 py-12 text-white md:py-32">
	<div class="mw flex flex-col gap-6 md:gap-12">
		<h1 class="text-center text-4xl md:text-6xl">¿prefieres que te guiemos?</h1>
		<h2 class="text-center text-3xl font-extrabold text-balance text-[#565FF4]">
			¿qué tipo de resultado buscas primero?
		</h2>
		<section class="grid gap-6 md:grid-cols-2 md:gap-12">
			<article class="space-y-6">
				<h1 class="text-2xl font-extrabold md:text-3xl md:font-black">
					Más oportunidades inmediatas
				</h1>
				<p class="text-lg text-white/50 md:text-xl">
					Diseñamos campañas enfocadas en captación rápida de <em>leads</em> calificados. Ideal si
					ya tienes un <strong class="font-extrabold text-white">proceso comercial sólido</strong>,
					pero necesitas flujo constante de contactos.
				</p>
				<a
					href="https://wa.me/51901776738?text={encodeURI(
						'Hola, vengo de su página y estoy interesado en conseguir más leads para mi negocio.'
					)}"
					target="_blank"
					rel="noopener noreferrer"
					class="group flex items-center justify-end gap-4 font-black sm:gap-6"
				>
					<span class="text-end text-xl text-yellow group-hover:underline sm:text-2xl"
						>quiero <em>leads</em> ahora</span
					>
					<div
						class="aspect-square rounded-full bg-yellow p-1.5 text-black transition duration-500 group-hover:rotate-360 sm:p-2"
					>
						<ArrowRight strokeWidth={2.5} />
					</div>
				</a>
			</article>
			<article class="space-y-6">
				<h1 class="text-2xl font-extrabold md:text-3xl md:font-black">
					Sistema integral a largo plazo
				</h1>
				<p class="text-lg text-white/50 md:text-xl">
					Construimos tu ecosistema automatizado: campañas + CRM + seguimiento. Ideal si quieres
					depender menos del esfuerzo humano y <strong class="font-extrabold text-white"
						>más de resultados medibles</strong
					>.
				</p>
				<a
					href="https://wa.me/51901776738?text={encodeURI(
						'Hola, vengo de su página y estoy interesado en un sistema completo para mi negocio.'
					)}"
					class="group flex items-center justify-end gap-4 font-black sm:gap-6"
				>
					<span class="text-end text-xl text-yellow group-hover:underline sm:text-2xl"
						>quiero un sistema completo</span
					>
					<div
						class="aspect-square rounded-full bg-yellow p-1.5 text-black transition duration-500 group-hover:rotate-360 sm:p-2"
					>
						<ArrowRight strokeWidth={2.5} />
					</div>
				</a>
			</article>
		</section>
	</div>
</article>
