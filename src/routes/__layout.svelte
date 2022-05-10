<script>
	import '../app.css';
	import SideNavBar from '$lib/navBar/SideNavBar.svelte';
</script>

<div class="relative flex h-full min-h-screen w-full">
	<SideNavBar />
	<div class="flex flex-1">
		<main class="flex w-full">
			<slot />
		</main>
	</div>
</div>
