# Invitation28
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lita's Birthday Invitation</title>
<style>
  body {
    margin: 0;
    font-family: 'Arial', sans-serif;
    background: linear-gradient(to bottom, #000000, #1a1a1a);
    color: #FFD700;
    text-align: center;
    overflow-x: hidden;
  }
  .container {
    padding: 50px 20px;
    opacity: 0;
    animation: fadeIn 2s forwards;
  }
  h1 {
    font-size: 3em;
    margin-bottom: 10px;
  }
  h2 {
    font-size: 1.5em;
    margin-bottom: 30px;
  }
  p {
    font-size: 1.2em;
    margin: 10px 0;
  }
  a {
    color: #FFD700;
    text-decoration: none;
  }
  #countdown {
    font-size: 2em;
    margin: 20px 0;
  }
  @keyframes fadeIn {
    to { opacity: 1; }
  }
  .map {
    width: 100%;
    max-width: 600px;
    height: 400px;
    margin: 20px auto;
    border: 2px solid #FFD700;
    border-radius: 10px;
  }
</style>
</head>
<body>
<div class="container">
  <h1>🎉 LITA’S BIRTHDAY</h1>
  <h2>✨ A Night to Remember — Let’s Celebrate Together</h2>
  <p>📅 Tuesday, October 28, 2025</p>
  <p>🕖 7:00 PM</p>
  <p>📍 Black Owl, Surabaya</p>
  <iframe class="map" 
    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3952.123456789!2d112.737!3d-7.249!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2dd7fb7!2sBlack%20Owl%20Surabaya!5e0!3m2!1sen!2sid!4v1690000000000!5m2!1sen!2sid"
    allowfullscreen="" loading="lazy"></iframe>
  <p>👗 Dresscode: Black</p>
  <p>💬 RSVP via WhatsApp: <a href="https://wa.me/6289633340703" target="_blank">+62 896-3334-0703</a></p>
  <p>💫 Black & Gold Elegant Theme</p>
  <div id="countdown"></div>
</div>

<audio id="bg-music" autoplay loop>
  <source src="https://cdn.pixabay.com/download/audio/2023/05/05/audio_123456.mp3?filename=lounge-music-ambient-12345.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>

<script>
  // Countdown Timer
  const eventDate = new Date("October 28, 2025 19:00:00").getTime();
  const countdown = document.getElementById("countdown");

  function updateCountdown() {
    const now = new Date().getTime();
    const distance = eventDate - now;

    if(distance < 0) {
      countdown.innerHTML = "🎉 The party is on! 🎉";
      clearInterval(timerInterval);
      return;
    }

    const days = Math.floor(distance / (1000 * 60 * 60 * 24));
    const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    const seconds = Math.floor((distance % (1000 * 60)) / 1000);

    countdown.innerHTML = `${days}d ${hours}h ${minutes}m ${seconds}s`;
  }

  const timerInterval = setInterval(updateCountdown, 1000);
  updateCountdown();
</script>
</body>
</html>
