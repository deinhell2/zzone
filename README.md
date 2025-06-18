<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>ZZONE99 PUBG MOBILE KLANI</title>
<style>
  /* Reset ve genel ayarlar */
  * {
    margin: 0; padding: 0; box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  body {
    background: #0e1217;
    color: #a0f0f9;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  a {
    color: #26f7e6;
    text-decoration: none;
  }
  a:hover {
    text-decoration: underline;
  }

  /* Header ve logo */
  header {
    width: 100%;
    padding: 20px 10px;
    background: #0a0f14;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 20px;
    box-shadow: 0 0 10px #00fff7aa;
  }
  header img {
    height: 70px;
    animation: glowLogo 3s infinite alternate;
  }
  @keyframes glowLogo {
    0% { filter: drop-shadow(0 0 5px #00ffe4); }
    100% { filter: drop-shadow(0 0 15px #00fff7); }
  }
  header h1 {
    font-size: 2.8rem;
    letter-spacing: 3px;
    color: #00fff7;
    font-weight: 900;
    text-shadow: 0 0 10px #00fff7;
  }

  /* Menü */
  nav {
    width: 100%;
    background: #131b24;
    display: flex;
    justify-content: center;
    gap: 40px;
    padding: 10px 0;
  }
  nav button {
    background: #00fff7;
    border: none;
    padding: 10px 25px;
    border-radius: 30px;
    cursor: pointer;
    font-weight: 700;
    color: #0e1217;
    font-size: 1.1rem;
    box-shadow: 0 0 10px #00fff7bb;
    transition: background 0.3s;
  }
  nav button:hover {
    background: #0ff8ea;
  }

  /* Bölümler */
  section {
    width: 90%;
    max-width: 1200px;
    margin: 40px 0;
    background: #131b24cc;
    border-radius: 15px;
    padding: 25px 40px;
    box-shadow: 0 0 15px #00fff7aa;
  }
  section h2 {
    text-align: center;
    font-size: 2rem;
    margin-bottom: 25px;
    color: #00fff7;
    text-shadow: 0 0 10px #00fff7aa;
  }

  /* Klan Açıklaması */
  #klan-aciklama p {
    line-height: 1.7;
    font-size: 1.15rem;
    text-align: justify;
    color: #a0f0f9;
  }

  /* Liderler */
  #liderler {
    display: flex;
    justify-content: center;
    gap: 60px;
    flex-wrap: wrap;
  }
  .lider {
    background: #0a1620;
    border-radius: 12px;
    width: 220px;
    padding: 15px;
    box-shadow: 0 0 10px #00fff7aa;
    text-align: center;
    transition: transform 0.3s ease;
    cursor: pointer;
  }
  .lider:hover {
    transform: scale(1.05);
    box-shadow: 0 0 25px #00fff7;
  }
  .lider img {
    width: 150px;
    border-radius: 12px;
    margin-bottom: 15px;
    filter: drop-shadow(0 0 8px #00fff7);
  }
  .lider h3 {
    font-size: 1.3rem;
    color: #00fff7;
    margin-bottom: 5px;
  }
  .lider span {
    font-size: 1rem;
    color: #80f0f9;
  }

  /* TikTok Profilleri animasyonlu popup */
  #tiktok-profil {
    position: fixed;
    right: 20px;
    top: 50%;
    transform: translateY(-50%);
    background: #0a1821cc;
    padding: 10px;
    border-radius: 15px;
    box-shadow: 0 0 12px #00fff7cc;
    cursor: pointer;
    transition: width 0.4s ease;
    width: 50px;
    overflow: hidden;
    display: flex;
    align-items: center;
  }
  #tiktok-profil.expanded {
    width: 220px;
  }
  #tiktok-profil:hover {
    width: 220px;
  }
  #tiktok-profil img {
    width: 35px;
    margin-right: 10px;
    filter: drop-shadow(0 0 4px #00fff7);
  }
  #tiktok-links {
    display: flex;
    flex-direction: column;
    gap: 8px;
    opacity: 0;
    transition: opacity 0.3s ease;
    user-select: none;
  }
  #tiktok-profil.expanded #tiktok-links,
  #tiktok-profil:hover #tiktok-links {
    opacity: 1;
    user-select: auto;
  }
  #tiktok-links a {
    color: #00fff7;
    font-weight: 700;
    font-size: 1rem;
  }
  #tiktok-links a:hover {
    text-decoration: underline;
  }

  /* Başvuru Formu */
  form {
    max-width: 600px;
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    gap: 15px;
  }
  label {
    font-weight: 700;
    font-size: 1.1rem;
    color: #00fff7;
  }
  input, select, textarea {
    padding: 10px;
    border-radius: 8px;
    border: none;
    font-size: 1rem;
    outline: none;
  }
  input:focus, select:focus, textarea:focus {
    box-shadow: 0 0 8px #00fff7aa;
  }
  button[type="submit"] {
    background: #00fff7;
    border: none;
    font-weight: 900;
    padding: 12px 0;
    color: #0e1217;
    border-radius: 30px;
    cursor: pointer;
    font-size: 1.2rem;
    box-shadow: 0 0 10px #00fff7bb;
    transition: background 0.3s ease;
  }
  button[type="submit"]:hover {
    background: #0ff8ea;
  }

  /* İletişim */
  #iletisim {
    text-align: center;
  }
  #iletisim h3 {
    margin-bottom: 15px;
    font-size: 1.4rem;
    color: #00fff7;
  }
  #iletisim a {
    font-size: 1.5rem;
    color: #00fff7;
    margin: 0 10px;
    display: inline-block;
    transition: transform 0.3s ease;
  }
  #iletisim a:hover {
    transform: scale(1.2);
  }

  /* Kayan Logo ve Slogan Alt Kısım */
  footer {
    width: 100%;
    background: #0a0f14;
    padding: 10px 0;
    position: fixed;
    bottom: 0;
    left: 0;
    overflow: hidden;
    box-shadow: 0 -2px 10px #00fff7aa;
  }
  .marquee-wrapper {
    display: flex;
    align-items: center;
    height: 50px;
    overflow: hidden;
    position: relative;
  }
  .marquee-content {
    display: flex;
    align-items: center;
    animation: marqueeAnim 15s linear infinite;
  }
  .marquee-content img {
    height: 40px;
    margin-right: 15px;
    filter: drop-shadow(0 0 8px #00fff7);
  }
  .marquee-content span {
    font-size: 1.4rem;
    font-weight: 900;
    color: #00fff7;
    letter-spacing: 3px;
    text-shadow: 0 0 10px #00fff7bb;
    white-space: nowrap;
    user-select: none;
  }
  @keyframes marqueeAnim {
    0% { transform: translateX(100%); }
    100% { transform: translateX(-100%); }
  }

  /* Responsive */
  @media(max-width: 768px) {
    #liderler {
      gap: 30px;
      justify-content: center;
    }
    nav {
      gap: 15px;
      flex-wrap: wrap;
    }
    nav button {
      padding: 8px 15px;
      font-size: 1rem;
    }
    section {
      padding: 20px 20px;
    }
    #tiktok-profil.expanded, #tiktok-profil:hover {
      width: 160px;
    }
  }
