---
layout: page
permalink: /people/
title: Team
nav: true
nav_order: 2
---
<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap");
/* ===== 탭 이동 시 전체 축 밀림 방지 ===== */
html {
  scrollbar-gutter: stable;
  overflow-y: scroll;
}
body { overflow-x: clip; }
/* Inter 폰트 — 커스텀 클래스까지 명시 */
body, p, li, td, .navbar, .navbar-brand, h1, h2, h3, h4, h5, h6,
.tm-group, .tm-note, .tm-body,
.pi-section, .pi-name, .pi-role, .pi-contact, .pi-adv {
  font-family: "Inter", -apple-system, BlinkMacSystemFont, sans-serif !important;
}
h1, h2, h3, .navbar-brand { font-weight: 700 !important; letter-spacing: -0.02em; }
body { font-weight: 400; letter-spacing: -0.005em; }
/* 네비게이션 */
.navbar .navbar-nav, .navbar ul { margin-left: 2rem !important; margin-right: auto !important; }
.navbar .container, .navbar .container-fluid, .navbar > div { justify-content: flex-start !important; }

/* ============================================================
   위계 1단계 — 대분류 (Principal Investigator / Graduate Students …)
   ============================================================ */
.tm-group {
  font-size: 1.38rem;
  font-weight: 800;
  letter-spacing: -0.025em;
  line-height: 1.2;
  border-top: 1px solid;
  padding-top: 1.15rem;
  margin: 2.6rem 0 1.2rem 0;
  clear: both;
}
.tm-group.first {
  border-top: none;
  padding-top: 0;
  margin-top: 1.6rem;
}
.tm-note {
  font-size: 0.86rem;
  font-style: italic;
  line-height: 1.5;
  margin: -0.5rem 0 0 0;
}

/* ============================================================
   위계 2단계 — 소분류 (Professional Position / Education)
   ============================================================ */
.pi-section {
  font-size: 0.76rem;
  font-weight: 700;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  border-top: 1px solid;
  padding-top: 0.7rem;
  margin: 1.6rem 0 0.55rem 0;
  clear: both;
}

/* ===== PI 헤더: 이름줄 ~ 이메일줄 + 사진 (모바일에서도 같은 배치 유지) ===== */
.pi-header {
  display: flex;
  align-items: stretch;
  justify-content: space-between;
  gap: 2rem;
  margin-bottom: 1.2rem;
}
.pi-header-text {
  flex: 1 1 auto;
  min-width: 0;
}
.pi-photo-wrap {
  flex: 0 0 auto;
  align-self: stretch;
  aspect-ratio: 1 / 1;
  height: auto;
  max-height: 145px;
  min-height: 112px;
  margin-right: 0.5rem;
  border-radius: 50%;
  overflow: hidden;
  background-color: var(--global-bg-color);
}
.pi-photo {
  width: 100%;
  height: 100%;
  display: block;
  object-fit: cover;
  object-position: center 25%;
}
.pi-namerow { display: flex; align-items: center; gap: 0.6rem; margin-bottom: 0.35rem; flex-wrap: wrap; }
.pi-name { font-size: 1.26rem; font-weight: 700; letter-spacing: -0.02em; margin: 0; line-height: 1.2; }
.pi-links { display: flex; align-items: center; gap: 0.5rem; }
.pi-links a {
  font-size: 1.02rem;
  line-height: 1;
  opacity: 0.85;
  transition: opacity 0.15s ease, transform 0.15s ease;
  text-decoration: none;
}
.pi-links a:hover { opacity: 1; transform: translateY(-1px); }
.pi-role { font-size: 0.88rem; line-height: 1.5; margin-bottom: 0.8rem; }
.pi-contact { font-size: 0.86rem; margin-bottom: 0; }
.pi-contact .label { font-weight: 700; display: inline-block; width: 60px; }

/* ===== 이력 표 ===== */
.pi-table { width: 100%; border-collapse: collapse; font-size: 0.86rem; }
.pi-table td { padding: 0.3rem 0; vertical-align: top; border: none; line-height: 1.5; }
.pi-table td.when { width: 155px; font-weight: 600; white-space: nowrap; padding-right: 0.8rem; }
.pi-end { clear: both; }

/* ===== 지도교수 표기 + 링크 ===== */
.pi-adv {
  font-size: 0.78rem;
  font-weight: 400;
  letter-spacing: -0.005em;
  white-space: nowrap;
}
.pi-adv a {
  color: inherit;
  text-decoration: underline;
  text-decoration-thickness: 1px;
  text-underline-offset: 2px;
  text-decoration-color: currentColor;
  transition: color 0.15s ease;
}

/* ===== Open Positions 본문 ===== */
.tm-body { font-size: 0.92rem; line-height: 1.65; }

