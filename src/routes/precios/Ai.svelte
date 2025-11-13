<script>
	let { title, what, why, smart = '', growth = '', elite = '' } = $props();
</script>

<article
	class="flex flex-col items-center gap-3 rounded-2xl bg-blue/5 p-4 text-start transition duration-500 hover:-translate-y-5"
>
	<h2 class="font-bold text-blue">{title}</h2>
	<p class="text-sm text-blue/50"><span class="font-bold text-blue-500">¿Qué es?</span> {what}</p>
	<p class="text-sm text-blue/50">
		<span class="font-bold text-blue-500">¿Para qué sirve?</span>
		{why}
	</p>
	<p class="flex w-full flex-wrap gap-1.5 text-sm">
		{#if smart}
			<span class="tag tag-blue">Start: {smart}</span>
		{:else}
			<span class="tag tag-disabled">Start: ❌</span>
		{/if}
		<span class="tag tag-pink">Growth: {growth}</span>
		<span class="tag tag-gold">Elite: {elite}</span>
	</p>
</article>
