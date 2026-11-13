<template>
    <section class="container section">
        <h2 class="section-title">Experience</h2>
        <p class="section-lead">Where I've worked and what I've picked up along the way.</p>

        <div class="timeline">
		    <div class="timeline-row">
			    <div class="timeline-time">
				    Currys<small>Sept 2020 - Apr 2023</small>
			    </div>
                <div class="timeline-content card-bordered card-accent">
                    <div class="thumbs">
                        <img class="img-fluid rounded" src="svg/currys-logo.svg" alt="Currys logo">
                    </div>
                    <h3>Full-Stack Developer</h3>
                    <p>This is where my commercial experience started. As a junior I was surrounded by talented developers, giving me a strong foundation to build on.</p>
                    <p>I upskilled quickly and was trusted to work on the insurance platform as the only developer, giving me full autonomy.</p>
                    <div>
                        <span class="tag">PHP</span>
                        <span class="tag">MySQL</span>
                        <span class="tag">Twig</span>
                        <span class="tag">Symfony</span>
                        <span class="tag">Behat Test</span>
                        <span class="tag">UnitTest</span>
                    </div>
                </div>
            </div>

            <div class="timeline-row">
                <div class="timeline-time">
                    Evident<small>May 2023 - May 2025</small>
                </div>
                <div class="timeline-content card-bordered card-accent">
                    <div class="thumbs">
                        <img class="img-fluid rounded" src="jpg/evident-logo.jpg" alt="Evident logo">
                    </div>
                    <h3>Full-Stack Developer</h3>
                    <p>
                        My work at Evident is really when I moved from a mid-level developer towards senior level. This came from exposure to more technologies, specifically APIs and Vue, and being involved in every part of the delivery cycle, from discovery all the way through to release.
                    </p>
                    <div>
                        <span class="tag">PHP</span>
                        <span class="tag">MySQL</span>
                        <span class="tag">Vue</span>
                        <span class="tag">Symfony</span>
                        <span class="tag">API Platform</span>
                        <span class="tag">PostgreSQL</span>
                        <span class="tag">Documentation Writing</span>
                        <span class="tag">Nuxt</span>
                    </div>
                </div>
            </div>

            <div class="timeline-row">
                <div class="timeline-time">
                    CentricFlow<small>June 2025 - Present</small>
                </div>
                <div class="timeline-content card-bordered card-accent current">
                    <span class="now-badge">Current role</span>
                    <h3>Senior Developer</h3>
                    <p class="promotion">Joined as PHP Developer, promoted to Senior Developer after successfully leading the rebrand project.</p>
                    <p>
                        Working on a large legacy recruitment and staffing SaaS platform covering CRM, booking plans, timesheets, candidate onboarding, compliance and client/candidate portals.
                    </p>
                    <p>
                        I led the end-to-end rebrand to Evertime CRM / Evertime Pay &amp; Bill, building a design system and full dark mode across 2,000+ legacy files, alongside mobile-first reworks, performance tuning and security hardening, with ~800 commits so far.
                    </p>
                    <div>
                        <span class="tag">PHP</span>
                        <span class="tag">MySQL</span>
                        <span class="tag">JavaScript</span>
                        <span class="tag">jQuery</span>
                        <span class="tag">Bootstrap</span>
                        <span class="tag">CSS / Dark mode</span>
                        <span class="tag">AJAX</span>
                        <span class="tag">PDO</span>
                        <span class="tag">Docker</span>
                    </div>
                </div>
            </div>

            <div class="timeline-row">
                <div class="timeline-content card-bordered next">
                    <p class="m-0">What's next...</p>
                </div>
            </div>
	    </div>
    </section>
</template>

<script>
    export default {
    name: 'timeline',
    };
</script>

<style scoped>
.timeline {
    position: relative;
    padding: 2rem 0;
    margin: 0 auto 1rem auto;
    overflow: hidden;
}
.timeline:after {
    content: "";
    position: absolute;
    top: 0;
    left: 50%;
    margin-left: -1px;
    width: 2px;
    height: 100%;
    display: block;
    background: linear-gradient(180deg, var(--accent), var(--accent-2), transparent);
}

