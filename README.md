<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>ZZONE99</title>
<style>
  /* Temel Reset */
  * {
    margin: 0; padding: 0; box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  body {
    background: linear-gradient(135deg, #001f3f, #0074D9);
    color: #e0f7ff;
    min-height: 100vh;
    overflow-x: hidden;
  }
  /* Giriş animasyonu kapsayıcısı */
  #intro {
    position: fixed;
    top: 0; left: 0; width: 100vw; height: 100vh;
    background: #001f3f;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    z-index: 9999;
  }
  /* Logo animasyonu */
  #intro img {
    width: 120px;
    animation: slideRight 3s ease forwards;
  }
  @keyframes slideRight {
    0% { transform: translateX(-150%); opacity: 0; }
    80% { transform: translateX(10px); opacity: 1; }
    100% { transform: translateX(0); opacity: 1; }
  }
  /* Klan ismi ve slogan */
  #intro h1 {
    color: #00ffff;
    font-size: 3rem;
    margin-top: 1rem;
    text-shadow: 0 0 15px #00ffff;
  }
  #intro p {
    color: #a0e7ff;
    margin-top: 0.5rem;
    font-size: 1.2rem;
    font-style: italic;
  }
  /* Giriş animasyonu gizleme animasyonu */
  .fadeOut {
    animation: fadeOutAnim 1s forwards;
  }
  @keyframes fadeOutAnim {
    to { opacity: 0; visibility: hidden; }
  }
  /* Ana içerik */
  main {
    padding: 2rem;
    max-width: 900px;
    margin: 100px auto 40px auto;
  }
  /* Açıklama */
  #description {
    background: rgba(0, 116, 217, 0.15);
    border-radius: 10px;
    padding: 20px;
    color: #d0e9ff;
    font-size: 1.1rem;
    line-height: 1.6;
    margin-bottom: 40px;
    text-align: center;
    box-shadow: 0 0 10px #0074D9;
  }
  /* Liderler bölümü */
  #leaders {
    display: flex;
    justify-content: center;
    gap: 3rem;
    flex-wrap: wrap;
    margin-bottom: 50px;
  }
  .leader-card {
    background: rgba(0, 116, 217, 0.2);
    border-radius: 15px;
    padding: 1rem 1.5rem;
    width: 180px;
    text-align: center;
    box-shadow: 0 0 15px #00ffff;
    transition: transform 0.3s ease;
  }
  .leader-card:hover {
    transform: scale(1.05);
    box-shadow: 0 0 25px #00ffff;
  }
  .leader-card img {
    width: 100px;
    border-radius: 50%;
    margin-bottom: 1rem;
    filter: drop-shadow(0 0 5px #00ffff);
  }
  .leader-card h3 {
    color: #00ffff;
    margin-bottom: 0.3rem;
    font-size: 1.3rem;
    text-shadow: 0 0 10px #00ffff;
  }
  .leader-card span {
    font-size: 0.9rem;
    color: #a0e7ff;
  }
  /* TikTok linkler */
  #contact {
    text-align: center;
    margin-bottom: 40px;
  }
  #contact h2 {
    color: #00ffff;
    margin-bottom: 1rem;
    text-shadow: 0 0 15px #00ffff;
  }
  .tiktok-links {
    display: flex;
    justify-content: center;
    gap: 2rem;
    flex-wrap: wrap;
  }
  .tiktok-links a {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    color: #00ffff;
    text-decoration: none;
    font-weight: 600;
    font-size: 1.1rem;
    transition: color 0.3s ease;
  }
  .tiktok-links a:hover {
    color: #a0e7ff;
  }
  .tiktok-links img {
    width: 30px;
    filter: drop-shadow(0 0 5px #00ffff);
  }
  /* Footer */
  footer {
    text-align: center;
    padding: 15px 0;
    font-size: 1rem;
    color: #00ffff;
    letter-spacing: 2px;
    text-shadow: 0 0 15px #00ffff;
    border-top: 1px solid #0074D9;
  }
  /* Responsive */
  @media (max-width: 600px) {
    #leaders {
      gap: 2rem;
    }
    .leader-card {
      width: 140px;
      padding: 1rem;
    }
    #intro h1 {
      font-size: 2rem;
    }
    #intro p {
      font-size: 1rem;
      max-width: 250px;
    }
  }
</style>
</head>
<body>

<!-- Giriş Animasyonu -->
<div id="intro">
  <img src="logo.png" alt="ZZONE99 Logo" />
  <h1>ZZONE99</h1>
  <p>NE DENGEMİZ NE DENGİMİZ VAR ZZONE MARKA</p>
</div>

<!-- Ana içerik -->
<main>
  <!-- Açıklama -->
  <section id="description">
    <p>
      İlk olarak “Für die GANG” adıyla kurulan ekip, daha sonra “AREA323” adı altında yükselişini sürdürmüş,        
      bugün ise yepyeni bir vizyonla ZZONE99 adıyla yoluna devam etmektedir.<br />
      Hedefimiz sadece oyun kazanmak değil, aynı zamanda kaliteli bir topluluk oluşturmaktır.
    </p>
  </section>

  <!-- Liderler Bölümü -->
  <section id="leaders" aria-label="Liderler">
    <div class="leader-card">
      <img src="mazz.png" alt="mAzz99 Logo" />
      <h3>mAzz99</h3>
      <span>ID: 516572604</span>
    </div>
    <div class="leader-card">
      <img src="yazz.png" alt="yAzz99 Logo" />
      <h3>yAzz99</h3>
      <span>ID: 520654025</span>
    </div>
  </section>

  <!-- İletişim -->
  <section id="contact" aria-label="İletişim">
    <h2>İletişim</h2>
    <div class="tiktok-links">
      <a href="https://www.tiktok.com/@mazz99theboss" target="_blank" rel="noopener noreferrer">
        <img src="tiktok-icon.png" alt="TikTok Icon" /> @mazz99theboss
      </a>
      <a href="https://www.tiktok.com/@babavizyondapm" target="_blank" rel="noopener noreferrer">
        <img src="tiktok-icon.png" alt="TikTok Icon" /> @babavizyondapm
      </a>
    </div>
  </section>
</main>

<!-- Footer -->
<footer>
  Für die Famillia | SINCE 2018
</footer>

<script>
  // Giriş animasyonunu yavaşlat ve gizle
  window.addEventListener('load', () => {
    setTimeout(() => {
      const intro = document.getElementById('intro');
      intro.classList.add('fadeOut');
      setTimeout(() => {
        intro.style.display = 'none';
      }, 1000);
    }, 3000); // 3 saniyeye ayarlandı
  });
</script>
</body>
