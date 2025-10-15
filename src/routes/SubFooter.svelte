<script>
	import { CalendarDays } from 'lucide-svelte';
</script>

<article class="bg-black px-6 py-12 text-white md:py-24">
	<div class="mw flex flex-col items-center justify-between gap-6 md:flex-row">
		<h1 class="max-w-125 text-yellow">
			¿realmente quieres <em>duplicar</em> tu inversión?
		</h1>
		<div class="flex max-w-125 flex-col gap-6">
			<div class="space-y-4">
				<h2 class="text-end text-3xl font-extrabold text-balance md:text-start">
					Agenda una breve cita de diagnóstico.
				</h2>
				<p class="text-lg text-white/50">
					En <strong class="font-extrabold text-yellow">15 minutos</strong> te mostramos cómo podrías
					duplicar tus oportunidades sin aumentar tu presupuesto.
				</p>
			</div>
			<div class="flex flex-col gap-3 md:flex-row md:items-center md:gap-4">
				<a
					href="https://wa.me/51901776738?text={encodeURI(
						'Hola, estoy interesado en sus servicios.'
					)}"
					target="_blank"
					rel="noopener noreferrer"
					class="btn btn-white text-lg !text-black"
				>
					<svg
						width="20"
						height="20"
						viewBox="0 0 32 32"
						xmlns="http://www.w3.org/2000/svg"
						fill="black"
					>
						<path
							d="M15.7904 2.69029C19.0372 2.63679 22.1922 3.77051 24.6628 5.87779C27.1335 7.98511 28.7504 10.9222 29.2097 14.1369C29.6688 17.3513 28.939 20.6227 27.1576 23.3374C25.3759 26.0523 22.6645 28.0238 19.5326 28.8817C16.5452 29.7 13.3723 29.449 10.5547 28.1851L4.23441 29.3127C3.75103 29.3988 3.25908 29.212 2.95447 28.827C2.64989 28.4416 2.58173 27.9195 2.77738 27.4689L4.68884 23.0627C3.11666 20.5346 2.4312 17.5457 2.75655 14.5718C3.10981 11.344 4.62893 8.35561 7.02869 6.16815C9.42847 3.98087 12.5438 2.74383 15.7904 2.69029ZM15.8347 5.35695C13.2372 5.39976 10.7442 6.38944 8.82426 8.13951C6.90453 9.88953 5.68881 12.2799 5.40629 14.8622C5.12377 17.4446 5.7943 20.0418 7.2904 22.1655C7.5579 22.5455 7.60813 23.0374 7.42322 23.4637L6.21228 26.2502L10.5 25.4872L10.7097 25.4663C10.9196 25.4626 11.1286 25.5087 11.319 25.6017C13.6522 26.7441 16.3227 26.9964 18.8282 26.3101C21.3336 25.6238 23.5031 24.047 24.9284 21.8752C26.3537 19.7033 26.9365 17.0849 26.569 14.5132C26.2015 11.9417 24.9087 9.5922 22.9323 7.90643C20.9559 6.2207 18.432 5.31419 15.8347 5.35695Z"
						/>
						<path
							d="M14.6666 13.3333C14.6666 13.8638 14.4558 14.3723 14.0807 14.7474C13.9463 14.8818 13.7938 14.9933 13.6302 15.0833C13.892 15.8368 14.321 16.5294 14.8958 17.1042C15.4702 17.6785 16.1624 18.1066 16.9153 18.3685C17.0053 18.2051 17.1183 18.0536 17.2526 17.9193L17.3997 17.7865C17.7556 17.495 18.2026 17.3333 18.6666 17.3333H20C20.464 17.3333 20.911 17.495 21.2669 17.7865L21.414 17.9193L21.5468 18.0664C21.8383 18.4223 22 18.8693 22 19.3333C22 19.8638 21.7891 20.3723 21.414 20.7474C21.0389 21.1225 20.5304 21.3333 20 21.3333H18.6666C16.5449 21.3333 14.5107 20.4899 13.0104 18.9896C11.5101 17.4893 10.6666 15.4551 10.6666 13.3333V12C10.6666 11.4696 10.8775 10.961 11.2526 10.5859C11.6276 10.2109 12.1362 10 12.6666 10C13.1971 10 13.7056 10.2109 14.0807 10.5859C14.4558 10.961 14.6666 11.4696 14.6666 12V13.3333Z"
						/>
					</svg>
					<span>WhatsApp</span></a
				>
				<a
					href="https://calendar.app.google/A1EYghs3JTvTm4pZ6"
					target="_blank"
					rel="noopener noreferrer"
					class="btn btn-white text-lg !text-black"
				>
					<CalendarDays size={20} strokeWidth={2.5} />
					<span>Agenda una cita</span></a
				>
			</div>
		</div>
	</div>
</article>
