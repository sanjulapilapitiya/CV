<template>
    <div class="container row align-items-center g-5 py-5 px-4 mx-auto">
        <div class="col-10 col-sm-8 col-lg-6 mx-auto">
            <img class="circular-image mx-auto d-block" src="jpg/aboutMe.jpg" alt="PHP Logo"/>
        </div>
      <div class="col-lg-6">
        <h1 class="aboutMe-header display-5 fw-bold text-emphasis lh-1 mb-3">A little about myself</h1>
        <p class="lead text-light ">Results-driven Software Engineer with 4+ years of experience in PHP, Symfony, Vue.js (2/3), JavaScript, and SQL. Strong 
background in API development, security, and system optimization. Passionate about web development, clean 
architecture, and modern best practices like TDD and component-based front-end design. Proven ability to improve code 
quality, optimize system performance, and enhance security in dynamic, agile environments. </p>
      </div>
    </div>
</template>

<script>
    export default {
    name: 'aboutMe',
    };
</script>

<style scoped>
.circular-image {
  width: 100%;
  max-width: 350px;
  aspect-ratio: 1 / 1; /* Keeps it square */
  border-radius: 50%;
  object-fit: cover;
  display: block;
  margin: 0 auto;
}

.aboutMe-header {
    background-color: beige;
    padding: 5%;
}
</style>