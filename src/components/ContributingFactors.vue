<template>
	<section class="py-5" id="contributing-factors">
		<div class="container py-4">
			<p class="eyebrow text-center">CONTRIBUTING FACTORS</p>

			<h2 class="text-center mb-3">Looking Beyond a Single Cause</h2>

			<p class="lead text-center mx-auto mb-5" style="max-width: 800px;">
				To understand why school violence occurs, it is important to
				recognize that a contributing factor is not automatically a cause. 
				Different incidents can involve multiple and overlapping circumstances,
				while some aspects remain unknown.
			</p>

			<p class="lead text-center mx-auto" style="max-width: 800px;">
				This section examines factors that may help provide context around
				school violence. The information presented is intended to help readers
				understand the complexity of the issue and form their own informed 
				opinions.
			</p>

			<div class="row justify-content-center g-4">
                <FactorsCard
                  v-for="factor in factors"
                  :key="factor.id"
                  :title="factor.title"
                  :description="factor.description"
                  :icon="factor.icon"
               />
            </div>


		</div>
	</section>

</template>

<script setup>

import FactorsCard from "./FactorsCard.vue";


const factors = [
	{
		id: 1,
		title: "Individual Factors",
		description: "Examine personal and behavioral circumstances that may be relevant to an incident",
		icon: "bi-person",
	},
	{
		id: 2,
		title: "Interpersonal Factors",
		description: "Explore relationships, grievances, conflict, rejection, bullying, and other social interactions.",
		icon: "bi-people",
	}, 
	{
		id: 3,
		title: "Environmental Factors",
		description: "Consider firearm access, school conditions, family, and community environments, and other external circumstances.",
		icon: "bi-building",
	},
];


</script>