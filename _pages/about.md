---
layout: about
title: Home
permalink: /
nav: false
nav_order: 1
subtitle: Department of Intelligent Semiconductor Engineering, Ajou University
news: true
selected_papers: true
social: true
announcements:
  enabled: true
  scrollable: false
  limit: 5
latest_posts:
  enabled: false
---
<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap");
/* ===== 탭 이동 시 전체 축 밀림 방지 ===== */
html {
  scrollbar-gutter: stable;
  overflow-y: scroll;
}
body { overflow-x: clip; }
body, p, li, td, th, .navbar, .navbar-brand, h1, h2, h3, h4, h5, h6,
.kimlab-text, .kimlab-cap {
  font-family: "Inter", -apple-system, BlinkMacSystemFont, sans-serif !important;
}
h1, h2, h3, .navbar-brand { font-weight: 700 !important; letter-spacing: -0.02em; }
body { font-weight: 400; letter-spacing: -0.005em; }
/* 네비게이션 — 다른 페이지와 동일하게 통일 */
.navbar .navbar-nav, .navbar ul { margin-left: 2rem !important; margin-right: auto !important; }
.navbar .container, .navbar .container-fluid, .navbar > div { justify-content: flex-start !important; }
/* 홈에서도 좌측 "Kim Lab" 브랜드가 항상 보이도록 */
.navbar .navbar-brand, #navbar .navbar-brand {
  visibility: visible !important;
  opacity: 1 !important;
  display: inline-block !important;
  transform: none !important;
  text-decoration: none;
}
/* ===== 소속 줄(subtitle) 강조 + 본문과의 간격 ===== */
.post-header .desc, p.desc {
  font-weight: 700 !important;
  font-size: 0.95rem !important;
  letter-spacing: -0.01em;
  line-height: 1.5;
  margin-bottom: 0 !important;
}
.post-header { margin-bottom: 2.1rem !important; }

/* ============================================================
   글자 규격 통일 — Team / Research 탭과 동일하게
   섹션 제목  1.38rem / 800   (= .tm-group, h2.rs-sec)
   본문       0.92rem         (= .tm-body, .rs-prose p)
   news 행    0.86rem         (= .pi-table, .nw-row)
   ============================================================ */
.post-content h2, .news h2, .publications h2, main h2 {
  font-size: 1.38rem !important;
  font-weight: 800 !important;
  letter-spacing: -0.025em !important;
  line-height: 1.2 !important;
  text-transform: capitalize;      /* "news" → "News" — 원치 않으면 이 줄 삭제 */
  margin: 2.4rem 0 1rem 0 !important;
}
.post-content h2 a, .news h2 a, .publications h2 a, main h2 a { color: inherit !important; }

.kimlab-text p {
  font-size: 0.92rem;
  line-height: 1.65;
  margin: 0 0 1rem 0;
}

.news table th, .news table td, .news p, .news li {
  font-size: 0.86rem !important;
  line-height: 1.5 !important;
}
.news table th { font-weight: 600 !important; white-space: nowrap; padding-right: 0.8rem; }
.news table td { padding-top: 0 !important; }

