<template>
    <section class="container section">
      <div class="row g-4">
        <div class="col-12 col-lg-7" id="icon-grid">
          <h2 class="section-title">My Skills</h2>
          <p class="section-lead">The tools I reach for day to day.</p>

          <div class="row row-cols-3 row-cols-md-4 g-3">
            <div v-for="skill in skills" :key="skill.name" class="col">
              <div class="skill-tile card-bordered">
                <img class="logo" :src="skill.src" :alt="`${skill.name} logo`" />
                <span class="skill-name">{{ skill.name }}</span>
              </div>
            </div>
          </div>
        </div>

        <div class="col-12 col-lg-5 d-flex flex-column justify-content-end gap-3">
            <a class="cta card-bordered" href="https://www.linkedin.com/in/sanjula-pilapitiya-8524361aa" target="_blank" rel="noopener">
                <img src="svg/linkedin-logo.svg" alt="" class="cta-icon" />
                <span>
                    <strong>Let's connect</strong>
                    <small>Find me on LinkedIn</small>
                </span>
            </a>
            <a class="cta card-bordered" href="CV.pdf" download="CV.pdf">
                <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" fill="currentColor" class="cta-icon cta-svg" viewBox="0 0 16 16" aria-hidden="true">
                    <path d="M.5 9.9a.5.5 0 0 1 .5.5v2.5a1 1 0 0 0 1 1h12a1 1 0 0 0 1-1v-2.5a.5.5 0 0 1 1 0v2.5a2 2 0 0 1-2 2H2a2 2 0 0 1-2-2v-2.5a.5.5 0 0 1 .5-.5"/>
                    <path d="M7.646 11.854a.5.5 0 0 0 .708 0l3-3a.5.5 0 0 0-.708-.708L8.5 10.293V1.5a.5.5 0 0 0-1 0v8.793L5.354 8.146a.5.5 0 1 0-.708.708z"/>
                </svg>
                <span>
                    <strong>Download my CV</strong>
                    <small>CV.pdf</small>
                </span>
            </a>
        </div>
      </div>
    </section>
</template>

<script setup>
const skills = [
    { name: "PHP", src: "svg/php-logo.svg" },
    { name: "JavaScript", src: "svg/javascript-logo.svg" },
    { name: "Vue", src: "svg/vue-logo.svg" },
    { name: "Symfony", src: "svg/symfony-logo.svg" },
    { name: "API Platform", src: "svg/apiPlatform-logo.svg" },
    { name: "Docker", src: "svg/docker-logo.svg" },
    { name: "Bootstrap", src: "svg/bootstrap-logo.svg" },
    { name: "Git", src: "svg/git-logo.svg" },
];
</script>

<style scoped>
.skill-tile {
    height: 100%;
    padding: 1.1rem 0.5rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 0.6rem;
}

.logo {
    max-width: 52px;
    max-height: 52px;
    filter: grayscale(1) brightness(1.4);
    opacity: 0.85;
    transition: filter 0.3s ease, opacity 0.3s ease;
}

.skill-tile:hover .logo {
    filter: none;
    opacity: 1;
}

.skill-name {
    font-size: 0.8rem;
    color: var(--text-muted);
    text-align: center;
}

.cta {
    display: flex;
    align-items: center;
    gap: 1rem;
    padding: 1.25rem 1.5rem;
    color: var(--text);
    text-decoration: none;
}

.cta:hover {
    color: var(--text);
}

.cta strong,
.cta small {
    display: block;
}

.cta small {
    color: var(--text-muted);
}

.cta-icon {
    width: 40px;
    height: 40px;
    flex-shrink: 0;
}

.cta-svg {
    color: var(--accent);
}
</style>
