<template>
	<article class="factor-card h-100">
		<div class="factor-card_icon">
			<i :class="`bi ${icon}`" aria-hidden="true"></i>
		</div>

		<h3 class="factor-card_title">{{ title }}</h3>

		<p class="factor-card_description">{{ description }}</p>
	</article>
</template>

<script setup>
	defineProps({
		title: {
          type: String,
          required: true,
		},
		description: {
			type: String,
			required: true,
		},
		icon: {
			type: String,
			required: true,
		},
	});
</script>