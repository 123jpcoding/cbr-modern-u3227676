<!-- this component returns a list of all the events -->
<template>
	<div class="">
		<!-- these would show while the data loads or if an error -->
		<p v-if="$fetchState.pending">Loading events...</p>
		<p v-else-if="$fetchState.error">Error while fetching events</p>

		<ul v-else class="list-group">
			<!-- this is a for loop, it just loops through the list of events returned from the API -->
			<li v-for="event in events" :key="event.id" class="list-group-item">
				<!-- now make a link for each item -->
				<!-- <NuxtLink :to="event.slug"> -->
				<NuxtLink :to="'/events/' + event.slug">
					<!-- return the rendered title -->
					{{  event.title.rendered  }}
				</NuxtLink>
				<!-- now show me the event year -->
				: {{ event.acf.year }}
			</li>
		</ul>

	</div>
</template>


<script>
export default {
	// data will return an array,
	data() {
		return {
			//empty array to be filled
			events: [], 
		}
	},
	//fetching data
	async fetch() {
		let apiData = await fetch ('http://cm.beneb.com/wp-json/wp/v2/events/?per_page=100')
		.then((response) =>
			response.json()
		)
		console.log(apiData)
		// // create empty array
		let yearArr = [];
		for (let i = 0; i < apiData.length; i++) {
			let year = "2018";
			let eventYear = apiData[i].acf.year;
			if (eventYear == year) {
				yearArr.push(apiData[i]);
			}
		}
		console.log(yearArr);
		this.events = yearArr;
	} 
}
</script>

