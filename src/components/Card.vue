<template>
  <div class="root">
    <div class="picture">
      <img :src="Picture" alt="Skill Illustration">
    </div>
    <div class="header">{{Heading}}</div>
    <hr class="material-hr">
    <div class="body">
      <ul>
        <li v-for="skill in skillBody">{{skill}}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: {
    Picture: String,
    Heading: String,
    skillBody: Array
  }
};
</script>

<style scoped>
.root {
  width: 50%;
  font-family: "Montserrat", sans-serif;
  box-shadow: 
    0 20px 30px  rgba(0, 0, 0, 0.1);
    /* 0 5px 10px rgba(0, 0, 0, 0.1); */
  /* border: 0.5px solid #dadada; */
  border-radius: 17px;
  padding: 10px;
  /* box-shadow: 2px 2px 5px #dadada; */
  margin: 20px;
  background: #fff;
}

.picture {
  display: flex;
  width: 9em;
  height: auto;
  margin: 0 auto;
}

.picture img{
  width: 100%;
  height: 100%;
}

.header {
  font-weight: 500;
  text-align: center;
  color: #2b70dc;
}

ul {
  padding: 0;
}

li {
  list-style: none;
  text-align: center;
  font-weight: 500;
  color: #434655;
}

.material-hr {
  background: #E9EFFF;
  height: 3px;
  width: 50%;
  border: none;
  border-radius: 10px;
}

@media only screen and (max-width: 768px) {
  .root {
    width: 70%;
  }
  .picture {
    width: 7em;
    height: auto;
  }
}

</style>