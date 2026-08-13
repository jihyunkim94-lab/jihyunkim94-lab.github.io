---
layout: page
permalink: /photos/
title: Photos
description: Life at Kim Lab
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
/* 네비게이션 */
.navbar .navbar-nav, .navbar ul { margin-left: 2rem !important; margin-right: auto !important; }
.navbar .container, .navbar .container-fluid, .navbar > div { justify-content: flex-start !important; }
/* ===== 테마 공통: 크기 / 레이아웃 ===== */
.ph-year {
  font-size: 1.05rem;
  font-weight: 700;
  letter-spacing: -0.02em;
  border-top: 1px solid;
  padding-top: 0.9rem;
  margin: 1.6rem 0 0.9rem 0;
}
.ph-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(210px, 1fr));
  gap: 1.1rem;
  margin-bottom: 0.5rem;
}
.ph-item { margin: 0; }
.ph-item img {
  width: 100%;
  aspect-ratio: 4 / 3;
  object-fit: cover;
  border-radius: 6px;
  display: block;
  cursor: zoom-in;
  transition: transform 0.2s ease, opacity 0.2s ease;
}
.ph-item img:hover { transform: translateY(-2px); opacity: 0.92; }
.ph-item figcaption { font-size: 0.78rem; line-height: 1.4; margin-top: 0.45rem; }
.ph-item .ph-cap { display: block; font-weight: 600; }
.ph-item .ph-date { display: block; opacity: 0.65; font-size: 0.72rem; margin-top: 1px; }
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
  .ph-grid { grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); gap: 0.8rem; }
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
html[data-theme="light"] h4, html[data-theme="light"] h5, html[data-theme="light"] h6,
html[data-theme="light"] .post-title { color: #191919 !important; }
html[data-theme="light"] .ph-year,
html[data-theme="light"] .ph-item .ph-cap { color: #191919 !important; }
html[data-theme="light"] .ph-item .ph-date { color: #5A5A5A !important; }
html[data-theme="light"] .ph-year { border-top-color: rgba(25,25,25,0.12) !important; }
/* ===== 다크 모드: 색상 ===== */
html[data-theme="dark"] .ph-year,
html[data-theme="dark"] .ph-item .ph-cap { color: #FCFCFC !important; }
html[data-theme="dark"] .ph-item .ph-date { color: #B5B5B5 !important; }
html[data-theme="dark"] .ph-year { border-top-color: rgba(252,252,252,0.28) !important; }
</style>

{% assign gallery = site.data.gallery %}
{% if gallery and gallery.size > 0 %}
  {% assign photos = gallery | sort: "date" | reverse %}
  {% assign years = photos | group_by_exp: "p", "p.date | date: '%Y'" %}
  {% for yr in years %}
  <div class="ph-year">{{ yr.name }}</div>
  <div class="ph-grid">
    {% for p in yr.items %}
    <figure class="ph-item">
      <img src="{{ '/assets/img/gallery/' | append: p.image | relative_url }}"
           alt="{{ p.caption | default: 'Kim Lab photo' }}"
           data-caption="{{ p.caption }}"
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
