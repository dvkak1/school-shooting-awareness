<template>
	<article class="incident-card">
		<div class="incident-card_header">
			<p class="incident-card_date">{{ date }}</p>
			<span class="incident-card_status">{{ status }}</span>
	    </div>

	    <h3 class="incident-card_title">
	    	{{ title }}
	    </h3>

	    <p class="incident-card_location">
	    	{{ location }}
	    </p>

	    <p class="incident-card_classification">
	    	{{ classification }}
	    </p>


	    <div class="incident-card_content">
	    	<h4>What Happened</h4>
	    	<p>{{ description }}</p>
	    </div>

	    <div class="incident-card_content">
           <h4>Historical Context</h4>
           <p>{{ context }}</p>
	    </div>
	</article>
</template>


<script setup>
defineProps({
	date: {
		type: String,
		required: true,
	},
	title: {
		type: String,
		required: true,
	},
	location: {
		type: String,
		required: true,
	},
	classification: {
		type: String,
		required: true,
	},
	status: {
		type: String,
		required: true,
	},
	description: {
		type: String,
		required: true,
	},
	context: {
		type: String,
		required: true,
	},
})	
</script>