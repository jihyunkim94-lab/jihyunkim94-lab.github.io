---
layout: page
permalink: /people/
title: Team
description: Members of Kim Lab
nav: true
nav_order: 2
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
/* 사진 크기·위치는 아래 변수 3개만 조절하면 됩니다 */
.pi-photo-wrap {
  --pi-size: 160px;      /* 사진 지름 */
  --pi-zoom: 1;          /* 1.1 = 확대(더 잘림), 0.9 = 축소(여백 생김) */
  --pi-pos: center 25%;  /* 머리가 잘리면 20% → 15% 로 낮추기 */

  float: right;
  width: var(--pi-size);
  height: var(--pi-size);
  margin: 0 0.5rem 1.5rem 2rem;
  border-radius: 50%;
  overflow: hidden;
  background-color: var(--global-bg-color);
}
.pi-photo {
  width: 100%;
  height: 100%;
  display: block;
  object-fit: cover;
  object-position: var(--pi-pos);
  transform: scale(var(--pi-zoom));
  transform-origin: center 30%;
}
.pi-namerow { display: flex; align-items: center; gap: 0.65rem; margin-bottom: 0.4rem; }
.pi-name { font-size: 1.6rem; font-weight: 700; letter-spacing: -0.02em; margin: 0; line-height: 1.2; }
.pi-links { display: flex; align-items: center; gap: 0.55rem; }
.pi-links a {
  font-size: 1.15rem;
  line-height: 1;
  opacity: 0.85;
  transition: opacity 0.15s ease, transform 0.15s ease;
  text-decoration: none;
}
.pi-links a:hover { opacity: 1; transform: translateY(-1px); }
.pi-role { font-size: 0.9rem; line-height: 1.5; margin-bottom: 0.9rem; }
.pi-contact { font-size: 0.88rem; margin-bottom: 1.2rem; }
.pi-contact .label { font-weight: 700; display: inline-block; width: 60px; }
.pi-section { font-size: 1.05rem; font-weight: 700; letter-spacing: -0.02em; border-top: 1px solid; padding-top: 0.9rem; margin: 1.4rem 0 0.7rem 0; clear: none; }
.pi-table { width: 100%; border-collapse: collapse; font-size: 0.86rem; }
.pi-table td { padding: 0.28rem 0; vertical-align: top; border: none; }
.pi-table td.when { width: 155px; font-weight: 600; white-space: nowrap; padding-right: 0.8rem; }
.pi-end { clear: both; }
.pi-placeholder { font-size: 0.88rem; opacity: 0.5; font-style: italic; margin-bottom: 2.5rem; }
@media (max-width: 700px) {
  .pi-photo-wrap { --pi-size: 140px; float: none; margin: 0 0 1rem 0; }
  .pi-table td.when { width: 120px; font-size: 0.8rem; }
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
html[data-theme="light"] p a, html[data-theme="light"] li a { color: #651FFF !important; }
html[data-theme="light"] .pi-name,
html[data-theme="light"] .pi-section,
html[data-theme="light"] .pi-table td,
html[data-theme="light"] .pi-contact .label { color: #191919 !important; }
html[data-theme="light"] .pi-role { color: #5A5A5A !important; }
html[data-theme="light"] .pi-section { border-top-color: rgba(25,25,25,0.12) !important; }
html[data-theme="light"] .pi-links a { color: #651FFF !important; }
html[data-theme="light"] .pi-photo-wrap { background-color: #FCFCFC; }
/* ===== 다크 모드: 색상 ===== */
html[data-theme="dark"] .pi-name,
html[data-theme="dark"] .pi-section,
html[data-theme="dark"] .pi-table td,
html[data-theme="dark"] .pi-contact .label { color: #FCFCFC !important; }
html[data-theme="dark"] .pi-role { color: #B5B5B5 !important; }
html[data-theme="dark"] .pi-section { border-top-color: rgba(252,252,252,0.28) !important; }
html[data-theme="dark"] .pi-links a { color: #86CFDA !important; }
html[data-theme="dark"] .pi-photo-wrap { background-color: #1F1F1F; }
</style>
<div class="pi-photo-wrap">
  <img class="pi-photo" src="{{ '/assets/img/prof_pic.jpg' | relative_url }}" alt="Jihyun Kim">
</div>
<div class="pi-namerow">
  <span class="pi-name">Jihyun Kim, Ph.D.</span>
  <span class="pi-links">
    <a href="{{ '/assets/pdf/CV_JIHYUN_KIM.pdf' | relative_url }}" target="_blank" title="Curriculum Vitae"><i class="ai ai-cv"></i></a>
    <a href="https://scholar.google.com/citations?hl=ko&user=68-RYuUAAAAJ" target="_blank" title="Google Scholar"><i class="ai ai-google-scholar"></i></a>
  </span>
</div>
<div class="pi-role">
  Assistant Professor<br>
  Dept. of Intelligent Semiconductor Engineering, Ajou University
</div>
<div class="pi-contact">
  <span class="label">Email</span> <a href="mailto:jhkim94@mit.edu">jhkim94@mit.edu</a>
</div>
<div class="pi-section">Professional Position</div>
<table class="pi-table">
  <tr>
    <td class="when">2026.09 – Present</td>
    <td>Assistant Professor, Department of Intelligent Semiconductor Engineering, Ajou University, Republic of Korea</td>
  </tr>
  <tr>
    <td class="when">2025.09 – 2026.08</td>
    <td>Postdoctoral Fellow, Research Laboratory of Electronics, Massachusetts Institute of Technology, United States</td>
  </tr>
  <tr>
    <td class="when">2025.03 – 2025.08</td>
    <td>Postdoctoral Fellow, Department of Chemical and Biomolecular Engineering, Yonsei University, Republic of Korea</td>
  </tr>
</table>
<div class="pi-section">Education</div>
<table class="pi-table">
  <tr>
    <td class="when">2019.03 – 2025.02</td>
    <td>M.S. &amp; Ph.D., Department of Advanced Materials Science and Engineering, Sungkyunkwan University, Republic of Korea</td>
  </tr>
  <tr>
    <td class="when">2013.03 – 2019.02</td>
    <td>B.S., School of Chemical Engineering, Sungkyunkwan University, Republic of Korea</td>
  </tr>
</table>
<div class="pi-end"></div>
<div class="pi-section">Graduate Students</div>
<div class="pi-placeholder">Joining September 2026.</div>
<div class="pi-section">Undergraduate Researchers</div>
<div class="pi-placeholder">Joining September 2026.</div>
<div class="pi-section">Open Positions</div>
Kim Lab is recruiting **graduate students** (M.S. / Ph.D.) and **undergraduate interns** starting September 2026. We welcome students with backgrounds in materials science, chemical engineering, electrical engineering, chemistry, or physics — and, more importantly, a willingness to learn what they do not yet know.
