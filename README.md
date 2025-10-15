<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lita's Birthday Invitation</title>
<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Roboto:wght@400;700&display=swap" rel="stylesheet">
<style>
  body {
    margin: 0;
    font-family: 'Roboto', sans-serif;
    background: linear-gradient(135deg, #000000, #1a1a1a);
    color: #FFD700;
    text-align: center;
    overflow-x: hidden;
    position: relative;
  }

  /* Glitter effect overlay */
  body::before {
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    background: radial-gradient(circle, rgba(255,215,0,0.3) 1px, transparent 1px);
    background-size: 10px 10px;
    pointer-events: none;
    animation: glitter 3s infinite linear;
  }

  @keyframes glitter {
    0% {background-position: 0 0;}
    100% {background-position: 100px 100px;}
  }

  .container {
    position: relative;
    max-width: 700px;
    margin: 50px auto;
    background: rgba(0,0,0,0.8);
    border: 2px solid #FFD700;
    border-radius: 20px;
    padding: 40px 30px;
    box-shadow: 0 0 30px rgba(255, 215, 0, 0.5);
    opacity: 0;
    animation: fadeInSlide 2s forwards;
  }

  @keyframes fadeInSlide {
    0% {opacity: 0; transform: translateY(50px);}
    100% {opacity: 1; transform: translateY(0);}
  }

  h1 {
    font-family: 'Great Vibes', cursive;
    font-size: 3.5em;
    margin-bottom: 10px;
    text-shadow: 0 0 10px #FFD700;
  }

  h2 {
    font-size: 1.5em;
    margin-bottom: 30px;
  }

  p {
    font-size: 1.2em;
    margin: 10px 0;
  }

  a.button {
    display: inline-block;
    padding: 12px 25px;
    margin: 20px 0;
    font-weight: bold;
    color: #000;
    background: #FFD700;
    border-radius: 30px;
    text-decoration: none;
    box-shadow: 0 0 15px rgba(255,215,0,0.5);
    transition: all 0.3s ease;
  }

  a.button:hover {
    transform: scale(1.05);
    box-shadow: 0 0 25px rgba(255,215,0,0.8);
  }

  #countdown {
    font-size: 2em;
    margin: 25px 0;
    font-weight: bold;
    letter-spacing: 1px;
    text-shadow: 0 0 10px #FFD700;
  }

  .map {
    width: 100%;
    height: 350px;
    margin: 20px auto;
    border: 2px solid #FFD700;
    border-radius: 15px;
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
  <a href="https://wa.me/6289633340703" target="_blank" class="button">💬 RSVP via WhatsApp</a>
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
