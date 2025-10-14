<script>
	let { text, href = '/', ...others } = $props();

	let hovered = $state(false);
	let span = $state();

	function handleHover() {
		hovered = true;
	}
</script>

<a
	{href}
	onmouseenter={handleHover}
	onmouseleave={() => (hovered = false)}
	{...others}
	style:--height={span?.offsetHeight + 'px'}
>
	<div>
		<span bind:this={span} class="block text-white">{text}</span>
		<span class="block text-yellow">{text}</span>
	</div></a
>

<style>
	div {
		height: var(--height);
		cursor: pointer;
		will-change: transform;
		transition: transform 0.4s ease;
	}
	a {
		display: block;
		overflow: hidden;
		transform: translateZ(0) var(--tw-rotate-x,) var(--tw-rotate-y,) var(--tw-rotate-z,)
			var(--tw-skew-x,) var(--tw-skew-y,);
	}
	a:hover {
		@media (hover: hover) {
			div {
				transform: translateY(calc(-1 * var(--height)));
			}
		}
	}
</style>
