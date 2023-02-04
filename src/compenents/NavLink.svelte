<script>
	import { page } from '$app/stores';
	import { onMount } from 'svelte';

	export let href;
	export let title;
	export let icon;
	// let currentPath;
	// onMount(() => {
	// 	currentPath = window.location.pathname;
	// });
</script>

<a
	class="list-group-item bg-dark  text-white"
	class:active={$page.url.pathname.split('/')[1] === href.split('/')[1]}
	{href}
	><img class="icon p-1" src="/dashboard.svg" alt="" />
	{title}
</a>

<!-- <a
	{href}
	class="list-group-item bg-dark  text-white"
	class:active={currentPath.split('/')[1] === href.split('/')[1]}
	><img class="icon p-1" src="/dashboard.svg" alt="" />
	{title}
</a> -->
<style>
	.list-group-item {
		border: none !important;
		padding: 5px;
		font-family: myFirstFont;
		font-size: 14px;
	}
	.list-group-item.active {
		border-top: 1px solid #8994a5 !important;
		border-bottom: 1px solid #8994a5 !important;
		z-index: 2;
		background-image: radial-gradient(#596573 5%, #404953 15%, #21262b 60%);
	}
</style>
