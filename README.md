# Happy-Women-s-Day-From-11A2
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Women’s Day From 11A2 💖</title>
<style>
  body {
    margin: 0;
    padding: 0;
    overflow: hidden;
    background: linear-gradient(135deg, #ffe6f2, #ffb6c1, #ffffff);
    background-size: 300% 300%;
    animation: gradientShift 12s ease infinite;
    font-family: 'Poppins', sans-serif;
    color: #d63384;
    text-align: center;
  }

  @keyframes gradientShift {
    0% {background-position: 0% 50%;}
    50% {background-position: 100% 50%;}
    100% {background-position: 0% 50%;}
  }

  h1 {
    margin-top: 30vh;
    font-size: 2.2em;
    text-shadow: 0 0 15px #fff, 0 0 25px #ff80bf;
    animation: fadeZoom 3s ease-in-out;
  }

  h2 {
    font-size: 1.3em;
    font-weight: normal;
    text-shadow: 0 0 10px #fff, 0 0 10px #ffb6c1;
    animation: fadeIn 4s ease-in-out;
  }

  footer {
    position: fixed;
    bottom: 15px;
    width: 100%;
    font-size: 1em;
    color: #d63384;
    text-shadow: 0 0 10px #fff;
    animation: fadeIn 5s ease-in-out;
  }

  @keyframes fadeZoom {
    from {opacity: 0; transform: scale(0.8);}
    to {opacity: 1; transform: scale(1);}
  }

  @keyframes fadeIn {
    from {opacity: 0;}
    to {opacity: 1;}
  }

  .heart {
    position: fixed;
    bottom: 0;
    width: 20px;
    height: 20px;
    background: #ff99cc;
    transform: rotate(45deg);
    animation: floatUp 6s ease-in infinite;
  }
  .heart::before, .heart::after {
    content: "";
    position: absolute;
    width: 20px;
    height: 20px;
    background: inherit;
    border-radius: 50%;
  }
  .heart::before { top: -10px; left: 0; }
  .heart::after { left: 10px; top: 0; }

  @keyframes floatUp {
    0% {transform: translateY(0) rotate(45deg); opacity: 1;}
    100% {transform: translateY(-800px) rotate(45deg); opacity: 0;}
  }

  #music-btn {
    position: fixed;
    bottom: 20px;
    right: 20px;
    background-color: #ff69b4;
    color: white;
    border: none;
    border-radius: 50%;
    width: 60px;
    height: 60px;
    font-size: 26px;
    box-shadow: 0 0 15px rgba(255, 105, 180, 0.6);
    cursor: pointer;
    transition: transform 0.2s, background-color 0.3s;
    z-index: 9999;
  }
  #music-btn:hover {
    transform: scale(1.1);
    background-color: #ff85c1;
  }
</style>
</head>
<body>
  <h1>💐 Happy Women’s Day From 11A2! 💖</h1>
  <h2>Wish all the girls a wonderful and joyful day!</h2>
  <footer>From 11A2 with love 💗</footer>

  <audio id="bg-music" loop>
    <source src="music/Beautiful_in_White.mp3" type="audio/mpeg">
  </audio>

  <button id="music-btn" onclick="toggleMusic()">🎵</button>

  <script>
  const music = document.getElementById("bg-music");
  const btn = document.getElementById("music-btn");
  let isPlaying = false;

  function toggleMusic() {
    if (isPlaying) {
      music.pause();
      btn.textContent = "🎵";
    } else {
      music.play();
      btn.textContent = "⏸️";
    }
    isPlaying = !isPlaying;
  }

  function createHeart() {
    const heart = document.createElement("div");
    heart.className = "heart";
    heart.style.left = Math.random() * 100 + "vw";
    const colors = ["#ff99cc", "#ffb6c1", "#ff80bf", "#ff69b4"];
    heart.style.background = colors[Math.floor(Math.random() * colors.length)];
    heart.style.animationDuration = (3 + Math.random() * 4) + "s";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 6000);
  }
  setInterval(createHeart, 300);
  </script>
</body>
</html>
