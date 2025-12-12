---
permalink: /portfolio/
title: "시공 포트폴리오"
layout: single
classes: wide
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;600&display=swap');

* {
  font-family: 'Noto Sans KR', -apple-system, sans-serif;
}

.portfolio-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 60px 30px;
}

.page-title {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 50px;
  text-align: center;
  color: #24292e;
}

.project-section {
  margin-bottom: 60px;
}

.section-title {
  font-size: 1.5rem;
  font-weight: 600;
  margin-bottom: 30px;
  color: #24292e;
  border-bottom: 2px solid #0366d6;
  padding-bottom: 10px;
}

.image-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
}

.image-item {
  position: relative;
  overflow: hidden;
  border-radius: 8px;
  cursor: pointer;
  transition: transform 0.3s;
}

.image-item:hover {
  transform: scale(1.05);
}

.image-item img {
  width: 100%;
  height: 250px;
  object-fit: cover;
  display: block;
}

@media (max-width: 768px) {
  .image-grid {
    grid-template-columns: 1fr;
  }
}
</style>

<div class="portfolio-container">
  <h1 class="page-title">Construction Portfolio</h1>
  
  <div class="project-section">
    <h2 class="section-title">사무공간 (Office)</h2>
    <div class="image-grid">
      <div class="image-item">
        <img src="/thehada/assets/images/office/1.jpg" alt="사무공간">
      </div>
      <div class="image-item">
        <img src="/thehada/assets/images/office/2.jpg" alt="사무공간">
      </div>
      <div class="image-item">
        <img src="/thehada/assets/images/office/3.jpg" alt="사무공간">
      </div>
      <div class="image-item">
        <img src="/thehada/assets/images/office/4.jpg" alt="사무공간">
      </div>
      <div class="image-item">
        <img src="/thehada/assets/images/office/5.jpg" alt="사무공간">
      </div>
    </div>
  </div>
  
  <div class="project-section">
    <h2 class="section-title">상업공간 (Commercial)</h2>
    <div class="image-grid">
      <div class="image-item">
        <img src="/thehada/assets/images/commercial/1.jpg" alt="상업공간">
      </div>
      <div class="image-item">
        <img src="/thehada/assets/images/commercial/2.jpg" alt="상업공간">
      </div>
      <div class="image-item">
        <img src="/thehada/assets/images/commercial/3.jpg" alt="상업공간">
      </div>
      <div class="image-item">
        <img src="/thehada/assets/images/commercial/4.jpg" alt="상업공간">
      </div>
      <div class="image-item">
        <img src="/thehada/assets/images/commercial/5.jpg" alt="상업공간">
      </div>
    </div>
  </div>
</div>