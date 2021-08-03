<template>
	<div class="flex">
		<!-- header -->
		<div class="w-1/4 pl-8">
			<Header />
		</div>

		<!-- header -->
		<div class="w-2/4">
			<Tweets />
		</div>

		<!-- header -->
		<div class="w-1/4">
			<Sidebar />
		</div>
	</div>
</template>

<script>
	import Header from "@/components/layout/Header.vue";
	import Tweets from "@/components/layout/Tweets.vue";
	import Sidebar from "@/components/layout/Sidebar.vue";
	export default {
		name: "Home",
		components: {
			Header,
			Tweets,
			Sidebar,
		},
	};
</script>
