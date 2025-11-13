<script>
	import Ai from './Ai.svelte';
	import Card from './Card.svelte';
	import Numbers from './Numbers.svelte';

	const cards = [
		{
			cta: 'EMPEZAR AHORA',
			title: 'Start',
			price: 600,
			content: [
				{
					emoji: '🌐',
					title: 'Website + Funnels',
					content: 'Website básico editable + 1 funnel optimizado'
				},
				{
					emoji: '🧰',
					title: 'CRM',
					content:
						'Gestión unificada omnicanal de usuarios, captura de leads, etiquetas y pipelines básicos'
				},
				{
					emoji: '📩',
					title: 'Email Marketing',
					content: '1 campaña mensual'
				},
				{
					emoji: '📅',
					title: 'Agenda inteligente',
					content: 'Calendario de citas integrado'
				},
				{
					emoji: '🤖',
					title: 'Automatizaciones',
					content: 'Seguimiento básico email/WhatsApp y todas las redes sociales'
				},
				{
					emoji: '📊',
					title: 'Métricas',
					content: 'Dashboard básico de leads y ventas'
				},
				{
					emoji: '💬',
					title: 'Chatbot IA',
					content:
						'Bot conversacional con RAG, personalidades múltiples, tiempos de respuesta variables, audios y comportamiento humano (con limitaciones)'
				},
				{
					emoji: '👨‍💼',
					title: 'Consultoría',
					content: 'Opcional'
				}
			],
			button: 'Empezar Ahora'
		},
		{
			cta: 'ESCALAR MI NEGOCIO',
			title: 'Growth',
			price: 900,
			tag: 'MÁS POPULAR',
			content: [
				{
					emoji: '🌐',
					title: 'Website + Funnels',
					content: 'Website + múltiples funnels optimizados'
				},
				{
					emoji: '🧰',
					title: 'CRM Completo',
					content:
						'Gestión unificada omnicanal de usuarios, CRM con secuencias y nurturing multi-canal'
				},
				{
					emoji: '📩',
					title: 'Email Marketing con IA',
					content: 'Campañas + IA para redacción y segmentación avanzada'
				},
				{
					emoji: '📅',
					title: 'Agenda + Inbox',
					content: 'Agenda + integración en inbox unificado'
				},
				{
					emoji: '📲',
					title: 'Gestión multicanal',
					content: 'Inbox unificado (IG, FB, WhatsApp, Email) + asistente preconfigurado'
				},
				{
					emoji: '🤖',
					title: 'Automatizaciones Avanzadas',
					content:
						'Recuperación de oportunidades, onboarding, upsell, seguimiento en todas las redes sociales'
				},
				{
					emoji: '🧪',
					title: 'Pruebas A/B',
					content: 'Funnels, formularios y campañas'
				},
				{
					emoji: '📤',
					title: 'Reseñas',
					content: 'Solicitud de reviews automatizada'
				},
				{
					emoji: '📊',
					title: 'Métricas Avanzadas',
					content: 'Reportes con segmentación y pruebas A/B'
				},
				{
					emoji: '💬',
					title: 'Chatbot Avanzado',
					content:
						'Bot íntegramente conversacional con RAG aumentado, personalidades múltiples, tiempos de respuesta variables, audios y comportamiento humano total'
				},
				{
					emoji: '🧩',
					title: 'Integraciones',
					content: 'Integraciones estándar (redes + CRM)'
				},
				{
					emoji: '📦',
					title: 'Gestión de Inventario',
					content: 'Control manual de inventario o control de usuarios y/o miembros'
				},
				{
					emoji: '🎫',
					title: 'Códigos de Descuento',
					content: '20 códigos para miembros/clientes'
				},
				{
					emoji: '👨‍💼',
					title: 'Consultoría',
					content: 'Opcional'
				}
			],
			button: 'Escalar mi Negocio'
		},
		{
			cta: 'PLAN PREMIUM',
			title: 'Elite AI Suite',
			price: 1200,
			premium: true,
			content: [
				{
					emoji: '🌐',
					title: 'Website Premium',
					content: 'Website avanzado + módulos dinámicos + blog con IA'
				},
				{
					emoji: '🧰',
					title: 'CRM Ultra Avanzado',
					content:
						'Gestión unificada omnicanal de usuarios, CRM con automatización avanzada + pipeline visual'
				},
				{
					emoji: '📩',
					title: 'Email Marketing Total',
					content: 'Email marketing potenciado con IA y automatización total'
				},
				{
					emoji: '📅',
					title: 'Agenda + Chatbot IA',
					content: 'Agenda + chatbot IA para reservas y ventas'
				},
				{
					emoji: '📲',
					title: 'Agentes IA 24/7',
					content: 'Agentes de IA multicanal con soporte 24/7'
				},
				{
					emoji: '🤖',
					title: 'Automatización Total',
					content:
						'Procesos internos automatizados + recordatorios y flujos de ventas, seguimiento en todas las redes sociales'
				},
				{
					emoji: '🧪',
					title: 'Pruebas A/B Avanzadas',
					content: 'Funnels, formularios y campañas avanzados'
				},
				{
					emoji: '📤',
					title: 'Reseñas + Chatbot',
					content: 'Reseñas + chatbot para feedback post-servicio'
				},
				{
					emoji: '📊',
					title: 'Reportes Ejecutivos',
					content: 'Reportes en tiempo real (ROI, tráfico, conversiones)'
				},
				{
					emoji: '💬',
					title: 'Chatbot Avanzado',
					content:
						'Bot íntegramente conversacional con RAG aumentado, personalidades múltiples, tiempos de respuesta variables, audios y comportamiento humano total'
				},
				{
					emoji: '🧩',
					title: 'Integraciones API',
					content: 'Integraciones personalizadas (ERP, inventarios, etc.)'
				},
				{
					emoji: '📦',
					title: 'Gestión de Inventario',
					content: 'Control automatizado con IA de inventario o control de usuarios y/o miembros'
				},
				{
					emoji: '🎫',
					title: 'Códigos de Descuento',
					content: 'Ilimitados para miembros/clientes'
				},
				{
					emoji: '📱',
					title: 'Marketing Digital Integrado',
					content:
						'Anuncios, estrategias de contenido, reposteos de reels y contenido automático entre redes, métricas de publicaciones, captura orgánica de leads calificados'
				},
				{
					emoji: '👨‍💼',
					title: 'Consultoría Premium',
					content: 'Incluida (1 a 1 mensual)'
				}
			],
			button: 'Escalar mi Negocio'
		}
	];

	const ais = [
		{
			title: '🔍 Motor de Búsqueda Híbrido',
			what: 'Sistema que combina búsqueda semántica (entiende significado) con búsqueda exacta (encuentra palabras específicas). Como tener Google dentro de tu chatbot.',
			why: 'El bot encuentra información precisa en tu base de conocimiento, productos o FAQs, entendiendo lo que el cliente pregunta aunque use diferentes palabras.',
			growth: '1,000 docs',
			elite: 'Ilimitado'
		},
		{
			title: '🎯 Reranker Cross-Encoder',
			what: 'IA que reordena las respuestas poniendo la más relevante primero, como un experto que revisa todas las opciones.',
			why: 'Garantiza que el bot siempre dé la mejor respuesta disponible, no solo la primera que encuentra.',
			growth: '✓ Estándar',
			elite: '✓ GPT-4o'
		}
	];
