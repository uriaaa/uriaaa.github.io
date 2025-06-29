---
title: "강나경"
layout: single
permalink: /portfolio/
author_profile: true
---

<!-- 🔹 오른쪽 고정 목차 네비게이터 스타일 -->
<style>
  .side-nav {
    position: fixed;
    top: 100px;
    right: 40px;
    width: 200px;
    background-color: #f9f9f9;
    border-left: 2px solid #ddd;
    padding: 15px;
    font-size: 14px;
    z-index: 999;
  }

  .side-nav a {
    display: block;
    margin-bottom: 8px;
    color: #444;
    text-decoration: none;
  }

  .side-nav a:hover {
    color: #000;
    font-weight: bold;
  }

  @media (max-width: 1000px) {
    .side-nav {
      display: none; /* 모바일에서는 숨김 */
    }
  }
</style>

<!-- 고정 네비게이터 HTML -->
<div class="side-nav">
  <strong>Career</strong>
  <a href="#dal">달의 기억</a>
  <a href="#color">Colorfly</a>

  <br><strong>Personal Work</strong>
  <a href="#cha">캐릭터</a>
  <a href="#sheet">캐릭터시트</a>
  <a href="#object">오브젝트</a>

  <br><strong>Extra Work</strong>
  <a href="#etc">기타</a>
</div>

----------------------------------------------
<h2>INDEX</h2>
<ul style="font-size: 16px; line-height: 1.8;">
  <li><strong>Career</strong>
    <ul>
      <li>달의 기억</li>
      <li>Colorfly</li>
    </ul>
  </li>
  <li><strong>Personal Work</strong>
    <ul>
      <li>캐릭터</li>
      <li>캐릭터시트</li>
      <li>오브젝트</li>
    </ul>
  </li>
  <li><strong>Extra Work</strong>
    <ul>
      <li>기타</li>
    </ul>
  </li>
</ul>


<hr>

<!-- Career Section -->      
<h2>Career</h2>

<!-- 모달 구조 -->
<div id="imgModal" style="display: none; position: fixed; z-index: 9999; padding-top: 80px; left: 0; top: 0; width: 100%; height: 100%; overflow: auto; background-color: rgba(0,0,0,0.9);">
  <span id="modalClose" style="position: absolute; top: 20px; right: 35px; color: #fff; font-size: 40px; font-weight: bold; cursor: pointer;">&times;</span>
  <img id="modalImage" style="margin: 40px auto; display: block; max-width: 100%; max-height: 100%;">
</div>



<h3 id="dal">1. 달의 기억</h3>

{% include amoon.html %}

<h3 id="color">2. Colorfly</h3>

{% include acolorfly.html %}

<h3>3. Personal Work</h3>

<h4 id="cha">&emsp;Character</h4>

{% include aself1.html %}

<h4 id="sheet">&emsp;Character Sheet</h4>

{% include aself2.html %}

<h4 id="object">&emsp;Object</h4>

{% include aself3.html %}

<h3 id="etc">4. Extra</h3>

{% include aself4.html %}

<!-- 모달 창 구조 -->
<div id="imgModal" style="display: none; position: fixed; z-index: 9999; padding-top: 60px; left: 0; top: 0; width: 100%; height: 100%; overflow: auto; background-color: rgba(0,0,0,0.9);">
  <span id="modalClose" style="position: absolute; top: 20px; right: 35px; color: #fff; font-size: 40px; font-weight: bold; cursor: pointer;">&times;</span>
  <img id="modalImage" style="margin: auto; display: block; max-width: 80%; max-height: 80%;">
</div>

<script>
document.addEventListener("DOMContentLoaded", function() {
  const modal = document.getElementById('imgModal');
  const modalImg = document.getElementById('modalImage');
  const closeBtn = document.getElementById('modalClose');

  document.querySelectorAll("img").forEach(img => {
    img.style.cursor = "zoom-in";
    img.addEventListener("click", () => {
      modal.style.display = "block";
      modalImg.src = img.src;
      modalImg.alt = img.alt;
    });
  });

  closeBtn.addEventListener("click", () => {
    modal.style.display = "none";
  });

  window.addEventListener("click", (event) => {
    if (event.target === modal) {
      modal.style.display = "none";
    }
  });
});
</script>
