<template>
  <div class="root">
    <div class="intro">
      Hi
      <span>,</span> I'm Naveen
      <span>:)</span>
    </div>
    <div class="sub-intro">Web Developer <span>|</span> Coder</div>
  </div>
</template>

<script>
export default {
  name: "home"
};
</script>

<style scoped>
.intro {
  margin-top: 100px;
  text-align: center;
  font-family: "Montserrat", sans-serif;
  font-weight: 400;
  font-size: 5rem;
  color: #434655;
}

.sub-intro {
  text-align: center;
  font-family: "Montserrat", sans-serif;
  font-weight: 400;
  margin-top: 20px;
  font-size: 2rem;
  color: #434655;
}

::-moz-selection { /* Code for Firefox */
  color: #fff;
  background: #000;
}

::selection {
  color: #fff;
  background: #000;
}

span {
  color: #2b70dc;
}

</style>