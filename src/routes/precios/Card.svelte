<script>
	let { cta, title, price, premium = false, content } = $props();
</script>

<article
	class="flex flex-col items-center gap-2 rounded-3xl border border-blue/25 p-6 transition duration-500 hover:-translate-y-5"
	class:bg-blue={premium}
	class:text-white={premium}
>
	<p class="pb-2 text-xl font-bold md:text-2xl">{title}</p>
	<p class="text-5xl font-black" class:text-yellow={premium}>${price}</p>
	<p class="text-slate-500">USD por mes</p>
	<section class="flex grow flex-col gap-3">
		{#each content as info}
			<article
				class="flex items-center gap-4 border-slate-200 pt-0.5 pb-3 not-last:border-b"
				class:border-slate-700={premium}
			>
				<p class="text-xl">{info.emoji}</p>
				<div class="space-y-1">
					<h3 class="leading-none">{info.title}</h3>
					<p class="text-sm text-slate-400" class:text-slate-500={premium}>{info.content}</p>
				</div>
			</article>
		{/each}
	</section>
	<a href="/" target="_blank" rel="noopener noreferrer" class="btn btn-yellow self-stretch">
		<span>{cta}</span>
	</a>
</article>
