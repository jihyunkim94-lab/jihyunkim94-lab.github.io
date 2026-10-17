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

/* ===== 저널 배지 숨김 (이 페이지만, Home은 유지) ===== */
.publications .abbr { display: none !important; }
.publications ol.bibliography > li .row > div:not(.abbr) {
  flex: 1 1 auto !important;
  max-width: 100% !important;
  width: 100% !important;
}

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

/* ===== 구역 헤더 ===== */
.pub-era {
  display: flex;
  align-items: baseline;
  flex-wrap: wrap;
  gap: 0.75rem;
  margin: 2.6rem 0 0.8rem 0;
  padding-bottom: 0.65rem;
  border-bottom: 1px solid;
}
.pub-era.first { margin-top: 0.4rem; }
.pub-era-tag {
  font-size: 0.6rem;
  font-weight: 600;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  padding: 0.2rem 0.55rem;
  border-radius: 3px;
  background: var(--global-theme-color);
  color: #FCFCFC;
}
.pub-era-title { font-size: 1.15rem; font-weight: 700; letter-spacing: -0.02em; }
.pub-era-range { font-size: 0.82rem; font-weight: 500; margin-left: auto; font-variant-numeric: tabular-nums; }

/* ===== 논문 번호 (자동 계산) ===== */
.publications ol.bibliography { padding-left: 0; }
.publications ol.bibliography > li {
  position: relative;
  padding-left: 2.9rem;
  list-style: none;
}
.publications ol.bibliography > li[data-num]::before {
  content: "(" attr(data-num) ")";
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

html[data-theme="light"] .publications h2.year,
html[data-theme="light"] .publications .year { color: rgba(25,25,25,0.28) !important; }
html[data-theme="light"] .publications ol.bibliography > li::before { color: #A8A8A8; }
html[data-theme="light"] .publications h2.year,
html[data-theme="light"] .publications .year,
html[data-theme="light"] hr { border-color: rgba(25,25,25,0.14) !important; }

html[data-theme="light"] .pub-era { border-bottom-color: rgba(25,25,25,0.22); }
html[data-theme="light"] .pub-era-title { color: #191919; }
html[data-theme="light"] .pub-era-range { color: #8A8A8A; }

/* ===== 다크 모드: 색상 ===== */
html[data-theme="dark"] .publications .title { color: #FCFCFC !important; }
html[data-theme="dark"] .publications .author,
html[data-theme="dark"] .publications .periodical { color: #B0B0B0 !important; }
html[data-theme="dark"] .publications .author a,
html[data-theme="dark"] .publications .author .more-authors { color: #B0B0B0 !important; }
html[data-theme="dark"] .publications .author em,
html[data-theme="dark"] .publications .author strong { color: #86CFDA !important; }

html[data-theme="dark"] .publications h2.year,
html[data-theme="dark"] .publications .year { color: #FCFCFC !important; }
html[data-theme="dark"] .publications ol.bibliography > li::before { color: #FCFCFC !important; }
html[data-theme="dark"] .publications h2.year,
html[data-theme="dark"] .publications .year,
html[data-theme="dark"] hr { border-color: rgba(252,252,252,0.45) !important; }

html[data-theme="dark"] .pub-era { border-bottom-color: rgba(252,252,252,0.45); }
html[data-theme="dark"] .pub-era-title { color: #FCFCFC; }
html[data-theme="dark"] .pub-era-range { color: #B0B0B0; }
</style>

<div class="publications">

<div class="pub-era first">
  <span class="pub-era-tag">At Ajou</span>
  <span class="pub-era-title">Ajou University</span>
  <span class="pub-era-range">2026 – Present</span>
</div>

{% bibliography --group_by none --query @*[ajou=true]* %}

<div class="pub-era">
  <span class="pub-era-tag">Before Ajou</span>
  <span class="pub-era-range">2020 – 2026</span>
</div>

{% bibliography --query @*[ajou!=true]* %}

</div>

<script>
(function () {
  function run() {
    var root = document.querySelector(".publications");
    if (!root) return;
    var all = root.querySelectorAll("ol.bibliography > li");
    var seen = {};
    var shown = [];
    all.forEach(function (li) {
      var t = li.querySelector(".title");
      var key = (t ? t.textContent : li.textContent).trim().toLowerCase();
      if (seen[key]) { li.style.display = "none"; }
      else { seen[key] = true; shown.push(li); }
    });
    var n = shown.length;
    shown.forEach(function (li, i) { li.setAttribute("data-num", n - i); });
  }
  if (document.readyState === "loading") document.addEventListener("DOMContentLoaded", run);
  else run();
})();
</script>
