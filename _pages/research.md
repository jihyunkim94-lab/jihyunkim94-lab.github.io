---
layout: page
permalink: /research/
title: Research
nav: true
nav_order: 3
---
<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap");
body, p, li, td, .navbar, .navbar-brand, h1, h2, h3, h4, h5, h6 {
  font-family: "Inter", -apple-system, BlinkMacSystemFont, sans-serif !important;
}
h1, h2, h3, .navbar-brand { font-weight: 700 !important; letter-spacing: -0.02em; }
body { font-weight: 400; letter-spacing: -0.005em; }

/* ===== ① 탭 이동 시 전체 축 밀림 방지 — 스크롤바 폭 항상 예약 =====
   페이지 길이에 따라 스크롤바가 생기거나 사라지면서
   컨테이너가 좌우로 약 7~8px 튀는 현상을 없앤다.
   (6개 탭 전부 동일 블록 사용)                                   */
html {
  scrollbar-gutter: stable;      /* 최신 브라우저 */
  overflow-y: scroll;            /* 구형 브라우저 폴백 */
}
body { overflow-x: clip; }       /* 가로 스크롤바로 인한 밀림 방지 */

/* 긴 문장·URL이 컨테이너를 넘기지 않도록 */
.pi-lead, .pi-body { overflow-wrap: break-word; word-break: break-word; }

/* 네비게이션 */
.navbar .navbar-nav, .navbar ul { margin-left: 2rem !important; margin-right: auto !important; }
.navbar .container, .navbar .container-fluid, .navbar > div { justify-content: flex-start !important; }
/* ===== 테마 공통: 크기 / 레이아웃 ===== */
.pi-lead {
  font-size: 1rem;
  line-height: 1.65;
  margin-bottom: 0.5rem;
}
.pi-section {
  font-size: 1.05rem;
  font-weight: 700;
  letter-spacing: -0.02em;
  border-top: 1px solid var(--line-color);
  padding-top: 0.9rem;
  margin: 1.6rem 0 0.7rem 0;
  clear: both;
}
.pi-body {
  font-size: 0.92rem;
  line-height: 1.65;
  margin-bottom: 0.5rem;
}
.pi-end { clear: both; }
@media (max-width: 700px) {
  .pi-lead { font-size: 0.95rem; }
  .pi-body { font-size: 0.88rem; }
}
/* ===== 라이트 모드: 색상 ===== */
html[data-theme="light"] {
  /* 헤딩 · 구분선 밝기 (이 두 줄만 조절) */
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
html[data-theme="light"] .pi-section { color: #191919 !important; }
html[data-theme="light"] .pi-lead { color: #191919 !important; }
html[data-theme="light"] .pi-body { color: #5A5A5A !important; }
html[data-theme="light"] .pi-body a { color: #651FFF !important; }
html[data-theme="light"] .pi-section { border-top-color: var(--line-color) !important; }
/* ===== 다크 모드: 색상 ===== */
html[data-theme="dark"] {
  /* 헤딩 · 구분선 밝기 (이 두 줄만 조절) */
  --year-color: rgba(252, 252, 252, 0.62);
  --line-color: rgba(252, 252, 252, 0.38);
}
html[data-theme="dark"] .pi-section { color: #FCFCFC !important; }
html[data-theme="dark"] .pi-lead { color: #FCFCFC !important; }
html[data-theme="dark"] .pi-body { color: #B5B5B5 !important; }
html[data-theme="dark"] .pi-body a { color: #86CFDA !important; }
html[data-theme="dark"] .pi-section { border-top-color: var(--line-color) !important; }
</style>

<div class="pi-lead">
We build materials from the atomic scale up, and turn them into device platforms that can be manufactured reproducibly and at scale.
</div>

<div class="pi-section">Solution-Processed 2D van der Waals Materials</div>

<div class="pi-body">
Electrochemically exfoliated nanosheets are formulated into stable inks and assembled into percolated network films. Slot-die printing, direct photopatterning, and orthogonal solvent chemistry allow wafer-scale vertical heterostructures to be built without mechanical transfer or vacuum deposition — the core of the V-PRIME platform.
</div>

<div class="pi-section">Atomic-Scale Dielectrics</div>

<div class="pi-body">
Sub-stoichiometric, high-k, and ferroelectric oxides engineered at the few-nanometer scale serve as the gate and capacitor layers of next-generation devices. Controlling stoichiometry and interface chemistry at this scale is what makes reconfigurable logic, DRAM, and low-power memory possible.
</div>

<div class="pi-section">Emerging Device Platforms</div>

<div class="pi-body">
Transistors, capacitors, optoelectronic synapses, and retina-inspired sensor arrays built from the materials above — aimed at in-sensor computing, neuromorphic architectures, and multivalued logic.
</div>

<div class="pi-end"></div>
