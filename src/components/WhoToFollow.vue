<template>
	<div class="border-b py-3 hover:bg-gray-100 px-4">
		<a :href="link">
			<div class="flex justify-between">
				<div>
					<img class="img-fluid rounded-full" :alt="username" :src="image" />
				</div>
				<div>
					<a class="font-bold text-black flex" :href="link">{{ name }}</a>
					<span class="text-info text-xs">{{ username }}</span>
				</div>
				<div>
					<button class="border-primary border rounded-full px-3 py-1 text-primary font-bold">Follow</button>
				</div>
			</div>
		</a>
	</div>
</template>
<script>
	export default {
		name: "WhoToFollow",
		props: {
			name: {
				type: String,
				required: true,
			},
			username: {
				type: String,
				required: true,
			},
			image: {
				type: String,
				required: true,
			},
			link: {
				type: String,
				required: true,
			},
		},
	};
</script>
