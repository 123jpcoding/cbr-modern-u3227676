<!-- this component returns a list of all the events -->
<template>
	<div class="container-fluid">
		<ul class="d-flex justify-content-start">
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

.nav-item .btn {
	color: #7187c0; 
	text-decoration: none;
    display: block;
	list-style: none;
	border-radius: 50px;
}



.nav-item .btn:hover {
	color: #ffff;
	background-color: #f496a8;
	transition: 0.5s;
	border-radius: 20px;
}

</style>