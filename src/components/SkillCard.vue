<template>
  <div class="root">
    <div class="header">{{skillHeading}}</div>
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
    skillHeading: String,
    skillBody: Array
  }
};
</script>

<style scoped>
.root {
  font-family: "Montserrat", sans-serif;
  border: 1px solid #dadada;
  border-radius: 20px;
  padding: 10px;
  box-shadow: 2px 2px 5px #dadada;
  margin: 20px auto;
}

.header {
  font-weight: 500;
}

li {
  list-style: none;
}

</style>