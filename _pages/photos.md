---
layout: page
permalink: /photos/
title: Photos
description:
nav: true
nav_order: 6
---
<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap");
body, p, li, td, .navbar, .navbar-brand, h1, h2, h3, h4, h5, h6 {
  font-family: "Inter", -apple-system, BlinkMacSystemFont, sans-serif !important;
}
h1, h2, h3, .navbar-brand { font-weight: 700 !important; letter-spacing: -0.02em; }
body { font-weight: 400; letter-spacing: -0.005em; }
/* ===== 탭 이동 시 전체 축 밀림 방지 — 스크롤바 폭 항상 예약 ===== */
html {
  scrollbar-gutter: stable;
  overflow-y: scroll;
}
body { overflow-x: clip; }
/* 긴 캡션이 컨테이너를 넘기지 않도록 */
.ph-item figcaption { overflow-wrap: break-word; word-break: break-word; }
/* 네비게이션 */
.navbar .navbar-nav, .navbar ul { margin-left: 2rem !important; margin-right: auto !important; }
.navbar .container, .navbar .container-fluid, .navbar > div { justify-content: flex-start !important; }
/* ===== 테마 공통: 크기 / 레이아웃 ===== */
/* 연도 헤딩 — Publications 연도 헤딩과 동일 규격 */
.ph-year {
  font-size: 1.5rem;
  font-weight: 700;
  letter-spacing: -0.02em;
  border-top: 1px solid var(--line-color);
  padding-top: 0.9rem;
  margin: 1.2rem 0 0.9rem 0;
  clear: both;
}
.ph-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(210px, 1fr));
  gap: 1.1rem;
  margin-bottom: 0.5rem;
}
/* 사진이 한 장뿐인 해 — 썸네일처럼 작게 놓이지 않도록 크게 */
.ph-grid:has(> .ph-item:only-child) {
  grid-template-columns: minmax(0, 560px);
}
/* 사진이 두 장인 해 — 지나치게 커지지 않게 상한 */
.ph-grid:has(> .ph-item:nth-child(2):last-child) {
  grid-template-columns: repeat(2, minmax(0, 340px));
}
/* YAML 에서 wide: true 를 준 사진은 두 칸 차지 */
.ph-item.is-wide { grid-column: span 2; }

