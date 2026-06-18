<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Intro rétro gaming</title>

  <!-- Optionnel : police rétro (Google Fonts) -->
  <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">

  <style>
    body {
      background: #050608;
      color: #33ff66;
      font-family: 'Press Start 2P', monospace;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
    }

    .screen {
      border: 2px solid #33ff66;
      padding: 20px;
      max-width: 600px;
      box-shadow: 0 0 15px #33ff66;
      background: #000;
    }

    .typing {
      white-space: pre-wrap; /* garde les retours à la ligne */
    }

    /* Curseur clignotant */
    .cursor {
      display: inline-block;
      width: 10px;
      background: #33ff66;
      margin-left: 4px;
      animation: blink 0.8s steps(1) infinite;
    }

    @keyframes blink {
      0%, 50% { opacity: 1; }
      51%, 100% { opacity: 0; }
    }
  </style>
</head>
<body>
  <div class="screen">
    <div id="text" class="typing"></div><span class="cursor"></span>
  </div>

  <script>
    // Ton texte (tu peux mettre celui de l’image ici)
    const fullText = `Bonjour !

Jeune développeuse en apprentissage à l'ENI, je suis passée par beaucoup de métiers avant de retourner à mes études dans le dev !

J’adore :
- 🍳 Cuisiner  
- 📚 Lire  
- 🎨 Peindre des figurines  
- 🎮 Jouer aux jeux‑vidéos  

PS : J’aime beaucoup **Toad**.
`;

    const textElement = document.getElementById('text');
    let index = 0;
    const speed = 25; // vitesse en ms par caractère

    function type() {
      if (index < fullText.length) {
        textElement.textContent += fullText.charAt(index);
        index++;
        setTimeout(type, speed);
      }
    }

    // Lance l’animation
    type();
  </script>
</body>
</html>

![Mon GIF](https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExN3F3azJ3bmJxOXRiN2d1M3c5ejMwOHZ6NGd4dHk0YW1kYnVic3RhciZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/MuE9MGdYDmem1FwE0o/giphy.gif)
