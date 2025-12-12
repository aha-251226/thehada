---
layout: splash
permalink: /
---

<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700;900&family=Montserrat:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Noto Sans KR', sans-serif;
            overflow-x: hidden;
            background: #fff;
        }
        
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: moveBackground 20s linear infinite;
        }
        
        @keyframes moveBackground {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }
        
        .hero-content {
            text-align: center;
            color: white;
            z-index: 1;
        }
        
        .hero h1 {
            font-family: 'Montserrat', sans-serif;
            font-size: 5rem;
            font-weight: 900;
            margin-bottom: 1rem;
            letter-spacing: -2px;
        }
        
        .hero p {
            font-size: 1.5rem;
            font-weight: 300;
            margin-bottom: 3rem;
            opacity: 0.9;
        }
        
        .scroll-indicator {
            position: absolute;
            bottom: 50px;
            left: 50%;
            transform: translateX(-50%);
            color: white;
            font-size: 2rem;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateX(-50%) translateY(0); }
            40% { transform: translateX(-50%) translateY(-20px); }
            60% { transform: translateX(-50%) translateY(-10px); }
        }
        
        .services {
            padding: 120px 5%;
            background: #fff;
        }
        
        .section-title {
            text-align: center;
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 80px;
            color: #1a1a1a;
        }
        
        .service-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 50px;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        .service-card {
            background: #fff;
            border-radius: 20px;
            padding: 50px 40px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.08);
            transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }
        
        .service-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(90deg, #667eea, #764ba2);
            transform: scaleX(0);
            transition: transform 0.4s;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 60px rgba(0,0,0,0.15);
        }
        
        .service-card:hover::before {
            transform: scaleX(1);
        }
        
        .service-number {
            font-family: 'Montserrat', sans-serif;
            font-size: 4rem;
            font-weight: 900;
            color: #f0f0f0;
            margin-bottom: 20px;
        }
        
        .service-title {
            font-size: 1.8rem;
            font-weight: 700;
            margin-bottom: 10px;
            color: #1a1a1a;
        }
        
        .service-subtitle {
            font-family: 'Montserrat', sans-serif;
            font-size: 1rem;
            font-weight: 400;
            color: #667eea;
            margin-bottom: 20px;
        }
        
        .service-desc {
            font-size: 1.05rem;
            line-height: 1.8;
            color: #666;
            margin-bottom: 30px;
        }
        
        .service-btn {
            display: inline-block;
            padding: 15px 35px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            transition: all 0.3s;
        }
        
        .service-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.4);
        }
        
        .about {
            padding: 120px 5%;
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
        }
        
        .about-content {
            max-width: 900px;
            margin: 0 auto;
            text-align: center;
        }
        
        .about-content h2 {
            font-size: 3rem;
            font-weight: 700;
            margin-bottom: 40px;
            color: #1a1a1a;
        }
        
        .about-content p {
            font-size: 1.3rem;
            line-height: 2;
            color: #444;
        }
        
        @media (max-width: 768px) {
            .hero h1 { font-size: 3rem; }
            .hero p { font-size: 1.2rem; }
            .section-title { font-size: 2rem; }
            .service-grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <section class="hero">
        <div class="hero-content">
            <h1>THEHADA</h1>
            <p>부동산 · 시공 · 연구 컨설팅</p>
        </div>
        <div class="scroll-indicator">↓</div>
    </section>
    
    <section class="services">
        <h2 class="section-title">Our Services</h2>
        <div class="service-grid">
            <div class="service-card" onclick="location.href='/thehada/realestate/'">
                <div class="service-number">01</div>
                <h3 class="service-title">부동산 컨설팅</h3>
                <p class="service-subtitle">Real Estate Consulting</p>
                <p class="service-desc">공장 및 창고 전문 부동산 중개<br>맞춤형 산업용 부동산 솔루션 제공</p>
                <a href="/thehada/realestate/" class="service-btn">자세히 보기</a>
            </div>
            
            <div class="service-card" onclick="location.href='/thehada/portfolio/'">
                <div class="service-number">02</div>
                <h3 class="service-title">시공 컨설팅</h3>
                <p class="service-subtitle">Construction Consulting</p>
                <p class="service-desc">축적된 경험과 노하우로<br>성공적인 프로젝트 수행</p>
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
    
    <section class="about">
        <div class="about-content">
            <h2>THEHADA</h2>
            <p>최신 기술과 풍부한 경험을 바탕으로<br>고객의 성공을 지원하는 전문 컨설팅 기업입니다</p>
        </div>
    </section>
</body>
</html>