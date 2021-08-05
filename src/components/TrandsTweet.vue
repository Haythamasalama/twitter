<template>
	<section class="bg-secondary py-1 rounded-lg my-2">
		<h5 class="font-bold capitalize text-xl border-b py-3 px-4">Trends for you</h5>
		<div class="border-b py-3 hover:bg-gray-100 px-4" v-for="trand in trands" :key="trand.id">
			<a class="text-secondary" :href="trand.link">
				<div class="flex flex-col">
					<span class="font-bold text-black">{{ trand.name }}</span>
					<span class="text-xs text-info pt-2">{{ trand.count }}</span>
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
		name: "TrandsTweet",
		data() {
			return {
				trands: [
					{
						id: 874789,
						name: "NFT",
						count: "10,089,556 Tweets",
						link: "https://twitter.com/NFT",
					},
					{
						id: 374769,
						name: "Ethereum",
						count: "989,556 Tweets",
						link: "https://twitter.com/Ethereum ",
					},
					{
						id: 274739,
						name: "Nuxt",
						count: "98,556 Tweets",
						link: "https://twitter.com/NFT",
					},
				],
			};
		},
	};
</script>
