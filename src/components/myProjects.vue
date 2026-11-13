<template>
    <section class="container section">
        <h2 class="section-title">Recent work</h2>
        <p class="section-lead">
            Highlights from my current role at CentricFlow, where I'm modernising a large legacy SaaS platform from the inside without a rewrite.
        </p>

        <!-- Featured: the rebrand -->
        <article class="featured card-bordered mb-4">
            <div class="featured-head">
                <span class="kicker">{{ featured.period }}</span>
                <h3 class="mb-2">{{ featured.title }}</h3>
                <p class="muted mb-0">{{ featured.summary }}</p>
            </div>
            <div class="row g-4 mt-1">
                <div class="col-md-7">
                    <ul class="point-list">
                        <li v-for="point in featured.points" :key="point">{{ point }}</li>
                    </ul>
                </div>
                <div class="col-md-5">
                    <div class="stats">
                        <div v-for="stat in featured.stats" :key="stat.label" class="stat">
                            <span class="stat-value gradient-text">{{ stat.value }}</span>
                            <span class="stat-label">{{ stat.label }}</span>
                        </div>
                    </div>
                </div>
            </div>
            <div class="mt-3">
                <span v-for="tag in featured.tags" :key="tag" class="tag">{{ tag }}</span>
            </div>
        </article>

        <!-- Other highlights -->
        <div class="row g-4">
            <div v-for="project in projects" :key="project.title" class="col-md-6">
                <article class="project card-bordered h-100">
                    <div class="project-icon" aria-hidden="true">{{ project.icon }}</div>
                    <h3 class="project-title">{{ project.title }}</h3>
                    <ul class="point-list">
                        <li v-for="point in project.points" :key="point">{{ point }}</li>
                    </ul>
                    <div class="mt-auto pt-2">
                        <span v-for="tag in project.tags" :key="tag" class="tag">{{ tag }}</span>
                    </div>
                </article>
            </div>
        </div>

        <!-- Earlier project with a screenshot -->
        <h3 class="sub-title mt-5 mb-3">From Evident</h3>
        <article class="card-bordered showcase">
            <div class="row g-0 align-items-center">
                <div class="col-lg-7">
                    <div class="shot">
                        <img src="png/publicDeviceRegistry.png" alt="Evident Device Register: world map with clustered device markers" class="img-fluid" loading="lazy">
                    </div>
                </div>
                <div class="col-lg-5">
                    <div class="p-4">
                        <h3 class="project-title">Evident Device Register</h3>
                        <p class="muted">
                            A public device register built on the Google Maps JavaScript API, plotting registered devices on an interactive world map with clustered markers, alongside a table view and user guides.
                        </p>
                        <span class="tag">Google Maps JavaScript API</span>
                        <span class="tag">Marker clustering</span>
                    </div>
                </div>
            </div>
        </article>
    </section>
</template>

<script setup>
const featured = {
    period: "May – Oct 2026 · CentricFlow",
    title: "Platform-wide rebrand: CentricFlow → Evertime CRM / Evertime Pay & Bill",
    summary:
        "Rebranded the whole product end to end in phased releases: every main tab, all SPAs, client and candidate portals, timesheet sites, gateway/login, emails and PDFs.",
    points: [
        "Built a coherent design system over years of one-off styling: buttons, badges, animated alerts, modals, cards, hover tables, breadcrumbs, gradient headers and footers, scrollbars and branded checkboxes.",
        "Added a full dark mode, including dark/light logo switching and untangling hard-coded colours and !important overrides that fought the new theme.",
        "Standardised settings pages into a consistent card layout with side navigation.",
        "Led it as phased releases with QA check calls and follow-up hotfix rounds, which earned a promotion from PHP Developer to Senior Developer.",
    ],
    stats: [
        { value: "2,000+", label: "legacy PHP files touched" },
        { value: "~260", label: "commits in the rebrand & mobile period" },
        { value: "~800", label: "commits at CentricFlow" },
    ],
    tags: ["Design systems", "CSS", "Dark mode", "Bootstrap", "jQuery", "PHP"],
};