</script>

<svelte:head>
	<title>Lista de Precios | Vozeo</title>
</svelte:head>

<main class="px-6">
	<article class="mw flex flex-col gap-8 pt-32 pb-16 md:gap-16 md:pt-40">
		<div class="space-y-6 text-center">
			<h1>Automatización Inteligente para tu Negocio 🚀</h1>
			<h2 class="text-lg text-balance md:text-xl">
				IA Conversacional + CRM + Marketing Digital + Automatización Total
			</h2>
		</div>
		<Numbers />
		<section class="grid gap-6 lg:grid-cols-3">
			{#each cards as card}
				<Card {...card} />
			{/each}
		</section>
		<section class="rounded-3xl bg-blue px-6 py-8 text-slate-500">
			<div class="mx-auto flex max-w-2xl flex-col items-center gap-4 text-center">
				<div class="flex flex-col gap-3">
					<h2 class="text-2xl font-black text-yellow md:text-4xl">⚡ Implementación Express</h2>
					<p class="text-xl text-yellow">Tiempo de implementación: Desde 10 días hábiles*</p>
				</div>
				<p>
					El primer mes se abona el doble del valor mensual del plan elegido como inversión única de
					setup que incluye:
				</p>
				<ul class="list-disc ps-2 text-start">
					<li>Migración completa de datos existentes</li>
					<li>Configuración de todas las herramientas</li>
					<li>Personalización de chatbot con IA</li>
					<li>Training completo para tu equipo</li>
					<li>Soporte dedicado durante el onboarding</li>
				</ul>
				<p class="text-sm">
					*El tiempo exacto depende de la complejidad del proyecto y volumen de datos a migrar
				</p>
			</div>
		</section>
		<section class="rounded-3xl border border-blue/25 px-6 py-8 text-slate-500">
			<div class="flex flex-col items-center gap-6 text-center">
				<div class="flex flex-col gap-4">
					<h2 class="text-2xl font-black text-blue md:text-4xl">🧠 Tecnología de IA Explicada</h2>
					<p class="text-lg text-blue">Comprende exactamente qué obtienes con cada plan</p>
				</div>
				<div class="grid gap-6 md:grid-cols-2 lg:grid-cols-4">
					{#each ais as ai}
						<Ai {...ai} />
					{/each}
				</div>
			</div>
		</section>
	</article>
</main>
