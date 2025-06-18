<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>ZZONE99</title>
<style>
  /* Reset */
  * {
    margin: 0; padding: 0; box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  body {
    background: linear-gradient(135deg, #00f0ff, #001522);
    color: #e0f7ff;
    min-height: 100vh;
    overflow-x: hidden;
  }
  /* Glow arka plan */
  body::before {
    content: "";
    position: fixed;
    top: -50%; left: -50%;
    width: 200%; height: 200%;
    background: radial-gradient(circle at center, #40f0ff, transparent 70%);
    filter: blur(100px);
    z-index: 0;
  }
  /* Giriş animasyonu kapsayıcısı */
  #intro {
    position: fixed;
    top: 0; left: 0; width: 100vw; height: 100vh;
    background: #001522;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    z-index: 9999;
    text-align: center;
    padding: 20px;
  }
  /* Logo büyüme animasyonu */
  #intro img {
    width: 150px;
    animation: grow 2s ease forwards;
    filter: drop-shadow(0 0 15px #00ffff);
  }
  @keyframes grow {
    0% {
      transform: scale(0.5);
      opacity: 0;
    }
    100% {
      transform: scale(1);
      opacity: 1;
    }
  }
  /* Klan ismi ve slogan */
  #intro h1 {
    margin-top: 1rem;
    font-size: 3rem;
    color: #00ffff;
    text-shadow:
      0 0 10px #00ffff,
      0 0 20px #00e6ff,
      0 0 30px #00ccff,
      0 0 40px #0099cc;
  }
  #intro p {
    color: #a0e7ff;
    font-style: italic;
    margin-top: 0.5rem;
    font-size: 1.2rem;
    text-shadow: 0 0 10px #007799;
  }
  /* KLANA KATIL butonu */
  #intro button {
    margin-top: 2rem;
    background: #00ffff;
    color: #001522;
    border: none;
    padding: 0.8rem 2rem;
    font-size: 1.2rem;
    font-weight: 700;
    border-radius: 30px;
    cursor: pointer;
    box-shadow:
      0 0 8px #00ffff,
      0 0 20px #00ccff;
    transition: background 0.3s ease;
  }
  #intro button:hover {
    background: #00ccff;
    box-shadow:
      0 0 15px #00ccff,
      0 0 30px #0099cc;
    color: #e0f7ff;
  }
  /* Fade out animasyonu */
  .fadeOut {
    animation: fadeOutAnim 1s forwards;
  }
  @keyframes fadeOutAnim {
    to {
      opacity: 0;
      visibility: hidden;
    }
  }
  /* Ana içerik */
  main {
    position: relative;
    z-index: 1;
    padding: 2rem;
    max-width: 900px;
    margin: 120px auto 40px auto;
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
  <button onclick="window.location.href='#basvuru'">KLANA KATIL</button>
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
  
  <!-- Başvuru formu örneği -->
  <section id="basvuru" aria-label="Başvuru Formu" style="max-width: 400px; margin: 0 auto;">
    <h2 style="color:#00ffff; text-align:center; margin-bottom: 1rem;">KLANA KATIL</h2>
    <form action="https://formspree.io/f/xldnljve" method="POST" style="display:flex; flex-direction: column; gap: 12px;">
      <input type="text" name="uid" placeholder="UID" required style="padding:10px; border-radius:6px; border:none;"/>
      <input type="text" name="oyun_ismi" placeholder="Oyun İsmi" required style="padding:10px; border-radius:6px; border:none;"/>
      <input type="text" name="isim" placeholder="İsim" required style="padding:10px; border-radius:6px; border:none;"/>
      <input type="number" name="yas" placeholder="Yaş" required min="10" max="100" style="padding:10px; border-radius:6px; border:none;"/>
      <select name="cihaz" required style="padding:10px; border-radius:6px; border:none;">
        <option value="" disabled selected>Cihaz Seçiniz</option>
        <option value="Android">Android</option>
        <option value="iOS">iOS</option>
      </select>
      <select name="aktiflik" required style="padding:10px; border-radius:6px; border:none;">
        <option value="" disabled selected>Aktiflik Durumu</option>
        <option value="Günlük">Günlük</option>
        <option value="Haftalık">Haftalık</option>
        <option value="Aylık">Aylık</option>
      </select>
      <button type="submit" style="background:#00ffff; color:#001522; padding:12px; border:none; border-radius:30px; font-weight:bold; cursor:pointer; box-shadow:0 0 8px #00ffff;">Gönder</button>
    </form>
  </section>
</main>

<!-- Footer -->
<footer>
  Für die Famillia | SINCE 2018
</footer>

<script>
  // Giriş animasyonunu 2 saniyede gizle
  window.addEventListener('load', () => {
    setTimeout(() => {
      const intro = document.getElementById('intro');
      intro.classList.add('fadeOut');
      setTimeout(() => {
        intro.style.display = 'none';
      }, 1000);
    }, 2000);
  });
</script>
</body>

