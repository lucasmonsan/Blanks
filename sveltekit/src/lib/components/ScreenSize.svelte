<script>
	import { onDestroy } from 'svelte';

	let width = 0;

	function updateWidth() {
		width = window.innerWidth;
	}

	if (typeof window !== 'undefined') {
		updateWidth(); // Definir o valor inicial
		window.addEventListener('resize', updateWidth); // Adicionar listener para redimensionamento
	}

	onDestroy(() => {
		if (typeof window !== 'undefined') window.removeEventListener('resize', updateWidth);
	}); // remover o listener quando o componente for destruído
</script>

<strong>{width}</strong>

<style>
	strong {
		position: fixed;
		top: 1rem;
		right: 1rem;
		font-size: 0.875rem;
		z-index: 1000;
		color: black;
		text-shadow:
			-2px -2px 0 white,
			2px -2px 0 white,
			-2px 2px 0 white,
			2px 2px 0 white;
	}
</style>
