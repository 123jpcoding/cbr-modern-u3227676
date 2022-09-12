<template>
	<div class="container">
		<h2>{{ $route.params.slug }}</h2>
		<h3>Filename: pages/events/2017/_slug.vue</h3>

		<SiteNavigation />

		<div class="event">
			<h2>{{ events.title.rendered }}</h2>

			<ul>
				<li>Date: {{ events[0].acf.date }}</li>
				<li>Time: {{ events[0].acf.time }}</li>
				<li>{{ events[0].acf.type }}</li>
			</ul>

		</div>
	</div>
</template>

<script>
// in this API call, we go get specific events
export default {
	async asyncData({ params }) {
		const events = await fetch(
			'http://cm.beneb.com/wp-json/wp/v2/events/?slug=${params.slug}').then((res) => {
				if (res.ok) {
					return res.json()
				}
				throw new Error(res.status)
			})
			return { events }
		}, 
	}

</script>
