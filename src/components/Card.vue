<template>
  <div class="root">
    <div class="picture">
      <img :src="Picture" alt="Skill Illustration">
    </div>
    <div class="header">{{Heading}}</div>
    <hr class="material-hr">
    <div class="body">
      <ul>
        <li 
          class="skills" 
          v-for="(skill,$skillIndex) in skillBody" 
          :key="$skillIndex"
        >
          {{skill}}
        </li>
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
  width: 60%;
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
  /* border: 0.5px solid #f1f1f1; */
  border-radius: 17px;
  padding: 1em;
  /* box-shadow: 2px 2px 5px #dadada; */
  margin: 20px;
  background: #fff;
  transition: all 300ms cubic-bezier(.33,0,.2,1);
}

.root:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.13);
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
  font-weight: 600;
  text-align: center;
  color: #2b70dc;
  letter-spacing: 1.1px;
  font-size: 1.1em;
  margin: 10px 0;
}

.skills {
  font-weight: 400;
  margin: 0.5em 0;
  color: #333;
  font-size: 1rem;
}

.body {
  margin-bottom: 10px;
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
  margin-bottom: 1.2em;
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