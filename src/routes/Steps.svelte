<script>
	import foco from '$lib/assets/steps/foco.avif';
	import ads from '$lib/assets/steps/ads.avif';
	import write from '$lib/assets/steps/write.avif';
	import compu from '$lib/assets/steps/compu.avif';
	import globos from '$lib/assets/steps/globos.avif';
	import mano from '$lib/assets/steps/mano.avif';

	const steps = [
		{
			img: foco,
			name: 'Estrategia de contenido',
			text: 'Contenido que posiciona tu autoridad y responde a lo que tus clientes buscan antes de decidir. Sin likes vacíos, solo intención.'
		},
		{
			img: ads,
			name: 'Paid Media',
			text: 'No buscamos clics, buscamos clientes. Diseñamos campañas que filtran, atraen y convierten tráfico real en prospectos listos para comprar.'
		},
		{
			img: write,
			name: 'Branding',
			text: 'Transformamos tu mensaje en una propuesta que corta el ruido: quién eres, por qué eres distinto y por qué deben comprarte a ti.'
		},
		{
			img: compu,
			name: 'Desarrollo Web',
			text: 'Contenido que posiciona tu autoridad y responde a lo que tus clientes buscan antes de decidir. Sin likes vacíos, solo intención.'
		},
		{
			img: globos,
			name: 'CRM / Automatizaciones',
			text: 'Una infraestructura que trabaja 24/7 para ti. Califica, nutre y da seguimiento automático hasta cerrar la venta. Deja de perseguir leads, empieza a escalar con método.'
		},
		{
			img: mano,
			name: 'Integración',
			text: 'Aplicamos en una sola campaña diversos recursos y herramientas que puedan llevarte al resultado que deseas.'
		}
	];
</script>

<article id="steps" class="px-6 py-12 md:py-32">
	<div class="mw flex flex-col gap-12">
		<h1 class="text-center text-4xl text-orange md:text-6xl">¿sabes por donde empezar?</h1>
		<section class="grid gap-6 sm:grid-cols-2 md:gap-12 lg:grid-cols-3">
			{#each steps as step}
				<article
					class="group relative flex flex-col items-start gap-4 overflow-hidden rounded-2xl bg-black px-6 py-8 text-white"
				>
					<div
						class="absolute top-0 left-full size-54 -translate-1/2 rounded-full bg-orange transition-all group-hover:size-64"
					></div>
					<img src={step.img} alt={step.name} class="relative h-32 object-contain" />
					<h1 class="relative text-2xl font-extrabold">{step.name}</h1>
					<p class="relative">{step.text}</p>
				</article>
			{/each}
		</section>
	</div>
</article>
