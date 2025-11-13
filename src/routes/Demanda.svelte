<script>
	import { CircleCheckBig } from 'lucide-svelte';
</script>

<article class="bg-cream px-6 py-12 md:py-32">
	<div class="mw flex flex-col gap-4 md:gap-12">
		<p class="text-lg leading-none md:text-2xl md:leading-[1.3]">sabes que hay demanda…</p>
		<h1 class="text-5xl leading-none text-blue md:text-8xl">
			pero no sabes a dónde se está <span class="text-orange">fugando</span> tu inversión?
		</h1>
		<div
			class="flex flex-col justify-between gap-6 pt-3 text-xl md:flex-row md:items-center md:pt-6 md:text-2xl"
		>
			<ul class="space-y-2">
				<li class="flex items-center gap-2 md:gap-3">
					<CircleCheckBig strokeWidth={3} class="size-5 md:size-6" />
					<p>Leads que no responden</p>
				</li>
				<li class="flex items-center gap-2 md:gap-3">
					<CircleCheckBig strokeWidth={3} class="size-5 md:size-6" />
					<p>Ventas que no cierran</p>
				</li>
				<li class="flex items-center gap-2 md:gap-3">
					<CircleCheckBig strokeWidth={3} class="size-5 md:size-6" />
					<p>Dinero flotando.</p>
				</li>
			</ul>
			<svg
				width="283"
				height="98"
				viewBox="0 0 283 98"
				fill="none"
				class="hidden text-orange/90 md:block"
			>
				<path
					d="M8.00012 48.5016C97.0483 48.5016 185.955 46.8769 275 46.1999M8.00012 48.5016C12.6733 51.7432 46.0001 69.5016 60.3569 90.0016M8.00012 48.5016C37.417 37.0368 53.6433 28.0016 64.0001 8.00165"
					stroke="currentColor"
					stroke-width="16"
					stroke-linecap="round"
					stroke-linejoin="round"
				/>
			</svg>
			<p class="font-extrabold text-blue">¿Te suena familiar?</p>
		</div>
	</div>
</article>
