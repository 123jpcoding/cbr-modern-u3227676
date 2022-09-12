<!-- this component returns a list of all the events -->
<template>
	<div class="container-fluid">
		<ul class="nav nav-tabs justify-content-end">
			<li class="nav-item">
				<NuxtLink class="btn" to="/events">
					2022
				</NuxtLink>
			</li>
			<li class="nav-item">
				<NuxtLink class="btn" to="/events/2021">
					2021
				</NuxtLink>
			</li>
			<li class="nav-item">
				<NuxtLink class="btn" to="/events/2020">
					2020
				</NuxtLink>
			</li>
			<li class="nav-item">
				<NuxtLink class="btn" to="/events/2019">
					2019
				</NuxtLink>
			</li>
			<li class="nav-item">
				<NuxtLink class="btn" to="/events/2018">
					2018
				</NuxtLink>
			</li>
			<li class="nav-item">
				<NuxtLink class="btn" to="/events/2017">
					2017
				</NuxtLink>
			</li>
		</ul>
	</div>
</template>

<style>
a.btn {
	color: #7187c0; 
}

a.btn:hover {
	color: #fbc589;
	background-color: #f496a8;
}
</style>