<link rel="stylesheet" href="style.css">
<script src="script.js"></script>
/* =========================================
   VIJAY BHASKAR PORTFOLIO
   Professional Dark Theme
   ========================================= */

:root {
    --bg-primary: #0a1020;
    --bg-secondary: #0f172a;
    --bg-card: #111c33;
    --bg-card-hover: #16243f;

    --text-primary: #e6edf7;
    --text-secondary: #a8b3c7;
    --text-muted: #71809a;

    --accent-blue: #38bdf8;
    --accent-cyan: #22d3ee;
    --accent-purple: #8b5cf6;
    --accent-teal: #14b8a6;

    --border: rgba(148, 163, 184, 0.16);
    --shadow: 0 15px 40px rgba(0, 0, 0, 0.35);

    --max-width: 1180px;
    --radius: 16px;
}

/* ---------- RESET ---------- */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
    scroll-padding-top: 80px;
}

body {
    font-family:
        Inter,
        "Segoe UI",
        Roboto,
        Arial,
        sans-serif;

    background:
        radial-gradient(
            circle at 15% 15%,
            rgba(56, 189, 248, 0.08),
            transparent 28%
        ),
        radial-gradient(
            circle at 85% 20%,
            rgba(139, 92, 246, 0.08),
            transparent 30%
        ),
        var(--bg-primary);

    color: var(--text-primary);
    line-height: 1.7;
    min-height: 100vh;
}

body.menu-open {
    overflow: hidden;
}

a {
    color: inherit;
    text-decoration: none;
}

img {
    max-width: 100%;
    display: block;
}

button,
input,
textarea {
    font: inherit;
}

button {
    cursor: pointer;
}

/* ---------- CONTAINER ---------- */

.container {
    width: min(92%, var(--max-width));
    margin: 0 auto;
}

/* ---------- NAVIGATION ---------- */

.navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;

    background: rgba(10, 16, 32, 0.88);
    border-bottom: 1px solid var(--border);

    backdrop-filter: blur(18px);
    -webkit-backdrop-filter: blur(18px);
}

.nav-container {
    min-height: 72px;

    display: flex;
    align-items: center;
    justify-content: space-between;
}

.logo {
    font-size: 1.25rem;
    font-weight: 800;
    letter-spacing: 0.5px;
}

.logo span {
    color: var(--accent-cyan);
}

.nav-links {
    display: flex;
    align-items: center;
    gap: 24px;
    list-style: none;
}

.nav-links a {
    color: var(--text-secondary);
    font-size: 0.92rem;
    font-weight: 600;

    transition:
        color 0.25s ease,
        transform 0.25s ease;
}

.nav-links a:hover {
    color: var(--accent-cyan);
    transform: translateY(-1px);
}

.menu-toggle {
    display: none;

    background: transparent;
    border: 0;
    color: var(--text-primary);

    font-size: 1.6rem;
}

/* ---------- HERO ---------- */

.hero {
    min-height: 100vh;
    padding: 150px 0 90px;

    display: flex;
    align-items: center;

    position: relative;
    overflow: hidden;
}

.hero::before {
    content: "";
    position: absolute;

    width: 450px;
    height: 450px;

    top: 10%;
    right: -150px;

    border-radius: 50%;

    background: rgba(56, 189, 248, 0.07);
    filter: blur(80px);

    pointer-events: none;
}

.hero-content {
    max-width: 850px;
}

.hero-tag {
    display: inline-flex;
    align-items: center;

    padding: 8px 14px;
    margin-bottom: 22px;

    border: 1px solid rgba(56, 189, 248, 0.25);
    border-radius: 999px;

    background: rgba(56, 189, 248, 0.06);

    color: var(--accent-cyan);
    font-size: 0.85rem;
    font-weight: 700;
}

.hero h1 {
    font-size: clamp(2.8rem, 7vw, 5.8rem);
    line-height: 1.05;

    letter-spacing: -2px;
    margin-bottom: 20px;
}

.hero h1 span {
    background: linear-gradient(
        90deg,
        var(--accent-cyan),
        var(--accent-blue),
        var(--accent-purple)
    );

    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
}

.hero-subtitle {
    color: var(--text-secondary);
    font-size: clamp(1.05rem, 2vw, 1.3rem);
    max-width: 700px;

    margin-bottom: 32px;
}

.hero-buttons {
    display: flex;
    flex-wrap: wrap;
    gap: 14px;
}

/* ---------- BUTTONS ---------- */

.btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;

    min-height: 48px;
    padding: 0 22px;

    border-radius: 10px;

    font-weight: 700;
    font-size: 0.92rem;

    transition:
        transform 0.25s ease,
        box-shadow 0.25s ease,
        background 0.25s ease;
}

.btn:hover {
    transform: translateY(-3px);
}

.btn-primary {
    color: #06101c;

    background: linear-gradient(
        135deg,
        var(--accent-cyan),
        var(--accent-blue)
    );

    box-shadow:
        0 10px 30px rgba(34, 211, 238, 0.15);
}

