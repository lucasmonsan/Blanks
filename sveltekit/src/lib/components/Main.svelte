<script>
	import { fade } from 'svelte/transition';

	export let color = '';
</script>

<main {...$$restProps} in:fade={{ delay: 250 }} out:fade style={`background-color:${color}`}>
	<slot />
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
		flex: 1;
		gap: var(--md);
		width: 100%;
		max-width: 1280px;
		min-height: 100%;
		padding: var(--xs);
		overflow-y: auto;
		scrollbar-width: none; /* Firefox */
		-ms-overflow-style: none; /* IE 10+ */

		&::-webkit-scrollbar {
			display: none; /* Chrome, Safari */
		}
	}
</style>
