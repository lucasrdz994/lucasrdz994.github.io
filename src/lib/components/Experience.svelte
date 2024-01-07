<script>
	import { Timeline, TimelineItem } from 'flowbite-svelte';

	const timeline = [
		{
			title: 'Desarrollador Full Stack en Dynamo Mobile.',
			date: 'Mayo 2023 - Presente',
			content:
				'En mi rol como Desarrollador Full Stack en Dynamo Mobile, desempeño un papel fundamental en la evolución y mejora constante de la plataforma de omnicanalidad, chatbot y contact center. Mi trabajo se centra en el desarrollo de nuevas funcionalidades que enriquecen la	experiencia del usuario y optimizan la eficiencia operativa.'
		},
		{
			title: 'Desarrollador Full Stack en Lumile Argentina.',
			date: 'Mayo 2021 - Abril 2023',
			content:
				'Mi experiencia en Lumile Argentina me ha permitido desempeñar un papel integral en el desarrollo de LumbreDocs, una plataforma esencial en el campo de la gestión de documentos y firma digital de los mismos. Mis responsabilidades hacían foco en la planificación, diseño y programación de mejoras y nuevas funcionalidades.'
		},
		{
			title: 'Desarrollador Web Freelance.',
			date: 'Abril 2016 - Marzo 2021',
			content:
				'Durante mi tiempo como Desarrollador Web Freelance, he tenido la oportunidad de diseñar y desarrollar una amplia variedad de proyectos web, desde landing pages, blogs, e-commerce y sistemas de gestión de stock y logística entre otros. Para dichos proyectos adopté herramientas serverless para la optimización de performance y tiempos ampliando mi	catálogo de conocimientos.'
		},
		{
			title: 'Gestión comercial en Amitosai Stores.',
			date: 'Junio 2016 - Mayo 2021',
			content:
				'Me he especializado en el desarrollo y mantenimiento de e-commerce, así como en la	creación de aplicaciones de logística mediante la integración con Mercado Libre mejorando	ampliamente la comunicación con los clientes y la experiencia de compra.'
		}
	];
</script>

<section id="experience" class="section-container bg-white/10">
	<div class="section-box flex flex-col items-center gap-12">
		<h2
			class="text-3xl leading-8 border-b-[0.75rem] border-solid border-primary-300 dark:border-slate-600 font-[roboto-slab]"
		>
			Experiencia
		</h2>
		<Timeline>
			{#each timeline as item}
				<TimelineItem
					title={item.title}
					date={item.date}
					classTime="text-gray-700 dark:text-gray-300"
					classDiv="bg-gray-300"
				>
					<p class="mb-4 text-base font-normal text-gray-700 dark:text-gray-400">
						{item.content}
					</p>
				</TimelineItem>
			{/each}
		</Timeline>
	</div>
</section>
