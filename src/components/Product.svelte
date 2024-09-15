<script>
	import ProductCard from './ProductCard.svelte';
	import SectionWrapper from './SectionWrapper.svelte';
	let productFeatures =[
		{
			featureList:[
				'Daily streak counte',
				'Weights and reps tracker',
				'Community challenges',
				'Every workout is new and exciting',
			],
			description: 'Smoley moley ensures all users have the information they need to train safely and train effectively.',
			imgUrl: '',
		},
		{
			featureList:[
				'Personalize your workout',
				'Get a personal trainer in your pocket',
				'Customize your training',
				'Guarantees progress on all core exercises',
			],
			description: 'Build your streaks and see your progress with out amazing tracking and analytics features.',
			imgUrl: '',
		},
		{
			featureList:[
					'Personalized workout plans',
					'Access to premium exercises',
					'Progress tracking and analytics',
					'Community support and motivation',
					'Access to exclusive workout challenges',
			],
			description: 'Enter as much information about yourself as you desire to ensure all workouts are presonalized to your every need.',
			imgUrl: '',
		},
	]

</script>

<SectionWrapper id="product">
	<div class="flex flex-col gap-10 sm:gap-14 md:gap-24 flex-1 items-center justify-center pb-10 md:pd-14"> 
		<div class="flex flex-col gap-2">
			<p class="opacity-60 text-base sm:text-lg md:text-xl text-center">
				Start you lifetime <span class="text-indigo-400">gym streak</span>
				today
			</p>
			<h3 class="text-4xl sm:text-5xl md:text-6xl max-w-[1000px] mx-auto w-full font-semibold text-center">Features For Everyone</h3>
		</div>

		{#each productFeatures as productFeature, index}
			<ProductCard {productFeature} {index}>
				{#if index === 0}
				Experience a begineer exercise <span class="text-indigo-400 font-medium">
					master</span> class 
				{:else if index === 1}
				Lay the foundations for <span class="text-indigo-400 font-medium">routine</span><br/>and consistency
				{:else}
				Workouts specific to your <span class="text-indigo-400 font-medium">environment</span> add
				<span class="text-indigo-400 font-medium">expertise</span>
				{/if}
			</ProductCard>			
		{/each}

	</div>
</SectionWrapper>