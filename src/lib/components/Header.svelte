<script lang="ts">
	import { Navbar, NavHamburger, NavUl, NavLi, DarkMode } from 'flowbite-svelte';
</script>

<Navbar let:NavContainer color="none">
	<NavContainer class="px-5 py-2 md:justify-end">
		<DarkMode class="md:hidden" />
		<NavHamburger />
		<NavUl
			classUl="items-center !text-base"
			nonActiveClass="text-gray-800 md:hover:text-primary-700 dark:text-gray-200 md:dark:hover:text-white"
		>
			<NavLi href="#experience">Experiencia</NavLi>
			<NavLi href="#skills">Habilidades</NavLi>
			<!-- <NavLi href="#projects">Proyectos</NavLi> -->
			<NavLi href="#about">Sobre mí</NavLi>
			<DarkMode class="hidden md:inline" />
		</NavUl>
	</NavContainer>
</Navbar>
