<template>
	<div class="container">
		<h2>{{ $route.params.slug }}</h2>
		<h3>Filename: pages/_pages.vue</h3>

		<SiteNavigation />

		<div class="page">
			<AboutInfo />
		</div>
	</div>
</template>

<script>
// in this API call, we load a page based off the URL paramter
// we access what is in the URL by using the params object
export default {
	async asyncData({ params }) {
		const page = await fetch(
			`http://cm.beneb.com/wp-json/wp/v2/pages/?slug=about`
		).then((res) => {
			if (res.ok) {
				return res.json()
			}
			throw new Error(res.status)
		})
		return { page }
	},
}
</script>