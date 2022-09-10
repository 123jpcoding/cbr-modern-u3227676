<template>
	<div class="container">
		<h2>All events</h2>
		<h3>Filename: pages/events/index.vue</h3>

		<SiteNavigation />


		<div class="events">
			<!-- Shows the Events Navigation -->
			<EventsNav />
			<h3>Upcoming Events</h3>
			<Events2022 />

			<!-- this is a really useful line of code that will just output what the API call returns -->
			<!-- <pre>{{ $data }}</pre> -->
		</div>
	</div>
</template>

<style>
</style>