---
layout: page
permalink: /publications/
title: Publications
nav: true
nav_order: 4
---
<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap");
body, p, li, td, .navbar, .navbar-brand, h1, h2, h3, h4, h5, h6 {
  font-family: "Inter", -apple-system, BlinkMacSystemFont, sans-serif !important;
}
h1, h2, h3, .navbar-brand { font-weight: 700 !important; letter-spacing: -0.02em; }
body { font-weight: 400; letter-spacing: -0.005em; }
/* ===== 탭 이동 시 전체 축 밀림 방지 ===== */
html {
  scrollbar-gutter: stable;
  overflow-y: scroll;
}
body { overflow-x: clip; }
/* 네비게이션 */
.navbar .navbar-nav, .navbar ul { margin-left: 2rem !important; margin-right: auto !important; }
.navbar .container, .navbar .container-fluid, .navbar > div { justify-content: flex-start !important; }

/* ============================================================
   저널 약어 배지 제거 + 배지가 쓰던 칸 회수
   ------------------------------------------------------------
   al-folio는 각 항목을 Bootstrap row(배지 칸 + 본문 칸)로 만든다.
   배지를 숨기는 것만으로는 빈 칸이 남으므로, row 자체를 블록으로
   되돌리고 열 너비를 100%로 풀어야 본문이 왼쪽으로 붙는다.
   ============================================================ */
.publications ol.bibliography > li .abbr,
.publications ol.bibliography > li abbr.badge,
.publications ol.bibliography > li .badge { display: none !important; }

.publications ol.bibliography > li > .row,
.publications ol.bibliography > li > div {
  display: block !important;
  margin-left: 0 !important;
  margin-right: 0 !important;
}
.publications ol.bibliography > li [class*="col-"] {
  flex: none !important;
  width: 100% !important;
  max-width: 100% !important;
  padding-left: 0 !important;
  padding-right: 0 !important;
  margin-left: 0 !important;
}
/* 링크 버튼(Abs / HTML 등)도 숨김 — 제목 클릭으로 대체 */
.publications ol.bibliography > li .links { display: none !important; }

/* ===== 테마 공통: 크기 / 굵기 / 간격 ===== */
.publications .title,
.publications ol.bibliography > li > div:not(.abbr) > .title {
  font-size: 1rem !important;
  font-weight: 700 !important;
  letter-spacing: -0.015em;
  line-height: 1.4;
  margin-bottom: 0.15rem;
}
.publications .author,
.publications .periodical {
  font-size: 0.82rem !important;
  line-height: 1.5;
  font-weight: 400 !important;
}
.publications .author em,
.publications .author strong { font-weight: 600 !important; }
.publications h2.year,
.publications h2.bibliography,
.publications .year {
  font-size: 1.5rem !important;
  font-weight: 700 !important;
  letter-spacing: -0.02em;
  margin: 1.2rem 0 0.6rem 0 !important;
  padding-top: 0.9rem !important;
  border-top: 1px solid !important;
  opacity: 1 !important;
}
/* ===== 제목 하이퍼링크 ===== */
.publications .title a.pub-link {
  color: inherit !important;
  text-decoration: none !important;
  background-image: linear-gradient(currentColor, currentColor);
  background-size: 0% 1px;
  background-repeat: no-repeat;
  background-position: left 100%;
  transition: background-size 0.25s ease, color 0.15s ease;
}
.publications .title a.pub-link:hover { background-size: 100% 1px; }
.publications ol.bibliography > li.has-link { cursor: pointer; }

/* ===== 논문 번호 + 정렬 ===== */
.publications { counter-reset: pubnum 43; }
.publications ol.bibliography { padding-left: 0; margin-left: 0; list-style: none; }
.publications ol.bibliography > li {
  counter-increment: pubnum -1;
  position: relative;
  padding-left: 2.7rem;      /* 번호가 들어갈 여백 — 본문 왼쪽 정렬선 */
  padding-right: 0;
  margin-bottom: 1.15rem;
  list-style: none;
  border-radius: 6px;
  transition: background-color 0.15s ease;
}
.publications ol.bibliography > li::before {
  content: "(" counter(pubnum) ")";
  position: absolute;
  left: 0;
  top: 0.12rem;
  width: 2.1rem;
  text-align: right;
  font-size: 0.78rem;
  font-weight: 500;
  font-variant-numeric: tabular-nums;
  line-height: 1.4;
}

