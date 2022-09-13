<!-- this component can hold site navigation -->
<!-- if we put it here we can avoid having to repeat the code -->

<template>
  <nav class="navbar navbar-light headWrapper">
    <div class="d-flex justify-content-start">
      <span class="navbar-brand">
        <img src="~assets/images/logo.png" alt="" width="150" height="150" class="d-inline-block align-text-top">
      </span>
      <NuxtLink class="title" to="/">
        Canberra Modern
      </NuxtLink>
    </div>
    <div class="d-flex navWrapper justify-content-end">
      <ul class="nav">
        <li class="nav-item">
          <NuxtLink class="btn" to="/">
            Home
          </NuxtLink>
        </li>
        <li class="nav-item">
          <NuxtLink class="btn" to="/about">
            About
          </NuxtLink>
        </li>
        <li class="nav-item">
          <NuxtLink class="btn" to="/events">
            Events
          </NuxtLink>
        </li>
        <li class="nav-item">
        <NuxtLink class="btn" to="/buildings">
          Buildings
        </NuxtLink>
        </li>
      </ul>
    </div>
  </nav>
</template>

<style>
  .title {
    display: flex;
    flex: inline-block;
  }
</style>

