---
layout: none
permalink: /
---

<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>THEHADA - 부동산·시공·연구 컨설팅</title>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Noto Sans KR', sans-serif;
            color: #333;
            background: #fff;
        }
        
        /* Header */
        header {
            position: fixed;
            top: 0;
            width: 100%;
            background: #fff;
            box-shadow: 0 2px 5px rgba(0,0,0,0.05);
            z-index: 1000;
        }
        
        nav {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 80px;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: #00A0E9;
            letter-spacing: -1px;
        }
        
        .nav-menu {
            display: flex;
            gap: 50px;
            list-style: none;
        }
        
        .nav-menu a {
            text-decoration: none;
            color: #333;
            font-size: 1rem;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-menu a:hover {
            color: #00A0E9;
        }
        
        /* Hero Section - White Background */
        .hero {
            margin-top: 80px;
            min-height: 450px;
            background: #fff;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 80px 40px;
        }
        
        .hero-content {
            text-align: center;
            max-width: 900px;
        }
        
        .hero-content h1 {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 25px;
            color: #1a1a1a;
            letter-spacing: -1px;
        }
        
        .hero-content p {
            font-size: 1.1rem;
            font-weight: 400;
            line-height: 1.8;
            color: #555;
        }
        
        /* Services Section */
        .services {
            max-width: 1400px;
            margin: 0 auto;
            padding: 80px 40px;
            background: #f8f9fa;
        }
        
        .section-title {
            text-align: center;
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 60px;
            color: #1a1a1a;
        }
        
        .service-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 40px;
        }
        
        .service-card {
            background: #fff;
            border: 1px solid #e0e0e0;
            border-radius: 10px;
            padding: 50px 35px;
            text-align: center;
            transition: all 0.3s;
            cursor: pointer;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            border-color: #00A0E9;
        }
        
        .service-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: #00A0E9;
            margin-bottom: 20px;
        }
        
        .service-title {
            font-size: 1.4rem;
            font-weight: 700;
            margin-bottom: 10px;
            color: #1a1a1a;
        }
        
        .service-subtitle {
            font-size: 0.9rem;
            color: #888;
            margin-bottom: 20px;
        }
        
        .service-desc {
            font-size: 0.95rem;
            line-height: 1.7;
            color: #666;
            margin-bottom: 25px;
        }
        
        .service-btn {
            display: inline-block;
            padding: 10px 25px;
            background: #00A0E9;
            color: white;
            text-decoration: none;
            border-radius: 5px;
            font-size: 0.9rem;
            font-weight: 500;
            transition: all 0.3s;
        }
        
        .service-btn:hover {
            background: #0080c0;
        }
        
        /* Footer */
        footer {
            background: #1a1a1a;
            color: #fff;
            padding: 40px;
            text-align: center;
            font-size: 0.9rem;
        }
        
        @media (max-width: 1024px) {
            .service-grid {
                grid-template-columns: 1fr;
            }
        }
        
        @media (max-width: 768px) {
            .nav-menu {
                display: none;
            }
            
            .hero-content h1 {
                font-size: 2rem;
            }
            
            .hero-content p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">THEHADA</div>
            <ul class="nav-menu">
                <li><a href="#about">회사소개</a></li>
                <li><a href="#services">사업영역</a></li>
                <li><a href="/thehada/portfolio/">포트폴리오</a></li>
                <li><a href="/thehada/assets/company-profile.pdf" download>회사소개서</a></li>
            </ul>
        </nav>
    </header>
    
    <section id="about" class="hero">
        <div class="hero-content">
            <h1>THEHADA</h1>
            <p>최신 기술과 풍부한 경험을 바탕으로<br>고객의 성공을 지원하는 전문 컨설팅 기업입니다</p>
        </div>
    </section>
    
    <section id="services" class="services">
        <h2 class="section-title">사업영역</h2>
        <div class="service-grid">
            <div class="service-card" onclick="location.href='/thehada/realestate/'">
                <div class="service-number">01</div>
                <h3 class="service-title">부동산 컨설팅</h3>
                <p class="service-subtitle">Real Estate Consulting</p>
                <p class="service-desc">공장 및 창고 전문 부동산 중개<br>맞춤형 산업용 부동산 솔루션</p>
                <a href="/thehada/realestate/" class="service-btn">자세히 보기</a>
            </div>
            
            <div class="service-card" onclick="location.href='/thehada/portfolio/'">
                <div class="service-number">02</div>
                <h3 class="service-title">시공 컨설팅</h3>
                <p class="service-subtitle">Construction Consulting</p>
                <p class="service-desc">축적된 경험과 노하우<br>성공적인 프로젝트 수행</p>
                <a href="/thehada/portfolio/" class="service-btn">포트폴리오</a>
            </div>
            
            <div class="service-card" onclick="window.open('https://aha-251226.github.io/home', '_blank')">
                <div class="service-number">03</div>
                <h3 class="service-title">연구 컨설팅</h3>
                <p class="service-subtitle">Research Consulting</p>
                <p class="service-desc">BIM, AI, LLM 기반<br>최첨단 건설 연구 컨설팅</p>
                <a href="https://aha-251226.github.io/home" target="_blank" class="service-btn">연구 홈페이지</a>
            </div>
        </div>
    </section>
    
    <footer>
        <p>&copy; 2025 THEHADA. All rights reserved.</p>
    </footer>
</body>
</html>