/* ===== 모바일: 배치는 그대로, 크기만 축소 ===== */
@media (max-width: 700px) {
  .tm-group { font-size: 1.18rem; margin: 2.1rem 0 0.95rem 0; }
  .tm-group.first { margin-top: 1.3rem; }
  /* 사진은 계속 이름·소속 오른쪽에, 텍스트는 왼쪽 정렬 유지 */
  .pi-header { gap: 1rem; margin-bottom: 1rem; }
  .pi-photo-wrap { max-height: 115px; min-height: 82px; margin-right: 0; }
  .pi-name { font-size: 1.1rem; }
  .pi-links a { font-size: 0.95rem; }
  .pi-role { font-size: 0.82rem; line-height: 1.45; margin-bottom: 0.6rem; }
  .pi-contact { font-size: 0.8rem; }
  .pi-contact .label { width: 50px; }
  .pi-table { font-size: 0.8rem; }
  .pi-table td.when { width: 108px; font-size: 0.76rem; padding-right: 0.6rem; }
  .pi-adv { display: block; margin-top: 0.1rem; white-space: normal; font-size: 0.72rem; }
  .tm-body { font-size: 0.89rem; }
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
html[data-theme="light"] .tm-group,
html[data-theme="light"] .pi-name,
html[data-theme="light"] .pi-table td,
html[data-theme="light"] .pi-contact .label,
html[data-theme="light"] .tm-body { color: #191919 !important; }
html[data-theme="light"] .pi-section { color: #8A8A8A !important; }
html[data-theme="light"] .tm-note { color: #9A9A9A !important; }
html[data-theme="light"] .pi-role { color: #5A5A5A !important; }
html[data-theme="light"] .pi-adv { color: #7A7A7A !important; }
html[data-theme="light"] .pi-adv a:hover { color: #651FFF !important; }
html[data-theme="light"] .tm-group { border-top-color: rgba(25,25,25,0.22) !important; }
html[data-theme="light"] .pi-section { border-top-color: rgba(25,25,25,0.10) !important; }
html[data-theme="light"] .pi-links a { color: #651FFF !important; }
html[data-theme="light"] .pi-photo-wrap { background-color: #FCFCFC; }
/* ===== 다크 모드: 색상 ===== */
html[data-theme="dark"] .tm-group,
html[data-theme="dark"] .pi-name,
html[data-theme="dark"] .pi-table td,
html[data-theme="dark"] .pi-contact .label,
html[data-theme="dark"] .tm-body { color: #FCFCFC !important; }
html[data-theme="dark"] .pi-section { color: #909090 !important; }
html[data-theme="dark"] .tm-note { color: #7F7F7F !important; }
html[data-theme="dark"] .pi-role { color: #B5B5B5 !important; }
html[data-theme="dark"] .pi-adv { color: #8F8F8F !important; }
html[data-theme="dark"] .pi-adv a:hover { color: #86CFDA !important; }
html[data-theme="dark"] .tm-group { border-top-color: rgba(252,252,252,0.42) !important; }
html[data-theme="dark"] .pi-section { border-top-color: rgba(252,252,252,0.18) !important; }
html[data-theme="dark"] .pi-links a { color: #86CFDA !important; }
html[data-theme="dark"] .pi-photo-wrap { background-color: #1F1F1F; }
</style>

<div class="tm-group first">Principal Investigator</div>

<div class="pi-header">
  <div class="pi-header-text">
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
  </div>
  <div class="pi-photo-wrap">
    <img class="pi-photo" src="{{ '/assets/img/prof_pic.jpg' | relative_url }}" alt="Jihyun Kim">
  </div>
</div>

<div class="pi-section">Professional Position</div>
<table class="pi-table">
  <tr>
    <td class="when">2026.09 – Present</td>
    <td>Assistant Professor, Department of Intelligent Semiconductor Engineering, Ajou University, Republic of Korea</td>
  </tr>
  <tr>
    <td class="when">2025.09 – 2026.08</td>
    <td>Postdoctoral Fellow, Research Laboratory of Electronics, Massachusetts Institute of Technology, United States
      <span class="pi-adv">(Advisor: <a href="https://sites.google.com/view/scheema/home" target="_blank" rel="noopener noreferrer">Prof. Suraj Cheema</a>)</span></td>
  </tr>
  <tr>
    <td class="when">2025.03 – 2025.08</td>
    <td>Postdoctoral Fellow, Department of Chemical and Biomolecular Engineering, Yonsei University, Republic of Korea
      <span class="pi-adv">(Advisor: <a href="https://sites.google.com/yonsei.ac.kr/mfmp/home" target="_blank" rel="noopener noreferrer">Prof. Joohoon Kang</a>)</span></td>
  </tr>
</table>

<div class="pi-section">Education</div>
<table class="pi-table">
  <tr>
    <td class="when">2019.03 – 2025.02</td>
    <td>M.S. &amp; Ph.D., Department of Advanced Materials Science and Engineering, Sungkyunkwan University, Republic of Korea
      <span class="pi-adv">(Advisor: <a href="https://sites.google.com/yonsei.ac.kr/mfmp/home" target="_blank" rel="noopener noreferrer">Prof. Joohoon Kang</a>)</span></td>
  </tr>
  <tr>
    <td class="when">2013.03 – 2019.02</td>
    <td>B.S., School of Chemical Engineering, Sungkyunkwan University, Republic of Korea</td>
  </tr>
</table>

<div class="pi-end"></div>

<div class="tm-group">Graduate Students</div>
<div class="tm-note">Recruiting — see Open Positions below.</div>

<div class="tm-group">Undergraduate Researchers</div>
<div class="tm-note">Recruiting — see Open Positions below.</div>

<div class="tm-group">Open Positions</div>

<div class="tm-body">
Kim Lab is recruiting <strong>graduate students</strong> (M.S. / Ph.D.) and <strong>undergraduate interns</strong> starting September 2026. We welcome students with backgrounds in materials science, chemical engineering, electrical engineering, chemistry, or physics — and, more importantly, a willingness to learn what they do not yet know.
</div>
