<template>
  <div class="container page">
    <div class="heading">Skills</div>
    <hr />
    <skill-card  
    v-for="skill in skills"
    v-bind:key="skill.id"
    v-bind:skillHeading="skill.title"
    v-bind:skillBody="skill.body"
    ></skill-card>
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
      { id: 3, title: 'Music Production', body: ["FL Studio"]}
    ]
    };
  }
};
</script>

<style scoped>
.heading {
  font-family: "Montserrat", sans-serif;
  font-size: 3em;
  font-weight: 500;
  color: #434655;
}
</style>