<script lang="ts">
	import { onMount } from 'svelte';

	const duration = 2000;
	let container = $state<HTMLElement | null>(null);
	let hasAnimated = $state(false);

	let numbers = $state([
		{ value: 0, target: 120, label: 'Campañas completamente optimizadas' },
		{ value: 0, target: 7, label: 'Embudos automatizados activos' },
		{
			value: 0,
			target: 300,
			label: 'Eficiencia de seguimiento y cierre para nuestros clientes.',
			unit: '%'
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
	class="grid items-start justify-items-center gap-6 text-center sm:grid-cols-2 sm:gap-8 md:grid-cols-3 lg:gap-12"
	bind:this={container}
>
	{#each numbers as number}
		<div class="flex max-w-40 flex-col items-center gap-4 last:max-w-50">
			<p class="text-5xl font-black">
				{#if number.unit}
					+{number.value}%
				{:else}
					+{number.value}
				{/if}
			</p>
			<p class=" leading-[22px] text-balance text-blue">{number.label}</p>
		</div>
	{/each}
</div>
