<script>
	import Link from './Link.svelte';
	import footer from '$lib/assets/footer.avif';
	import { PhoneCall, SendHorizontal } from 'lucide-svelte';
</script>

<footer class="border-t-4 border-white bg-black px-6 text-white">
	<div class="mw">
		<div class="relative flex flex-col justify-between gap-10 py-12 md:flex-row md:gap-6">
			<section class="order-2 flex flex-col gap-4 md:order-1">
				<h2 class="text-2xl leading-none font-extrabold">Mapa del Sitio</h2>
				<nav class="flex flex-col gap-2">
					<Link text="Inicio" href="/" />
					<Link text="¿Qué te ofrecemos?" href="/" />
					<Link text="Te guiamos" href="/#guiamos" />
					<Link text="Nuestra Metodología" href="/#how" />
					<Link text="Clientes" href="/#clientes" />
				</nav>
			</section>
			<img
				src={footer}
				alt="Logo vertical de Vozeo"
				class="top-1/2 left-1/2 order-1 mx-auto w-[50%] shrink-0 md:absolute md:order-[unset] md:w-[209px] md:-translate-1/2"
				width="209"
			/>
			<div class="order-3 flex flex-col gap-10 md:order-2">
				<section class="flex flex-col gap-4">
					<h2 class="text-2xl leading-none font-extrabold">Conversemos</h2>
					<nav class="flex flex-col gap-2">
						<div class="group flex items-center gap-2">
							<SendHorizontal class="size-4 group-hover:text-yellow sm:size-5" />
							<Link text="vozeoagency@gmail.com" href="mailto:vozeoagency@gmail.com" />
						</div>
						<div class="group flex items-center gap-2">
							<PhoneCall class="size-4 group-hover:text-yellow sm:size-5" />
							<Link text="+51 901 776 738" href="tel:+51901776738" />
						</div>
					</nav>
				</section>
				<section class="flex flex-col gap-4">
					<h2 class="text-2xl leading-none font-extrabold">Síguenos en</h2>
					<nav class="flex gap-8 text-white md:justify-start md:gap-6">
						<a
							href="https://wa.me/51901776738?text={encodeURI(
								'Hola, estoy interesado en sus servicios.'
							)}"
							target="_blank"
							rel="noopener noreferrer"
							aria-label="Whatsapp"
							class="transition-all duration-250 hover:-rotate-15 hover:text-yellow"
						>
							<svg width="32" height="32" viewBox="0 0 32 32" fill="none">
								<path
									d="M15.7904 2.69029C19.0372 2.63679 22.1922 3.77051 24.6628 5.87779C27.1335 7.98511 28.7504 10.9222 29.2097 14.1369C29.6688 17.3513 28.939 20.6227 27.1576 23.3374C25.3759 26.0523 22.6645 28.0238 19.5326 28.8817C16.5452 29.7 13.3723 29.449 10.5547 28.1851L4.23441 29.3127C3.75103 29.3988 3.25908 29.212 2.95447 28.827C2.64989 28.4416 2.58173 27.9195 2.77738 27.4689L4.68884 23.0627C3.11666 20.5346 2.4312 17.5457 2.75655 14.5718C3.10981 11.344 4.62893 8.35561 7.02869 6.16815C9.42847 3.98087 12.5438 2.74383 15.7904 2.69029ZM15.8347 5.35695C13.2372 5.39976 10.7442 6.38944 8.82426 8.13951C6.90453 9.88953 5.68881 12.2799 5.40629 14.8622C5.12377 17.4446 5.7943 20.0418 7.2904 22.1655C7.5579 22.5455 7.60813 23.0374 7.42322 23.4637L6.21228 26.2502L10.5 25.4872L10.7097 25.4663C10.9196 25.4626 11.1286 25.5087 11.319 25.6017C13.6522 26.7441 16.3227 26.9964 18.8282 26.3101C21.3336 25.6238 23.5031 24.047 24.9284 21.8752C26.3537 19.7033 26.9365 17.0849 26.569 14.5132C26.2015 11.9417 24.9087 9.5922 22.9323 7.90643C20.9559 6.2207 18.432 5.31419 15.8347 5.35695Z"
									fill="currentColor"
								/>
								<path
									d="M14.6666 13.3333C14.6666 13.8638 14.4558 14.3723 14.0807 14.7474C13.9463 14.8818 13.7938 14.9933 13.6302 15.0833C13.892 15.8368 14.321 16.5294 14.8958 17.1042C15.4702 17.6785 16.1624 18.1066 16.9153 18.3685C17.0053 18.2051 17.1183 18.0536 17.2526 17.9193L17.3997 17.7865C17.7556 17.495 18.2026 17.3333 18.6666 17.3333H20C20.464 17.3333 20.911 17.495 21.2669 17.7865L21.414 17.9193L21.5468 18.0664C21.8383 18.4223 22 18.8693 22 19.3333C22 19.8638 21.7891 20.3723 21.414 20.7474C21.0389 21.1225 20.5304 21.3333 20 21.3333H18.6666C16.5449 21.3333 14.5107 20.4899 13.0104 18.9896C11.5101 17.4893 10.6666 15.4551 10.6666 13.3333V12C10.6666 11.4696 10.8775 10.961 11.2526 10.5859C11.6276 10.2109 12.1362 10 12.6666 10C13.1971 10 13.7056 10.2109 14.0807 10.5859C14.4558 10.961 14.6666 11.4696 14.6666 12V13.3333Z"
									fill="currentColor"
								/>
							</svg>
						</a>
						<a
							href="https://www.facebook.com/profile.php?id=61582296562064"
							target="_blank"
							rel="noopener noreferrer"
							aria-label="Facebook"
							class="transition-all duration-250 hover:-rotate-15 hover:text-yellow"
							><svg width="32" height="32" viewBox="0 0 32 32" fill="none">
								<path
									d="M16.8665 3C21.1133 3 23.2371 2.99986 24.8592 3.82629C26.2861 4.55336 27.4467 5.714 28.1737 7.14096C29.0001 8.76315 29 10.887 29 15.134V16.867C29 21.114 29.0001 23.2379 28.1737 24.8601C27.4467 26.2871 26.2861 27.4477 24.8592 28.1748C23.2649 28.987 21.1862 28.9998 17.0833 29V20.334H20.3333L21.4167 16.0005H17.0833V12.7504C17.0833 12.4631 17.1976 12.1865 17.4007 11.9834C17.6039 11.7803 17.8795 11.667 18.1667 11.667H21.4167V7.33351H18.1667C16.7302 7.33351 15.3527 7.90373 14.3369 8.91943C13.3211 9.93529 12.75 11.3137 12.75 12.7504V16.0005H9.5V20.334H12.75V28.9915C10.0271 28.9633 8.42641 28.8298 7.14079 28.1748C5.71389 27.4477 4.55329 26.2871 3.82625 24.8601C2.99986 23.2379 3 21.114 3 16.867V15.134C3 10.887 2.99986 8.76315 3.82625 7.14096C4.55329 5.714 5.71389 4.55336 7.14079 3.82629C8.76292 2.99986 10.8867 3 15.1335 3H16.8665Z"
									fill="currentColor"
								/>
							</svg></a
						>
						<a
							href="https://www.instagram.com/vozeo_pe/"
							target="_blank"
							rel="noopener noreferrer"
							aria-label="Instagram"
							class="transition-all duration-250 hover:-rotate-15 hover:text-yellow"
							><svg width="32" height="32" viewBox="0 0 32 32" fill="currentColor">
								<path
									d="M16 12.2083C18.0941 12.2083 19.7917 13.9059 19.7917 16C19.7917 18.0941 18.0941 19.7917 16 19.7917C13.9059 19.7917 12.2083 18.0941 12.2083 16C12.2083 13.9059 13.9059 12.2083 16 12.2083Z"
								/>
								<path
									fill-rule="evenodd"
									clip-rule="evenodd"
									d="M16.8665 3C21.1133 3 23.2371 2.99986 24.8592 3.82625C26.2861 4.55329 27.4467 5.71389 28.1737 7.14079C29.0001 8.76292 29 10.8867 29 15.1335V16.8665C29 21.1133 29.0001 23.2371 28.1737 24.8592C27.4467 26.2861 26.2861 27.4467 24.8592 28.1737C23.2371 29.0001 21.1133 29 16.8665 29H15.1335C10.8867 29 8.76292 29.0001 7.14079 28.1737C5.71389 27.4467 4.55329 26.2861 3.82625 24.8592C2.99986 23.2371 3 21.1133 3 16.8665V15.1335C3 10.8867 2.99986 8.76292 3.82625 7.14079C4.55329 5.71389 5.71389 4.55329 7.14079 3.82625C8.76292 2.99986 10.8867 3 15.1335 3H16.8665ZM16 9.5C12.4101 9.5 9.5 12.4101 9.5 16C9.5 19.5899 12.4101 22.5 16 22.5C19.5899 22.5 22.5 19.5899 22.5 16C22.5 12.4101 19.5899 9.5 16 9.5ZM23.0417 7.33333C22.1442 7.33333 21.4167 8.06087 21.4167 8.95833C21.4167 9.8558 22.1442 10.5833 23.0417 10.5833C23.9391 10.5833 24.6667 9.8558 24.6667 8.95833C24.6667 8.06087 23.9391 7.33333 23.0417 7.33333Z"
								/>
							</svg>
						</a>
						<a
							href="https://www.linkedin.com/company/105482185"
							target="_blank"
							rel="noopener noreferrer"
							aria-label="LinkedIn"
							class="transition-all duration-250 hover:-rotate-15 hover:text-yellow"
							><svg width="32" height="32" viewBox="0 0 32 32" fill="none">
								<g clip-path="url(#clip0_2015_26)">
									<path
										d="M26.6481 3H5.35191C4.053 3 3 4.053 3 5.35191V26.648C3 27.947 4.053 29 5.35191 29H26.648C27.947 29 29 27.947 29 26.648V5.35191C29 4.053 27.947 3 26.6481 3ZM11.0455 25.4501C11.0455 25.8281 10.7391 26.1346 10.3611 26.1346H7.44757C7.06954 26.1346 6.76313 25.8281 6.76313 25.4501V13.2369C6.76313 12.8588 7.06954 12.5524 7.44757 12.5524H10.3611C10.7391 12.5524 11.0455 12.8588 11.0455 13.2369V25.4501ZM8.90431 11.4011C7.37569 11.4011 6.13647 10.1619 6.13647 8.63329C6.13647 7.10466 7.37569 5.86544 8.90431 5.86544C10.4329 5.86544 11.6722 7.10466 11.6722 8.63329C11.6722 10.1619 10.433 11.4011 8.90431 11.4011ZM26.2714 25.5052C26.2714 25.8528 25.9896 26.1346 25.6421 26.1346H22.5157C22.1681 26.1346 21.8863 25.8528 21.8863 25.5052V19.7765C21.8863 18.9219 22.137 16.0316 19.653 16.0316C17.7262 16.0316 17.3354 18.01 17.2569 18.8978V25.5052C17.2569 25.8528 16.9752 26.1346 16.6276 26.1346H13.6038C13.2563 26.1346 12.9745 25.8528 12.9745 25.5052V13.1817C12.9745 12.8342 13.2563 12.5524 13.6038 12.5524H16.6276C16.9751 12.5524 17.2569 12.8342 17.2569 13.1817V14.2472C17.9714 13.1751 19.0332 12.3475 21.2939 12.3475C26.3 12.3475 26.2714 17.0245 26.2714 19.5943V25.5052Z"
										fill="currentColor"
									/>
								</g>
								<defs>
									<clipPath id="clip0_2015_26">
										<rect width="26" height="26" fill="white" transform="translate(3 3)" />
									</clipPath>
								</defs>
							</svg>
						</a>
					</nav>
				</section>
			</div>
		</div>
		<div class="flex items-center justify-between gap-6 py-6">
			<p>Vozeo &copy; 2025</p>
			<Link text="Política de Privacidad" href="/privacidad" />
		</div>
	</div>
</footer>
