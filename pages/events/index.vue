<template>
	<div class="container">
		<SiteNavigation />
		<h2>All Events</h2>


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