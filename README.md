<html lang="tr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>ZZONE99</title>

  <!-- Font Awesome TikTok ikonu için -->
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"
  />

  <style>
    /* Temel ve tema renkleri */
    body {
      margin: 0;
      background: linear-gradient(135deg, #000014 0%, #001022 100%);
      color: #00ffff;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      overflow-x: hidden;
      min-height: 100vh;
    }

    /* Preloader ekranı */
    #preloader {
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      background: linear-gradient(135deg, #000014, #001022);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      z-index: 9999;
      user-select: none;
    }

    /* Logo ve yazı bir arada */
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

    /* Shine efekti */
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

    /* Slogan */
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

    /* Particle efekti */
    #preloader .particles {
      position: absolute;
      width: 100%;
      height: 100%;
      top: 0; left: 0;
      pointer-events: none;
      overflow: visible;
      z-index: 0;
    }
    #preloader .particle {
      position: absolute;
      background: #00fff7;
      border-radius: 50%;
      opacity: 0.8;
      filter: drop-shadow(0 0 3px #00fff7);
      animation: floatParticle linear infinite;
    }
    #preloader .particle:nth-child(1) { width: 6px; height: 6px; top: 20%; left: 15%; animation-duration: 6s; animation-delay: 0s; }
    #preloader .particle:nth-child(2) { width: 4px; height: 4px; top: 50%; left: 80%; animation-duration: 8s; animation-delay: 2s; }
    #preloader .particle:nth-child(3) { width: 5px; height: 5px; top: 70%; left: 40%; animation-duration: 5s; animation-delay: 4s; }
    #preloader .particle:nth-child(4) { width: 3px; height: 3px; top: 30%; left: 60%; animation-duration: 7s; animation-delay: 1s; }
    #preloader .particle:nth-child(5) { width: 6px; height: 6px; top: 80%; left: 20%; animation-duration: 9s; animation-delay: 3s; }
    @keyframes floatParticle {
      0% { transform: translateY(0) translateX(0); opacity: 0.8; }
      50% { transform: translateY(-10px) translateX(5px); opacity: 1; }
      100% { transform: translateY(0) translateX(0); opacity: 0.8; }
    }

    /* Ana içerik gizli */
    #content {
      display: none;
      padding: 30px 15px 60px;
      max-width: 960px;
      margin: auto;
    }

    /* LİDERLER bölümü */
    #liderler {
      margin-top: 40px;
      text-align: center;
      color: #00ffff;
    }
    #liderler h2 {
      font-size: 2.4rem;
      font-weight: 900;
      margin-bottom: 25px;
      text-shadow:
        0 0 6px #00fff7,
        0 0 12px #00fff7;
      user-select: none;
    }
    #liderler .lider-list {
      display: flex;
      justify-content: center;
      gap: 50px;
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
      user-select: none;
    }
    #liderler .lider-item .nick {
      font-size: 1.6rem;
      font-weight: 700;
      letter-spacing: 0.05em;
      color: #00fff7;
      margin-bottom: 6px;
      user-select: text;
    }
    #liderler .lider-item .id {
      font-size: 1.1rem;
      color: #00bbbb;
      user-select: text;
    }
    #liderler .tiktok-links {
      margin-top: 10px;
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

    /* Başvuru formu */

    #basvuru {
      margin-top: 60px;
      background: #001222dd;
      border-radius: 16px;
      padding: 25px 20px;
      box-shadow: 0 0 15px #00fff7aa;
      max-width: 600px;
      margin-left: auto;
      margin-right: auto;
      color: #00ffff;
      user-select: none;
    }
    #basvuru h2 {
      text-align: center;
      font-size: 2rem;
      margin-bottom: 20px;
      font-weight: 900;
      text-shadow: 0 0 8px #00fff7;
    }

    #basvuru form {
      display: flex;
      flex-direction: column;
      gap: 15px;
    }
    #basvuru label {
      font-weight: 600;
      font-size: 1rem;
      margin-bottom: 4px;
      user-select: text;
    }
    #basvuru input,
    #basvuru select,
    #basvuru textarea {
      background: #000020;
      border: 1.8px solid #00fff7aa;
      border-radius: 10px;
      color: #00ffff;
      padding: 10px 14px;
      font-size: 1rem;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      transition: border-color 0.3s ease;
      resize: none;
    }
    #basvuru input:focus,
    #basvuru select:focus,
    #basvuru textarea:focus {
      outline: none;
      border-color: #00ffff;
      box-shadow: 0 0 10px #00fff7;
    }
    #basvuru button {
      margin-top: 10px;
      background: #00fff7;
      color: #000014;
      font-weight: 900;
      padding: 12px 0;
      border-radius: 12px;
      border: none;
      font-size: 1.2rem;
      cursor: pointer;
      transition: background 0.3s ease;
      user-select: none;
    }
    #basvuru button:hover {
      background: #00ccc9;
    }
    #basvuru .info-msg {
      margin-top: 15px;
      text-align: center;
      font-weight: 700;
      font-size: 1rem;
      color: #0ff;
      user-select: none;
    }

    /* Responsive */
    @media (max-width: 650px) {
      #liderler .lider-list {
        flex-direction: column;
        align-items: center;
      }
      #basvuru {
        max-width: 90%;
      }
    }
  </style>
