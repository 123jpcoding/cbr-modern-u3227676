<!-- this component can hold site navigation -->
<!-- if we put it here we can avoid having to repeat the code -->
<template>
	<nav>
  <NuxtLink class="btn" to="/">
      Home
    </NuxtLink>
    <NuxtLink class="btn" to="/about">
      About
    </NuxtLink>
		<NuxtLink class="btn" to="/buildings">
      Buildings
    </NuxtLink>
    <NuxtLink class="btn" to="/events">
      Events
    </NuxtLink>
	</nav>
</template>

