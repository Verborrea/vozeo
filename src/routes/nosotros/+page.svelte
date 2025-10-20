<script>
	import hero from '$lib/assets/nosotros/rostro.avif';
	import diferentes from '$lib/assets/nosotros/diferentes.avif';
	import Numbers from './Numbers.svelte';
	import Valores from './Valores.svelte';
	import Que from './Que.svelte';
</script>

<svelte:head>
	<title>La Agencia | Vozeo</title>
	<meta
		name="description"
		content="Automatizamos tu proceso comercial con Paid Media, Estrategia, WhatsApp y CRM. Más leads, menos esfuerzo, todo medible."
	/>
</svelte:head>

<main>
	<article id="hero" class="content-end bg-cream px-6 pt-18 md:pt-32">
		<div class="mw flex flex-col-reverse justify-between gap-6 py-12 md:flex-row md:items-center">
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
			<img
				src={hero}
				alt="Ilustración vectorial alusiva de un rostro feliz"
				class="w-full object-cover md:w-[400px]"
			/>
		</div>
	</article>
	<Que />
	<article class="content-end bg-cream px-6 pt-18 md:pt-32">
		<div class="mw flex flex-col justify-between gap-6 py-12 md:items-center md:gap-8 lg:flex-row">
			<div class="flex max-w-85 flex-col gap-4 sm:gap-6">
				<h1 class="text-4xl text-orange lg:text-5xl xl:text-6xl">¿Porqué somos diferentes?</h1>
				<div class="sm:text-lg md:text-xl">
					<p>
						Porque no dependemos de la suerte, sino del sistema. Cada parte de nuestra metodología
						combina tecnología, datos y emoción:
					</p>
				</div>
			</div>
			<img
				src={diferentes}
				alt="Ilustración vectorial alusiva de un rostro pensativo"
				class="object-cover lg:w-[380px]"
			/>
			<Valores />
		</div>
	</article>
</main>
