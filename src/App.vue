<template>
  <div id="app">
    <!-- <div id="nav">
      <div class="nav-logo">
        <router-link to="/">LOGO</router-link>
      </div>
      <div class="nav-links">
        <router-link to="/">Home</router-link>
        <router-link to="/skills">Skills</router-link>
        <router-link to="/gallery">Gallery</router-link>
        <router-link to="/about">About</router-link>
      </div>
    </div>-->

    <nav class="navbar navbar-expand-lg navbar-light bg-transparent pt-4">
      <router-link to="/">LOGO</router-link>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse pr-4" id="navbarSupportedContent">
        <ul class="navbar-nav ml-auto">
          <li class="nav-item mx-2">
            <router-link to="/">Home</router-link>
          </li>
          <li class="nav-item mx-2">
            <router-link to="/skills">Skills</router-link>
          </li>
          <li class="nav-item mx-2">
            <router-link to="/gallery">Gallery</router-link>
          </li>
          <li class="nav-item mx-2">
            <router-link to="/about">About</router-link>
          </li>
        </ul>
      </div>
    </nav>

    <router-view />
  </div>
</template>

<style>
/* #app {
  font-family: "Raleway", sans-serif;
} */
nav {
  font-family: "Raleway", sans-serif;
  font-weight: 600;
  font-size: 1.2em;
}

nav a {
  color: #434655;
  margin: 0 10px;
  text-decoration: none;
  transition: 0.5s ease all;
}

nav a:hover {
  text-decoration: none;
  font-size: 1.3em;
}

nav a.router-link-exact-active {
  color: #2b70dc;
}
</style>
