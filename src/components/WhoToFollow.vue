<template>
	<section class="bg-secondary py-1 rounded-lg my-2">
		<h5 class="font-bold capitalize text-xl border-b py-3 px-4">Who to follow</h5>
		<div class="border-b py-3 hover:bg-gray-100 px-4" v-for="follow in follows" :key="follow.id">
			<a href="#">
				<div class="flex justify-between">
					<div>
						<img class="img-fluid rounded-full" :src="follow.image" />
					</div>
					<div>
						<a class="font-bold text-black flex" href="#">{{ follow.name }}</a>
						<span class="text-info text-xs">{{ follow.username }}</span>
					</div>
					<div>
						<button class="border-primary border rounded-full px-3 py-1 text-primary font-bold">Follow</button>
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
		name: "WhoToFollow",
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
