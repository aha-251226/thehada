---
permalink: /portfolio/
title: ""
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
  justify-content: flex-start;
  padding: 60px 60px;
}

.slide-label {
  text-align: left;
}

.slide-label-ko {
  font-size: 1.25rem;
  font-weight: 400;
  color: white;
  text-shadow: 2px 2px 8px rgba(0,0,0,0.5);
  margin-bottom: 5px;
}

.slide-label-en {
  font-size: 1rem;
  font-weight: 400;
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
  .slide-label-ko {
    font-size: 1rem;
  }
  
  .slide-label-en {
    font-size: 0.875rem;
  }
  
  .nav-button {
    font-size: 2rem;
    padding: 15px 20px;
  }
}
</style>

<div class="portfolio-slider" id="slider">
  <button class="nav-button prev-button" onclick="changeSlide(-1)">‹</button>
  <button class="nav-button next-button" onclick="changeSlide(1)">›</button>
  <div class="slide-counter"><span id="current">1</span> / <span id="total">0</span></div>
</div>

<script>
// 이미지 목록 정의
const images = [
  // Office 이미지
  { src: '/thehada/assets/images/office/_GSS7942.jpg', category: '사무공간', categoryEn: 'Office' },
  { src: '/thehada/assets/images/office/_GSS7954.jpg', category: '사무공간', categoryEn: 'Office' },
  { src: '/thehada/assets/images/office/_GSS7957.jpg', category: '사무공간', categoryEn: 'Office' },
  { src: '/thehada/assets/images/office/_GSS7970.jpg', category: '사무공간', categoryEn: 'Office' },
  { src: '/thehada/assets/images/office/_GSS7994.jpg', category: '사무공간', categoryEn: 'Office' },
  { src: '/thehada/assets/images/office/_GSS8003.jpg', category: '사무공간', categoryEn: 'Office' },
  { src: '/thehada/assets/images/office/1.jpg', category: '사무공간', categoryEn: 'Office' },
  { src: '/thehada/assets/images/office/1-1.jpg', category: '사무공간', categoryEn: 'Office' },
  { src: '/thehada/assets/images/office/05.jpg', category: '사무공간', categoryEn: 'Office' },
  { src: '/thehada/assets/images/office/06.jpg', category: '사무공간', categoryEn: 'Office' },
  { src: '/thehada/assets/images/office/07.jpg', category: '사무공간', categoryEn: 'Office' },
  { src: '/thehada/assets/images/office/12.jpg', category: '사무공간', categoryEn: 'Office' },
  { src: '/thehada/assets/images/office/03.jpg', category: '사무공간', categoryEn: 'Office' },
  { src: '/thehada/assets/images/office/_GSS7819.jpg', category: '사무공간', categoryEn: 'Office' },
  { src: '/thehada/assets/images/office/_GSS7894.jpg', category: '사무공간', categoryEn: 'Office' },
  { src: '/thehada/assets/images/office/01.jpg', category: '사무공간', categoryEn: 'Office' },
  { src: '/thehada/assets/images/office/02.jpg', category: '사무공간', categoryEn: 'Office' },
  
  // Commercial 이미지
  { src: '/thehada/assets/images/commercial/_GSS7942.jpg', category: '상업공간', categoryEn: 'Commercial' },
  { src: '/thehada/assets/images/commercial/_GSS7954.jpg', category: '상업공간', categoryEn: 'Commercial' },
  { src: '/thehada/assets/images/commercial/_GSS7957.jpg', category: '상업공간', categoryEn: 'Commercial' },
  { src: '/thehada/assets/images/commercial/_GSS7970.jpg', category: '상업공간', categoryEn: 'Commercial' },
  { src: '/thehada/assets/images/commercial/_GSS7994.jpg', category: '상업공간', categoryEn: 'Commercial' },
  { src: '/thehada/assets/images/commercial/_GSS8003.jpg', category: '상업공간', categoryEn: 'Commercial' },
  { src: '/thehada/assets/images/commercial/1.jpg', category: '상업공간', categoryEn: 'Commercial' },
  { src: '/thehada/assets/images/commercial/1-1.jpg', category: '상업공간', categoryEn: 'Commercial' },
  { src: '/thehada/assets/images/commercial/05.jpg', category: '상업공간', categoryEn: 'Commercial' },
  { src: '/thehada/assets/images/commercial/06.jpg', category: '상업공간', categoryEn: 'Commercial' },
  { src: '/thehada/assets/images/commercial/07.jpg', category: '상업공간', categoryEn: 'Commercial' },
  { src: '/thehada/assets/images/commercial/12.jpg', category: '상업공간', categoryEn: 'Commercial' },
  { src: '/thehada/assets/images/commercial/03.jpg', category: '상업공간', categoryEn: 'Commercial' },
  { src: '/thehada/assets/images/commercial/_GSS7819.jpg', category: '상업공간', categoryEn: 'Commercial' },
  { src: '/thehada/assets/images/commercial/_GSS7894.jpg', category: '상업공간', categoryEn: 'Commercial' },
  { src: '/thehada/assets/images/commercial/01.jpg', category: '상업공간', categoryEn: 'Commercial' },
  { src: '/thehada/assets/images/commercial/02.jpg', category: '상업공간', categoryEn: 'Commercial' },
];

const slider = document.getElementById('slider');
let currentSlide = 0;

// 슬라이드 생성
images.forEach((img, index) => {
  const slideDiv = document.createElement('div');
  slideDiv.className = 'slide' + (index === 0 ? ' active' : '');
  slideDiv.innerHTML = `
    <img src="${img.src}" alt="${img.category}">
    <div class="slide-overlay">
      <div class="slide-label">
        <div class="slide-label-ko">${img.category}</div>
        <div class="slide-label-en">${img.categoryEn}</div>
      </div>
    </div>
  `;
  slider.insertBefore(slideDiv, slider.firstChild);
});

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