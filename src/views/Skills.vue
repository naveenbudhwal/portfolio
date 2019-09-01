<template>
  <div class="root">
    <div class="heading">Skills</div>
    <hr />
    <div class="container page">
      <skill-card  
      v-for="skill in skills"
      v-bind:key="skill.id"
      v-bind:skillHeading="skill.title"
      v-bind:skillBody="skill.body"
      ></skill-card>
    </div>
  </div>
  
</template>

<script>
import SkillCard from "../components/SkillCard.vue";

export default {
  name: "Skills",
  components: { SkillCard },
  data() {
    return {
      skills: [
      { id: 1, title: 'Web Development', body: ["VueJS", "NodeJS", "MongoDB", "ExpressJS"]},
      { id: 2, title: 'Designing', body: ["Abobe Illustrator", "Adobe Photoshop", "Adobe Premiere Pro"]},
      { id: 3, title: 'Music Production', body: ["FL Studio"]},
      {id: 4, title: 'Programming', body: ['C / C++', 'Python']}
    ]
    };
  }
};
</script>

<style scoped>

.container {
  display: flex;  
}

.heading {
  font-family: "Montserrat", sans-serif;
  font-size: 3em;
  font-weight: 500;
  color: #434655;
  margin-left: 20%;
}

hr {
  width: 80%;
}

@media only screen and (max-width: 768px) {
  .container {
    flex-direction: column;
  }
}

</style>