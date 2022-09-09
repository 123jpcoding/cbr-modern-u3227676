<template>
	<div class="container">
		<h2>All events</h2>
		<h3>Filename: pages/events/index.vue</h3>

		<SiteNavigation />


		<div class="events">
			<!-- Shows the Events Navigation -->
			<PastEventsNav />
			<h3>Upcoming Events</h3>
			<UpcomingEvents />

			<!-- this is a really useful line of code that will just output what the API call returns -->
			<!-- <pre>{{ $data }}</pre> -->
		</div>
	</div>
</template>

<style>
</style>