</style>
</head>
<body>

<header>
  <img src="logo.png" alt="ZZONE99 Logo" />
  <h1>ZZONE99</h1>
</header>

<nav>
  <button onclick="scrollToSection('klan-aciklama')">Klan Hakkında</button>
  <button onclick="scrollToSection('liderler')">LİDERLER</button>
  <button onclick="scrollToSection('basvuru')">KLANA KATIL</button>
  <button onclick="scrollToSection('iletisim')">İLETİŞİM</button>
</nav>

<section id="klan-aciklama">
  <h2>Klan Hakkında</h2>
  <p>
   İlk olarak “Für die GANG” adıyla kurulan ekip, daha sonra “AREA323” adı altında yükselişini sürdürmüş,bugün ise yepyeni bir vizyonla ZZONE99 adıyla yoluna devam etmektedir.Hedefimiz sadece oyun kazanmak değil, aynı zamanda kaliteli bir topluluk oluşturmak.
    <br><br>
    "Ne dengemiz ne dengimiz var ZZONE99 marka!" sloganıyla hareket ederiz. Her zaman sınırları zorlar, yeni stratejiler geliştirir ve oyun içinde dayanışmayı en üst seviyeye çıkarırız. 
    <br><br>
    Bizim için sadece oyun değil, aynı zamanda bir aile olmak önemlidir. Klan üyelerimiz arasında karşılıklı saygı ve destek en öncelikli değerdir.
  </p>
</section>