.ph-item { margin: 0; }
.ph-item img {
  width: 100%;
  aspect-ratio: 4 / 3;          /* YAML의 ratio 값이 있으면 그것으로 덮어씀 */
  object-fit: cover;
  object-position: center;
  border-radius: 8px;
  display: block;
  cursor: zoom-in;
  transition: transform 0.25s ease, box-shadow 0.25s ease;
}
.ph-item img:hover {
  transform: translateY(-3px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.14);
}
.ph-item figcaption { font-size: 0.78rem; line-height: 1.45; margin-top: 0.55rem; }
.ph-item .ph-cap { display: block; font-weight: 600; }
.ph-item .ph-date { display: block; opacity: 0.65; font-size: 0.72rem; margin-top: 2px; }
.ph-empty { font-size: 0.88rem; opacity: 0.5; font-style: italic; margin-top: 1rem; }
/* 확대 보기 */
.ph-lightbox {
  position: fixed;
  inset: 0;
  z-index: 9999;
  display: none;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  gap: 0.9rem;
  padding: 2.5rem;
  background: rgba(0, 0, 0, 0.88);
  cursor: zoom-out;
}
.ph-lightbox.on { display: flex; }
.ph-lightbox .ph-lb-img {
  max-width: 92vw;
  max-height: 78vh;
  object-fit: contain;
  border-radius: 4px;
}
.ph-lightbox .ph-lb-cap {
  color: #FCFCFC;
  font-size: 0.84rem;
  text-align: center;
  max-width: 60ch;
  line-height: 1.5;
}
.ph-lightbox .ph-lb-close {
  position: absolute;
  top: 1rem;
  right: 1.4rem;
  color: #FCFCFC;
  font-size: 1.8rem;
  line-height: 1;
  background: none;
  border: none;
  cursor: pointer;
  opacity: 0.7;
}
.ph-lightbox .ph-lb-close:hover { opacity: 1; }
@media (max-width: 700px) {
  .ph-year { font-size: 1.3rem; }
  .ph-grid { grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); gap: 0.8rem; }
  .ph-grid:has(> .ph-item:only-child),
  .ph-grid:has(> .ph-item:nth-child(2):last-child) { grid-template-columns: minmax(0, 1fr); }
  .ph-item.is-wide { grid-column: span 1; }
}
@media (prefers-reduced-motion: reduce) {
  .ph-item img { transition: none; }
}
/* ===== 라이트 모드: 색상 ===== */
html[data-theme="light"] {
  /* 연도 · 연도 구분선 밝기 (이 두 줄만 조절) */
  --year-color: rgba(25, 25, 25, 0.45);
  --line-color: rgba(25, 25, 25, 0.26);
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
html[data-theme="light"] .ph-item .ph-cap { color: #191919 !important; }
html[data-theme="light"] .ph-item .ph-date { color: #5A5A5A !important; }
html[data-theme="light"] .ph-year { color: var(--year-color) !important; }
html[data-theme="light"] .ph-year { border-top-color: var(--line-color) !important; }
/* ===== 다크 모드: 색상 ===== */
html[data-theme="dark"] {
  /* 연도 · 연도 구분선 밝기 (이 두 줄만 조절) */
  --year-color: rgba(252, 252, 252, 0.62);
  --line-color: rgba(252, 252, 252, 0.38);
}
html[data-theme="dark"] .ph-item .ph-cap { color: #FCFCFC !important; }
html[data-theme="dark"] .ph-item .ph-date { color: #B5B5B5 !important; }
html[data-theme="dark"] .ph-year { color: var(--year-color) !important; }
html[data-theme="dark"] .ph-year { border-top-color: var(--line-color) !important; }
html[data-theme="dark"] .ph-item img:hover { box-shadow: 0 8px 24px rgba(0, 0, 0, 0.5); }
</style>
{% assign gallery = site.data.gallery %}
{% if gallery and gallery.size > 0 %}
  {% assign photos = gallery | sort: "date" | reverse %}
  {% assign years = photos | group_by_exp: "p", "p.date | date: '%Y'" %}
  {% for yr in years %}
  <div class="ph-year">{{ yr.name }}</div>
  <div class="ph-grid">
    {% for p in yr.items %}
    <figure class="ph-item{% if p.wide %} is-wide{% endif %}">
      <img src="{{ '/assets/img/gallery/' | append: p.image | relative_url }}"
           alt="{{ p.caption | default: 'Kim Lab photo' }}"
           data-caption="{{ p.caption }}"
           {% if p.ratio or p.focus %}style="{% if p.ratio %}aspect-ratio: {{ p.ratio }};{% endif %}{% if p.focus %}object-position: {{ p.focus }};{% endif %}"{% endif %}
           loading="lazy">
      <figcaption>
        {% if p.caption %}<span class="ph-cap">{{ p.caption }}</span>{% endif %}
        {% if p.date %}<span class="ph-date">{{ p.date | date: "%b %d, %Y" }}</span>{% endif %}
      </figcaption>
    </figure>
    {% endfor %}
  </div>
  {% endfor %}
{% else %}
  <div class="ph-empty">Photos coming soon.</div>
{% endif %}
<div class="ph-lightbox" id="phLightbox">
  <button class="ph-lb-close" type="button" aria-label="close">&times;</button>
  <img class="ph-lb-img" src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" alt="">
  <div class="ph-lb-cap"></div>
</div>
<script>
(function () {
  var box = document.getElementById("phLightbox");
  if (!box) return;
  var boxImg = box.querySelector(".ph-lb-img");
  var boxCap = box.querySelector(".ph-lb-cap");
  var blank = boxImg.getAttribute("src");
  document.querySelectorAll(".ph-item img").forEach(function (img) {
    img.addEventListener("click", function () {
      boxImg.src = img.src;
      boxImg.alt = img.alt;
      boxCap.textContent = img.dataset.caption || "";
      box.classList.add("on");
      document.body.style.overflow = "hidden";
    });
  });
  function close() {
    box.classList.remove("on");
    boxImg.src = blank;
    document.body.style.overflow = "";
  }
  box.addEventListener("click", close);
  document.addEventListener("keydown", function (e) {
    if (e.key === "Escape" && box.classList.contains("on")) close();
  });
})();
</script>
