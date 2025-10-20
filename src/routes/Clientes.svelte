<script>
	import ventanas from '$lib/assets/socios/ventanas.avif';
	import thermia from '$lib/assets/socios/thermia.avif';
	import gdc from '$lib/assets/socios/gdc.avif';
	import mundonegocio from '$lib/assets/socios/mundonegocio.avif';
	import cxzh from '$lib/assets/socios/cxzh.avif';
	import decokasa from '$lib/assets/socios/decokasa.avif';
	import infounsa from '$lib/assets/socios/infounsa.avif';
	import mundobaby from '$lib/assets/socios/mundobaby.avif';
	import rocket from '$lib/assets/socios/rocket.avif';
	import burger from '$lib/assets/socios/burger.avif';
	import sunset from '$lib/assets/socios/sunset.avif';
	import digastro from '$lib/assets/socios/digastro.avif';

	const socios = [
		{ src: ventanas, alt: 'Ventanas Windows' },
		{ src: thermia, alt: 'Thermia Barcelona' },
		{ src: gdc, alt: 'GDC' },
		{ src: mundonegocio, alt: 'Mundo Negocio' },
		{ src: cxzh, alt: 'CXZH' },
		{ src: decokasa, alt: 'DecoKasa' },
		{ src: infounsa, alt: 'Info UNSA' },
		{ src: mundobaby, alt: 'Mundo Baby' },
		{ src: rocket, alt: 'Rocketh 88 - Academia' },
		{ src: burger, alt: 'Burgerthoven' },
		{ src: sunset, alt: 'Sunset Grill' },
		{ src: digastro, alt: 'Di Gastro' }
	];
</script>

<article id="clientes" class="bg-cream px-6 py-12 md:py-32">
	<div class="mw flex flex-col gap-12">
		<h1 class="text-center text-4xl md:text-6xl">¿quiénes confiaron en nosotros?</h1>
		<section
			class="grid items-center justify-items-center gap-6 sm:grid-cols-2 md:grid-cols-3 md:gap-10 lg:grid-cols-4"
		>
			{#each socios as socio}
				<img src={socio.src} alt={socio.alt} />
			{/each}
		</section>
	</div>
</article>
