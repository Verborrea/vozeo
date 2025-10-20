<script lang="ts">
	import { onMount } from 'svelte';

	const duration = 2000;
	let container = $state<HTMLElement | null>(null);
	let hasAnimated = $state(false);

	let numbers = $state([
		{
			value: 0,
			target: 80,
			label: 'del proceso de venta Automatizado',
			unit: '%',
			desc: '1 sistema que trabaja 24/7 que logra conversiones, visitas agendadas, citas con Inteligencia Artificial.'
		},
		{
			value: 0,
			target: 300,
			label: 'eficiencia de seguimiento y cierre para nuestros clientes.',
			unit: '%',
			desc: 'El 30% de facturación proviene de los seguimientos,  y metodología diseñada para escalar.'
		},
		{
			value: 0,
			target: 35,
			label: 'de reducción en el CPL',
			unit: '%',
			desc: 'Puedes ahorrarte contratar más personal, todo se basa en datos.'
		}
	]);

	function startAnimation() {
		const start = performance.now();

		function animate(now: number) {
			const elapsed = now - start;
			const t = Math.min(elapsed / duration, 1);
			const eased = 1 - Math.pow(1 - t, 2); // easeOutCubic

			numbers = numbers.map((n) => ({
				...n,
				value: Math.floor(n.target * eased)
			}));

			if (t < 1) requestAnimationFrame(animate);
			else {
				numbers = numbers.map((n) => ({ ...n, value: n.target }));
			}
		}

		requestAnimationFrame(animate);
	}

	onMount(() => {
		if (!container || hasAnimated) return;

		const observer = new IntersectionObserver(
			([entry]) => {
				if (entry.isIntersecting) {
					hasAnimated = true;
					startAnimation();
				}
			},
			{ threshold: 0.1 }
		);

		observer.observe(container);

		// Cleanup por si el componente se desmonta antes
		return () => observer.disconnect();
	});
</script>

<div
	class="grid items-center justify-items-center gap-6 sm:grid-cols-[180px_auto] lg:gap-12"
	bind:this={container}
>
	{#each numbers as number}
		<div class="flex max-w-50 flex-col items-center gap-4 text-center text-blue">
			<p class="text-5xl font-black">
				{#if number.unit}
					+{number.value}%
				{:else}
					+{number.value}
				{/if}
			</p>
			<p class=" leading-[22px]">{number.label}</p>
		</div>
		<p>{number.desc}</p>
	{/each}
</div>
