<template>
  <div class="col-12 col-md-6 col-lg-4">
   <div class="overview-card h-100 p-4 text-center">
   	<div class="icon-wrap mb-3">
   		<i :class="['bi', icon]"></i>
   	</div>
   	<h5 class="card-title mb-2">{{ title }}</h5>
   	<p class="card-text mb-0">{{ description }}</p>
   </div>
</div>
</template>

<script setup>
	defineProps({
		title: {type: String, required: true},
		description: { type: String, required: true },
		icon: { type: String, required: true },
	});
</script>