const projects = [
    {
        icon: "◐",
        title: "Loading states & perceived performance",
        points: [
            "Site-wide preloader (dark-mode aware) and skeleton loaders on heavy pages like candidate/client lists and the booking plan.",
            "Loading, loaded and failed states on AJAX sections and form submits, with double clicks blocked while sections load.",
            "Converted the reference form so every section loads via AJAX with its own loading and error states.",
        ],
        tags: ["UX", "AJAX", "Skeleton loaders"],
    },
    {
        icon: "⚡",
        title: "Load-time & query optimisation",
        points: [
            "Removed an unneeded JS bundle and unused stylesheets, replaced by a small custom stylesheet.",
            "Responsive logo images, so smaller screens get smaller files.",
            "Fixed N+1 queries, swapped SELECT * for only the needed columns, tightened joins and added pagination.",
            "Cut dashboard auto-refresh from every 30 seconds to every 15 minutes / hourly.",
        ],
        tags: ["Web performance", "MySQL", "Front-end assets"],
    },
    {
        icon: "▯",
        title: "Mobile-first rework of legacy pages",
        points: [
            "Rebuilt candidate onboarding for phones: welcome screen, progress bar, agency-branded colours and a screen-fitting signature pad.",
            "Phone-friendly 10MB uploads with preview/remove cards and a live size meter that stops submissions the server would silently drop, without losing answers.",
            "Responsive dashboard with widget-style customisable sections, diary/calendar, timesheets and headers.",
        ],
        tags: ["Responsive design", "Forms", "Mobile UX"],
    },
    {
        icon: "⛨",
        title: "Legacy modernisation & security",
        points: [
            "Moved raw SQL to PDO prepared statements and fixed SQL injection issues.",
            "Added agency-ID scoping to queries for multi-tenant data isolation, plus an HSTS header.",
            "Set up a Docker dev environment and a test branch for the PHP 7.2 → 8.5 upgrade.",
            "Moved hard-coded staging URLs to environment config and gave the timesheet/gateway apps their own subdomains.",
        ],
        tags: ["Security", "PDO", "Docker"],
    },
];
</script>

<style scoped>
.muted {
    color: var(--text-muted);
}

.featured {
    padding: 2rem;
    /* gradient border: surface fill on padding-box, gradient shows through the transparent border */
    background:
        linear-gradient(var(--surface), var(--surface)) padding-box,
        var(--gradient) border-box;
    border: 1px solid transparent;
}

.featured:hover {
    border-color: transparent;
}

.kicker {
    display: inline-block;
    font-size: 0.78rem;
    font-weight: 600;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--accent);
    margin-bottom: 0.5rem;
}

.featured h3 {
    font-size: clamp(1.3rem, 2.4vw, 1.7rem);
}

.point-list {
    padding-left: 1.1rem;
    margin-bottom: 1rem;
    color: var(--text-muted);
}

.point-list li {
    margin-bottom: 0.5rem;
    line-height: 1.55;
}

.point-list li::marker {
    color: var(--accent);
}

.stats {
    display: grid;
    gap: 0.75rem;
}

.stat {
    padding: 1rem 1.25rem;
    background: var(--surface-2);
    border: 1px solid var(--border);
    border-radius: 10px;
    display: flex;
    flex-direction: column;
}

.stat-value {
    font-family: var(--font-display);
    font-size: 1.9rem;
    font-weight: 700;
    line-height: 1.1;
}

.stat-label {
    font-size: 0.85rem;
    color: var(--text-muted);
}

.project {
    padding: 1.75rem;
    display: flex;
    flex-direction: column;
}

.project-icon {
    width: 44px;
    height: 44px;
    display: grid;
    place-items: center;
    font-size: 1.3rem;
    color: var(--accent);
    background: var(--accent-soft);
    border: 1px solid rgba(34, 211, 238, 0.35);
    border-radius: 12px;
    margin-bottom: 1rem;
}

.project-title {
    font-size: 1.2rem;
    margin-bottom: 0.9rem;
}

.sub-title {
    font-size: 1.3rem;
    color: var(--text-muted);
}

.showcase {
    overflow: hidden;
}

.shot {
    border-right: 1px solid var(--border);
}

.shot img {
    display: block;
    width: 100%;
}

@media (max-width: 991px) {
    .shot {
        border-right: 0;
        border-bottom: 1px solid var(--border);
    }
}
</style>
