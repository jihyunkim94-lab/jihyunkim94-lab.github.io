---
layout: page
permalink: /publications/
title: Publications
nav: true
nav_order: 4
---

<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap");

body, p, li, td, .navbar, .navbar-brand, h1, h2, h3, h4, h5, h6 {
  font-family: "Inter", -apple-system, BlinkMacSystemFont, sans-serif !important;
}
h1, h2, h3, .navbar-brand { font-weight: 700 !important; letter-spacing: -0.02em; }
body { font-weight: 400; letter-spacing: -0.005em; }

/* 네비게이션 */
.navbar .navbar-nav, .navbar ul { margin-left: 2rem !important; margin-right: auto !important; }
.navbar .container, .navbar .container-fluid, .navbar > div { justify-content: flex-start !important; }

/* ===== 테마 공통: 크기 / 굵기 / 간격 ===== */
.publications .title,
.publications ol.bibliography > li > div:not(.abbr) > .title {
  font-size: 1rem !important;
  font-weight: 700 !important;
  letter-spacing: -0.015em;
  line-height: 1.4;
}
.publications .author,
.publications .periodical {
  font-size: 0.82rem !important;
  line-height: 1.45;
  font-weight: 400 !important;
}
.publications .author em,
.publications .author strong { font-weight: 600 !important; }

.publications h2.year,
.publications .year {
  font-size: 1.5rem !important;
  font-weight: 700 !important;
  letter-spacing: -0.02em;
  margin: 1.2rem 0 0.6rem 0 !important;
}

/* ===== 논문 번호 ===== */
.publications { counter-reset: pubnum 43; }
.publications ol.bibliography { padding-left: 0; }
.publications ol.bibliography > li {
  counter-increment: pubnum -1;
  position: relative;
  padding-left: 2.9rem;
  list-style: none;
}
.publications ol.bibliography > li::before {
  content: "(" counter(pubnum) ")";
  position: absolute;
  left: 0;
  top: 0.25rem;
  width: 2.2rem;
  text-align: right;
  font-size: 0.78rem;
  font-weight: 500;
  font-variant-numeric: tabular-nums;
}

/* ===== 라이트 모드: 색상 ===== */
html[data-theme="light"] {
  --global-theme-color: #651FFF;
  --global-hover-color: #651FFF;
  --global-text-color: #191919;
  --global-divider-color: rgba(25, 25, 25, 0.12);
  --global-bg-color: #FCFCFC;
  background-color: #FCFCFC;
}
html[data-theme="light"] body { background-color: #FCFCFC; color: #191919; }

html[data-theme="light"] .navbar .nav-link,
html[data-theme="light"] .navbar .nav-item.active .nav-link,
html[data-theme="light"] .navbar .dropdown-toggle,
html[data-theme="light"] .navbar-brand { color: #191919 !important; }

html[data-theme="light"] .navbar .nav-link:hover,
html[data-theme="light"] .navbar .nav-item.active .nav-link:hover,
html[data-theme="light"] .navbar .dropdown-toggle:hover,
html[data-theme="light"] .navbar-brand:hover { color: #651FFF !important; }

html[data-theme="light"] h1, html[data-theme="light"] h2, html[data-theme="light"] h3,
html[data-theme="light"] .post-title { color: #191919 !important; }

html[data-theme="light"] .publications .title { color: #191919 !important; }
html[data-theme="light"] .publications .author,
html[data-theme="light"] .publications .periodical { color: #5A5A5A !important; }
html[data-theme="light"] .publications .author a,
html[data-theme="light"] .publications .author .more-authors { color: #5A5A5A !important; }
html[data-theme="light"] .publications .author em,
html[data-theme="light"] .publications .author strong { color: #651FFF !important; }

html[data-theme="light"] .abbr abbr, html[data-theme="light"] .abbr .badge,
html[data-theme="light"] abbr.badge, html[data-theme="light"] .badge { color: #FCFCFC !important; }

html[data-theme="light"] .publications h2.year,
html[data-theme="light"] .publications .year { color: rgba(25,25,25,0.28) !important; }
html[data-theme="light"] .publications ol.bibliography > li::before { color: #A8A8A8; }
html[data-theme="light"] .publications h2.year,
html[data-theme="light"] .publications .year,
html[data-theme="light"] hr { border-color: rgba(25,25,25,0.14) !important; }

/* ===== 다크 모드: 색상 ===== */
html[data-theme="dark"] .publications .title { color: #FCFCFC !important; }
html[data-theme="dark"] .publications .author,
html[data-theme="dark"] .publications .periodical { color: #B0B0B0 !important; }
html[data-theme="dark"] .publications .author a,
html[data-theme="dark"] .publications .author .more-authors { color: #B0B0B0 !important; }
html[data-theme="dark"] .publications .author em,
html[data-theme="dark"] .publications .author strong { color: #86CFDA !important; }

html[data-theme="dark"] .publications h2.year,
html[data-theme="dark"] .publications .year { color: rgba(252,252,252,0.42) !important; }
html[data-theme="dark"] .publications ol.bibliography > li::before { color: #9A9A9A; }
html[data-theme="dark"] .publications h2.year,
html[data-theme="dark"] .publications .year,
html[data-theme="dark"] hr { border-color: rgba(252,252,252,0.28) !important; }
</style>

<div class="publications">
{% bibliography %}
</div>
