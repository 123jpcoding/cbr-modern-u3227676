<!-- this component can hold site navigation -->
<!-- if we put it here we can avoid having to repeat the code -->

<template>
  <nav class="navbar navbar-light headWrapper">
    <div class="d-flex justify-content-start">
      <span class="navbar-brand">
        <a href="/">
        <img id="logo" src="~assets/images/logo.png" alt="" width="160" height="160" class="d-inline-block align-text-top">
      </a>
      </span>
      <NuxtLink class="title" to="/">
        CANBERRA MODERN
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
        <li class="nav-item">
        <NuxtLink class="btn" to="/partners">
          Partners
        </NuxtLink>
        </li>
        <li class="nav-item">
        <NuxtLink class="btn" to="/videos">
          Videos
        </NuxtLink>
        </li>
        <li class="nav-item">
        <NuxtLink class="btn" to="/links">
          Links
        </NuxtLink>
        </li>
      </ul>
    </div>
  </nav>
</template>

<style>
  .title {
    font-weight: 700;
    text-decoration: none;
    color: #7187c0;
    font-size: 2rem;
    margin-top: 2em;
    font-style: italic;
  }

  .title:hover {
    text-decoration: none;
    color: #f496a8;
    transition: 0.5s;
  }

@media(max-width: 770px) { 
  .title {
    font-size: 2rem;
  }
}

</style>

