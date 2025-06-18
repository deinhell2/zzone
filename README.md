<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>ZZONE99 PUBG Mobile Klanı</title>
<style>
  /* Genel Reset */
  * {
    margin: 0; padding: 0; box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  body {
    background: #0e1217;
    color: #00fff7;
    overflow-x: hidden;
  }
  /* Preloader (Giriş Animasyonu) */
  #preloader {
    position: fixed;
    inset: 0;
    background: #0e1217;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    z-index: 9999;
  }
  #preloader img {
    height: 120px;
    filter: drop-shadow(0 0 15px #00fff7);
    animation: pulseLogo 2s infinite ease-in-out;
  }
  #preloader h1 {
    margin-top: 15px;
    font-size: 4rem;
    font-weight: 900;
    letter-spacing: 8px;
    color: #00fff7;
    text-shadow: 0 0 20px #00fff7aa;
    animation: pulseText 2s infinite ease-in-out;
  }
  #preloader p {
    margin-top: 8px;
    font-size: 1.2rem;
    color: #00b3b3cc;
    font-weight: 600;
    letter-spacing: 3px;
    text-shadow: 0 0 15px #00b3b3aa;
    animation: pulseText 2s infinite ease-in-out;
  }
  @keyframes pulseLogo {
    0%,100% { filter: drop-shadow(0 0 15px #00fff7); transform: scale(1); }
    50% { filter: drop-shadow(0 0 30px #0ff); transform: scale(1.05); }
  }
  @keyframes pulseText {
    0%,100% { opacity: 1; text-shadow: 0 0 20px #00fff7aa; }
    50% { opacity: 0.7; text-shadow: 0 0 40px #0ff; }
  }
  @keyframes fadeOutPreloader {
    from { opacity: 1; }
    to { opacity: 0; }
  }
  
  /* Ana içerik */
  header {
    text-align: center;
    padding: 1rem 0;
  }
  header img {
    height: 70px;
    filter: drop-shadow(0 0 5px #00fff7);
  }
  header h2 {
    color: #00fff7;
    margin-top: 10px;
    font-size: 2.5rem;
    letter-spacing: 6px;
    text-shadow: 0 0 15px #00fff7aa;
  }
  
  /* Liderler Bölümü */
  #liderler {
    max-width: 1000px;
    margin: 2rem auto;
    display: flex;
    justify-content: center;
    gap: 50px;
    flex-wrap: wrap;
  }
  .lider {
    background: #111720cc;
    padding: 15px;
    border-radius: 15px;
    width: 200px;
    box-shadow: 0 0 15px #00fff7aa;
    text-align: center;
    transition: transform 0.3s ease;
  }
  .lider:hover {
    transform: scale(1.1);
  }
  .lider img {
    width: 100px;
    height: 100px;
    object-fit: contain;
    margin-bottom: 15px;
    filter: drop-shadow(0 0 10px #00fff7);
    background: transparent;
  }
  .lider .nick {
    font-size: 1.5rem;
    font-weight: 900;
    color: #00fff7;
    text-shadow: 0 0 10px #00fff7bb;
  }
  .lider .id {
    margin-top: 8px;
    font-size: 1rem;
    color: #00b3b3cc;
    font-weight: 600;
  }
  
  /* Klana Katıl Butonu Ortala */
  #basvuruBtn {
    display: block;
    margin: 2rem auto;
    padding: 12px 35px;
    font-size: 1.3rem;
    font-weight: 700;
    color: #0e1217;
    background: #00fff7;
    border: none;
    border-radius: 40px;
    cursor: pointer;
    box-shadow: 0 0 20px #00fff7bb;
    transition: background 0.3s ease;
  }
  #basvuruBtn:hover {
    background: #00d1ca;
  }
  
  /* Başvuru Popup */
  #basvuruPopup {
    position: fixed;
    top: 0; left: 0;
    width: 100vw; height: 100vh;
    background: rgba(14,18,23,0.95);
    display: none;
    justify-content: center;
    align-items: center;
    z-index: 10000;
  }
  #basvuruPopup.active {
    display: flex;
  }
  #basvuruPopup form {
    background: #111720;
    padding: 25px 30px;
    border-radius: 20px;
    max-width: 450px;
    width: 90%;
    box-shadow: 0 0 20px #00fff7aa;
  }
  #basvuruPopup form h3 {
    color: #00fff7;
    text-align: center;
    margin-bottom: 20px;
    font-size: 1.8rem;
    letter-spacing: 3px;
  }
  #basvuruPopup form label {
    display: block;
    color: #00b3b3cc;
    margin-bottom: 5px;
    font-weight: 600;
  }
  #basvuruPopup form input, #basvuruPopup form select {
    width: 100%;
    padding: 8px 10px;
    margin-bottom: 15px;
    border-radius: 10px;
    border: none;
    outline: none;
    font-size: 1rem;
  }
  #basvuruPopup form button {
    width: 100%;
    padding: 10px;
    background: #00fff7;
    color: #0e1217;
    font-weight: 700;
    font-size: 1.2rem;
    border-radius: 40px;
    cursor: pointer;
    border: none;
    transition: background 0.3s ease;
  }
  #basvuruPopup form button:hover {
    background: #00d1ca;
  }
  #basvuruPopup .closeBtn {
    position: absolute;
    top: 15px; right: 20px;
    font-size: 2rem;
    color: #00fff7;
    cursor: pointer;
  }
  
  /* Responsive */
  @media (max-width:600px) {
    #liderler {
      gap: 30px;
    }
    .lider {
      width: 140px;
      padding: 10px;
    }
    .lider img {
      width: 80px;
      height: 80px;
    }
    .lider .nick {
      font-size: 1.2rem;
    }
    #basvuruBtn {
      font-size: 1.1rem;
      padding: 10px 30px;
    }
  }
