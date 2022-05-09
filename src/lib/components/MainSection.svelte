<script>
	export let heading;
</script>

<div class="grid grid-cols-1 items-start gap-6 md:grid-cols-12">
	<div
		class="col-span-2 pt-8 text-lg font-extrabold text-black dark:text-white md:pt-0 md:text-right md:text-base md:font-normal md:text-opacity-40"
	>
		{#if heading}
			<h2>{heading}</h2>
		{/if}
	</div>
	<div class="col-span-10">
		<slot />
	</div>
</div>
