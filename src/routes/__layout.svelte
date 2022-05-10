<script>
	import '../app.css';
</script>

<div class="relative flex h-full min-h-screen w-full">
	<nav
		class="border-gray-150 dark:boarder-gray-800  lg:translate:-x-0 absolute flex h-full max-h-screen min-h-screen w-3/4 flex-none transform flex-col overflow-y-auto border-r bg-white pb-10 transition duration-200 ease-in-out dark:bg-gray-900 sm:w-1/2 sm:pb-0 md:w-1/3 lg:relative lg:z-auto lg:w-56 lg:bg-gray-50 lg:dark:bg-gray-900 2xl:w-72"
	/>
	<div class="flex flex-1">
		<main class="flex w-full">
			<slot />
		</main>
	</div>
</div>
