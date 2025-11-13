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
		},
		{
			title: '📄 Chunking Inteligente',
			what: 'División inteligente de documentos grandes en fragmentos que mantienen sentido completo.',
			why: 'Permite al bot procesar manuales, catálogos y documentos extensos sin perder contexto ni dar respuestas incompletas.',
			growth: '2048 tokens',
			elite: 'Dinámico'
		},
		{
			title: '✅ Umbral de Confianza',
			what: 'Sistema que mide qué tan seguro está el bot de su respuesta antes de enviarla.',
			why: 'Evita que el bot "invente" respuestas. Si no está seguro, pide aclaraciones o deriva a un humano, protegiendo tu reputación.',
			start: '50% fijo',
			growth: 'Ajustable',
			elite: 'ML adaptativo'
		},
		{
			title: '🔌 Function Calling',
			what: 'Capacidad del bot para conectarse y ejecutar acciones en otros sistemas (CRM, inventario, pagos).',
			why: 'El bot puede consultar stock, crear pedidos, agendar citas o verificar pagos en tiempo real sin intervención humana.',
			growth: '3 APIs',
			elite: 'Ilimitado + Custom'
		},
		{
			title: '🧠 Planner Multi-Agente',
			what: 'Sistema que descompone tareas complejas en pasos simples que el bot ejecuta secuencialmente.',
			why: 'Permite al bot manejar procesos complejos como "cambiar pedido y reprogramar envío" ejecutando cada paso correctamente.',
			growth: '5 pasos',
			elite: 'Ilimitado'
		},
		{
			title: '💭 Memoria Dual Persistente',
			what: 'Sistema de memoria que recuerda preferencias del cliente (semántica) y conversaciones anteriores (episódica).',
			why: 'El bot recuerda a cada cliente, sus compras anteriores, preferencias y problemas resueltos, creando una experiencia personalizada.',
			start: '48 horas',
			growth: '30 días',
			elite: 'Permanente'
		},
		{
			title: '🛡️ Self-Check Multi-Layer',
			what: 'Sistema de verificación que revisa cada respuesta antes de enviarla (gramática, tono, políticas, seguridad).',
			why: 'Garantiza que cada mensaje sea profesional, correcto y alineado con tu marca, evitando errores costosos.',
			start: '2 capas',
			growth: '4 capas',
			elite: '5 capas + Custom'
		},
		{
			title: '🚦 Guardrails Adaptativos',
			what: 'Barreras de seguridad que previenen comportamientos no deseados del bot.',
			why: 'Protege información sensible, evita promesas que no puedes cumplir y mantiene conversaciones dentro de límites seguros.',
			start: 'Templates',
			growth: 'Customizable',
			elite: 'AI-Powered'
		},
		{
			title: '📊 Observabilidad Total',
			what: 'Sistema completo de monitoreo que rastrea cada interacción, métrica y resultado.',
			why: 'Ves en tiempo real qué funciona, dónde hay problemas y cómo mejorar, con dashboards ejecutivos claros.',
			start: 'Básica',
			growth: 'Completa',
			elite: 'Predictiva + Alertas'
		},
		{
			title: '🎭 Personalidades Dinámicas',
			what: 'Diferentes "personalidades" del bot según contexto (formal para B2B, amigable para B2C, técnica para soporte).',
			why: 'El bot adapta automáticamente su tono y estilo según el cliente, creando conexiones más naturales y efectivas.',
			start: '1 fija',
			growth: '3 switchables',
			elite: 'Ilimitadas + A/B'
		},
		{
			title: '🔄 Continuous Learning',
			what: 'Sistema que mejora automáticamente basándose en cada interacción y feedback.',
			why: 'El bot se vuelve más inteligente con el tiempo, aprendiendo de errores y mejorando respuestas sin intervención manual.',
			growth: 'Manual',
			elite: 'Automático'
		},
		{
			title: '🌐 Gestión Multicanal',
			what: 'Capacidad de gestionar todas las redes sociales y canales de comunicación desde un solo lugar.',
			why: 'No más cambiar entre WhatsApp, Instagram, Facebook, Email. Todo centralizado, sin perder ningún mensaje.',
			start: 'WhatsApp + Email',
			growth: 'Todas las redes',
			elite: '+ Custom channels'
		},
		{
			title: '📈 Lead Scoring & Nurturing',
			what: 'Sistema que califica automáticamente qué tan "caliente" está cada lead y los nutre hasta la venta.',
			why: 'Prioriza los leads más prometedores y mantiene a los tibios en proceso automático hasta que estén listos para comprar.',
			growth: 'Básico',
			elite: 'IA Predictiva'
		},
		{
			title: '🎯 Campañas Automatizadas',
			what: 'Secuencias de marketing que se ejecutan solas según comportamiento del cliente.',
			why: 'Carrito abandonado, cumpleaños, recompra, onboarding — todo automatizado sin que tengas que hacer nada.',
			start: '2 flujos',
			growth: '10 flujos',
			elite: 'Ilimitados'
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
