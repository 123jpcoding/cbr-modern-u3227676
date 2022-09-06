<!-- this component can hold site navigation -->
<!-- if we put it here we can avoid having to repeat the code -->
<template>
	<nav>
  <NuxtLink to="/">
      Home
    </NuxtLink>
    <NuxtLink to="/about">
      About
    </NuxtLink>
		<NuxtLink to="/buildings">
      Buildings
    </NuxtLink>
    <NuxtLink to="/events">
      Events
    </NuxtLink>
	</nav>
</template>

<style>
  nav, a { 
    color: red;
    font-family: courier;
    font-size: 25px;
  }

  nav, a:hover {
    color: green;
  }
</style>