<template>
	<section class="flex border-b-8 px-3 py-3">
		<div class="mx-2">
			<img class="rounded-full" alt="HaythamASalama" src="https://pbs.twimg.com/profile_images/1358878150000857096/nzevXiro_normal.jpg" />
		</div>

		<div class="flex flex-col w-full">
			<div class="mx-1 py-3">
				<span class="cursor-text text-2xl text-info w-auto outline-none" contenteditable>{{ tweet }}</span>
			</div>
			<div class="flex justify-between border-t pt-3 mt-3">
				<div class="flex flex-row">
					<svg class="text-primary w-8 hover:bg-primary-300 rounded-full p-1" fill="currentColor" viewBox="0 0 24 24"><path d="M19.75 2H4.25C3.01 2 2 3.01 2 4.25v15.5C2 20.99 3.01 22 4.25 22h15.5c1.24 0 2.25-1.01 2.25-2.25V4.25C22 3.01 20.99 2 19.75 2zM4.25 3.5h15.5c.413 0 .75.337.75.75v9.676l-3.858-3.858a.75.75 0 00-.53-.22h-.003a.74.74 0 00-.532.224l-4.317 4.384-1.813-1.806a.75.75 0 00-.53-.22c-.193-.03-.395.08-.535.227L3.5 17.642V4.25c0-.413.337-.75.75-.75zm-.744 16.28l5.418-5.534 6.282 6.254H4.25a.75.75 0 01-.744-.72zm16.244.72h-2.42l-5.007-4.987 3.792-3.85 4.385 4.384v3.703c0 .413-.337.75-.75.75z" /></svg>
					<svg class="text-primary w-8 hover:bg-primary-300 rounded-full p-1" fill="currentColor" viewBox="0 0 24 24">
						<path d="M19 10.5V8.8h-4.4v6.4h1.7v-2h2v-1.7h-2v-1H19zm-7.3-1.7h1.7v6.4h-1.7V8.8zm-3.6 1.6c.4 0 .9.2 1.2.5l1.2-1C9.9 9.2 9 8.8 8.1 8.8c-1.8 0-3.2 1.4-3.2 3.2s1.4 3.2 3.2 3.2c1 0 1.8-.4 2.4-1.1v-2.5H7.7v1.2h1.2v.6c-.2.1-.5.2-.8.2-.9 0-1.6-.7-1.6-1.6 0-.8.7-1.6 1.6-1.6z" />
						<path d="M20.5 2.02h-17a2.25 2.25 0 00-2.25 2.247v15.507A2.251 2.251 0 003.5 22.02h17c1.24 0 2.25-1.008 2.25-2.246V4.267A2.25 2.25 0 0020.5 2.02zm.75 17.754a.75.75 0 01-.75.746h-17a.75.75 0 01-.75-.746V4.267c0-.412.336-.747.75-.747h17c.414 0 .75.335.75.747v15.507z" />
					</svg>
					<svg class="text-primary w-8 hover:bg-primary-300 rounded-full p-1" fill="currentColor" viewBox="0 0 24 24"><path d="M20.222 9.16h-1.334c.015-.09.028-.182.028-.277V6.57c0-.98-.797-1.777-1.778-1.777H3.5V3.358a.75.75 0 00-1.5 0V20.83a.75.75 0 101.5 0v-1.434h10.556a1.78 1.78 0 001.778-1.777v-2.313c0-.095-.014-.187-.028-.278h4.417a1.78 1.78 0 001.778-1.778v-2.31a1.78 1.78 0 00-1.778-1.78zM17.14 6.293c.152 0 .277.124.277.277v2.31a.28.28 0 01-.278.28H3.5V6.29h13.64zm-2.807 9.014v2.312a.278.278 0 01-.278.277H3.5v-2.868h10.556c.153 0 .277.126.277.28zM20.5 13.25a.278.278 0 01-.278.277H3.5V10.66h16.722c.153 0 .278.124.278.277v2.313z" /></svg>
					<svg class="text-primary w-8 hover:bg-primary-300 rounded-full p-1" fill="currentColor" viewBox="0 0 24 24">
						<g>
							<path d="M12 22.75C6.072 22.75 1.25 17.928 1.25 12S6.072 1.25 12 1.25 22.75 6.072 22.75 12 17.928 22.75 12 22.75zm0-20C6.9 2.75 2.75 6.9 2.75 12S6.9 21.25 12 21.25s9.25-4.15 9.25-9.25S17.1 2.75 12 2.75z"></path>
							<path d="M12 17.115c-1.892 0-3.633-.95-4.656-2.544-.224-.348-.123-.81.226-1.035.348-.226.812-.124 1.036.226.747 1.162 2.016 1.855 3.395 1.855s2.648-.693 3.396-1.854c.224-.35.688-.45 1.036-.225.35.224.45.688.226 1.036-1.025 1.594-2.766 2.545-4.658 2.545z"></path>
							<circle cx="14.738" cy="9.458" r="1.478"></circle>
							<circle cx="9.262" cy="9.458" r="1.478"></circle>
						</g>
					</svg>
					<svg class="text-primary w-8 hover:bg-primary-300 rounded-full p-1" fill="currentColor" viewBox="0 0 24 24">
						<path d="M-37.9 18c-.1-.1-.1-.1-.1-.2.1 0 .1.1.1.2z" />
						<path d="M-37.9 18c-.1-.1-.1-.1-.1-.2.1 0 .1.1.1.2zM18 2.2h-1.3v-.3c0-.4-.3-.8-.8-.8-.4 0-.8.3-.8.8v.3H7.7v-.3c0-.4-.3-.8-.8-.8-.4 0-.8.3-.8.8v.3H4.8c-1.4 0-2.5 1.1-2.5 2.5v13.1c0 1.4 1.1 2.5 2.5 2.5h2.9c.4 0 .8-.3.8-.8 0-.4-.3-.8-.8-.8H4.8c-.6 0-1-.5-1-1V7.9c0-.3.4-.7 1-.7H18c.6 0 1 .4 1 .7v1.8c0 .4.3.8.8.8.4 0 .8-.3.8-.8v-5c-.1-1.4-1.2-2.5-2.6-2.5zm1 3.7c-.3-.1-.7-.2-1-.2H4.8c-.4 0-.7.1-1 .2V4.7c0-.6.5-1 1-1h1.3v.5c0 .4.3.8.8.8.4 0 .8-.3.8-.8v-.5h7.5v.5c0 .4.3.8.8.8.4 0 .8-.3.8-.8v-.5H18c.6 0 1 .5 1 1v1.2z" />
						<path d="M15.5 10.4c-3.4 0-6.2 2.8-6.2 6.2 0 3.4 2.8 6.2 6.2 6.2 3.4 0 6.2-2.8 6.2-6.2 0-3.4-2.8-6.2-6.2-6.2zm0 11c-2.6 0-4.7-2.1-4.7-4.7s2.1-4.7 4.7-4.7 4.7 2.1 4.7 4.7c0 2.5-2.1 4.7-4.7 4.7z" />
						<path d="M18.9 18.7c-.1.2-.4.4-.6.4-.1 0-.3 0-.4-.1l-3.1-2v-3c0-.4.3-.8.8-.8.4 0 .8.3.8.8v2.2l2.4 1.5c.2.2.3.6.1 1z" />
					</svg>
				</div>
				<button @click="newTeweet()" class="bg-primary-100 text-center text-white font-bold capitalize rounded-full px-3 py-2 hover:bg-primary-500" disabled>Tweet</button>
			</div>
		</div>
	</section>
</template>

<script>
	import axios from "axios";

	export default {
		name: "NewTweet",
		data() {
			return {
				edited: false,
				tweet: "What's happening?",
			};
		},
		methods: {
			newTeweet() {
				axios
					.post("https://vue-twitter-95986-default-rtdb.firebaseio.com/teweet.json", {
						actions: {
							comments: 0,
							like: 0,
							retweets: 0,
							share: 0,
						},
						content: "data.data[id].content",
						time: 0,
					})
					.then(function (response) {
						console.log(response);
					})
					.catch(function (error) {
						console.log(error);
					});
			},
		},
	};
</script>
