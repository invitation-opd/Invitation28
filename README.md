<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Lita’s Birthday</title>
  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background-color: #000;
      color: #f5c542;
      text-align: center;
      overflow-x: hidden;
    }
    header {
      background: linear-gradient(to bottom, #111, #000);
      padding: 80px 20px;
    }
    h1 {
      font-size: 48px;
      margin: 0;
      color: #f5c542;
    }
    h2 {
      color: #fff;
      font-weight: 300;
    }
    section {
      padding: 60px 20px;
    }
    .countdown {
      font-size: 24px;
      color: #fff;
      margin-top: 20px;
    }
    .button {
      display: inline-block;
      padding: 14px 28px;
      margin-top: 30px;
      background-color: #f5c542;
      color: #000;
      border-radius: 6px;
      font-weight: bold;
      text-decoration: none;
      transition: 0.3s;
    }
    .button:hover {
      background-color: #fff;
      color: #000;
    }
    iframe {
      border: none;
      width: 90%;
      height: 300px;
      border-radius: 10px;
    }
    footer {
      background: #111;
      padding: 30px;
      font-size: 14px;
      color: #888;
    }
    .fade-in {
      opacity: 0;
      transform: translateY(20px);
      animation: fadeIn 1.2s forwards;
    }
    @keyframes fadeIn {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    audio {
      display: none;
    }
  </style>
</head>
<body>

  <!-- Musik -->
  <audio autoplay loop>
    <source src="https://cdn.pixabay.com/download/audio/2022/02/15/audio_4a89dd62d2.mp3" type="audio/mpeg">
  </audio>

  <!-- Header -->
  <header class="fade-in">
    <h1>Lita’s Birthday</h1>
    <h2>Ulang Tahun ke-32</h2>
    <p>Selasa, 28 Oktober 2025 • Pukul 19.00 WIB<br>Black Owl, Surabaya</p>
    <p><b>Dresscode:</b> Hitam Elegan 🖤</p>
  </header>

  <!-- Countdown -->
  <section class="fade-in">
    <h2>Hitung Mundur Menuju Hari Spesial 🎉</h2>
    <div class="countdown" id="countdown"></div>
  </section>

  <!-- Sambutan -->
  <section class="fade-in">
    <h2>Pesan dari Lita 💌</h2>
    <p>Terima kasih sudah jadi bagian dari momen spesial ini.<br>
    Aku berharap kebersamaan kita selalu indah dan penuh tawa 💕</p>
  </section>

  <!-- Lokasi -->
  <section class="fade-in">
    <h2>Lokasi Acara 📍</h2>
    <iframe 
      src="https://www.google.com/maps?q=Black+Owl+Surabaya&output=embed"
      allowfullscreen>
    </iframe>
  </section>

  <!-- RSVP -->
  <section class="fade-in">
    <h2>Konfirmasi Kehadiran 💬</h2>
    <a class="button" href="https://wa.me/6289633340703?text=Hai%20Lita!%20Saya%20akan%20datang%20ke%20ulang%20tahunmu%20🥳" target="_blank">
      RSVP via WhatsApp
    </a>
  </section>

  <!-- Footer -->
  <footer>
    <p>© 2025 Lita’s Birthday • Made with 💛 Elegan Hitam & Emas</p>
  </footer>

  <script>
    // Countdown Script
    const countdownDate = new Date("Oct 28, 2025 19:00:00").getTime();
    const timer = setInterval(() => {
      const now = new Date().getTime();
      const distance = countdownDate - now;
      const days = Math.floor(distance / (1000 * 60 * 60 * 24));
      const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      const seconds = Math.floor((distance % (1000 * 60)) / 1000);

      document.getElementById("countdown").innerHTML =
        days + " hari " + hours + " jam " + minutes + " menit " + seconds + " detik";

      if (distance < 0) {
        clearInterval(timer);
        document.getElementById("countdown").innerHTML = "Selamat Ulang Tahun Lita 🎂🎉";
      }
    }, 1000);
  </script>

</body>
</html>
