<!-- this component returns a list of all the buildings -->
<template>
	<div class="">
		<!-- these would show while the data loads or if an error -->
		<p v-if="$fetchState.pending">Loading About Page...</p>
		<p v-else-if="$fetchState.error">Error while loading About Page</p>

		<li v-for="page in buildings" :key="page.id" class="list-group-item">
			<h3>
				<NuxtLink :to="'/about/' + page.slug">
					<!-- return the rendered title -->
					{{ page.title.rendered }}
				</NuxtLink>
			</h3>
			<!-- now show me the building year -->
			<p>{{ page.content.rendered }}</p>
		</li>

		<h3>this list is stored in components/BuildingsList.vue</h3>

	</div>
</template>


<script>
export default {
	// layout: 'home',
	async fetch() {
		this.buildings = await fetch('http://cm.beneb.com/wp-json/wp/v2/buildings/?per_page=20').then((res) =>
			res.json()
		)
	},
	data() {
		return {
			buildings: [],
		}
	},
}
</script>

