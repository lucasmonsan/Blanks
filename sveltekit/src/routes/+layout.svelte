<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';
	import ScreenSize from '$lib/components/ScreenSize.svelte';

	import '$lib/styles/normalize.css';
	import '$lib/styles/variables.css';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<ScreenSize />

{@render children?.()}
