---
layout: page
permalink: /research/
title: Research
nav: true
nav_order: 3
---

{% raw %}
<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap");
/* Prevent horizontal shift between tabs: always reserve scrollbar width */
html {
  scrollbar-gutter: stable;
  overflow-y: scroll;
}
body { overflow-x: clip; }
/* Inter font, declared explicitly on custom classes */
body, p, li, td, .navbar, .navbar-brand, h1, h2, h3, h4, h5, h6,
.rs-sec, .rs-lede, .rs-prose, .rs-refs, .rs-refnote, .rs-fig {
  font-family: "Inter", -apple-system, BlinkMacSystemFont, sans-serif !important;
}
h1, h2, h3, .navbar-brand { font-weight: 700 !important; letter-spacing: -0.02em; }
body { font-weight: 400; letter-spacing: -0.005em; }
/* Navigation */
.navbar .navbar-nav, .navbar ul { margin-left: 2rem !important; margin-right: auto !important; }
.navbar .container, .navbar .container-fluid, .navbar > div { justify-content: flex-start !important; }

/* Hierarchy, matched to the Team page
   1. group heading  h2.rs-sec   1.38rem / 800   = Team .tm-group
   2. body           .rs-prose p 0.92rem         = Team .tm-body
   3. references     .rs-refs    0.80rem grey    = Team .pi-adv          */
h2.rs-sec {
  font-size: 1.38rem !important;
  font-weight: 800 !important;
  letter-spacing: -0.025em;
  line-height: 1.2;
  border-top: 1px solid;
  padding-top: 1.15rem;
  margin: 2.6rem 0 1.2rem 0;
  clear: both;
}
h2.rs-sec.first {
  border-top: none;
  padding-top: 0;
  margin-top: 1.6rem;
}
h2.rs-sec .num {
  font-size: 0.82em;
  font-weight: 800;
  font-variant-numeric: tabular-nums;
  letter-spacing: 0.02em;
  margin-right: 0.6em;
}

/* ===== 섹션 삽화 =====
   크기는 .rs-fig 의 width 하나로 조절한다 (160~220px 권장).
   원형으로 바꾸려면
     .rs-fig { border-radius: 50%; }
     .rs-fig img { aspect-ratio: 1 / 1; object-fit: cover; }
   단, 좌우가 잘리므로 권하지는 않음.                              */
.rs-fig {
  float: right;
  width: 190px;
  margin: 0.15rem 0 1rem 1.7rem;
  border-radius: 10px;
  overflow: hidden;
  line-height: 0;
}
.rs-fig img {
  width: 100%;
  height: auto;
  display: block;
}
.rs-fig figcaption {
  font-size: 0.68rem;
  line-height: 1.4;
  letter-spacing: 0.01em;
  padding: 0.45rem 0.1rem 0;
}

/* Body text */
.rs-lede {
  font-size: 0.92rem !important;
  font-weight: 500;
  line-height: 1.65;
  margin: 0 0 1rem 0;
}
.rs-prose p {
  font-size: 0.92rem;
  line-height: 1.65;
  margin: 0 0 1rem 0;
}
.rs-prose sup { font-size: 0.68em; line-height: 0; }
.rs-prose sup a {
  text-decoration: none;
  font-variant-numeric: tabular-nums;
  font-weight: 600;
  padding: 0 0.05em;
}
.rs-prose sup a:hover { text-decoration: underline; }

/* References */
.rs-refnote {
  font-size: 0.76rem;
  line-height: 1.5;
  margin: -0.5rem 0 0.8rem 0;
}
ol.rs-refs {
  margin: 0;
  padding-left: 1.5em;
  font-size: 0.8rem;
  line-height: 1.6;
}
ol.rs-refs li {
  margin-bottom: 0.5em;
  scroll-margin-top: 5rem;
}
ol.rs-refs .self { font-weight: 700; }
ol.rs-refs .eq { font-size: 0.85em; vertical-align: super; line-height: 0; }

@media (max-width: 700px) {
  h2.rs-sec { font-size: 1.18rem !important; margin: 2.1rem 0 0.95rem 0; }
  h2.rs-sec.first { margin-top: 1.3rem; }
  .rs-lede, .rs-prose p { font-size: 0.89rem; }
  ol.rs-refs { font-size: 0.76rem; }
  .rs-refnote { font-size: 0.73rem; }
  .rs-fig {
    float: none;
    width: 100%;
    max-width: 260px;
    margin: 0.4rem auto 1.2rem auto;
  }
  .rs-fig figcaption { text-align: center; }
}

