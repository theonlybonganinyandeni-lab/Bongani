<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Panic Date 💖</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');
    body {
      margin: 0;
      padding: 0;
      font-family: 'Poppins', sans-serif;
      height: 100vh;
      overflow: hidden;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background: radial-gradient(circle at center, #ffeef7, #ffd6e8, #ffc6e0);
      position: relative;
    }

    h1 {
      color: #ff4b6e;
      font-size: 2.7em;
      text-shadow: 0 2px 4px rgba(0,0,0,0.1);
      margin-bottom: 0.2em;
    }

    h2 {
      color: #333;
      font-size: 1.2em;
      margin-bottom: 1em;
      text-align: center;
    }

    .box {
      background: rgba(255, 255, 255, 0.85);
      border-radius: 20px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.1);
      padding: 40px 30px;
      text-align: center;
      z-index: 2;
    }

    button {
      background: #ff4b6e;
      color: white;
      border: none;
      padding: 12px 30px;
      border-radius: 30px;
      font-size: 1em;
      cursor: pointer;
      transition: 0.3s ease;
    }

    button:hover {
      background: #ff1f52;
      transform: scale(1.05);
    }

    /* Floating hearts */
    .heart {
      position: absolute;
      bottom: 0;
      width: 20px;
      height: 20px;
      background: rgba(255, 75, 110, 0.7);
      transform: rotate(45deg);
      animation: floatUp 6s linear infinite;
    }

    .heart::before, .heart::after {
      content: '';
      position: absolute;
      width: 20px;
      height: 20px;
      background: rgba(255, 75, 110, 0.7);
      border-radius: 50%;
    }

    .heart::before { top: -10px; left: 0; }
    .heart::after { left: -10px; top: 0; }

    @keyframes floatUp {
      0% { transform: translateY(0) scale(1) rotate(45deg); opacity: 1; }
      100% { transform: translateY(-100vh) scale(0.5) rotate(45deg); opacity: 0; }
    }

    /* Soft animated glow background */
    .glow {
      position: absolute;
      width: 200px;
      height: 200px;
      background: radial-gradient(circle, rgba(255,255,255,0.4), transparent);
      border-radius: 50%;
      animation: moveGlow 12s ease-in-out infinite;
      z-index: 0;
    }

    @keyframes moveGlow {
      0%, 100% { transform: translate(0, 0); }
      50% { transform: translate(100px, -100px); }
    }
  </style>
</head>
<body>
  <div class="glow"></div>
  <h1>Thandiwe Sithole 💖</h1>

  <div class="box">
    <h2>Will you go on a <strong>Panic Date</strong> with me between<br>October 27 – 31 ?</h2>
    <button onclick="sayYes()">Say Yes 💕</button>
  </div>

  <canvas id="confetti"></canvas>

  <script>
    // Floating hearts
    function createHeart() {
      const heart = document.createElement('div');
      heart.classList.add('heart');
      heart.style.left = Math.random() * 100 + 'vw';
      heart.style.animationDuration = (4 + Math.random() * 3) + 's';
      document.body.appendChild(heart);
      setTimeout(() => heart.remove(), 6000);
    }
    setInterval(createHeart, 300);

    // Confetti effect when she says yes
    const confettiCanvas = document.getElementById('confetti');
    const ctx = confettiCanvas.getContext('2d');
    confettiCanvas.width = window.innerWidth;
    confettiCanvas.height = window.innerHeight;

    let confetti = [];

    function randomColor() {
      const colors = ['#ff4b6e', '#ffd6e8', '#ff85a2', '#fff'];
      return colors[Math.floor(Math.random() * colors.length)];
    }

    function createConfetti() {
      confetti.push({
        x: Math.random() * confettiCanvas.width,
        y: Math.random() * confettiCanvas.height - confettiCanvas.height,
        size: Math.random() * 6 + 2,
        color: randomColor(),
        speed: Math.random() * 3 + 2
      });
    }

    function drawConfetti() {
      ctx.clearRect(0, 0, confettiCanvas.width, confettiCanvas.height);
      confetti.forEach((c, i) => {
        ctx.beginPath();
        ctx.arc(c.x, c.y, c.size, 0, 2 * Math.PI);
        ctx.fillStyle = c.color;
        ctx.fill();
        c.y += c.speed;
        if (c.y > confettiCanvas.height) confetti.splice(i, 1);
      });
      requestAnimationFrame(drawConfetti);
    }

    function sayYes() {
      alert('Yay! I can’t wait to go on our Panic Date 💞');
      for (let i = 0; i < 100; i++) createConfetti();
    }

    drawConfetti();
  </script>
</body>
</html>
