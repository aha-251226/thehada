---
permalink: /realestate/
title: 
layout: single
classes: wide
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;600&display=swap');

* {
  font-family: 'Noto Sans KR', -apple-system, sans-serif;
}

.page-wrapper {
  display: grid;
  grid-template-columns: 200px 1fr;
  gap: 80px;
  max-width: 1000px;
  margin: 0 auto;
  padding: 60px 30px;
}

.sidebar-profile {
  position: sticky;
  top: 80px;
  height: fit-content;
}

.profile-image {
  width: 120px;
  height: 120px;
  border-radius: 12px;
  object-fit: cover;
  margin-bottom: 20px;
  display: block;
}

.profile-name {
  font-size: 0.88rem;
  font-weight: 600;
  margin-bottom: 12px;
  color: #24292e;
  line-height: 1.3;
}

.profile-bio {
  font-size: 0.45rem;
  color: #586069;
  line-height: 1.5;
  margin-bottom: 20px;
}

.profile-meta {
  font-size: 0.65rem;
  color: #586069;
  margin-bottom: 8px;
}

.profile-links {
  list-style: none;
  padding: 0;
  margin: 20px 0 0 0;
  border-top: 1px solid #e1e4e8;
  padding-top: 20px;
}

.profile-links li {
  margin-bottom: 12px;
}

.profile-links a {
  color: #586069;
  text-decoration: none;
  font-size: 0.65rem;
  transition: color 0.2s;
}

.profile-links a:hover {
  color: #0366d6;
}

.main-content {
  max-width: 700px;
}

.article-header {
  margin-bottom: 40px;
}

.article-title {
  font-size: 1.6rem;
  font-weight: 700;
  margin-bottom: 10px;
  color: #24292e;
  line-height: 1.25;
}

.article-meta {
  font-size: 0.7rem;
  color: #586069;
  margin-bottom: 30px;
}

.main-content h2 {
  font-size: 1.2rem;
  font-weight: 600;
  margin: 40px 0 20px 0;
  color: #24292e;
}

.main-content p {
  font-size: 0.65rem;
  line-height: 1.75;
  color: #24292e;
  margin-bottom: 20px;
  text-align: justify;
}

.main-content strong {
  font-weight: 600;
  font-size: 0.65rem;
  color: #24292e;
  display: block;
  margin-top: 30px;
  margin-bottom: 12px;
}

.main-content ul {
  list-style: none;
  padding-left: 0;
  margin-bottom: 25px;
}

.main-content li {
  font-size: 0.65rem;
  line-height: 1.75;
  color: #24292e;
  padding-left: 24px;
  position: relative;
  margin-bottom: 8px;
  text-align: justify;
}

.main-content li:before {
  content: "•";
  position: absolute;
  left: 8px;
  color: #586069;
}

@media (max-width: 768px) {
  .page-wrapper {
    grid-template-columns: 1fr;
    gap: 40px;
  }
  
  .sidebar-profile {
    position: relative;
    top: 0;
  }
  
  .article-title {
    font-size: 1.4rem;
  }
}
</style>

<div class="page-wrapper">
  <aside class="sidebar-profile">
    <img src="/thehada/assets/images/profile.jpg" alt="박영준" class="profile-image">
    <h3 class="profile-name">박영준</h3>
    <p class="profile-bio">부동산 컨설팅 전문가</p>
    <div class="profile-meta">서울, 대한민국</div>
    <ul class="profile-links">
      <li><a href="tel:010-1234-5678">010-1234-5678</a></li>
      <li><a href="mailto:contact@thehada.com">contact@thehada.com</a></li>
    </ul>
  </aside>
  
  <main class="main-content">
    <div class="article-header">
      <div class="article-meta">Real Estate Consulting</div>
    </div>
    
    <p>THEHADA의 부동산 컨설팅 서비스는 공장 및 창고 전문 중개를 통해 고객의 성공적인 부동산 거래를 지원합니다.</p>
    
    <strong>공장 부동산 중개</strong>
    <ul>
      <li>제조업 시설 매매 및 임대</li>
      <li>입지 분석 및 컨설팅</li>
      <li>공장 설립 인허가 지원</li>
    </ul>
    
    <strong>창고 부동산 중개</strong>
    <ul>
      <li>물류센터 및 창고 매매/임대</li>
      <li>물류 최적화 입지 분석</li>
      <li>시설 용도 변경 컨설팅</li>
    </ul>
    
    <strong>산업용 부동산 투자 자문</strong>
    <ul>
      <li>공장 및 창고 투자 가치 평가</li>
      <li>임대 수익률 분석</li>
      <li>매각 전략 수립</li>
    </ul>
    
    <strong>맞춤형 부동산 솔루션</strong>
    <ul>
      <li>고객 요구사항에 맞는 물건 발굴</li>
      <li>계약 및 등기 절차 지원</li>
      <li>세무 및 법률 자문 연계</li>
    </ul>
  </main>
</div>