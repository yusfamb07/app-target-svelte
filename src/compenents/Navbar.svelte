<script>
	import NavLink from './NavLink.svelte';
	import icon from '../lib/dashboard.svg';
	import { page } from '$app/stores';
	// let path;

	// function getPath(currentPath) {
	// 	path = currentPath;
	// 	console.log(path);
	// }

	// $: getPath($page.url.pathname);
</script>

<nav class="navbar navbar navbar-expand-lg navbar-dark bg-dark">
	<div class="container-fluid">
		<a class="navbar-brand" />
		<!-- <form class="d-flex">
              <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
              <button class="btn btn-outline-success" type="submit">Search</button>
            </form> -->
		<div class="d-flex align-items-center gap-3">
			<img src="/notification.svg" alt="" />
			<img src="/profile.png" class="mr-5" alt="" />
			<p class="username">Username</p>
			<img src="/down.png" class="mr-5" alt="" />
		</div>
	</div>
</nav>
<div class="bg-dark sidebar-wrapper p-0" id="sidebar-wrapper">
	<ul class="list-group bg-dark d-flex align items-center gap-3">
		<div class="sidebar-heading bg-dark d-flex gap-2 ">
			<div class="row">
				<div class="col-sm-4">
					<img src="/logo.png" alt="" />
				</div>
				<div class="col-md-8 mt-1">
					<h6>Approval Targeting</h6>
					<p class="p-sidebar">Aproval for Target Request</p>
				</div>
			</div>
		</div>

		<li
			class="list-group-item bg-dark"
			class:active={$page.url.pathname.includes('/users/dashboard')}
		>
			<a class="text-white" id="txt-link" href="/users/dashboard"
				><img class="icon p-1" src="/dashboard.svg" alt="" />Dashboard Approval Target</a
			>
		</li>

		<li
			class="list-group-item bg-dark"
			class:active={$page.url.pathname.includes('/users/lawfull')}
		>
			<a class="text-white" id="txt-link" href="/users/lawfull"
				><img class="icon p-1" src="/lawfull.svg" alt="" /> Lawful Interception Request</a
			>
		</li>

		<li
			class="list-group-item bg-dark"
			class:active={$page.url.pathname.includes('/users/geolocation')}
		>
			<a class="text-white" id="txt-link" href="/users/geolocation"
				><img class="icon p-1" src="/geo.svg" alt="" /> Geolocation Request</a
			>
		</li>

		<li
			class="list-group-item bg-dark"
			class:active={$page.url.pathname.includes('/users/telecomunication')}
		>
			<a class="text-white" id="txt-link" href="/users/telecomunication"
				><img class="icon p-1" src="/tele.svg" alt="" /> Telecomunication Request</a
			>
		</li>
	</ul>
	<!-- <div class="sidebar-heading border-bottom bg-dark">Start Bootstrap</div> -->
</div>

<style>
	.list-group-item {
		border-top: 1px solid #8994a5 !important;
		border-bottom: 1px solid #8994a5 !important;
		border: none !important;
		padding: 5px;
		font-family: myFirstFont;
		font-size: 14px;
	}
	.list-group-item.active {
		border-top: 1px solid #8994a5 !important;
		border-bottom: 1px solid #8994a5 !important;
		background-image: radial-gradient(#596573 5%, #404953 15%, #21262b 60%);
	}
	/* nav li a {
		border: none !important;
		padding: 5px;
		font-family: myFirstFont;
		font-size: 14px;
	}
	nav li.active a {
		border-top: 1px solid #8994a5 !important;
		border-bottom: 1px solid #8994a5 !important;
		z-index: 2;
		background-image: radial-gradient(#596573 5%, #404953 15%, #21262b 60%);
	} */
</style>
