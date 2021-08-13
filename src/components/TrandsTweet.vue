<template>
	<div class="border-b py-3 hover:bg-gray-100 px-4">
		<a class="text-secondary" :href="link">
			<div class="flex flex-col">
				<span class="font-bold text-black">{{ name }}</span>
				<span class="text-xs text-info pt-2">{{ count }}</span>
			</div>
		</a>
	</div>
</template>
<script>
	export default {
		name: "TrandsTweet",
		props: {
			name: {
				type: String,
				required: true,
			},
			link: {
				type: String,
				required: true,
			},
			count: {
				type: String,
				required: true,
			},
		},
	};
</script>
