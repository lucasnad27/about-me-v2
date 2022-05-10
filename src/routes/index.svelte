<script>
	import config from '$lib/conf';
	import IntroductionSection from '$lib/sections/IntroductionSection.svelte';
	import ListSection from '$lib/sections/ListSection.svelte';
	import MainSection from '$lib/components/MainSection.svelte';
	import FloatingNavBar from '$lib/navBar/FloatingNavBar.svelte';

	let onlineItems = [
		{
			name: 'Github',
			link: 'https://github.com/lucasnad27',
			details: 'Follow'
		},
		{
			name: 'Polywork',
			link: 'https://www.polywork.com/lucasnad27',
			details: 'Follow'
		},
		{
			name: 'LinkedIn',
			link: 'https://www.linkedin.com/in/lucasnad27/',
			details: 'Connect'
		}
	];
	let workItems = [
		{
			name: 'Granicus',
			link: 'https://granicus.com',
			details: 'Dir of Engineering',
			moreInfo: '2019-2021'
		},
		{
			name: 'Host Compliance',
			link: 'https://granicus.com/solution/govservice/host-compliance/',
			details: 'Dir. of Engineering',
			moreInfo: '2018-2019'
		},
		{
			name: 'SiriusXM',
			link: 'https://www.siriusxmcvs.com',
			details: 'Dir. of Platform Engineering',
			moreInfo: '2017-2018'
		},
		{
			name: 'Automatic Labs',
			link: 'https://www.cnet.com/roadshow/reviews/automatic-labs-automatic-review/',
			details: 'Engineering Lead',
			moreInfo: '2014-2017'
		}
	];
	let mapUrl = `https://api.mapbox.com/styles/v1/mapbox/outdoors-v11/static/pin-l+555555(-104.997,39.7521)/-105.7434,39.6485,8.71,0/1200x600?access_token=${config.mapboxToken}`;
</script>

<div class="relative flex max-h-screen w-full flex-col overflow-y-auto bg-white dark:bg-black">
	<FloatingNavBar />
	<!-- I'd like to find a better way of applying some space here -->
	<div class="p-4" />
	<div class="mx-auto w-full max-w-3xl px-4 pt-12 pb-10 md:px-8">
		<div class="space-y-8 pb-24 md:space-y-16">
			<MainSection>
				<IntroductionSection />
			</MainSection>
			<MainSection heading="Online">
				<ListSection items={onlineItems} />
			</MainSection>
			<MainSection heading="Where">
				<img class="w-full rounded-xl" src={mapUrl} alt="Map of Denver, CO" />
				<p
					class="texxt-sm text-quaternary flex items-center justify-end space-x-2 pt-2 md:text-right"
				>
					<svg
						xmlns="http://www.w3.org/2000/svg"
						width="12"
						height="12"
						viewBox="0 0 24 24"
						fill="none"
						stroke="currentColor"
						stroke-width="2"
						stroke-linecap="round"
						stroke-linejoin="round"
						><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z" /><circle
							cx="12"
							cy="10"
							r="3"
						/></svg
					>
					<span>Denver, CO</span>
				</p>
			</MainSection>
			<MainSection heading="Work">
				<ListSection items={workItems} />
			</MainSection>
		</div>
	</div>
</div>
