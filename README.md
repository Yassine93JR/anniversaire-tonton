<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Joyeux anniversaire tonton</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: Arial, Helvetica, sans-serif;
    }

    body {
      min-height: 100vh;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      background: linear-gradient(135deg, #12001f, #3b0066, #ff4fd8, #ffd700);
      background-size: 400% 400%;
      animation: fondAnime 8s ease infinite;
      color: white;
      text-align: center;
    }

    @keyframes fondAnime {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    .carte {
      width: 90%;
      max-width: 430px;
      padding: 35px 22px;
      border-radius: 30px;
      background: rgba(255, 255, 255, 0.13);
      backdrop-filter: blur(12px);
      box-shadow: 0 0 35px rgba(255, 255, 255, 0.35);
      border: 2px solid rgba(255, 255, 255, 0.25);
      animation: entrer 1.2s ease;
      position: relative;
      z-index: 2;
    }

    @keyframes entrer {
      from { transform: scale(0.8); opacity: 0; }
      to { transform: scale(1); opacity: 1; }
    }

    h1 {
      font-size: 2.7rem;
      line-height: 1.1;
      margin-bottom: 20px;
      text-shadow: 0 0 15px #fff, 0 0 25px #ffd700;
      animation: brille 1.5s infinite alternate;
    }

    @keyframes brille {
      from { text-shadow: 0 0 10px #fff, 0 0 20px #ff4fd8; }
      to { text-shadow: 0 0 18px #fff, 0 0 35px #ffd700; }
    }

    .message {
      font-size: 1.25rem;
      margin-bottom: 25px;
      line-height: 1.5;
    }

    .noms {
      font-size: 1.5rem;
      font-weight: bold;
      color: #ffe66d;
      text-shadow: 0 0 12px #ffd700;
    }

    .coeur {
      font-size: 3rem;
      margin-top: 20px;
      animation: coeur 1s infinite alternate;
    }

    @keyframes coeur {
      from { transform: scale(1); }
      to { transform: scale(1.2); }
    }

    .paillette {
      position: absolute;
      top: -20px;
      width: 8px;
      height: 8px;
      background: gold;
      border-radius: 50%;
      box-shadow: 0 0 12px gold;
      animation: tomber linear infinite;
    }

    @keyframes tomber {
      to {
        transform: translateY(110vh) rotate(360deg);
        opacity: 0;
      }
    }

    .ballon {
      position: absolute;
      bottom: -120px;
      font-size: 3rem;
      animation: monter 7s linear infinite;
      opacity: 0.9;
    }

    @keyframes monter {
      to {
        transform: translateY(-120vh);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <div class="carte">
    <h1>Joyeux anniversaire tonton 🎉</h1>
    <p class="message">On te souhaite une magnifique journée remplie de joie, de bonheur et de beaux souvenirs.</p>
    <p>De la part de</p>
    <p class="noms">Manel, Marwane et Yassine</p>
    <div class="coeur">❤️</div>
  </div>

  <script>
    for (let i = 0; i < 70; i++) {
      const paillette = document.createElement('div');
      paillette.className = 'paillette';
      paillette.style.left = Math.random() * 100 + 'vw';
      paillette.style.animationDuration = Math.random() * 3 + 3 + 's';
      paillette.style.animationDelay = Math.random() * 5 + 's';
      paillette.style.background = ['gold', 'white', '#ff4fd8', '#00eaff'][Math.floor(Math.random() * 4)];
      document.body.appendChild(paillette);
    }

    const ballons = ['🎈', '🎉', '✨', '🎂'];
    for (let i = 0; i < 12; i++) {
      const ballon = document.createElement('div');
      ballon.className = 'ballon';
      ballon.textContent = ballons[Math.floor(Math.random() * ballons.length)];
      ballon.style.left = Math.random() * 100 + 'vw';
      ballon.style.animationDuration = Math.random() * 4 + 5 + 's';
      ballon.style.animationDelay = Math.random() * 6 + 's';
      document.body.appendChild(ballon);
    }
  </script>
</body>
</html>
