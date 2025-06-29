---
title: "강나경"
layout: single
permalink: /portfolio/
author_profile: true
---

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

<h3>1. 달의 기억</h3>
{% include amoon.html %}

<h3>2. Colorfly</h3>
{% include acolorfly.html %}

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
