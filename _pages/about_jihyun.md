<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap");

body, p, li, a, span, td, .navbar, .navbar-brand, h1, h2, h3, h4, h5, h6 {
  font-family: "Inter", -apple-system, BlinkMacSystemFont, sans-serif !important;
}
h1, h2, h3, .navbar-brand { font-weight: 700 !important; letter-spacing: -0.02em; }
body { font-weight: 400; letter-spacing: -0.005em; }

/* ===== 라이트 모드 ===== */
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

html[data-theme="light"] p a,
html[data-theme="light"] li a,
html[data-theme="light"] .pi-contact a { color: #651FFF !important; }

html[data-theme="light"] .pi-name,
html[data-theme="light"] .pi-section,
html[data-theme="light"] .pi-table td,
html[data-theme="light"] .pi-contact .label { color: #191919 !important; }
html[data-theme="light"] .pi-role { color: #5A5A5A !important; }
html[data-theme="light"] .pi-section { border-top-color: rgba(25,25,25,0.12) !important; }

/* ===== 다크 모드 ===== */
html[data-theme="dark"] .pi-name,
html[data-theme="dark"] .pi-section,
html[data-theme="dark"] .pi-table td,
html[data-theme="dark"] .pi-contact .label { color: #FCFCFC !important; }
html[data-theme="dark"] .pi-role { color: #B5B5B5 !important; }
html[data-theme="dark"] .pi-section { border-top-color: rgba(252,252,252,0.18) !important; }

/* ===== 사진 & 상단 정렬 ===== */
.profile img {
  max-width: 210px !important;
  width: 100% !important;
  border-radius: 6px;
  display: block;
  margin-left: auto;
}
.profile { padding-top: 0 !important; align-self: flex-start !important; }

div:has(> .pi-name) {
  align-self: flex-start !important;
  margin-top: 0 !important;
  padding-top: 0 !important;
}
div:has(> .profile) { align-items: flex-start !important; }
.row, .profiles .row { align-items: flex-start !important; }

/* ===== PI 정보 ===== */
.pi-name { font-size: 1.6rem; font-weight: 700; letter-spacing: -0.02em; margin: 0 0 0.4rem 0; }
.pi-contact { font-size: 0.88rem; margin-bottom: 1.2rem; }
.pi-contact .label { font-weight: 700; display: inline-block; width: 60px; }
.pi-role { font-size: 0.9rem; line-height: 1.5; margin-bottom: 0.9rem; }
.pi-section { font-size: 1.05rem; font-weight: 700; letter-spacing: -0.02em; border-top: 1px solid; padding-top: 0.9rem; margin: 1.4rem 0 0.7rem 0; }
.pi-table { width: 100%; border-collapse: collapse; font-size: 0.86rem; }
.pi-table td { padding: 0.28rem 0; vertical-align: top; border: none; }
.pi-table td.when { width: 160px; font-weight: 600; white-space: nowrap; padding-right: 0.8rem; }
</style>

<div class="pi-name">Jihyun Kim, Ph.D.</div>

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
