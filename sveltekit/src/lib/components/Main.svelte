<script>
	import { fade } from 'svelte/transition';
</script>

<main {...$$restProps} in:fade={{ delay: 250 }} out:fade>
	<slot />
</main>

<style>
	main {
		position: absolute;
		display: flex;
		flex-direction: column;
		align-items: center;
		flex: 1;
		width: 100%;
		max-width: var(--max-width-page);
		min-height: 100%;
		padding: var(--padd-page);
		overflow-y: auto;
		scrollbar-width: none; /* Firefox */
		-ms-overflow-style: none; /* IE 10+ */

		&::-webkit-scrollbar {
			display: none; /* Chrome, Safari */
		}
	}
</style>
