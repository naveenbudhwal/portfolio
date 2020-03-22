<template>
  <div id="app">
    <NavBar/>
    <transition name="fade-up" mode="out-in">
      <router-view />
    </transition>
  </div>
</template>


<script>
import NavBar from '@/components/NavBar.vue'

export default {
  name: "Home",
  components: {
    NavBar,
  },
};
</script>


<style>

/*** Transition styles ***/

.fade-up-enter {
  opacity: 0;
  transform: translateY(80px);
}

.fade-up-enter-active,
.fade-up-leave-active {
  transition: all 0.3s ease-in-out;
}

.fade-up-leave {
  opacity: 0;
  transform: translateY(-80px);
}

/*** ***/

#app {
  font-family: "Montserrat", sans-serif;
}

body {
  margin: 0;
  padding: 0;
}

ul {
  padding: 0;
  margin: 0;
}

::-moz-selection {
  /* Code for Firefox */
  color: #000;
  background: rgba(0, 0, 0, 0.1);
}

::selection {
  color: #000;
  background: rgba(0, 0, 0, 0.1);
}

/* ScrollBar styles */
/* width */
::-webkit-scrollbar {
  width: 8px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #e2e2e2;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #888;
  border-radius: 20px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #555;
}
</style>
