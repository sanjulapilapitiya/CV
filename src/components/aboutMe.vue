<template>
    <div class="container row align-items-center g-5 py-5 px-4 mx-auto">
        <div class="col-10 col-sm-8 col-lg-6 mx-auto">
            <div class="avatar-ring mx-auto">
                <img class="circular-image" src="jpg/aboutMe.jpg" alt="Photo of me"/>
            </div>
        </div>
      <div class="col-lg-6">
        <div class="about-card card-bordered card-accent">
          <p class="eyebrow">Senior developer · front-end focus</p>
          <h1 class="display-5 fw-bold lh-1 mb-3">A little about <span class="gradient-text">myself</span></h1>
          <p class="lead about-text">
            Senior Developer with 6+ years of commercial experience across PHP, Symfony, Vue.js, JavaScript and SQL, with a
            growing focus on the front end. Most recently I led a full platform rebrand of a large legacy SaaS product, building a
            design system and dark mode across 2,000+ files and reworking key pages mobile-first.
          </p>
          <p class="about-text mb-0">
            I care about interfaces that feel consistent and fast: clear loading feedback, responsive layouts and trimmed-down
            assets, backed by solid work underneath: API development, query optimisation and security hardening. I enjoy
            bringing modern practices like component-based front-end design and TDD into codebases of any age.
          </p>
        </div>
      </div>
    </div>
</template>

<script>
    export default {
    name: 'aboutMe',
    };
</script>

<style scoped>
.avatar-ring {
  width: 100%;
  max-width: 350px;
  padding: 6px;
  border-radius: 50%;
  background: var(--gradient);
  box-shadow: 0 20px 60px -20px rgba(167, 139, 250, 0.5);
}

.circular-image {
  width: 100%;
  aspect-ratio: 1 / 1;
  border-radius: 50%;
  object-fit: cover;
  display: block;
  border: 6px solid var(--bg);
}

.about-card {
  padding: 2rem;
}

.eyebrow {
  text-transform: uppercase;
  letter-spacing: 0.12em;
  font-size: 0.8rem;
  font-weight: 600;
  color: var(--accent);
  margin-bottom: 0.75rem;
}

.about-text {
  color: var(--text-muted);
  margin-bottom: 0;
}
</style>
