<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>💖 Te Amo 💖</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(to bottom, #ffe6f0, #fff0f5);
      font-family: 'Segoe Script', cursive;
      overflow: hidden;
      text-align: center;
    }

    h1 {
      margin-top: 50px;
      font-size: 48px;
      color: #ff3399;
      text-shadow: 2px 2px #fff;
    }

    .mensaje {
      position: absolute;
      font-size: 24px;
      color: #ff66cc;
      animation: flotar 6s ease-in-out infinite;
      opacity: 0.8;
    }

    @keyframes flotar {
      0% {transform: translateY(100vh); opacity: 0;}
      50% {opacity: 1;}
      100% {transform: translateY(-100vh); opacity: 0;}
    }
  </style>
</head>
<body>
  <h1>💌 Te amo mucho 💌</h1>

  <script>
    const frases = [
      "Eres hermosa 🌸",
      "Te amo 💖",
      "Eres increible de verdad ✨",
      "la chica mas bonita de todo el planeta 💭",
      "Teamodoro 🌹",
      "Eres una chica fuerte nunca te rindas❤️"
    ];

    for (let i = 0; i < 30; i++) {
      let msg = document.createElement("div");
      msg.className = "mensaje";
      msg.innerText = frases[Math.floor(Math.random() * frases.length)];
      msg.style.left = Math.random() * window.innerWidth + "px";
      msg.style.top = Math.random() * window.innerHeight + "px";
      msg.style.animationDelay = (Math.random() * 5) + "s";
      document.body.appendChild(msg);
    }
  </script>
</body>
</html>