<section id="liderler">
  <h2>LİDERLER</h2>
  <div id="liderler">
    <div class="lider">
      <img src="mazz.png" alt="mAzz99" />
      <h3>mAzz99</h3>
      <span>516572604</span>
    </div>
    <div class="lider">
      <img src="yazz.png" alt="yAzz99" />
      <h3>yAzz99</h3>
      <span>520654025</span>
    </div>
  </div>
</section>

<section id="basvuru">
  <h2>KLANA KATIL</h2>
  <form action="https://formspree.io/f/xldnljve" method="POST">
    <label for="uid">UID (Oyuncu ID'niz)</label>
    <input type="number" id="uid" name="UID" required placeholder="UID numaranızı girin" />
    
    <label for="oyunIsmi">Oyun İsim</label>
    <input type="text" id="oyunIsmi" name="OyunIsmi" required placeholder="Oyundaki nickinizi yazın" />
    
    <label for="isim">İsim</label>
    <input type="text" id="isim" name="Isim" required placeholder="Gerçek isminiz" />
    
    <label for="yas">Yaş</label>
    <input type="number" id="yas" name="Yas" required min="10" max="100" placeholder="Yaşınızı girin" />
    
    <label for="cihaz">Kullandığınız Cihaz</label>
    <select id="cihaz" name="Cihaz" required>
      <option value="" disabled selected>Cihaz seçin</option>
      <option value="Android">Android</option>
      <option value="iOS">iOS</option>
      <option value="Emülatör">Emülatör</option>
    </select>
    
    <label for="aktiflik">Aktiflik Durumu</label>
    <textarea id="aktiflik" name="Aktiflik" rows="3" placeholder="Günlük oynama süreniz, oyun içi aktifliğiniz vb." required></textarea>
    
    <button type="submit">Başvuruyu Gönder</button>
  </form>
</section>

<section id="iletisim">
  <h2>İLETİŞİM</h2>
  <h3>Bizi Takip Edin</h3>
  <div>
    <a href="https://www.tiktok.com/@mazz99theboss" target="_blank" aria-label="mAzz99 TikTok Profili">
      <img src="tiktok-icon.svg" alt="TikTok Icon" width="30" /> @mazz99theboss
    </a>
    <a href="https://www.tiktok.com/@babavizyondapm" target="_blank" aria-label="BabavizyondaPM TikTok Profili">
      <img src="tiktok-icon.svg" alt="TikTok Icon" width="30" /> @babavizyondapm
    </a>
  </div>
</section>

<!-- TikTok Profil Animasyonu -->
<div id="tiktok-profil" tabindex="0" role="button" aria-expanded="false" aria-label="TikTok Profilleri">
  <img src="tiktok-icon.svg" alt="TikTok" />
  <div id="tiktok-links" aria-hidden="true">
    <a href="https://www.tiktok.com/@mazz99theboss" target="_blank">@mazz99theboss</a>
    <a href="https://www.tiktok.com/@babavizyondapm" target="_blank">@babavizyondapm</a>
  </div>
</div>

<footer>
  <div class="marquee-wrapper" aria-label="Kayan Logo ve Slogan">
    <div class="marquee-content" aria-hidden="true">
      <img src="logo.png" alt="" />
      <span>NE DENGEMİZ NE DENGİMİZ VAR ZZONE99 MARKA &nbsp;&nbsp;&nbsp;</span>
      <img src="logo.png" alt="" />
      <span>NE DENGEMİZ NE DENGİMİZ VAR ZZONE99 MARKA &nbsp;&nbsp;&nbsp;</span>
    </div>
  </div>
</footer>

<script>
  // Bölüme scroll
  function scrollToSection(id) {
    document.getElementById(id).scrollIntoView({ behavior: 'smooth' });
  }

  // TikTok Profil açma-kapama animasyonu
  const tiktokDiv = document.getElementById('tiktok-profil');
  tiktokDiv.addEventListener('click', () => {
    tiktokDiv.classList.toggle('expanded');
    const expanded = tiktokDiv.classList.contains('expanded');
    tiktokDiv.setAttribute('aria-expanded', expanded);
    document.getElementById('tiktok-links').setAttribute('aria-hidden', !expanded);
  });
  // Klavyeden erişim için enter tuşu
  tiktokDiv.addEventListener('keydown', (e) => {
    if (e.key === 'Enter' || e.key === ' ') {
      e.preventDefault();
      tiktokDiv.click();
    }
  });
</script>

</body>
