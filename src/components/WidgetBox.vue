<template>
	<section class="bg-secondary py-1 rounded-lg my-4">
		<h5 class="font-bold capitalize text-xl border-b py-3 px-4">{{ title }}</h5>
		<slot></slot>
		<div class="py-3 px-4">
			<a :href="showMoreLink" class="text-primary text-left">show more</a>
		</div>
	</section>
</template>
<script>
	export default {
		name: "WidgetBox",
		props: {
			title: {
				type: String,
				required: true,
			},
			showMoreLink: {
				type: String,
				required: true,
				default: "#",
			},
		},
	};
</script>
