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
	import axios from "axios";

	export default {
		name: "Tweets",
		components: {
			NewTweet,
			Tweet,
		},
		data() {
			return {
				teweet: null,
				info: null,
				twetts: null,
			};
		},
		mounted() {
			axios.get("https://vue-twitter-95986-default-rtdb.firebaseio.com/teweet.json").then((data) => {
				const twett = [];
				for (const id in data.data) {
					twett.push({
						actions: {
							comments: data.data[id].actions.comments,
							like: data.data[id].actions.like,
							retweets: data.data[id].actions.retweets,
							share: data.data[id].actions.share,
						},
						content: data.data[id].content,
						id: id,
						time: data.data[id].time,
						user: {
							image: data.data[id].user.image,
							name: data.data[id].user.name,
							username: data.data[id].user.username,
							verified: data.data[id].user.verified,
						},
					});
				}
				this.twetts = twett;
			});
		},
	};
</script>
