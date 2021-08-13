<template>
	<div class="border-b py-3 hover:bg-gray-100 px-4">
		<a :href="link">
			<div class="flex justify-between">
				<div class="flex flex-col">
					<span class="font-bold text-black flex">{{ title }}</span>
					<span class="text-info">{{ info }}</span>
				</div>
				<div>
					<button class="border-primary border rounded-full px-3 py-1 text-primary font-bold">Follow</button>
				</div>
				<div>
					<svg class="text-info w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
					</svg>
				</div>
			</div>
		</a>
	</div>
</template>
<script>
	export default {
		name: "TopicsToFollow",
		props: {
			title: {
				type: String,
				required: true,
			},
			info: {
				type: String,
				required: true,
			},
			link: {
				type: String,
				required: true,
			},
		},
	};
</script>