</head>
<body>

  <!-- Preloader -->
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

  <!-- Site içeriği -->
  <div id="content">

    <!-- LİDERLER -->
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

    <!-- Başvuru Formu -->
    <section id="basvuru">
      <h2>Klana Katıl</h2>
      <form id="applyForm" action="https://formspree.io/f/xldnljve" method="POST" novalidate>
        <label for="uid">UID (Oyuncu ID):</label>
        <input type="text" id="uid" name="UID" required placeholder="Örnek: 123456789" />

        <label for="gameName">Oyun İsim (Nickname):</label>
        <input type="text" id="gameName" name="GameName" required placeholder="Oyundaki isminiz" />

        <label for="name">Gerçek İsim:</label>
        <input type="text" id="name" name="RealName" required placeholder="Adınız Soyadınız" />

        <label for="age">Yaş:</label>
        <input type="number" id="age" name="Age" min="12" max="99" required placeholder="Yaşınız" />

        <label for="device">Cihaz:</label>
        <select id="device" name="Device" required>
          <option value="">Cihazınızı seçin</option>
          <option value="Android">Android</option>
          <option value="iOS">iOS</option>
          <option value="PC">PC</option>
          <option value="Diğer">Diğer</option>
        </select>

        <label for="activity">Aktiflik Durumu:</label>
        <textarea id="activity" name="Activity" rows="3" placeholder="Ne sıklıkta oynuyorsunuz?" required></textarea>

        <button type="submit">Başvuruyu Gönder</button>
      </form>
      <div class="info-msg" id="formMessage" role="alert" aria-live="polite"></div>
    </section>

  </div>

  <script>
    // Preloader 2 saniye sonra gizle
    window.addEventListener('load', () => {
      setTimeout(() => {
        document.getElementById('preloader').style.display = 'none';
        document.getElementById('content').style.display = 'block';
      }, 2000);
    });

    // Basit form gönderim kontrolü ve mesaj gösterimi
    const form = document.getElementById('applyForm');
    const msg = document.getElementById('formMessage');

    form.addEventListener('submit', async (e) => {
      e.preventDefault();
      msg.textContent = "Başvurunuz gönderiliyor...";

      const formData = new FormData(form);

      try {
        const response = await fetch(form.action, {
          method: 'POST',
          body: formData,
          headers: {
            'Accept': 'application/json'
          }
        });
        if (response.ok) {
          msg.textContent = "Başvurunuz başarıyla gönderildi. Teşekkürler!";
          form.reset();
        } else {
          msg.textContent = "Başvuru gönderilirken bir hata oluştu. Lütfen tekrar deneyin.";
        }
      } catch (error) {
        msg.textContent = "Sunucuya bağlanırken sorun oluştu. İnternet bağlantınızı kontrol edin.";
      }
    });
  </script>
</body>