/* Light theme */
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
html[data-theme="light"] h2.rs-sec { color: #191919 !important; border-top-color: rgba(25,25,25,0.22) !important; }
html[data-theme="light"] h2.rs-sec .num { color: #651FFF !important; }
html[data-theme="light"] .rs-lede,
html[data-theme="light"] .rs-prose p { color: #191919 !important; }
html[data-theme="light"] .rs-prose sup a { color: #651FFF !important; }
html[data-theme="light"] ol.rs-refs,
html[data-theme="light"] .rs-refnote,
html[data-theme="light"] .rs-fig figcaption { color: #7A7A7A !important; }
html[data-theme="light"] ol.rs-refs .self { color: #191919 !important; }
html[data-theme="light"] .rs-fig { background-color: #F2F2F2; }
/* Dark theme */
html[data-theme="dark"] h2.rs-sec { color: #FCFCFC !important; border-top-color: rgba(252,252,252,0.42) !important; }
html[data-theme="dark"] h2.rs-sec .num { color: #86CFDA !important; }
html[data-theme="dark"] .rs-lede,
html[data-theme="dark"] .rs-prose p { color: #FCFCFC !important; }
html[data-theme="dark"] .rs-prose sup a { color: #86CFDA !important; }
html[data-theme="dark"] ol.rs-refs,
html[data-theme="dark"] .rs-refnote,
html[data-theme="dark"] .rs-fig figcaption { color: #8F8F8F !important; }
html[data-theme="dark"] ol.rs-refs .self { color: #FCFCFC !important; }
html[data-theme="dark"] .rs-fig { background-color: #232323; }
</style>
{% endraw %}

<div class="rs-prose">
  <h2 class="rs-sec first">Vision</h2>
  <p class="rs-lede">Computing is spreading from the Internet of Things toward an Internet of Everything, and silicon cannot follow it everywhere. A silicon chip takes long time and enormous cost to bring into production, and it has to be built on a rigid surface &mdash; a poor fit for surfaces that bend, or for devices meant to be ubiquitous and item-level customer electronics.</p>
  <p>We build the technology that fills that gap: low-cost, high-performance electronics and intelligent sensors that can be made quickly, over large areas, and on almost any surface. Our approach starts with the material and works upward, in three stages.</p>

  <h2 class="rs-sec"><span class="num">01</span>Design the material</h2>
  <figure class="rs-fig">
    <img src="{{ '/assets/img/01-material.png' | relative_url }}" alt="Solution-processed van der Waals inks and layered building blocks" loading="lazy">
    <figcaption>Conductor, semiconductor, and insulator inks as building blocks.</figcaption>
  </figure>
  <p>Every electronic device is built from three kinds of materials: conductors that carry current, semiconductors that switch it, and insulators that block it. We design and synthesize all three ourselves as nanomaterials, and our goal is to engineer their properties at the atomic scale.</p>
  <p>For example, controlling the stoichiometry, ion incorporation, and composition of a dielectric layer<sup><a href="#r1">1</a>&ndash;<a href="#r3">3</a></sup>, or the defect density and heterojunction design of a semiconducting channel<sup><a href="#r4">4</a>,<a href="#r5">5</a></sup>, lets us tune the electrical and optical characteristics of the material itself. We are now extending this design space toward finer control &mdash; over local composition, crystalline phase, and the interfaces between layers &mdash; in order to develop exotic material properties that conventional thin films do not offer.</p>

  <h2 class="rs-sec"><span class="num">02</span>Make it at scale</h2>
  <figure class="rs-fig">
    <img src="{{ '/assets/img/02-scale.png' | relative_url }}" alt="Wafer-scale photopatterned van der Waals thin films" loading="lazy">
    <figcaption>Photopatterned films across a full wafer.</figcaption>
  </figure>
  <p>A material is only useful if it can be produced uniformly and reproducibly across an entire wafer. To achieve this, we first disperse atomically thin (van der Waals) materials into high-quality inks with a variety of electronic properties<sup><a href="#r5">5</a></sup>. These inks can be integrated into a range of solution-based processes, including spin-coating, slot-die printing, and inkjet printing<sup><a href="#r2">2</a>,<a href="#r6">6</a></sup>, which makes the platform low-cost and scalable, with deposition completed across a full wafer in a matter of seconds. Together, these steps let us produce high-quality van der Waals thin films over wafer-scale areas.</p>
  <p>Printing covers flat surfaces well, and some applications additionally require integration into three-dimensional structures, capacitors being one example. For these, we use atomic layer deposition to grow the designed material one atomic layer at a time, so that it conforms to deep, high-aspect-ratio trenches<sup><a href="#r3">3</a></sup>. Printing for planar, large-area integration and ALD for three-dimensional integration together provide the process building blocks that a printed electronics platform requires.</p>

  <h2 class="rs-sec"><span class="num">03</span>Build the device</h2>
  <figure class="rs-fig">
    <img src="{{ '/assets/img/03-device.png' | relative_url }}" alt="Transistor arrays and a graphene channel device" loading="lazy">
    <figcaption>Transistor arrays built from the printed films.</figcaption>
  </figure>
  <p>Using these scalable films, we develop advanced device fabrication processes, such as photopatterning<sup><a href="#r7">7</a></sup>, to build high-performance transistor, photodetector, and capacitor arrays over large areas<sup><a href="#r2">2</a>,<a href="#r3">3</a></sup>.</p>
  <p>We also work on next-generation devices, including retina-inspired neuromorphic sensors and optoelectronic synapses<sup><a href="#r4">4</a>,<a href="#r8">8</a>,<a href="#r9">9</a></sup>, which have generally been demonstrated using complex device structures such as multiple gate terminals. Our aim is to obtain them from structurally simple devices instead, letting the material properties we design at the atomic scale supply the behavior that would otherwise have to come from the device architecture. Working this way, we aim to build devices with a wide range of functions in a scalable and reproducible manner.</p>

  <h2 class="rs-sec">Looking ahead</h2>
  <p>These three axes converge on one thing: a printed electronics platform. What the Internet of Everything needs is electronics cheap enough to put anywhere, in the right form factor, and good enough to be worth putting there. That is what we are building.</p>

  <h2 class="rs-sec">References</h2>
  <div class="rs-refnote">&dagger; These authors contributed equally.</div>
  <ol class="rs-refs">
    <li id="r1">Kim, K.<span class="eq">&dagger;</span>, <span class="self">Kim, J.</span><span class="eq">&dagger;</span> <em>et al.</em> Sub-stoichiometric zirconium oxide as a solution-processed dielectric for reconfigurable electronics. <em>Nat. Electron.</em> <strong>8</strong>, 461&ndash;473 (2025).</li>
    <li id="r2">Kwon, Y. A.<span class="eq">&dagger;</span>, <span class="self">Kim, J.</span><span class="eq">&dagger;</span> <em>et al.</em> Wafer-scale transistor arrays fabricated using slot-die printing of molybdenum disulfide and sodium-embedded alumina. <em>Nat. Electron.</em> <strong>6</strong>, 443&ndash;450 (2023).</li>
    <li id="r3">Cheema, S. S. <em>et al.</em> Giant energy storage and power density negative capacitance superlattices. <em>Nature</em> <strong>629</strong>, 803&ndash;809 (2024).</li>
    <li id="r4"><span class="self">Kim, J.</span> <em>et al.</em> Multilevel optical programming of intrinsic vacancies in solution-processed MoS<sub>2</sub> films for retinomorphic color differentiation. <em>Adv. Opt. Mater.</em> (2026).</li>
    <li id="r5"><span class="self">Kim, J.</span> <em>et al.</em> All-solution-processed van der Waals heterostructures for wafer-scale electronics. <em>Adv. Mater.</em> <strong>34</strong>, 2106110 (2022).</li>
    <li id="r6">Song, O., Rhee, D., <span class="self">Kim, J.</span> <em>et al.</em> All inkjet-printed electronics based on electrochemically exfoliated two-dimensional metal, semiconductor, and dielectric. <em>npj 2D Mater. Appl.</em> <strong>6</strong>, 64 (2022).</li>
    <li id="r7">Kwak, I. C.<span class="eq">&dagger;</span>, <span class="self">Kim, J.</span><span class="eq">&dagger;</span> <em>et al.</em> Orthogonal photopatterning of two-dimensional percolated network films for wafer-scale heterostructures. <em>Nat. Electron.</em> <strong>8</strong>, 235&ndash;243 (2025).</li>
    <li id="r8"><span class="self">Kim, J.</span> <em>et al.</em> Multicolor optoelectronic synapse enabled by photon-modulated remote doping in solution-processed van der Waals heterostructures. <em>Adv. Funct. Mater.</em> (2025).</li>
    <li id="r9">Nam, K.<span class="eq">&dagger;</span>, <span class="self">Kim, J.</span><span class="eq">&dagger;</span>, Ji, S.<span class="eq">&dagger;</span> <em>et al.</em> Light-induced field-tunneling synapses in solution-processed van der Waals heterostructures for scalable, retina-inspired optical sensing. <em>Adv. Funct. Mater.</em> (2026).</li>
  </ol>
</div>
