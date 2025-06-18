<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1" />
<title>ZZONE99</title>
<style>
  /* Reset ve temel */
  * {
    margin:0; padding:0; box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  body {
    background: linear-gradient(135deg, #0d1f2d, #001a33);
    color: #00e5ff;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  /* Preloader açılış animasyonu */
  #preloader {
    position: fixed;
    z-index: 9999;
    background: #001a33;
    top:0;left:0;right:0;bottom:0;
    display: flex;
    justify-content:center;
    align-items:center;
    flex-direction: column;
    color: #00e5ff;
    font-size: 3rem;
    font-weight: 900;
    letter-spacing: 0.2em;
    user-select:none;
  }
  #preloader img {
    width: 100px;
    margin-bottom: 20px;
    filter: drop-shadow(0 0 5px #00e5ff);
    animation: glow 2s infinite alternate;
  }
  @keyframes glow {
    from { filter: drop-shadow(0 0 5px #00e5ff);}
    to { filter: drop-shadow(0 0 20px #00ffff);}
  }

  /* Ana konteyner */
  .container {
    max-width: 960px;
    width: 95%;
    margin-top: 140px;
    text-align: center;
    position: relative;
    z-index: 10;
  }

  /* Logo ve başlık */
  header {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 15px;
    margin-bottom: 25px;
  }
  header img {
    width: 80px;
    height: 80px;
    filter: drop-shadow(0 0 8px #00ffff);
    animation: logoGlow 3s infinite alternate;
  }
  @keyframes logoGlow {
    0% { filter: drop-shadow(0 0 8px #00ffff); }
    50% { filter: drop-shadow(0 0 20px #00e5ff);}
    100% { filter: drop-shadow(0 0 8px #00ffff);}
  }
  header h1 {
    font-size: 2.8rem;
    letter-spacing: 0.25em;
    text-shadow: 0 0 10px #00e5ff;
    user-select:none;
  }

  /* Liderler bölümü */
  #liderler {
    background: rgba(0, 229, 255, 0.1);
    border-radius: 12px;
    padding: 20px;
    margin-bottom: 30px;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 40px;
  }
  .lider {
    display: flex;
    flex-direction: column;
    align-items: center;
    color: #00e5ff;
    cursor: default;
    user-select:none;
    width: 140px;
  }
  .lider img {
    width: 100px;
    height: 100px;
    object-fit: contain;
    border-radius: 15px;
    margin-bottom: 10px;
    filter: drop-shadow(0 0 10px #00e5ff);
    transition: transform 0.3s ease;
  }
  .lider:hover img {
    transform: scale(1.1) rotate(5deg);
    filter: drop-shadow(0 0 25px #00ffff);
  }
  .lider .nick {
    font-weight: 700;
    font-size: 1.3rem;
    text-shadow: 0 0 8px #00e5ff;
    margin-bottom: 4px;
  }
  .lider .id {
    font-size: 0.9rem;
    color: #a0f9ff;
    font-style: italic;
  }

  /* Butonlar */
  .buttons {
    display: flex;
    justify-content: center;
    gap: 30px;
    margin-bottom: 40px;
    flex-wrap: wrap;
  }
  button, #tiktok-btn {
    background: #00e5ff;
    border: none;
    color: #001a33;
    font-weight: 700;
    padding: 15px 35px;
    border-radius: 50px;
    font-size: 1.1rem;
    cursor: pointer;
    box-shadow: 0 0 12px #00e5ff;
    transition: background 0.3s ease, color 0.3s ease;
    user-select:none;
  }
  button:hover, #tiktok-btn:hover {
    background: #00c4cc;
    color: #000d12;
  }

  /* TikTok Popup */
  #tiktok-popup {
    position: fixed;
    bottom: 80px;
    right: 20px;
    background: rgba(0, 229, 255, 0.12);
    border: 2px solid #00e5ff;
    padding: 15px 25px;
    border-radius: 12px;
    box-shadow: 0 0 20px #00e5ff;
    display: none;
    flex-direction: column;
    gap: 10px;
    min-width: 200px;
    z-index: 50;
  }
  #tiktok-popup.active {
    display: flex;
  }
  #tiktok-popup a {
    color: #00e5ff;
    text-decoration: none;
    font-weight: 600;
    font-size: 1.1rem;
    transition: color 0.3s ease;
  }
  #tiktok-popup a:hover {
    color: #00ffff;
    text-shadow: 0 0 5px #00e5ff;
  }

  /* Başvuru formu modal */
  #basvuru-modal {
    position: fixed;
    top:0;left:0;right:0;bottom:0;
    background: rgba(0, 0, 0, 0.8);
    display: none;
    justify-content: center;
    align-items: center;
    z-index: 100;
    padding: 15px;
  }
  #basvuru-modal.active {
    display: flex;
  }
  #basvuru-form {
    background: #001a33;
    border-radius: 15px;
    padding: 25px 30px;
    width: 100%;
    max-width: 420px;
    color: #00e5ff;
    box-shadow: 0 0 20px #00e5ff;
    user-select:none;
  }
  #basvuru-form label {
    display: block;
    margin-bottom: 6px;
    font-weight: 600;
    text-align: left;
  }
  #basvuru-form input, #basvuru-form select {
    width: 100%;
    padding: 10px 12px;
    margin-bottom: 15px;
    border-radius: 8px;
    border: none;
    font-size: 1rem;
    font-family: inherit;
    outline: none;
  }
  #basvuru-form input:focus, #basvuru-form select:focus {
    box-shadow: 0 0 8px #00ffff;
  }
  #basvuru-form button[type="submit"] {
    width: 100%;
    background: #00e5ff;
    border: none;
    padding: 12px;
    border-radius: 50px;
    font-weight: 700;
    cursor: pointer;
    color: #001a33;
    font-size: 1.1rem;
    box-shadow: 0 0 15px #00e5ff;
    transition: background 0.3s ease;
  }
  #basvuru-form button[type="submit"]:hover {
    background: #00c4cc;
  }
  #basvuru-feedback {
    margin-top: 8px;
    font-weight: 600;
    font-size: 0.9rem;
  }
  #basvuru-feedback.error {
    color: #ff3333;
  }

  /* Ziyaretçi sayacı */
  #visitor-counter {
    width: 100%;
    max-width: 960px;
    background: rgba(0, 229, 255, 0.1);
    border-radius: 15px;
    overflow: hidden;
    margin-bottom: 40px;
    box-shadow: 0 0 10px #00e5ff;
  }
  #visitor-bar {
    height: 25px;
    background: #00e5ff;
    width: 0;
    transition: width 1s ease;
  }
  #visitor-text {
    color: #00e5ff;
    font-weight: 700;
    padding: 6px 12px;
    user-select:none;
    text-align: center;
  }

  /* Footer */
  footer {
    margin: 40px 0 20px;
    color: #00787f;
    font-weight: 600;
    font-size: 1rem;
    letter-spacing: 0.12em;
    user-select:none;
    text-align: center;
  }
  footer .famiilla {
    font-weight: 900;
    font-size: 1.4rem;
    margin-bottom: 5px;
    color: #00e5ff;
    text-shadow: 0 0 12px #00ffff;
  }
  footer .since {
    font-style: italic;
    font-weight: 500;
    color: #00aabb;
  }

  /* Responsive */
  @media (max-width: 600px) {
    header {
      flex-direction: column;
      gap: 8px;
    }
    header h1 {
      font-size: 2rem;
    }
    .lider {
      width: 100px;
    }
    .lider img {
      width: 80px;
      height: 80px;
    }
    .buttons {
      flex-direction: column;
      gap: 18px;
    }
    button, #tiktok-btn {
      width: 100%;
      padding: 15px 0;
      font-size: 1.2rem;
      border-radius: 12px;
    }
    #basvuru-form {
      padding: 20px;
    }
  }
