<template>
  <div class="social-media-bar">
    <a href="mailto:naveenbudhwal@gmail.com" target="_blank" rel="noopener">
      <i class="far fa-envelope"></i>
    </a>
    <a href="https://www.instagram.com/naveenbudhwal" target="_blank" rel="noopener">
      <i class="fab fa-instagram"></i>
    </a>
    <a href="https://www.linkedin.com/in/naveenbudhwal" target="_blank" rel="noopener">
      <i class="fab fa-linkedin-in"></i>
    </a>
    <a href="https://www.github.com/naveenbudhwal" target="_blank" rel="noopener">
      <i class="fab fa-github"></i>
    </a>
    <a href="https://www.twitter.com/naveenbudhwal" target="_blank" rel="noopener">
      <i class="fab fa-twitter"></i>
    </a>
  </div>
</template>

<script>
  export default {

  }
</script>

<style scoped>

.social-media-bar:hover > a {
  color: #333333aa;
}

.social-media-bar:hover > a:hover {
  color: #333;
}

a {
  color: #333;
  font-size: 1.6rem;
  margin: 0 0.6em;
  transition: color 140ms cubic-bezier(.33,0,.2,1);
}

</style>