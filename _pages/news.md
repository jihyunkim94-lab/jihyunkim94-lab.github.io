---
layout: page
permalink: /news/
title: News
description: Updates from Kim Lab
nav: true
nav_order: 5
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

/* 긴 제목·URL이 컨테이너를 넘기지 않도록 */
.nw-row .what { overflow-wrap: break-word; word-break: break-word; }

/* 네비게이션 */
.navbar .navbar-nav, .navbar ul { margin-left: 2rem !important; margin-right: auto !important; }
.navbar .container, .navbar .container-fluid, .navbar > div { justify-content: flex-start !important; }
/* ===== 테마 공통: 크기 / 레이아웃 ===== */
.nw-list { margin-top: 0.5rem; }
/* 연도 헤딩 — Publications 연도 헤딩과 동일 규격 */
.nw-year {
  font-size: 1.5rem;
  font-weight: 700;
  letter-spacing: -0.02em;
  border-top: 1px solid var(--line-color);
  padding-top: 0.9rem;
  margin: 1.2rem 0 0.6rem 0;
  clear: both;
}
.nw-row {
  display: flex;
  align-items: flex-start;
  gap: 0.8rem;
  padding: 0.3rem 0;
  font-size: 0.86rem;
  line-height: 1.5;
  border-radius: 6px;
}
.nw-row .when {
  flex: 0 0 130px;
  font-weight: 600;
  white-space: nowrap;
  font-variant-numeric: tabular-nums;
}
.nw-row .what { flex: 1 1 auto; min-width: 0; }
.nw-row .what p { margin: 0; }
.nw-row .what a {
  text-decoration: none;
  background-image: linear-gradient(currentColor, currentColor);
  background-size: 0% 1px;
  background-repeat: no-repeat;
  background-position: left 100%;
  transition: background-size 0.25s ease;
}
.nw-row .what a:hover { background-size: 100% 1px; }
.nw-empty { font-size: 0.88rem; opacity: 0.5; font-style: italic; margin-top: 1rem; }
@media (max-width: 700px) {
  .nw-year { font-size: 1.3rem; }
  .nw-row { flex-direction: column; gap: 0.15rem; padding: 0.5rem 0; }
  .nw-row .when { flex: none; font-size: 0.8rem; }
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
html[data-theme="light"] .nw-row .when { color: #191919 !important; }
html[data-theme="light"] .nw-row .what { color: #5A5A5A !important; }
html[data-theme="light"] .nw-row .what a { color: #651FFF !important; }
html[data-theme="light"] .nw-year { color: var(--year-color) !important; }
html[data-theme="light"] .nw-year { border-top-color: var(--line-color) !important; }
/* ===== 다크 모드: 색상 ===== */
html[data-theme="dark"] {
  /* 연도 · 연도 구분선 밝기 (이 두 줄만 조절) */
  --year-color: rgba(252, 252, 252, 0.62);
  --line-color: rgba(252, 252, 252, 0.38);
}
html[data-theme="dark"] .nw-row .when { color: #FCFCFC !important; }
html[data-theme="dark"] .nw-row .what { color: #B5B5B5 !important; }
html[data-theme="dark"] .nw-row .what a { color: #86CFDA !important; }
html[data-theme="dark"] .nw-year { color: var(--year-color) !important; }
html[data-theme="dark"] .nw-year { border-top-color: var(--line-color) !important; }
</style>

<div class="nw-list">
{% assign items = site.news | sort: "date" | reverse %}
{% if items.size == 0 %}
  <div class="nw-empty">No news yet.</div>
{% else %}
  {% assign current_year = "" %}
  {% for item in items %}
    {% assign y = item.date | date: "%Y" %}
    {% if y != current_year %}
      {% assign current_year = y %}
      <div class="nw-year">{{ y }}</div>
    {% endif %}
    <div class="nw-row">
      <div class="when">{{ item.date | date: "%b %d, %Y" }}</div>
      <div class="what">
        {% if item.inline %}
          {{ item.content | markdownify | remove: "<p>" | remove: "</p>" }}
        {% else %}
          <a href="{{ item.url | relative_url }}">{{ item.title }}</a>
        {% endif %}
      </div>
    </div>
  {% endfor %}
{% endif %}
</div>
