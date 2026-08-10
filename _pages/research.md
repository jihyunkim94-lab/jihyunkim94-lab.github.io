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

html[data-theme="light"] .pi-section, html[data-theme="light"] .pi-body { color: #191919 !important; }
html[data-theme="light"] .pi-section { border-top-color: rgba(25,25,25,0.12) !important; }

/* 다크 모드 */
html[data-theme="dark"] .pi-section, html[data-theme="dark"] .pi-body { color: #FCFCFC !important; }
html[data-theme="dark"] .pi-section { border-top-color: rgba(252,252,252,0.18) !important; }

/* 공통 섹션 스타일 */
.pi-section { font-size: 1.05rem; font-weight: 700; letter-spacing: -0.02em; border-top: 1px solid; padding-top: 0.9rem; margin: 1.6rem 0 0.7rem 0; }
.pi-body { font-size: 0.92rem; line-height: 1.65; margin-bottom: 0.5rem; }
.pi-lead { font-size: 1rem; line-height: 1.65; margin-bottom: 0.5rem; }
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