@media (max-width: 700px) {
  .publications h2.year,
  .publications h2.bibliography,
  .publications .year { font-size: 1.3rem !important; }
  .publications ol.bibliography > li { padding-left: 2.3rem; }
  .publications ol.bibliography > li::before { width: 1.8rem; }
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
html[data-theme="light"] .post-title { color: #191919 !important; }
html[data-theme="light"] .publications .title { color: #191919 !important; }
html[data-theme="light"] .publications .title a.pub-link:hover { color: #651FFF !important; }
html[data-theme="light"] .publications ol.bibliography > li.has-link:hover { background-color: rgba(101, 31, 255, 0.05); }
html[data-theme="light"] .publications .author,
html[data-theme="light"] .publications .periodical { color: #5A5A5A !important; }
html[data-theme="light"] .publications .author a,
html[data-theme="light"] .publications .author .more-authors { color: #5A5A5A !important; }
html[data-theme="light"] .publications .author em,
html[data-theme="light"] .publications .author strong { color: #651FFF !important; }
html[data-theme="light"] .publications h2.year,
html[data-theme="light"] .publications h2.bibliography,
html[data-theme="light"] .publications .year { color: var(--year-color) !important; }
html[data-theme="light"] .publications ol.bibliography > li::before { color: #A8A8A8; }
html[data-theme="light"] .publications h2.year,
html[data-theme="light"] .publications h2.bibliography,
html[data-theme="light"] .publications .year { border-top-color: var(--line-color) !important; }
/* ===== 다크 모드: 색상 ===== */
html[data-theme="dark"] {
  /* 연도 · 연도 구분선 밝기 (이 두 줄만 조절) */
  --year-color: rgba(252, 252, 252, 0.62);
  --line-color: rgba(252, 252, 252, 0.38);
}
html[data-theme="dark"] .publications .title { color: #FCFCFC !important; }
html[data-theme="dark"] .publications .title a.pub-link:hover { color: #86CFDA !important; }
html[data-theme="dark"] .publications ol.bibliography > li.has-link:hover { background-color: rgba(134, 207, 218, 0.07); }
html[data-theme="dark"] .publications .author,
html[data-theme="dark"] .publications .periodical { color: #B0B0B0 !important; }
html[data-theme="dark"] .publications .author a,
html[data-theme="dark"] .publications .author .more-authors { color: #B0B0B0 !important; }
html[data-theme="dark"] .publications .author em,
html[data-theme="dark"] .publications .author strong { color: #86CFDA !important; }
html[data-theme="dark"] .publications h2.year,
html[data-theme="dark"] .publications h2.bibliography,
html[data-theme="dark"] .publications .year { color: var(--year-color) !important; }
html[data-theme="dark"] .publications ol.bibliography > li::before { color: #8F8F8F !important; }
html[data-theme="dark"] .publications h2.year,
html[data-theme="dark"] .publications h2.bibliography,
html[data-theme="dark"] .publications .year { border-top-color: var(--line-color) !important; }
</style>
<div class="publications">
{% bibliography %}
</div>
<script>
(function () {
  function linkify() {
    var items = document.querySelectorAll(".publications ol.bibliography > li");
    items.forEach(function (li) {
      var titleEl = li.querySelector(".title");
      if (!titleEl || titleEl.querySelector("a")) return;
      // 1순위: 링크 버튼 영역의 외부 링크 (숨겨져 있어도 DOM에는 존재)
      var href = null;
      var btn = li.querySelector('.links a[href^="http"]:not(.abs), .links a[href^="/"]:not(.abs)');
      if (btn) href = btn.getAttribute("href");
      // 2순위: 저자명 링크를 뺀 나머지 외부 링크
      if (!href) {
        var all = li.querySelectorAll('a[href^="http"]');
        for (var i = 0; i < all.length; i++) {
          if (all[i].closest(".author")) continue;
          if (all[i].classList.contains("abs")) continue;
          href = all[i].getAttribute("href");
          break;
        }
      }
      // 3순위: data-doi 속성
      if (!href) {
        var doiEl = li.hasAttribute("data-doi") ? li : li.querySelector("[data-doi]");
        if (doiEl) {
          var doi = doiEl.getAttribute("data-doi");
          if (doi) href = "https://doi.org/" + doi.replace(/^https?:\/\/doi\.org\//, "");
        }
      }
      if (!href) return;
      var a = document.createElement("a");
      a.href = href;
      a.target = "_blank";
      a.rel = "noopener noreferrer";
      a.className = "pub-link";
      while (titleEl.firstChild) a.appendChild(titleEl.firstChild);
      titleEl.appendChild(a);
      li.classList.add("has-link");
      li.dataset.href = href;
    });
    document.querySelectorAll(".publications ol.bibliography > li.has-link").forEach(function (li) {
      li.addEventListener("click", function (e) {
        if (e.target.closest("a") || e.target.closest("button")) return;
        if (window.getSelection().toString()) return;
        window.open(li.dataset.href, "_blank", "noopener");
      });
    });
  }
  if (document.readyState === "loading") {
    document.addEventListener("DOMContentLoaded", linkify);
  } else {
    linkify();
  }
})();
</script>