</style>
</head>
<body>

<!-- Açılış animasyonu (Preloader) -->
<div id="preloader">
  <img src="logo.png" alt="ZZONE99 Logo" />
  ZZONE99
</div>

<div class="container" role="main" aria-label="Ana içerik">

  <!-- Başlık ve logo -->
  <header>
    <img src="logo.png" alt="ZZONE99 Logo" />
    <h1>ZZONE99</h1>
  </header>

  <!-- Liderler bölümü -->
  <section id="liderler" aria-label="Liderler">
    <div class="lider" tabindex="0" aria-describedby="lider1-desc">
      <img src="mazz.png" alt="mAzz99 avatar" />
      <div class="nick">mAzz99</div>
      <div class="id" id="lider1-desc">516572604</div>
    </div>
    <div class="lider" tabindex="0" aria-describedby="lider2-desc">
      <img src="yazz.png" alt="yAzz99 avatar" />
      <div class="nick">yAzz99</div>
      <div class="id" id="lider2-desc">520654025</div>
    </div>
  </section>

  <!-- Butonlar -->
  <div class="buttons">
    <button id="basvuru-open-btn" aria-haspopup="dialog" aria-controls="basvuru-modal">KLANA KATIL</button>
    <button id="tiktok-btn" aria-expanded="false" aria-controls="tiktok-popup">TikTok Profilleri</button>
  </div>

  <!-- TikTok Popup -->
  <nav id="tiktok-popup" role="region" aria-label="TikTok Profilleri" tabindex="-1">
    <a href="https://www.tiktok.com/@mazz99theboss" target="_blank" rel="noopener" aria-label="mAzz99 TikTok profili">@mazz99theboss</a>
    <a href="https://www.tiktok.com/@babavizyondapm" target="_blank" rel="noopener" aria-label="babavizyondapm TikTok profili">@babavizyondapm</a>
  </nav>

  <!-- Başvuru Formu Modal -->
  <div id="basvuru-modal" role="dialog" aria-modal="true" aria-labelledby="basvuru-title" tabindex="-1">
    <form id="basvuru-form" action="https://formspree.io/f/xldnljve" method="POST" novalidate>
      <h2 id="basvuru-title" style="text-align:center; margin-bottom: 18px;">Klan Başvuru Formu</h2>
      <label for="uid">UID (Oyuncu Kimliği):</label>
      <input type="text" id="uid" name="UID" required autocomplete="off" />
      
      <label for="oyunIsmi">Oyun İsmi:</label>
      <input type="text" id="oyunIsmi" name="OyunIsmi" required autocomplete="off" />
      
      <label for="isim">Gerçek İsim:</label>
      <input type="text" id="isim" name="Isim" required autocomplete="off" />
      
      <label for="yas">Yaş:</label>
      <input type="number" id="yas" name="Yas" min="10" max="99" required autocomplete="off" />
      
      <label for="cihaz">Cihaz:</label>
      <select id="cihaz" name="Cihaz" required>
        <option value="" disabled selected>Seçiniz</option>
        <option value="Android">Android</option>
        <option value="iOS">iOS</option>
        <option value="PC">PC</option>
        <option value="Diğer">Diğer</option>
      </select>
      
      <label for="aktiflik">Aktiflik Durumu:</label>
      <select id="aktiflik" name="Aktiflik" required>
        <option value="" disabled selected>Seçiniz</option>
        <option value="Günlük">Günlük</option>
        <option value="Haftalık">Haftalık</option>
        <option value="Aylık">Aylık</option>
        <option value="Düşük">Düşük</option>
      </select>
      
      <button type="submit" aria-label="Başvuruyu Gönder">Başvur</button>
      <div id="basvuru-feedback" role="alert" aria-live="polite"></div>
    </form>
  </div>

  <!-- Ziyaretçi Sayacı -->
  <section id="visitor-counter" aria-label="Ziyaretçi Sayacı">
    <div id="visitor-text" aria-live="polite" aria-atomic="true">Ziyaretçi Sayısı: 0</div>
    <div id="visitor-bar"></div>
  </section>

