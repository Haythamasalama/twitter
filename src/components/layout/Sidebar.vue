<template>
	<section class="py-2">
		<!-- search box -->
		<search-box />
		<!-- trands tweet -->
		<widget-box title="trends for you">
			<trands-to-follow v-for="trand in trands" :key="trand.id" :name="trand.name" :link="trand.link" :count="trand.count" />
		</widget-box>
		<!-- who to follow -->
		<widget-box title="who to follow">
			<who-to-follow v-for="follow in follows" :key="follow.id" :name="follow.name" :username="follow.username" :image="follow.image" :link="follow.link" />
		</widget-box>
		<!-- topics to follow -->
		<widget-box title="topics to follow">
			<topics-to-follow v-for="topic in topics" :key="topic.id" :title="topic.title" :info="topic.info" :link="topic.link" />
		</widget-box>
	</section>
</template>
<script>
	import SearchBox from "@/components/SearchBox.vue";
	import TrandsTweet from "@/components/TrandsTweet.vue";
	import WhoToFollow from "@/components/WhoToFollow.vue";
	import TopicsToFollow from "@/components/TopicsToFollow.vue";
	import WidgetBox from "@/components/WidgetBox.vue";

	export default {
		name: "Sidebar",
		components: {
			"search-box": SearchBox,
			"trands-to-follow": TrandsTweet,
			"who-to-follow": WhoToFollow,
			"topics-to-follow": TopicsToFollow,
			"widget-box": WidgetBox,
		},
		data() {
			return {
				follows: [
					{
						id: 1005,
						name: "Haytham Salama",
						username: "@HaythamAsalama",
						image: "https://pbs.twimg.com/profile_images/1358878150000857096/nzevXiro_normal.jpg",
						link: "https://twitter.com/HaythamAsalama",
					},
					{
						id: 1708,
						name: "Haytham Salama",
						username: "@HaythamAsalama",
						image: "https://pbs.twimg.com/profile_images/1358878150000857096/nzevXiro_normal.jpg",
						link: "https://twitter.com/HaythamAsalama",
					},
				],
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
