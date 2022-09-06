<template>
	<div class="container">
		<h2>{{  $route.params.slug  }}</h2>
		<h3>Filename: pages/about/_slug.vue</h3>

		<SiteNavigation />

		<div class="page">
			<!-- the buiding returns an array with one item in it, so need to reference it below -->
			<h2>{{  page.title.rendered  }}</h2>

			<p>{{  page.content.rendered  }}</p>

			<p>{{  page.except.rendered  }}</p>

			<!-- <pre>{{ $data }}</pre> -->
		</div>
	</div>
</template>

<script>
// in this API call, we go get a specifci building, filtered by the ID in the URL
// we access what is in the URL by using the params object
export default {
	async asyncData({ params }) {
		const page = await fetch(
			`http://cm.beneb.com/wp-json/wp/v2/pages/?slug=about/${params.slug}`
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
