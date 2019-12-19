<template>
  <div class="horizontal-card">
    <div class="picture">
      <img :src="Picture" class="card-img" alt="Hobby image">
    </div>
    <div class="horizontal-card-body">
      <h5 class="horizontal-card-title"> {{Heading}}</h5>
      <p class="horizontal-card-text"> {{Body}} </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HorizontalCard',
  props: {
    Picture: String,
    Heading: String,
    Body: String
  }
};
</script>

<style>

.horizontal-card {
  /* height: 150px; */
  display: flex;
  background: #fff;
  font-family: "Montserrat", sans-serif;
  box-shadow: 0 10px 20px rgba(0,0,0,0.1);
  padding: 10px;
  border-radius: 15px;
  max-width: 800px; 
  margin: 10px 0;
} 

.picture {
  display: flex;
  justify-content: center;
  width: 30%; 
}

.card-img {
  width: 100%;
  height: 100%;
}

.horizontal-card-body {
  align-self: center;
  margin: 0 20px;
  width: 70%;
}

.horizontal-card-title {
  margin-bottom: 7px;
  color: #2b70dc;
  text-transform: uppercase;
  font-weight: 600;
  font-size: 1.3em;
  letter-spacing: 1.2px;
}

.horizontal-card-text {
  font-weight: 400;
  text-align: justify; 
  margin: 0;
}

@media only screen and (max-width: 768px) {
  .horizontal-card-title, .horizontal-card-text {
    text-align: center;
  }
  .horizontal-card {
    flex-direction: column;
    margin: 30px 10%;
  }
  .picture {
    width: 100%;
  }
  .card-img {
    width: 180px;
    height: 180px;
  }
  .horizontal-card-title {
    margin: 10px 0;
  }
  .horizontal-card-text {
    margin-bottom: 20px;
  }
}

</style>