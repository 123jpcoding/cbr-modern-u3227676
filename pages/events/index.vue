<template>
	<div class="container">
		<h2>All events</h2>
		<h3>Filename: pages/events/index.vue</h3>

		<SiteNavigation />


		<div class="events">
			<!-- The building list is over in the components folder -->
			<!-- the code below loads the component here so we can use it again -->
			<EventsList />

			<!-- this is a really useful line of code that will just output what the API call returns -->
			<!-- <pre>{{ $data }}</pre> -->
		</div>
	</div>
</template>

<script>
// in this API call, we go get a specific building, filtered by the ID in the URL
// we access what is in the URL by using the params object
export default {
	async asyncData({ params }) {
		const events = await fetch(
			`http://cm.beneb.com/wp-json/wp/v2/events/`
		).then((res) => {
			if (res.ok) {
				return res.json()
			}
			throw new Error(res.status)
		})
		return { events }
	},
}
</script>


<style>
</style>