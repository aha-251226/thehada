---
permalink: /portfolio/
title: "시공 포트폴리오"
layout: single
classes: wide
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;600&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Noto Sans KR', -apple-system, sans-serif;
}

.portfolio-slider {
  width: 100vw;
  height: 100vh;
  position: relative;
  overflow: hidden;
  margin-left: calc(-50vw + 50%);
}

.slide {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  opacity: 0;
  transition: opacity 0.5s ease-in-out;
}

.slide.active {
  opacity: 1;
}

.slide img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.slide-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to bottom, rgba(0,0,0,0.3) 0%, rgba(0,0,0,0) 50%);
  display: flex;
  align-items: flex-start;
  justify-content: center;
  padding: 60px 40px;
}

.slide-label {
  font-size: 2.5rem;
  font-weight: 700;
  color: white;
  text-shadow: 2px 2px 8px rgba(0,0,0,0.5);
}

.nav-button {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(255,255,255,0.3);
  border: none;
  color: white;
  font-size: 3rem;
  padding: 20px 30px;
  cursor: pointer;
  z-index: 100;
  transition: background 0.3s;
  backdrop-filter: blur(5px);
}

.nav-button:hover {
  background: rgba(255,255,255,0.5);
}

.prev-button {
  left: 20px;
}

.next-button {
  right: 20px;
}

.slide-counter {
  position: absolute;
  bottom: 40px;
  left: 50%;
  transform: translateX(-50%);
  background: rgba(0,0,0,0.5);
  color: white;
  padding: 10px 25px;
  border-radius: 25px;
  font-size: 1rem;
  backdrop-filter: blur(5px);
  z-index: 100;
}

@media (max-width: 768px) {
  .slide-label {
    font-size: 1.5rem;
  }
  
  .nav-button {
    font-size: 2rem;
    padding: 15px 20px;
  }
}
</style>

<div class="portfolio-slider">
  <!-- Office Slides -->
  <div class="slide active">
    <img src="/thehada/assets/images/office/1.jpg" alt="Office 1">
    <div class="slide-overlay">
      <div class="slide-label">사무공간 (Office)</div>
    </div>
  </div>
  
  <div class="slide">
    <img src="/thehada/assets/images/office/2.jpg" alt="Office 2">
    <div class="slide-overlay">
      <div class="slide-label">사무공간 (Office)</div>
    </div>
  </div>
  
  <div class="slide">
    <img src="/thehada/assets/images/office/3.jpg" alt="Office 3">
    <div class="slide-overlay">
      <div class="slide-label">사무공간 (Office)</div>
    </div>
  </div>
  
  <div class="slide">
    <img src="/thehada/assets/images/office/4.jpg" alt="Office 4">
    <div class="slide-overlay">
      <div class="slide-label">사무공간 (Office)</div>
    </div>
  </div>
  
  <div class="slide">
    <img src="/thehada/assets/images/office/5.jpg" alt="Office 5">
    <div class="slide-overlay">
      <div class="slide-label">사무공간 (Office)</div>
    </div>
  </div>
  
  <!-- Commercial Slides -->
  <div class="slide">
    <img src="/thehada/assets/images/commercial/1.jpg" alt="Commercial 1">
    <div class="slide-overlay">
      <div class="slide-label">상업공간 (Commercial)</div>
    </div>
  </div>
  
  <div class="slide">
    <img src="/thehada/assets/images/commercial/2.jpg" alt="Commercial 2">
    <div class="slide-overlay">
      <div class="slide-label">상업공간 (Commercial)</div>
    </div>
  </div>
  
  <div class="slide">
    <img src="/thehada/assets/images/commercial/3.jpg" alt="Commercial 3">
    <div class="slide-overlay">
      <div class="slide-label">상업공간 (Commercial)</div>
    </div>
  </div>
  
  <div class="slide">
    <img src="/thehada/assets/images/commercial/4.jpg" alt="Commercial 4">
    <div class="slide-overlay">
      <div class="slide-label">상업공간 (Commercial)</div>
    </div>
  </div>
  
  <div class="slide">
    <img src="/thehada/assets/images/commercial/5.jpg" alt="Commercial 5">
    <div class="slide-overlay">
      <div class="slide-label">상업공간 (Commercial)</div>
    </div>
  </div>
  
  <button class="nav-button prev-button" onclick="changeSlide(-1)">‹</button>
  <button class="nav-button next-button" onclick="changeSlide(1)">›</button>
  <div class="slide-counter"><span id="current">1</span> / <span id="total">10</span></div>
</div>

<script>
let currentSlide = 0;
const slides = document.querySelectorAll('.slide');
const totalSlides = slides.length;
document.getElementById('total').textContent = totalSlides;

function showSlide(index) {
  slides.forEach(slide => slide.classList.remove('active'));
  slides[index].classList.add('active');
  document.getElementById('current').textContent = index + 1;
}

function changeSlide(direction) {
  currentSlide += direction;
  if (currentSlide < 0) currentSlide = totalSlides - 1;
  if (currentSlide >= totalSlides) currentSlide = 0;
  showSlide(currentSlide);
}

// 키보드 화살표 지원
document.addEventListener('keydown', (e) => {
  if (e.key === 'ArrowLeft') changeSlide(-1);
  if (e.key === 'ArrowRight') changeSlide(1);
});
</script>