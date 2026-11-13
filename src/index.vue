<template>
  <div class="background">
    <aboutMe />
    <timeline />
    <myProjects />
    <skillsIconGrid />
    <basefooter />
  </div>
</template>

<script setup>
import skillsIconGrid from "./components/skillsIconGrid.vue";
import basefooter from "./components/footer.vue";
import aboutMe from "./components/aboutMe.vue";
import timeline from "./components/timeline.vue";
import myProjects from "./components/myProjects.vue";
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Space+Grotesk:wght@500;700&display=swap");

/* ---- Design tokens: one palette shared by every section ---- */
:root {
  --bg: #0b0f1a;
  --surface: #121829;
  --surface-2: #182036;
  --border: #26304a;
  --border-strong: #3a4766;
  --text: #e7ecf5;
  --text-muted: #9ba8c0;
  --accent: #22d3ee;       /* cyan */
  --accent-2: #a78bfa;     /* violet */
  --accent-soft: rgba(34, 211, 238, 0.12);
  --gradient: linear-gradient(135deg, var(--accent) 0%, var(--accent-2) 100%);
  --radius: 14px;
  --font-body: "Inter", system-ui, -apple-system, "Segoe UI", sans-serif;
  --font-display: "Space Grotesk", var(--font-body);
}

html, body {
  margin: 0;
  padding: 0;
  height: 100%;
  background-color: var(--bg);
  color: var(--text);
  font-family: var(--font-body);
}

.background {
  background:
    radial-gradient(900px 500px at 10% -10%, rgba(34, 211, 238, 0.10), transparent 60%),
    radial-gradient(900px 500px at 100% 20%, rgba(167, 139, 250, 0.10), transparent 60%),
    var(--bg);
  /* Bootstrap's CSS loads after ours, so override its text variables here
     (inherited by everything inside) rather than fighting its body/heading rules */
  --bs-body-color: var(--text);
  --bs-heading-color: var(--text);
  --bs-emphasis-color: var(--text);
  --bs-secondary-color: var(--text-muted);
  color: var(--text);
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

h1, h2, h3, h4 {
  font-family: var(--font-display);
  color: var(--text);
}

/* ---- Shared section + component styles ---- */
.section {
  padding: 4rem 1rem;
}

.section-title {
  font-size: clamp(1.75rem, 3vw, 2.25rem);
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.section-title::after {
  content: "";
  display: block;
  width: 64px;
  height: 4px;
  margin-top: 0.6rem;
  border-radius: 4px;
  background: var(--gradient);
}

.section-lead {
  color: var(--text-muted);
  max-width: 60ch;
  margin-bottom: 2rem;
}

.gradient-text {
  background: var(--gradient);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}

.card-bordered {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: var(--radius);
  transition: border-color 0.25s ease, transform 0.25s ease, box-shadow 0.25s ease;
}

/* The one hover style every card on the site uses */
.card-bordered:hover {
  border-color: rgba(34, 211, 238, 0.55);
  transform: translateY(-3px);
  box-shadow: 0 12px 30px -12px rgba(34, 211, 238, 0.25);
}

/* Thick accent edge on the left; dims along with the rest of the border on hover */
.card-accent {
  border-left: 4px solid var(--accent);
}

.card-accent:hover {
  border-left-color: rgba(34, 211, 238, 0.55);
}

.tag {
  display: inline-block;
  padding: 0.25rem 0.7rem;
  margin: 0.2rem;
  font-size: 0.78rem;
  font-weight: 500;
  color: var(--accent);
  background: var(--accent-soft);
  border: 1px solid rgba(34, 211, 238, 0.35);
  border-radius: 999px;
}

@media (prefers-reduced-motion: reduce) {
  .card-bordered,
  .card-bordered:hover {
    transition: none;
    transform: none;
  }
}
</style>
