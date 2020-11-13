<template>
	<q-item
		clickable
		tag="a"
		target="_blank"
		@click="$router.push(routs).catch((err) => {})"
	>
		<q-item-section v-if="icon" avatar>
			<q-icon :name="icon" />
		</q-item-section>

		<q-item-section>
			<q-item-label>{{ title }}</q-item-label>
			<q-item-label caption>
				{{ caption }}
			</q-item-label>
		</q-item-section>
	</q-item>
</template>

<script>
	export default {
		name: "EssentialRouts",
		props: {
			title: {
				type: String,
				required: true,
			},

			caption: {
				type: String,
				default: "",
			},

			routs: {
				type: String,
				default: "",
			},

			icon: {
				type: String,
				default: "",
			},
		},
	};
</script>

<style></style>
