<template>
	<main class="mx-4 h-full border-r border-l">
		<section>
			<!-- home-bar -->
			<section class="flex justify-between border-b p-3">
				<h4 class="font-bold text-xl">Home</h4>
				<svg class="text-primary w-7 hover:bg-primary-300 rounded-full p-1" fill="currentColor" viewBox="0 0 24 24">
					<path d="M22.772 10.506l-5.618-2.192-2.16-6.5a.751.751 0 00-1.424-.001l-2.16 6.5-5.62 2.192a.751.751 0 00.001 1.398l5.62 2.192 2.16 6.5a.752.752 0 001.424 0l2.16-6.5 5.62-2.192a.751.751 0 00-.001-1.397zm-6.49 2.32a.748.748 0 00-.44.46l-1.56 4.695-1.56-4.693a.753.753 0 00-.438-.462l-4.155-1.62 4.154-1.622c.208-.08.37-.25.44-.462l1.56-4.693 1.56 4.694c.07.212.23.382.438.463l4.155 1.62-4.155 1.622zM6.663 3.812h-1.88V2.05a.75.75 0 00-1.5 0v1.762H1.5a.75.75 0 000 1.5h1.782v1.762a.75.75 0 001.5 0V5.312h1.88a.75.75 0 100-1.5zm2.535 15.622h-1.1v-1.016a.75.75 0 10-1.5 0v1.016H5.57a.75.75 0 000 1.5H6.6v1.016a.75.75 0 101.5 0v-1.016h1.098a.75.75 0 000-1.5z" />
				</svg>
			</section>

			<!-- new tweet -->
			<section>
				<new-tweet />
			</section>

			<!-- tweets -->
			<section class="mb-10">
				<tweet v-for="twett in twetts" :key="twett.id" :name="twett.user.name" :username="twett.user.username" :userImage="twett.user.image" :userVerified="twett.user.verified" :time="twett.time" :content="twett.content" :actionLike="twett.actions.like" :actionRetweets="twett.actions.retweets" :actionComments="twett.actions.comments" :actionShare="twett.actions.share" />
			</section>
		</section>
	</main>
</template>
<script>
	import NewTweet from "@/components/NewTweet.vue";
	import Tweet from "@/components/Tweet.vue";

	export default {
		name: "Tweets",
		components: {
			NewTweet,
			Tweet,
		},
		data() {
			return {
				twetts: [
					{
						id: 1,
						user: {
							name: "coinemarkCamp",
							username: "@CoinMarketCap",
							verified: false,
							image: "https://pbs.twimg.com/profile_images/1273411415215411202/9HeiHTVY_normal.jpg",
						},
						content: `
						<p class="text-break px-2 my-2">Two releases today: - 3.1.5 (stable) - bug fixes (specifically script setup features) - 3.2.0-beta.1 - tons of features / perf improvements which we will dive into in a blog post when it hits stable. If you are curious, check out the changelog:</p>
						<div class="m-4 mb-1 border rounded-lg">
							<img class="rounded-lg" alt="coinemarkCamp" src="https://images.unsplash.com/photo-1486312338219-ce68d2c6f44d?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1052&q=80" />
							<p class="p-3">The Alabama Securities Commission asked BlockFi to show why it should not be required stop selling unregistered securities in the state.</p>
						</div>
						`,
						time: "7m",
						actions: {
							like: 16,
							retweets: 10,
							comments: 5,
							share: 3,
						},
					},
					{
						id: 2,
						user: {
							name: "Elon Musk",
							username: "@elonmusk",
							verified: true,
							image: "https://pbs.twimg.com/profile_images/1416443682157473795/dGtFbtht_normal.jpg",
						},
						content: `
						<p class="text-break px-2 my-2">Aiming to stack ship on booster today</p>
						<div class="m-4 mb-1 border rounded-lg">
							<img class="rounded-lg" alt="Musk" src="https://pbs.twimg.com/media/E8DErhlVUAAORur?format=jpg&name=small" />
						</div>
						`,
						time: "4h",
						actions: {
							like: 150,
							retweets: 14,
							comments: 50,
							share: 15,
						},
					},
					{
						id: 3,
						user: {
							name: "Haytham Salama",
							username: "@HaythamAslaama",
							verified: true,
							image: "https://pbs.twimg.com/profile_images/1358878150000857096/nzevXiro_normal.jpg",
						},
						content: `
						<p class="text-break px-2 my-2">This the first tweet in twitter</p>
						`,
						time: "2d",
						actions: {
							like: 1006,
							retweets: 0,
							comments: 0,
							share: 0,
						},
					},
				],
			};
		},
	};
</script>
