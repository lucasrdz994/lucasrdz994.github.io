<script lang="ts">
	import VueIcon from '$lib/assets/icons/vuedotjs.svg';
	import SvelteIcon from '$lib/assets/icons/svelte.svg';
	import JavaScriptIcon from '$lib/assets/icons/javascript.svg';
	import TypeScriptIcon from '$lib/assets/icons/typescript.svg';
	import NodeJsIcon from '$lib/assets/icons/nodedotjs.svg';
	import RedisIcon from '$lib/assets/icons/redis.svg';
	import MongoDbIcon from '$lib/assets/icons/mongodb.svg';
	import MysqlDbIcon from '$lib/assets/icons/mysql.svg';
	import ElasticSearchIcon from '$lib/assets/icons/elasticsearch.svg';
	import RabbitMqIcon from '$lib/assets/icons/rabbitmq.svg';

	const skills = [
		{
			title: 'Vue',
			icon: VueIcon,
			iconAlt: 'vue-icon'
		},
		{
			title: 'Svelte',
			icon: SvelteIcon,
			iconAlt: 'svelte-icon'
		},
		{
			title: 'JavaScript',
			icon: JavaScriptIcon,
			iconAlt: 'javascript-icon'
		},
		{
			title: 'TypeScript',
			icon: TypeScriptIcon,
			iconAlt: 'typescript-icon'
		},
		{
			title: 'NodeJs',
			icon: NodeJsIcon,
			iconAlt: 'nodejs-icon'
		},
		{
			title: 'Redis',
			icon: RedisIcon,
			iconAlt: 'redis-icon'
		},
		{
			title: 'MongoDB',
			icon: MongoDbIcon,
			iconAlt: 'mongodb-icon'
		},
		{
			title: 'MySQL',
			icon: MysqlDbIcon,
			iconAlt: 'mysql-icon'
		},
		{
			title: 'ElasticSearch',
			icon: ElasticSearchIcon,
			iconAlt: 'elasticsearch-icon'
		},
		{
			title: 'RabbitMQ',
			icon: RabbitMqIcon,
			iconAlt: 'rabbitmq-icon'
		}
	];
</script>

<section id="skills" class="section-container bg-white/10">
	<div class="section-box flex flex-col items-center gap-12">
		<h2
			class="text-3xl leading-8 border-b-[0.75rem] border-solid border-primary-300 dark:border-slate-600 font-[roboto-slab]"
		>
			Mis habilidades
		</h2>
		<p class="mb-8">
			Poseo un enfoque sólido en JavaScript mediante un amplio conjunto de habilidades para llevar a
			cabo proyectos web de principio a fin. Mi experiencia abarca desde la creación de interfaces
			de usuario atractivas y funcionales utilizando las últimas tecnologías front-end, hasta la
			implementación de servidores robustos y bases de datos eficientes.
		</p>

		<section class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-6">
			{#each skills as item}
				<article
					class="p-5 border rounded-xl shadow-lg bg-primary-50 dark:bg-slate-900 dark:border-slate-700 flex flex-col items-center justify-center gap-y-3"
				>
					<img src={item.icon} alt={item.iconAlt} class="w-10 h-10" />
					<h4>{item.title}</h4>
				</article>
			{/each}
		</section>
	</div>
</section>
