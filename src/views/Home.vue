<template>
	<!-- header -->
	<div class="col">
		<Header />
	</div>

	<!-- header -->
	<div class="col-6">
		<Tweets />
	</div>

	<!-- header -->
	<div class="col">
		<Sidebar />
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