</style>
</head>
<body>

<!-- Preloader (Giriş Animasyonu) -->
<div id="preloader">
  <img src="logo.png" alt="ZZONE99 Logo" />
  <h1>ZZONE99</h1>
  <p>NE DENGEMİZ NE DENGİMİZ VAR ZZONE99 MARKA</p>
</div>

<header>
  <img src="logo.png" alt="ZZONE99 Logo" />
  <h2>ZZONE99</h2>
</header>

<section id="liderler">
  <div class="lider">
    <img src="mazz.png" alt="mAzz99" />
    <div class="nick">mAzz99</div>
    <div class="id">516572604</div>
  </div>
  <div class="lider">
    <img src="yazz.png" alt="yAzz99" />
    <div class="nick">yAzz99</div>
    <div class="id">520654025</div>
  </div>
</section>

<button id="basvuruBtn">KLANA KATIL</button>

<!-- Başvuru Popup -->
<div id="basvuruPopup">
  <span class="closeBtn" id="closePopup">&times;</span>
  <form action="https://formspree.io/f/xldnljve" method="POST">
    <h3>Başvuru Formu</h3>
    <label for="uid">UID</label>
    <input type="text" id="uid" name="UID" required />
    <label for="oyunismi">Oyun İsmi</label>
    <input type="text" id="oyunismi" name="Oyun_Ismi" required />
    <label for="isim">İsim</label>
    <input type="text" id="isim" name="İsim" required />
    <label for="yas">Yaş</label>
    <input type="number" id="yas" name="Yaş" required min="10" max="99" />
    <label for="cihaz">Cihaz</label>
    <select id="cihaz" name="Cihaz" required>
      <option value="" disabled selected>Seçiniz</option>
      <option value="Android">Android</option>
      <option value="iOS">iOS</option>
      <option value="PC">PC</option>
    </select>
    <label for="aktiflik">Aktiflik</label>
    <select id="aktiflik" name="Aktiflik" required>
      <option value="" disabled selected>Seçiniz</option>
      <option value="Günlük">Günlük</option>
      <option value="Haftalık">Haftalık</option>
      <option value="Aylık">Aylık</option>
    </select>
    <button type="submit">Başvur</button>
  </form>
</div>

<script>
  // Preloader yönetimi
  window.addEventListener('load', () => {
    const preloader = document.getElementById('preloader');
    preloader.style.animation = 'fadeOutPreloader 1s ease forwards';
    setTimeout(() => {
      preloader.style.display = 'none';
    }, 1000);
  });

  // Başvuru popup kontrolü
  const basvuruBtn = document.getElementById('basvuruBtn');
  const basvuruPopup = document.getElementById('basvuruPopup');
  const closePopup = document.getElementById('closePopup');

  basvuruBtn.addEventListener('click', () => {
    basvuruPopup.classList.add('active');
  });
  closePopup.addEventListener('click', () => {
    basvuruPopup.classList.remove('active');
  });
  // Popup dışına tıklayınca kapat
  window.addEventListener('click', e => {
    if(e.target === basvuruPopup){
      basvuruPopup.classList.remove('active');
    }
  });
</script>

</body>
