<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>ZZONE99</title>

  <style>
    /* --- Orijinal site temel renkleri ve font */
    body {
      margin: 0;
      background: #000014;
      color: #00ffff;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      overflow-x: hidden;
    }

    /* --- Sayfa tam ortalama için flex container */
    #preloader {
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      background: #000014;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      z-index: 9999;
      user-select: none;
    }

    /* Logo ve ZZONE99 yazısı yan yana */
    #preloader .logo-text-wrapper {
      display: flex;
      align-items: center;
      gap: 20px;
      filter: drop-shadow(0 0 8px #0ff);
      cursor: default;
      position: relative;
    }

    #preloader .logo-text-wrapper:hover {
      filter: drop-shadow(0 0 20px #0ff);
      transform: scale(1.1) rotate(3deg);
      transition: all 0.3s ease;
    }

    #preloader img {
      width: 110px;
      border-radius: 12px;
      box-shadow: 0 0 10px #0ff88c;
      border: 2px solid #00ffd4aa;
      filter: drop-shadow(0 0 10px #00fffbaa);
      position: relative;
      z-index: 10;
      transition: all 0.3s ease;
    }

    #preloader .logo-text {
      font-size: 5rem;
      font-weight: 900;
      color: #00fff7;
      text-shadow:
        0 0 10px #00fff7,
        0 0 20px #00fff7,
        0 0 30px #00fff7,
        0 0 40px #0ff,
        0 0 70px #0ff;
      position: relative;
      user-select: none;
      z-index: 5;
      transition: all 0.3s ease;
    }

    #preloader .logo-text-wrapper:hover .logo-text {
      text-shadow:
        0 0 15px #00fff7,
        0 0 30px #00fff7,
        0 0 45px #00fff7,
        0 0 60px #0ff,
        0 0 100px #0ff;
    }

    /* Shine efekti - animasyonlu parlak çizgi */
    #preloader .shine-effect {
      position: absolute;
      top: 0; left: -75%;
      width: 50%; height: 100%;
      background: linear-gradient(120deg, transparent, rgba(255,255,255,0.3), transparent);
      transform: skewX(-20deg);
      animation: shine 3s linear infinite;
      pointer-events: none;
      border-radius: 12px;
      z-index: 20;
    }

    @keyframes shine {
      0% { left: -75%; }
      100% { left: 125%; }
    }

    /* Slogan altına ekleniyor */
    #preloader .slogan {
      margin-top: 15px;
      font-size: 1.3rem;
      font-weight: 600;
      color: #3ef0f7;
      text-shadow: 0 0 6px #00fff7;
      user-select: none;
      letter-spacing: 0.06em;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      text-align: center;
    }

    /* Particle efektleri için container */
    #preloader .particles {
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0; left: 0;
      pointer-events: none;
      overflow: visible;
      z-index: 0;
    }

    /* Particle elementleri */
    #preloader .particle {
      position: absolute;
      background: #00fff7;
      border-radius: 50%;
      opacity: 0.8;
      filter: drop-shadow(0 0 3px #00fff7);
      animation: floatParticle linear infinite;
    }

    /* Particle boyutları ve konumları */
    #preloader .particle:nth-child(1) {
      width: 6px; height: 6px;
      top: 20%; left: 15%;
      animation-duration: 6s;
      animation-delay: 0s;
    }
    #preloader .particle:nth-child(2) {
      width: 4px; height: 4px;
      top: 50%; left: 80%;
      animation-duration: 8s;
      animation-delay: 2s;
    }
    #preloader .particle:nth-child(3) {
      width: 5px; height: 5px;
      top: 70%; left: 40%;
      animation-duration: 5s;
      animation-delay: 4s;
    }
    #preloader .particle:nth-child(4) {
      width: 3px; height: 3px;
      top: 30%; left: 60%;
      animation-duration: 7s;
      animation-delay: 1s;
    }
    #preloader .particle:nth-child(5) {
      width: 6px; height: 6px;
      top: 80%; left: 20%;
      animation-duration: 9s;
      animation-delay: 3s;
    }

    @keyframes floatParticle {
      0% { transform: translateY(0) translateX(0); opacity: 0.8; }
      50% { transform: translateY(-10px) translateX(5px); opacity: 1; }
      100% { transform: translateY(0) translateX(0); opacity: 0.8; }
    }

    /* --- Ana site içeriği gizli başta, sonra gösterilecek */
    #content {
      display: none;
    }

    /* --- Responsive düzenleme */
    @media(max-width: 600px) {
      #preloader img {
        width: 70px;
      }
      #preloader .logo-text {
        font-size: 3rem;
      }
      #preloader .slogan {
        font-size: 1rem;
      }
    }

    /* --- LİDERLER bölümü */

    #liderler {
      margin: 50px auto;
      max-width: 900px;
      color: #00ffff;
      text-align: center;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }
    #liderler h2 {
      font-size: 2.4rem;
      font-weight: 900;
      margin-bottom: 25px;
      text-shadow:
        0 0 6px #00fff7,
        0 0 12px #00fff7;
    }

    #liderler .lider-list {
      display: flex;
      justify-content: center;
      gap: 60px;
      flex-wrap: wrap;
    }
    #liderler .lider-item {
      background: #001122;
      border-radius: 14px;
      padding: 20px;
      width: 200px;
      box-shadow: 0 0 10px #00fff7aa;
      transition: transform 0.3s ease;
      cursor: default;
    }
    #liderler .lider-item:hover {
      transform: scale(1.05);
      box-shadow: 0 0 18px #00fff7;
    }

    #liderler .lider-item img {
      width: 120px;
      border-radius: 12px;
      margin-bottom: 12px;
      filter: drop-shadow(0 0 6px #00fff7);
    }
    #liderler .lider-item .nick {
      font-size: 1.6rem;
      font-weight: 700;
      letter-spacing: 0.05em;
      color: #00fff7;
      margin-bottom: 6px;
      user-select: none;
    }
    #liderler .lider-item .id {
      font-size: 1.1rem;
      color: #00bbbb;
      user-select: text;
    }

    /* --- TikTok sosyal medya ikonları */
    #liderler .tiktok-links {
      margin-top: 15px;
      display: flex;
      justify-content: center;
      gap: 18px;
    }
    #liderler .tiktok-links a {
      color: #00ffff;
      font-size: 2rem;
      transition: color 0.3s ease;
      text-decoration: none;
    }
    #liderler .tiktok-links a:hover {
      color: #00fff7aa;
    }

  </style>

  <!-- TikTok ikonları için font awesome cdn -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />

