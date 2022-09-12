<template>
	<div class="container">
		<h2>{{ $route.params.slug }}</h2>
		<h3>Filename: pages/events/_slug.vue</h3>

		<SiteNavigation />

		<div class="event">
			<h2>{{ events.title.rendered }}</h2>
			<p v-if="$fetchState.pending">
				<span class="loading"></span>
			</p>
			<p v-else-if="$fetchState.error">Error while fetching events</p>

			<section>
				<img :src="event.image" :alt="event.title" />
				<p>{{ event.content }}</p>
			</section>
			<button @click="goBack">Back</button>

		</div>
	</div>
</template>

<script>
// in this API call, we go get specific events
export default {
	data() {
		return {
			event: {}
		}
	},
	async fetch() {
		this.event = await this.$http.$get(
			`http://cm.beneb.com/wp-json/wp/v2/events/?per_page=100/${this.$route.params.slug}`
		)
	},
	methods: {
		goBack() {
			return this.$router.go(-1)
		}
	}
}
</script>