.btn-secondary {
    color: var(--text-primary);

    border: 1px solid var(--border);
    background: var(--bg-card);
}

.btn-secondary:hover {
    background: var(--bg-card-hover);
}

/* ---------- SECTIONS ---------- */

section {
    padding: 100px 0;
}

.section-header {
    margin-bottom: 45px;
}

.section-label {
    display: block;

    margin-bottom: 8px;

    color: var(--accent-cyan);
    font-size: 0.78rem;
    font-weight: 800;

    letter-spacing: 2px;
    text-transform: uppercase;
}

.section-title {
    font-size: clamp(2rem, 4vw, 3rem);
    line-height: 1.15;
    margin-bottom: 12px;
}

.section-description {
    max-width: 700px;
    color: var(--text-secondary);
}

/* ---------- ABOUT ---------- */

.about-grid {
    display: grid;
    grid-template-columns: 1.2fr 0.8fr;
    gap: 35px;
}

.card {
    background:
        linear-gradient(
            145deg,
            rgba(17, 28, 51, 0.96),
            rgba(13, 23, 42, 0.96)
        );

    border: 1px solid var(--border);
    border-radius: var(--radius);

    padding: 28px;

    box-shadow: var(--shadow);

    transition:
        transform 0.3s ease,
        border-color 0.3s ease;
}

.card:hover {
    transform: translateY(-5px);
    border-color: rgba(56, 189, 248, 0.3);
}

.card h3 {
    margin-bottom: 12px;
}

.card p {
    color: var(--text-secondary);
}

/* ---------- SKILLS ---------- */

.skills-grid {
    display: grid;

    grid-template-columns:
        repeat(4, 1fr);

    gap: 18px;
}

.skill-card {
    padding: 24px;

    background: var(--bg-card);

    border: 1px solid var(--border);
    border-radius: 14px;

    transition:
        transform 0.25s ease,
        border-color 0.25s ease;
}

.skill-card:hover {
    transform: translateY(-5px);
    border-color: rgba(34, 211, 238, 0.35);
}

.skill-icon {
    width: 46px;
    height: 46px;

    display: grid;
    place-items: center;

    margin-bottom: 15px;

    border-radius: 12px;

    background: rgba(56, 189, 248, 0.08);

    color: var(--accent-cyan);
    font-size: 1.25rem;
}

.skill-card h3 {
    font-size: 1rem;
    margin-bottom: 6px;
}

.skill-card p {
    color: var(--text-muted);
    font-size: 0.88rem;
}

/* ---------- PROJECTS ---------- */

.projects-grid {
    display: grid;

    grid-template-columns:
        repeat(2, 1fr);

    gap: 22px;
}

.project-card {
    position: relative;

    padding: 28px;

    background: var(--bg-card);

    border: 1px solid var(--border);
    border-radius: var(--radius);

    overflow: hidden;

    transition:
        transform 0.3s ease,
        border-color 0.3s ease;
}

.project-card::before {
    content: "";

    position: absolute;

    width: 160px;
    height: 160px;

    top: -90px;
    right: -80px;

    border-radius: 50%;

    background: rgba(56, 189, 248, 0.08);
}

.project-card:hover {
    transform: translateY(-6px);
    border-color: rgba(56, 189, 248, 0.35);
}

.project-number {
    color: var(--accent-cyan);
    font-size: 0.8rem;
    font-weight: 800;

    letter-spacing: 1px;
}

.project-card h3 {
    margin: 10px 0;
}

.project-card p {
    color: var(--text-secondary);
}

.project-tags {
    display: flex;
    flex-wrap: wrap;

    gap: 8px;

    margin-top: 20px;
}

.project-tags span {
    padding: 5px 10px;

    border-radius: 999px;

    background: rgba(139, 92, 246, 0.1);

    color: #b9a5ff;

    font-size: 0.75rem;
    font-weight: 700;
}

/* ---------- TIMELINE ---------- */

.timeline {
    position: relative;

    max-width: 850px;
}

.timeline::before {
    content: "";

    position: absolute;

    left: 8px;
    top: 0;
    bottom: 0;

    width: 2px;

    background:
        linear-gradient(
            to bottom,
            var(--accent-cyan),
            var(--accent-purple)
        );
}

.timeline-item {
    position: relative;

    padding-left: 40px;
    margin-bottom: 35px;
}

.timeline-item::before {
    content: "";

    position: absolute;

    left: 0;
    top: 6px;

    width: 18px;
    height: 18px;

    border-radius: 50%;

    background: var(--bg-primary);

    border: 3px solid var(--accent-cyan);
}

.timeline-date {
    color: var(--accent-cyan);

    font-size: 0.82rem;
    font-weight: 800;

    margin-bottom: 5px;
}

.timeline-item h3 {
    margin-bottom: 5px;
}

.timeline-item p {
    color: var(--text-secondary);
}

/* ---------- RESUME ---------- */

