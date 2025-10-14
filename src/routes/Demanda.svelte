<script>
	import { CircleCheckBig } from 'lucide-svelte';
	import arrow from '$lib/assets/arrow.png';
</script>

<article class="bg-cream px-6 py-12 md:py-32">
	<div class="mw flex flex-col gap-6 md:gap-12">
		<p class="text-2xl">Sabes que hay demanda…</p>
		<h1 class="text-5xl text-blue md:text-8xl">
			pero no sabes dónde se está fugando tu inversión.
		</h1>
		<div
			class="flex flex-col justify-between gap-6 pt-3 text-2xl md:flex-row md:items-center md:pt-6"
		>
			<ul>
				<li class="flex items-center gap-3">
					<CircleCheckBig strokeWidth={3} />
					<p>Leads que no responden</p>
				</li>
				<li class="flex items-center gap-3">
					<CircleCheckBig strokeWidth={3} />
					<p>Ventas que no cierran</p>
				</li>
				<li class="flex items-center gap-3">
					<CircleCheckBig strokeWidth={3} />
					<p>Dinero flotando.</p>
				</li>
			</ul>
			<img src={arrow} alt="Flecha izquierda dibujada a mano" width="276" class="hidden md:block" />
			<p class="font-extrabold text-blue">¿Te suena familiar?</p>
		</div>
	</div>
</article>
