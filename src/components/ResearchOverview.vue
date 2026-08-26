<template>
	<section class="py-5" id="research-overview">
		<p class="eyebrow text-center">RESEARCH OVERVIEW</p>
		<h2 class="text-center mb-3">Understanding School Violence through Evidence</h2>
		<p class="lead text-center mx-auto mb-5" style="max-width: 700px;">
			This project examines documented incidents of school violence in the Philippines, available research, contributing factors and how these issues are discussed in public.
		</p>

	<div class="row justify-content-center g-4 px-4">
		<OverviewCard 
		   v-for="card in cards"
		   :key="card.title"
		   :title="card.title"
		   :description="card.description"
		   :icon="card.icon"
		 />
	</div>
 </section>
</template>

<script setup>
	import OverviewCard from './OverviewCard.vue';

	const cards = [
        {
        	title: 'Documented Incidents',
        	description: 'Examine reported incidents and the information available about them from credible sources.',
        	icon: 'bi-file-earmark-text',
        },
        {
        	 title: 'Contributing Factors',
        	 description: "Explore factors discussed in research surrounding school violence and its broader context.",
        	 icon: 'bi-diagram-3',
        },
        {
        	 title:'Evidence & Context',
        	 description: 'Distinguish documented evidence from assumptions, speculation and unsupported claims.',
        	 icon: 'bi-search',
        },
	];
</script>