/* 슬라이더 아래 섹션 겹침 방지 */
.news, .publications, .post-list, h2 { clear: both; }
.news { padding-top: 1.2rem; }
/* ===== Publications 항목 ===== */
.publications .title {
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
html[data-theme="light"] h4, html[data-theme="light"] h5, html[data-theme="light"] h6,
html[data-theme="light"] .post-title,
html[data-theme="light"] .news .date,
html[data-theme="light"] .news table th { color: #191919 !important; }
html[data-theme="light"] .post-header .desc,
html[data-theme="light"] p.desc { color: #2E2E2E !important; }
html[data-theme="light"] .kimlab-text p { color: #191919 !important; }
html[data-theme="light"] .abbr abbr, html[data-theme="light"] .abbr .badge,
html[data-theme="light"] abbr.badge, html[data-theme="light"] .badge { color: #FCFCFC !important; }
html[data-theme="light"] p a, html[data-theme="light"] li a,
html[data-theme="light"] .news a { color: #651FFF !important; }
html[data-theme="light"] .publications .title { color: #191919 !important; }
html[data-theme="light"] .publications .author,
html[data-theme="light"] .publications .periodical { color: #5A5A5A !important; }
html[data-theme="light"] .publications .author a,
html[data-theme="light"] .publications .author .more-authors { color: #5A5A5A !important; }
html[data-theme="light"] .publications .author em,
html[data-theme="light"] .publications .author strong { color: #651FFF !important; }
/* ===== 다크 모드: 색상 ===== */
html[data-theme="dark"] .post-header .desc,
html[data-theme="dark"] p.desc { color: #D5D5D5 !important; }
html[data-theme="dark"] .kimlab-text p { color: #FCFCFC !important; }
html[data-theme="dark"] .publications .title { color: #FCFCFC !important; }
html[data-theme="dark"] .publications .author,
html[data-theme="dark"] .publications .periodical { color: #B0B0B0 !important; }
html[data-theme="dark"] .publications .author a,
html[data-theme="dark"] .publications .author .more-authors { color: #B0B0B0 !important; }
html[data-theme="dark"] .publications .author em,
html[data-theme="dark"] .publications .author strong { color: #86CFDA !important; }

/* ===== 슬라이더 ===== */
.kimlab-intro::after { content: ""; display: block; clear: both; }
.kimlab-slider { float: right; width: 300px; max-width: 100%; margin: -100px 0 1.5rem 2rem; }

/* 슬라이드 5개를 같은 그리드 칸에 겹쳐 쌓아 컨테이너 높이를 고정 */
.kimlab-slides { display: grid; }
.kimlab-slide {
  grid-area: 1 / 1;
  visibility: hidden;
  opacity: 0;
  transition: opacity 0.35s ease;
  pointer-events: none;
}
.kimlab-slide.active {
  visibility: visible;
  opacity: 1;
  pointer-events: auto;
}

.kimlab-slide img { width: 100%; aspect-ratio: 1 / 1.386; object-fit: cover; object-position: top center; border-radius: 6px; display: block; }
.kimlab-cap { font-size: 0.72rem; line-height: 1.35; margin-top: 0.5rem; }
.kimlab-cap .tag { display: block; letter-spacing: 0.12em; font-size: 0.58rem; opacity: 0.55; margin-bottom: 2px; }
.kimlab-cap .ttl { font-weight: 700; }
.kimlab-cap .src { opacity: 0.7; }
.kimlab-nav { display: flex; justify-content: space-between; align-items: center; margin-top: 0.5rem; }
.kimlab-btn { border: 1px solid rgba(128,128,128,0.35); background: transparent; color: inherit; border-radius: 4px; padding: 0 0.55rem; font-size: 0.95rem; line-height: 1.7; cursor: pointer; }
.kimlab-dots { display: flex; gap: 0.3rem; }
.kimlab-dot { width: 6px; height: 6px; border-radius: 50%; background: rgba(128,128,128,0.4); cursor: pointer; }
.kimlab-dot.on { background: var(--global-theme-color); }

/* ===== 모바일 ① : 설명이 먼저, 논문 슬라이더가 그 다음 + 글자 규격 ===== */
@media (max-width: 768px) {
  .kimlab-intro { display: flex; flex-direction: column; }
  .kimlab-text { order: 1; }
  .kimlab-slider {
    order: 2;
    float: none;
    width: 100%;
    max-width: 320px;
    margin: 1.6rem auto 0.5rem auto;
  }
  .post-header { margin-bottom: 1.5rem !important; }
  .post-content h2, .news h2, .publications h2, main h2 {
    font-size: 1.18rem !important;
    margin: 2rem 0 0.85rem 0 !important;
  }
  .kimlab-text p { font-size: 0.89rem; }
  .news table th, .news table td, .news p, .news li { font-size: 0.8rem !important; }
  .publications .title { font-size: 0.94rem !important; }
  .publications .author, .publications .periodical { font-size: 0.78rem !important; }
}

/* ===== 모바일 ② : 저널 약어 배지를 내용에 맞는 크기로 ===== */
@media (max-width: 576px) {
  .publications ol.bibliography > li .abbr {
    height: auto !important;
    text-align: left !important;
    margin-bottom: 0.4rem !important;
  }
  .publications ol.bibliography > li .abbr abbr,
  .publications ol.bibliography > li .abbr .badge,
  .publications abbr.badge,
  .publications .badge {
    display: inline-block !important;
    width: auto !important;
    max-width: max-content !important;
    font-size: 0.62rem !important;
    font-weight: 600 !important;
    letter-spacing: 0.01em !important;
    padding: 0.2rem 0.5rem !important;
    line-height: 1.25 !important;
    border-radius: 4px !important;
    white-space: nowrap;
  }
}

@media (prefers-reduced-motion: reduce) {
  .kimlab-slide { transition: none; }
}
</style>

<div class="kimlab-intro">

  <div class="kimlab-slider">
    <div class="kimlab-slides">
      <div class="kimlab-slide active">
        <img src="{{ '/assets/img/featured/paper1.png' | relative_url }}" alt="">
        <div class="kimlab-cap">
          <span class="tag">FEATURED WORK</span>
          <span class="ttl">Sub-stoichiometric zirconium oxide as a solution-processed dielectric for reconfigurable electronics</span><br>
          <span class="src"><em>Nature Electronics</em> 8, 461–473 (2025)</span>
        </div>
      </div>
      <div class="kimlab-slide">
        <img src="{{ '/assets/img/featured/paper2.png' | relative_url }}" alt="">
        <div class="kimlab-cap">
          <span class="tag">COVER ARTICLE</span>
          <span class="ttl">Orthogonal photopatterning of two-dimensional percolated network films for wafer-scale heterostructures</span><br>
          <span class="src"><em>Nature Electronics</em> — March 2025 cover</span>
        </div>
      </div>
      <div class="kimlab-slide">
        <img src="{{ '/assets/img/featured/paper3.png' | relative_url }}" alt="">
        <div class="kimlab-cap">
          <span class="tag">FEATURED WORK</span>
          <span class="ttl">Orthogonal photopatterning of two-dimensional percolated network films for wafer-scale heterostructures</span><br>
          <span class="src"><em>Nature Electronics</em> 8, 235–243 (2025)</span>
        </div>
      </div>
      <div class="kimlab-slide">
        <img src="{{ '/assets/img/featured/paper4.png' | relative_url }}" alt="">
        <div class="kimlab-cap">
          <span class="tag">FEATURED WORK</span>
          <span class="ttl">Wafer-scale transistor arrays fabricated using slot-die printing of molybdenum disulfide and sodium-embedded alumina</span><br>
          <span class="src"><em>Nature Electronics</em> 6, 443–450 (2023)</span>
        </div>
      </div>
      <div class="kimlab-slide">
        <img src="{{ '/assets/img/featured/paper5.png' | relative_url }}" alt="">
        <div class="kimlab-cap">
          <span class="tag">COVER ARTICLE</span>
          <span class="ttl">All-solution-processed van der Waals heterostructures for wafer-scale electronics</span><br>
          <span class="src"><em>Advanced Materials</em> — 2022 cover</span>
        </div>
      </div>
    </div>
    <div class="kimlab-nav">
      <button class="kimlab-btn kimlab-prev" aria-label="previous">&#8249;</button>
      <div class="kimlab-dots">
        <span class="kimlab-dot on"></span><span class="kimlab-dot"></span><span class="kimlab-dot"></span><span class="kimlab-dot"></span><span class="kimlab-dot"></span>
      </div>
      <button class="kimlab-btn kimlab-next" aria-label="next">&#8250;</button>
    </div>
  </div>

  <div class="kimlab-text">
    <p>Kim Lab designs materials at the <strong>atomic scale</strong> and engineers them into <strong>scalable, reproducible platforms</strong> for next-generation electronics.</p>
    <p>Our guiding question: how do we translate control at the level of individual atomic layers into materials that can be made reliably, repeatedly, and at scale — and what devices become possible once we can? Answering it means working across materials characterizations, thin-film engineering, and device physics.</p>
    <p>We are always looking for curious students who want to build things that do not exist yet.</p>
  </div>

</div>

<div style="clear: both;"></div>

<script>
(function () {
  var root = document.querySelector(".kimlab-slider");
  if (!root) return;
  var slides = root.querySelectorAll(".kimlab-slide");
  var dots = root.querySelectorAll(".kimlab-dot");
  var i = 0;
  function show(n) {
    i = (n + slides.length) % slides.length;
    slides.forEach(function (s, k) { s.classList.toggle("active", k === i); });
    dots.forEach(function (d, k) { d.classList.toggle("on", k === i); });
  }
  root.querySelector(".kimlab-prev").addEventListener("click", function () { show(i - 1); });
  root.querySelector(".kimlab-next").addEventListener("click", function () { show(i + 1); });
  dots.forEach(function (d, k) { d.addEventListener("click", function () { show(k); }); });
  setInterval(function () { show(i + 1); }, 6000);
})();
</script>

<script>
(function () {
  function addBrand() {
    var nav = document.querySelector("#navbar") || document.querySelector("nav.navbar");
    if (!nav) return;
    if (nav.querySelector(".navbar-brand")) return;
    var host = nav.querySelector(".container")
            || nav.querySelector(".container-fluid")
            || nav;
    var a = document.createElement("a");
    a.className = "navbar-brand title font-weight-lighter";
    a.href = "{{ '/' | relative_url }}";
    a.textContent = "{{ site.title | default: 'Kim Lab' }}";
    host.insertBefore(a, host.firstChild);
  }
  if (document.readyState === "loading") {
    document.addEventListener("DOMContentLoaded", addBrand);
  } else {
    addBrand();
  }
})();
</script>
