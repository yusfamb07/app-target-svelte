<script>
	import { onMount } from 'svelte';
	import { loadScript } from '../compenents/document.js';

	onMount(async () => {
		new DataTable('#example');
	});
</script>
