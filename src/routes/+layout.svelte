<script lang="ts">
	import { onMount } from 'svelte';
	import '../app.css';

	onMount(() => {
		if (
			localStorage['color-theme'] === 'dark' ||
			(!('color-theme' in localStorage) &&
				window.matchMedia('(prefers-color-scheme: dark)').matches)
		) {
			document.documentElement.classList.add('dark');
			localStorage['color-theme'] = 'dark';
		} else {
			document.documentElement.classList.remove('dark');
			localStorage.removeItem('color-theme');
		}
	});
</script>

<slot />
