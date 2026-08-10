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

/* 네비게이션 왼쪽 정렬 */
.navbar-nav, .navbar-nav.ms-auto, .navbar-nav.ml-auto, .navbar ul.ms-auto {
  margin-left: 0 !important; margin-right: auto !important; padding-left: 0 !important;
}
nav.navbar > .container, nav.navbar > .container-fluid, nav.navbar > div, .navbar-collapse {
  justify-content: flex-start !important;
}
.navbar .nav-item:first-child .nav-link { padding-left: 0 !important; }

/* 라이트 모드 */
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
html[data-theme="light"] h4, html[data-theme="light"] h5, html[data-theme="light"] h6,
html[data-theme="light"] .post-title { color: #191919 !important; }

html[data-theme="light"] p a, html[data-theme="light"] li a { color: #651FFF !important; }

/* 배지 */
html[data-theme="light"] .abbr abbr, html[data-theme="light"] .abbr .badge,
html[data-theme="light"] abbr.badge, html[data-theme="light"] .badge { color: #FCFCFC !important; }

/* 논문 목록 */
html[data-theme="light"] .publications .author,
html[data-theme="light"] .publications .periodical {
  font-size: 0.82rem !important; color: #5A5A5A !important; line-height: 1.45;
}
html[data-theme="light"] .publications .author a,
html[data-theme="light"] .publications .author .more-authors { color: #5A5A5A !important; }
html[data-theme="light"] .publications .author em,
html[data-theme="light"] .publications .author strong { color: #651FFF !important; font-weight: 600; }
html[data-theme="light"] .publications h2.year,
html[data-theme="light"] .publications .year { color: rgba(25,25,25,0.15) !important; }

/* 다크 모드 */
html[data-theme="dark"] .pi-name, html[data-theme="dark"] .pi-section,
html[data-theme="dark"] .pi-table td { color: #FCFCFC !important; }
html[data-theme="dark"] .pi-role { color: #B5B5B5 !important; }

/* 공통 섹션 스타일 */
.pi-section { font-size: 1.05rem; font-weight: 700; letter-spacing: -0.02em; border-top: 1px solid rgba(25,25,25,0.12); padding-top: 0.9rem; margin: 1.6rem 0 0.7rem 0; }
.pi-body { font-size: 0.92rem; line-height: 1.6; }
</style>

<div class="publications">

{% bibliography %}

</div>