.resume-box {
    display: flex;

    align-items: center;
    justify-content: space-between;

    gap: 30px;

    padding: 38px;

    background:
        linear-gradient(
            135deg,
            rgba(34, 211, 238, 0.08),
            rgba(139, 92, 246, 0.08)
        );

    border: 1px solid var(--border);
    border-radius: var(--radius);
}

.resume-box p {
    color: var(--text-secondary);
    margin-top: 8px;
}

/* ---------- CONTACT ---------- */

.contact-grid {
    display: grid;

    grid-template-columns: 0.8fr 1.2fr;

    gap: 25px;
}

.contact-list {
    display: grid;
    gap: 14px;
}

.contact-item {
    display: flex;
    align-items: center;
    gap: 14px;

    padding: 16px;

    background: var(--bg-card);

    border: 1px solid var(--border);
    border-radius: 12px;

    transition: border-color 0.25s ease;
}

.contact-item:hover {
    border-color: rgba(34, 211, 238, 0.35);
}

.contact-icon {
    width: 42px;
    height: 42px;

    display: grid;
    place-items: center;

    border-radius: 10px;

    background: rgba(34, 211, 238, 0.08);

    color: var(--accent-cyan);
}

.contact-item small {
    display: block;
    color: var(--text-muted);
    margin-bottom: 2px;
}

.contact-item span,
.contact-item a {
    color: var(--text-primary);
    font-weight: 600;
    word-break: break-word;
}

/* ---------- FORM ---------- */

.form-group {
    margin-bottom: 18px;
}

.form-group label {
    display: block;

    margin-bottom: 7px;

    color: var(--text-secondary);

    font-size: 0.88rem;
    font-weight: 600;
}

.form-control {
    width: 100%;

    padding: 13px 15px;

    border: 1px solid var(--border);
    border-radius: 10px;

    outline: none;

    background: #0b1427;
    color: var(--text-primary);

    transition:
        border-color 0.25s ease,
        box-shadow 0.25s ease;
}

.form-control:focus {
    border-color: var(--accent-cyan);

    box-shadow:
        0 0 0 3px rgba(34, 211, 238, 0.08);
}

textarea.form-control {
    min-height: 140px;
    resize: vertical;
}

/* ---------- FOOTER ---------- */

footer {
    padding: 35px 0;

    border-top: 1px solid var(--border);

    background: #080e1b;
}

.footer-content {
    display: flex;

    align-items: center;
    justify-content: space-between;

    gap: 20px;
}

.footer-content p {
    color: var(--text-muted);
    font-size: 0.88rem;
}

.social-links {
    display: flex;
    gap: 10px;
}

.social-links a {
    width: 40px;
    height: 40px;

    display: grid;
    place-items: center;

    border: 1px solid var(--border);
    border-radius: 10px;

    color: var(--text-secondary);

    transition:
        color 0.25s ease,
        border-color 0.25s ease,
        transform 0.25s ease;
}

.social-links a:hover {
    color: var(--accent-cyan);

    border-color: rgba(34, 211, 238, 0.4);

    transform: translateY(-3px);
}

/* ---------- SCROLL REVEAL ---------- */

.reveal {
    opacity: 0;
    transform: translateY(25px);

    transition:
        opacity 0.7s ease,
        transform 0.7s ease;
}

.reveal.active {
    opacity: 1;
    transform: translateY(0);
}

/* ---------- RESPONSIVE ---------- */

@media (max-width: 1000px) {
    .skills-grid {
        grid-template-columns:
            repeat(2, 1fr);
    }

    .about-grid {
        grid-template-columns: 1fr;
    }
}

@media (max-width: 800px) {
    .menu-toggle {
        display: block;
    }

    .nav-links {
        position: fixed;

        top: 72px;
        left: 0;
        right: 0;

        display: none;
        flex-direction: column;
        align-items: flex-start;

        padding: 25px;

        background: #0a1020;

        border-bottom: 1px solid var(--border);
    }

    .nav-links.active {
        display: flex;
    }

    .projects-grid,
    .contact-grid {
        grid-template-columns: 1fr;
    }

    .resume-box,
    .footer-content {
        flex-direction: column;
        align-items: flex-start;
    }
}

@media (max-width: 550px) {
    section {
        padding: 75px 0;
    }

    .hero {
        padding-top: 125px;
    }

    .skills-grid {
        grid-template-columns: 1fr;
    }

    .hero-buttons {
        flex-direction: column;
        align-items: stretch;
    }

    .btn {
        width: 100%;
    }

    .card,
    .project-card {
        padding: 22px;
    }
}

/* ---------- ACCESSIBILITY ---------- */

:focus-visible {
    outline: 2px solid var(--accent-cyan);
    outline-offset: 3px;
}

/* ---------- REDUCED MOTION ---------- */

@media (prefers-reduced-motion: reduce) {
    *,
    *::before,
    *::after {
        scroll-behavior: auto !important;
        transition-duration: 0.01ms !important;
        animation-duration: 0.01ms !important;
    }
}
