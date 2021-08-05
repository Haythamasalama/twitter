<template>
	<section class="bg-secondary py-1 rounded-lg my-2">
		<h5 class="font-bold capitalize text-xl border-b py-3 px-4">Topics to follow</h5>
		<div class="border-b py-3 hover:bg-gray-100 px-4" v-for="topic in topics" :key="topic.id">
			<a :href="topic.link">
				<div class="flex justify-between">
					<div class="flex flex-col">
						<span class="font-bold text-black flex">{{ topic.title }}</span>
						<span class="text-info">{{ topic.info }}</span>
					</div>
					<div>
						<button class="border-primary border rounded-full px-3 py-1 text-primary font-bold">Follow</button>
					</div>
					<div>
						<svg class="text-info w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" /></svg>
					</div>
				</div>
			</a>
		</div>
		<div class="py-3 px-4">
			<a href="#" class="text-primary text-left"> Show more </a>
		</div>
	</section>
</template>
<script>
	export default {
		name: "TopicsToFollow",
		data() {
			return {
				topics: [
					{
						id: 5005,
						title: "Chemistry",
						info: "Science",
						link: "https://twitter.com/Science",
					},
					{
						id: 8945,
						title: "Matrial Design",
						info: "Design",
						link: "https://twitter.com/Design",
					},
					{
						id: 6050,
						title: "Cryptocurrency",
						info: "exchange",
						link: "https://twitter.com/exchange",
					},
				],
			};
		},
	};
</script>
