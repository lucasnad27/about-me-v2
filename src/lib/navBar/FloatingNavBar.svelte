<script>
	// TODO: find a way to figure out if the main page has begun scrolling
	// binding to window scrollY doesn't seem to work
	let y = 0;
</script>

<div
	class="filter-blur sticky top-0 z-10 flex flex-col justify-center px-3 py-2 dark:border-b dark:border-gray-900 {y >
	0
		? 'bg-white shadow shadow-slate min-h-48'
		: ''}"
>
	<div class="flex flex-none items-center justify-between">
		<span class="flex items-center space-x-3">
			<span
				class="flex cursor-pointer items-center justify-center rounded-md p-2 hover:bg-gray-200 dark:hover:bg-gray-800 lg:hidden"
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="16"
					height="16"
					viewBox="0 0 24 24"
					fill="none"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
					stroke-linejoin="round"
					class="text-primary"
					><line x1="3" y1="12" x2="21" y2="12" /><line x1="3" y1="6" x2="21" y2="6" /><line
						x1="3"
						y1="18"
						x2="21"
						y2="18"
					/></svg
				>
			</span>
			<h2
				class="translate-y-full transform text-sm font-bold text-slate-400 opacity-0 line-clamp-1"
			>
				Home
			</h2>
		</span>
	</div>
</div>
