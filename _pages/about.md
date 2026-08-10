---
layout: about
title: about
permalink: /
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

body, p, li, a, span, .navbar, .navbar-brand, h1, h2, h3, h4, h5, h6 {
  font-family: "Inter", -apple-system, BlinkMacSystemFont, sans-serif !important;
}
h1, h2, h3, .navbar-brand { font-weight: 700 !important; letter-spacing: -0.02em; }
body { font-weight: 400; letter-spacing: -0.005em; }

html[data-theme="light"] {
  --global-theme-color: #651FFF;
  --global-hover-color: #651FFF;
  --global-divider-color: rgba(101, 31, 255, 0.15);
  --global-bg-color: #FCFCFC;
  background-color: #FCFCFC;
}
html[data-theme="light"] body { background-color: #FCFCFC; }
html[data-theme="light"] a,
html[data-theme="light"] a:hover,
html[data-theme="light"] .navbar .nav-item.active .nav-link { color: #651FFF !important; }

.kimlab-slider { float: right; width: 300px; max-width: 100%; margin: -100px 0 1.5rem 2rem; }
.kimlab-slide { display: none; }
.kimlab-slide.active { display: block; }
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
@media (max-width: 768px) { .kimlab-slider { float: none; width: 100%; max-width: 320px; margin: 0 auto 1.5rem auto; } }
</style>

<div class="kimlab-slider">
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

  <div class="kimlab-nav">
    <button class="kimlab-btn kimlab-prev" aria-label="previous">&#8249;</button>
    <div class="kimlab-dots">
      <span class="kimlab-dot on"></span><span class="kimlab-dot"></span><span class="kimlab-dot"></span><span class="kimlab-dot"></span><span class="kimlab-dot"></span>
    </div>
    <button class="kimlab-btn kimlab-next" aria-label="next">&#8250;</button>
  </div>
</div>

Kim Lab designs materials at the **atomic scale** and engineers them into **scalable, reproducible platforms** for next-generation electronics.

Our guiding question: how do we translate control at the level of individual atomic layers into materials that can be made reliably, repeatedly, and at scale — and what device architectures become possible once we can? Answering it means working across materials characterizations, thin-film engineering, and device physics.

We are always looking for curious students who want to build things that do not exist yet.

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
