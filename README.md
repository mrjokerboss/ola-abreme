<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Para Ti 💖</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to bottom, #ffe6f0, #fff);
      font-family: 'Segoe UI', sans-serif;
      overflow: hidden;
    }

    h1 {
      text-align: center;
      margin-top: 20vh;
      font-size: 3em;
      color: #d63384;
      animation: fadeIn 2s ease-in-out;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .heart {
      position: absolute;
      width: 20px;
      height: 20px;
      background: url('https://upload.wikimedia.org/wikipedia/commons/thumb/f/f0/Heart_corazón.svg/1024px-Heart_corazón.svg.png') no-repeat center;
      background-size: contain;
      animation: fall 5s linear infinite;
    }

    @keyframes fall {
      0% { top: -50px; opacity: 1; }
      100% { top: 100vh; opacity: 0; }
    }
  </style>
</head>
<body>
  <h1>Gracias por estar aquí 💗</h1>

  <!-- Música suave de fondo -->
  <audio autoplay loop>
    <source src="https://www.bensound.com/bensound-music/bensound-sweet.mp3" type="audio/mpeg">
    Tu navegador no soporta audio HTML5.
  </audio>

  <!-- Corazones cayendo -->
  <script>
    function createHeart() {
      const heart = document.createElement('div');
      heart.className = 'heart';
      heart.style.left = Math.random() * window.innerWidth + 'px';
      heart.style.animationDuration = (3 + Math.random() * 2) + 's';
      document.body.appendChild(heart);

      setTimeout(() => heart.remove(), 5000);
    }

    setInterval(createHeart, 300);
  </script>
</body>
</html>

