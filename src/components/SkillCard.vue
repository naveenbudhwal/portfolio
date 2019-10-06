<template>
  <div class="root">
    <div class="picture">
      <img :src="skillPicture" alt="Skill Illustration">
    </div>
    <div class="header">{{skillHeading}}</div>
    <hr>
    <div class="body">
      <ul>
        <li v-for="skill in skillBody">{{skill}}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "SkillCard",
  props: {
    skillPicture: String,
    skillHeading: String,
    skillBody: Array
  }
};
</script>

<style scoped>
.root {
  width: 50%;
  font-family: "Montserrat", sans-serif;
  border: 1px solid #dadada;
  border-radius: 10px;
  padding: 10px;
  /* box-shadow: 2px 2px 5px #dadada; */
  margin: 20px;
  background: #fff;
}

.picture {
  display: flex;
}

.picture img{
  width: 9em;
  height: auto;
  margin: 0 auto;
}

.header {
  font-weight: 500;
  text-align: center;
  color: #2b70dc;
  font-weight: 500;
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

</style>