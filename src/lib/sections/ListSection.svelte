<script>
	// would be ideal to give the user better typing here
	export let items;
</script>

<div class="flex-col space-y-3">
	{#each items as item}
		<a
			target="_blank"
			rel="noopener noreferrer"
			href={item.link}
			class="group flex items-center space-x-4"
			><strong
				class="text-gray-1000 flex-none font-medium group-hover:text-blue-600 group-hover:underline dark:text-gray-100 dark:group-hover:text-blue-500"
				>{item.name}</strong
			><span
				class="w-full shrink border-t border-dashed border-gray-300 dark:border-gray-800"
			/><span class="flex-none text-slate-400">{item.details}</span>
			{#if item.moreInfo}
				<span class="flex-none font-mono text-gray-400">{item.moreInfo}</span>
			{/if}</a
		>
	{/each}
</div>