</head>
<body>

  <!-- Giriş ekranı (preloader) -->
  <div id="preloader" aria-label="Site giriş ekranı">
    <div class="logo-text-wrapper">
      <img src="logo.png" alt="ZZONE99 Logo" />
      <div class="logo-text">ZZONE99</div>
      <div class="shine-effect"></div>
    </div>
    <div class="slogan">NE DENGEMİZ NE DENGİMİZ VAR ZZONE MARKA</div>
    <div class="particles" aria-hidden="true">
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
      <div class="particle"></div>
    </div>
  </div>

  <!-- Ana site içeriği -->
  <div id="content">

    <!-- Diğer site içerik burada olacak -->
    <!-- ... -->
    
    <!-- LİDERLER kısmı -->
    <section id="liderler">
      <h2>LİDERLER</h2>
      <div class="lider-list">
        <div class="lider-item">
          <img src="mazz.png" alt="mAzz99 Logo" />
          <div class="nick">mAzz99</div>
          <div class="id">516572604</div>
          <div class="tiktok-links">
            <a href="https://www.tiktok.com/@mazz99theboss" target="_blank" rel="noopener noreferrer" aria-label="TikTok mAzz99">
              <i class="fab fa-tiktok"></i>
            </a>
          </div>
        </div>
        <div class="lider-item">
          <img src="yazz.png" alt="yAzz99 Logo" />
          <div class="nick">yAzz99</div>
          <div class="id">520654025</div>
          <div class="tiktok-links">
            <a href="https://www.tiktok.com/@babavizyondapm" target="_blank" rel="noopener noreferrer" aria-label="TikTok yAzz99">
              <i class="fab fa-tiktok"></i>
            </a>
          </div>
        </div>
      </div>
    </section>

    <!-- Buraya mevcut sitenin diğer içeriği gelecek (bozulmayacak) -->

  </div>

  <script>
    // 2 saniyelik preloader gizleme
    window.addEventListener('load', () => {
      setTimeout(() => {
        const preloader = document.getElementById('preloader');
        const content = document.getElementById('content');
        preloader.style.display = 'none';
        content.style.display = 'block';
      }, 2000);
    });
  </script>

</body>
