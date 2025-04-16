<template>
  <div class="background">
    <aboutMe />
    <timeline />
    <skillsIconGrid />
    <basefooter />
  </div>
</template>

<script setup>
import skillsIconGrid from "./components/skillsIconGrid.vue";
import basefooter from "./components/footer.vue";
import aboutMe from "./components/aboutMe.vue";
import timeline from "./components/timeline.vue";
</script>

<style>
html, body {
  margin: 0;
  padding: 0;
  height: 100%;
}

.background {
  background-color: #121212;
  min-height: 100vh; /* Ensure it covers at least the full height */
  display: flex;
  flex-direction: column;
}
</style>
