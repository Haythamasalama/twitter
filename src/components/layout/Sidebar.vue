<template>
	<section class="py-2">
		<!-- search box -->
		<search-box />
		<!-- trands tweet -->
		<trands-to-follow />
		<!-- who to follow -->
		<who-to-follow v-for="follow in follows" :key="follow.id" :name="follow.name" :username="follow.username" :image="follow.image" :link="follow.link" />
		<!-- topics to follow -->
		<topics-to-follow />
	</section>
</template>
<script>
	import SearchBox from "@/components/SearchBox.vue";
	import TrandsTweet from "@/components/TrandsTweet.vue";
	import WhoToFollow from "@/components/WhoToFollow.vue";
	import TopicsToFollow from "@/components/TopicsToFollow.vue";

	export default {
		name: "Sidebar",
		components: {
			"search-box": SearchBox,
			"trands-to-follow": TrandsTweet,
			"who-to-follow": WhoToFollow,
			"topics-to-follow": TopicsToFollow,
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
			};
		},
	};
</script>
