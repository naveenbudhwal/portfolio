<template>
  <div class="container">
    <div class="photo">
      <img class="image" src="../assets/about_me_pic.jpg" alt="My Photo">
    </div>
    <div class="intro mx-5">
      <div class="intro-heading pb-4">Hey<span>,</span> I<span>'</span>m Naveen<span>.</span></div>
      <div class="intro-body">
        I enjoy turning complex problems into simple, beautiful and intuitive designs. When I'm not coding, tweeting or pushing pixels, you'll find me cooking, gardening or working out in the park.
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>

.container {
  font-family: "Montserrat", sans-serif;
  display: flex;
  margin-top: 5%;
}

.image {
  width: 270px;
  height: auto;
  -webkit-box-shadow: 0 10px 6px -6px #777;
       -moz-box-shadow: 0 10px 6px -6px #777;
            box-shadow: 0 10px 6px -6px #777;
}

.intro-heading {
  color: #434655;
  font-weight: 500;
  font-size: 2.5em;
}

.intro-body {
  color: #535353;
  font-size: 1.2em;
}

span {
  color: #2b70dc;
}

@media only screen and (max-width: 768px) {
  .container {
    flex-direction: column;
  }
  .image {
    margin-bottom: 8%;
  }
}

</style>