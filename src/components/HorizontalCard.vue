<template>
  <div class="card mb-3">
    <div class="row no-gutters">
      <div class="col-md-4">
        <img :src="Picture" class="card-img" alt="Hobby image">
      </div>
      <div class="col-md-8">
        <div class="card-body">
          <h5 class="card-title"> {{Heading}}</h5>
          <p class="card-text"> {{Body}} </p>
        </div>
      </div>
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

.card {
  margin: 0 15%;
  font-family: "Montserrat", sans-serif;
  box-shadow: 0 5px 5px rgba(0,0,0,0.1);
  max-width: 850px;
}

.col-md-4 {
  display: flex;
  justify-content: center;
}

.card-img {
  width: 150px;
  height: auto;
}

.card-title {
  color: #2b70dc;
  text-transform: uppercase;
  font-weight: 600;
}

@media only screen and (max-width: 576px) {
  .card-title, .card-text {
    text-align: center;
  }
  .card {
    margin: 0 10%;
  }
  .card-img {
    width: 180px;
    height: auto;
  }
}

@media only screen and (max-width: 768px) {
  .card-img {
    width: 180px;
    height: 180px;
  }
}

</style>