.timeline-row {
    padding-left: 50%;
    position: relative;
    margin-bottom: 30px;
}
.timeline-row .timeline-time {
    position: absolute;
    right: 50%;
    top: 15px;
    text-align: right;
    margin-right: 20px;
    color: var(--text);
    font-family: var(--font-display);
    font-weight: 600;
    font-size: 1.5rem;
}
.timeline-row .timeline-time small {
    display: block;
    font-family: var(--font-body);
    font-weight: 400;
    font-size: 0.85rem;
    color: var(--accent);
}
.timeline-row .timeline-content {
    position: relative;
    padding: 24px 28px;
    /* background, border, radius and hover come from .card-bordered / .card-accent */
    color: var(--text);
    display: flex;
    align-items: flex-start;
    flex-direction: column;
    text-align: left;
}
/* hover itself comes from the shared .card-bordered style; keep the arrow's edge in sync */
.timeline-row .timeline-content:after {
    transition: border-color 0.25s ease;
}
.timeline .timeline-row .timeline-content:hover:after {
    border-color: rgba(34, 211, 238, 0.55);
}
.timeline-row .timeline-content.next {
    align-items: center;
    color: var(--text-muted);
    border-style: dashed;
}
/* Arrow pointing at the rail */
.timeline-row .timeline-content:after {
    content: "";
    position: absolute;
    top: 20px;
    height: 16px;
    width: 16px;
    background: var(--surface);
    border-top: 1px solid var(--border);
    border-right: 1px solid var(--border);
}
/* Dot on the rail */
.timeline-row .timeline-content:before {
    content: "";
    position: absolute;
    top: 18px;
    right: -50px;
    width: 20px;
    height: 20px;
    border-radius: 50%;
    z-index: 10;
    background: var(--bg);
    border: 3px solid var(--accent);
    box-shadow: 0 0 0 4px var(--accent-soft);
}
.timeline-row .timeline-content.current:before {
    background: var(--accent);
}
.timeline-row .timeline-content h3 {
    font-size: 1.35rem;
    margin-bottom: 0.75rem;
}
.timeline-row .timeline-content p {
    color: var(--text-muted);
    margin-bottom: 1rem;
    line-height: 160%;
}
.timeline-row .timeline-content .thumbs {
    margin-bottom: 1rem;
    display: flex;
}
.timeline-row .timeline-content .thumbs img {
    max-width: 60px;
    padding: 6px;
    background: #fff;
    border-radius: 10px;
}
.timeline-row .timeline-content p.promotion {
    color: var(--accent);
    font-size: 0.9rem;
    font-weight: 500;
    margin-bottom: 0.75rem;
}
.now-badge {
    font-size: 0.75rem;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--bg);
    background: var(--gradient);
    padding: 0.25rem 0.7rem;
    border-radius: 999px;
    margin-bottom: 1rem;
}
.timeline-row:nth-child(even) .timeline-content {
    margin-left: 40px;
}
.timeline-row:nth-child(even) .timeline-content:after {
    left: -12px; /* clears the 4px accent edge */
    border-color: var(--accent);
    transform: rotate(-135deg);
}
.timeline-row:nth-child(even) .timeline-content:before {
    left: -51px;
    right: initial;
}
.timeline-row:nth-child(odd) {
    padding-left: 0;
    padding-right: 50%;
}
.timeline-row:nth-child(odd) .timeline-time {
    right: auto;
    left: 50%;
    text-align: left;
    margin-right: 0;
    margin-left: 20px;
}
.timeline-row:nth-child(odd) .timeline-content {
    margin-right: 40px;
}
.timeline-row:nth-child(odd) .timeline-content:after {
    right: -9px;
    transform: rotate(45deg);
}

@media (max-width: 992px) {
    .timeline {
        padding: 0;
    }
    .timeline:after {
        display: none;
    }
    .timeline .timeline-row:nth-child(odd),
    .timeline .timeline-row:nth-child(even) {
        padding: 0;
    }
    .timeline .timeline-row:nth-child(odd) .timeline-time,
    .timeline .timeline-row:nth-child(even) .timeline-time {
        position: relative;
        top: 0;
        left: 0;
        margin: 0 0 10px 0;
        text-align: left;
    }
    .timeline .timeline-row:nth-child(odd) .timeline-content,
    .timeline .timeline-row:nth-child(even) .timeline-content {
        margin: 0;
    }
    .timeline .timeline-row .timeline-content:before,
    .timeline .timeline-row .timeline-content:after {
        display: none;
    }
}
</style>