</div>

<!-- Footer -->
<footer>
  <div class="famiilla">Für die Famiilla</div>
  <div class="since">SINCE 2018</div>
</footer>

<script>
  // Preloader 2 saniye sonra gizle
  window.addEventListener('load', () => {
    setTimeout(() => {
      const preloader = document.getElementById('preloader');
      if (preloader) preloader.style.display = 'none';
    }, 2000);
  });

  // Başvuru Modal açma/kapatma
  const basvuruBtn = document.getElementById('basvuru-open-btn');
  const basvuruModal = document.getElementById('basvuru-modal');
  const basvuruForm = document.getElementById('basvuru-form');
  const basvuruFeedback = document.getElementById('basvuru-feedback');

  basvuruBtn.addEventListener('click', () => {
    basvuruModal.classList.add('active');
    basvuruModal.focus();
  });
  basvuruModal.addEventListener('click', (e) => {
    if (e.target === basvuruModal) {
      basvuruModal.classList.remove('active');
      basvuruFeedback.textContent = '';
      basvuruFeedback.classList.remove('error');
      basvuruForm.reset();
    }
  });

  // Formspree AJAX gönderimi
  basvuruForm.addEventListener('submit', (e) => {
    e.preventDefault();
    basvuruFeedback.textContent = '';
    basvuruFeedback.classList.remove('error');

    const data = new FormData(basvuruForm);
    fetch(basvuruForm.action, {
      method: 'POST',
      body: data,
      headers: { 'Accept': 'application/json' }
    }).then(response => {
      if (response.ok) {
        basvuruFeedback.textContent = 'Başvurunuz başarıyla gönderildi! Teşekkürler.';
        basvuruForm.reset();
      } else {
        response.json().then(data => {
          if (data.errors) {
            basvuruFeedback.textContent = data.errors.map(e => e.message).join(', ');
          } else {
            basvuruFeedback.textContent = 'Başvuru gönderilirken hata oluştu.';
          }
          basvuruFeedback.classList.add('error');
        });
      }
    }).catch(() => {
      basvuruFeedback.textContent = 'İnternet bağlantınızı kontrol edin.';
      basvuruFeedback.classList.add('error');
    });
  });

  // TikTok popup aç/kapa
  const tiktokBtn = document.getElementById('tiktok-btn');
  const tiktokPopup = document.getElementById('tiktok-popup');
  tiktokBtn.addEventListener('click', () => {
    const isActive = tiktokPopup.classList.toggle('active');
    tiktokBtn.setAttribute('aria-expanded', isActive);
    if (isActive) tiktokPopup.focus();
  });

  // Ziyaretçi sayacı (basit demo, localStorage ile sayar)
  const visitorText = document.getElementById('visitor-text');
  const visitorBar = document.getElementById('visitor-bar');
  function updateVisitorCount() {
    let count = localStorage.getItem('zzone99VisitorCount') || 0;
    count = parseInt(count, 10) + 1;
    localStorage.setItem('zzone99VisitorCount', count);
    visitorText.textContent = `Ziyaretçi Sayısı: ${count}`;
    // Bar genişliğini max 1000 ziyaretçi baz al
    let widthPercent = Math.min(100, (count / 1000) * 100);
    visitorBar.style.width = widthPercent + '%';
  }
  updateVisitorCount();

</script>
</body>

