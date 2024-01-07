<script lang="ts">
	import Header from '$lib/components/Header.svelte';
	import { Button, GradientButton } from 'flowbite-svelte';
	import { DownloadOutline, GithubSolid, LinkedinSolid } from 'flowbite-svelte-icons';

	import dev from '$lib/assets/images/dev.svg';

	async function handleDownloadResume() {
		const link = document.createElement('a');
		link.href = '/files/resume.pdf';
		link.download = 'lucas-rodriguez-resume';
		link.click();
		link.remove();
	}
</script>

<section class="flex flex-col items-center relative min-h-screen hero-wrapper">
	<Header />
	<div class="section-box flex items-center gap-12 pb-[92px] flex-1">
		<section class="flex-1">
			<h3
				class="inline-block text-4xl lg:text-6xl mb-2 whitespace-nowrap border-b-[1.2rem] border-solid border-primary-300 dark:border-slate-800 font-[roboto-slab]"
			>
				Lucas Rodríguez
			</h3>
			<h1 class="text-xl lg:text-2xl mb-8 uppercase">Full Stack Developer</h1>
			<p class="text-sm lg:text-base text-balance mb-8">
				Hola! 👋 Soy <strong>desarrollador</strong> de aplicaciones web <strong>Full Stack</strong>
				con <strong>TypeScript</strong> , haciendo uso de herramientas y frameworks modernos para
				crear interfaces y servicios funcionales de <strong>alto rendimiento</strong>. 🚀
			</p>
			<div class="flex items-center gap-6 flex-wrap">
				<GradientButton
					color="purpleToBlue"
					size="xl"
					pill
					shadow
					class="font-semibold"
					on:click={handleDownloadResume}
				>
					<DownloadOutline class="w-4 h-4 me-2" />
					Descarga mi Curriculum
				</GradientButton>
				<div class="flex items-center gap-x-6">
					<Button
						class="p-4 shadow-lg"
						color="light"
						pill
						outline
						href="https://www.linkedin.com/in/lucas-damian-rodriguez/"
						target="_blank"
					>
						<LinkedinSolid size="lg" class="text-slate-800 dark:text-slate-50" />
					</Button>
					<Button
						class="p-4 shadow-lg"
						color="light"
						pill
						outline
						href="https://github.com/lucasrdz994"
						target="_blank"
					>
						<GithubSolid size="lg" class="text-slate-800 dark:text-slate-50" />
					</Button>
				</div>
			</div>
		</section>

		<div class="dev-image-wrapper hidden lg:flex items-center justify-center">
			<img src={dev} alt="A bird sitting on a nest of eggs." />
		</div>
	</div>
</section>

<style>
	.hero-wrapper {
		background: rgb(116, 209, 227);
		background: linear-gradient(
			45deg,
			rgba(116, 209, 227, 0.3) 0%,
			rgba(154, 218, 231, 0.3) 50%,
			rgba(201, 246, 255, 0.3) 100%
		);
	}
</style>
