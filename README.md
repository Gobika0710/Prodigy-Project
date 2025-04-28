# Prodigy-Project
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Retro Game Hub</title>
  <style>
    /* Retro Gaming Color Palette */
    :root {
      --retro-dark: #1a1a2e;
      --retro-purple: #c4a7e7;
      --retro-pink: #b9a1a9;
      --retro-blue: #adf3fc;
      --retro-yellow: #5780d8;
      --retro-white: #af6868;
      --retro-pixel-font: 'Press Start 2P', cursive;
    }
    @import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap');

    * { margin: 0; padding: 0; box-sizing: border-box; }
    body {
      font-family: var(--retro-pixel-font);
      background-color: var(--retro-dark);
      color: var(--retro-white);
      overflow-x: hidden;
      background-image: 
        linear-gradient(rgba(250, 250, 252, 0.9), rgba(254, 254, 255, 0.9)),
        url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><rect width="2" height="2" x="20" y="20" fill="%23e91e63"/><rect width="2" height="2" x="50" y="50" fill="%2300bcd4"/><rect width="2" height="2" x="80" y="20" fill="%23ffeb3b"/></svg>');
      background-size: 100px 100px;
    }

    /* Navigation */
    .retro-nav {
      position: fixed;
      top: 0;
      width: 100%;
      background-color: var(--retro-purple);
      padding: 15px 0;
      transition: all 0.4s;
      z-index: 1000;
      box-shadow: 0 4px 8px rgba(167, 159, 159, 0.3);
      border-bottom: 3px solid var(--retro-pink);
    }
    .retro-nav.scrolled {
      padding: 8px 0;
      background-color: rgba(232, 229, 226, 0.95);
      border-bottom: 3px solid var(--retro-blue);
    }
    .nav-container {
      display: flex;
      justify-content: space-between;
      align-items: center;
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
    }
    .logo {
      font-size: 1.5rem;
      color: var(--retro-yellow);
      text-shadow: 3px 3px 0 var(--retro-pink);
      letter-spacing: 2px;
    }
    .nav-menu {
      display: flex;
      list-style: none;
    }
    .nav-item {
      margin: 0 10px;
    }
    .nav-link {
      color: var(--retro-white);
      text-decoration: none;
      font-size: 0.9rem;
      padding: 8px 15px;
      border-radius: 4px;
      transition: all 0.3s;
      text-transform: uppercase;
      letter-spacing: 1px;
      position: relative;
      overflow: hidden;
    }
    .nav-link::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 2px;
      background-color: var(--retro-blue);
      transform: scaleX(0);
      transform-origin: right;
      transition: transform 0.3s;
    }
    .nav-link:hover::after {
      transform: scaleX(1);
      transform-origin: left;
    }
    .nav-link:hover {
      color: var(--retro-yellow);
      text-shadow: 2px 2px 0 var(--retro-pink);
    }
    .nav-link.active {
      color: var(--retro-yellow);
      background-color: var(--retro-pink);
      box-shadow: 3px 3px 0 var(--retro-blue);
    }

    main {
      margin-top: 80px;
      padding: 40px 20px;
      max-width: 1200px;
      margin-left: auto;
      margin-right: auto;
    }
    section {
      min-height: 100vh;
      padding: 40px 0;
      border-bottom: 2px dashed var(--retro-blue);
    }
    h1, h2, h3 {
      color: var(--retro-yellow);
      margin-bottom: 20px;
      text-shadow: 3px 3px 0 var(--retro-pink);
    }
    p {
      margin-bottom: 15px;
      font-size: 0.9rem;
      line-height: 1.8;
    }
    .game-container {
      background-color: rgba(210, 230, 212, 0.3);
      border: 4px solid var(--retro-pink);
      padding: 20px;
      margin: 30px 0;
      position: relative;
    }
    .game-container::before {
      content: '◼◼◼◼◼◼◼◼';
      position: absolute;
      top: -15px;
      left: 20px;
      color: var(--retro-blue);
      font-size: 0.8rem;
      letter-spacing: 3px;
    }
  </style>
</head>

<body>
  <!-- Retro Game Navigation -->
  <nav class="retro-nav" id="retroNav">
    <div class="nav-container">
      <div class="logo">RETRO HUB</div>
      <ul class="nav-menu">
        <li class="nav-item"><a href="#home" class="nav-link">Home</a></li>
        <li class="nav-item"><a href="#games" class="nav-link">Games</a></li>
        <li class="nav-item"><a href="#highscores" class="nav-link">High Scores</a></li>
        <li class="nav-item"><a href="#consoles" class="nav-link">Consoles</a></li>
        <li class="nav-item"><a href="#about" class="nav-link">About</a></li>
      </ul>
    </div>
  </nav>

  <main>
    <section id="home">
      <h1>RETRO GAME HUB</h1>
      <div class="game-container">
        <p>Welcome to the ultimate retro gaming experience! Relive the golden age of video games with our collection of classic titles from the 80s and 90s.</p>
        <p>Use the navigation menu above to explore our game library, check high scores, and learn about vintage consoles.</p>
      </div>
    </section>

    <section id="games">
      <h2>CLASSIC GAMES</h2>
      <div class="game-container">
        <p>Explore our collection of timeless classics:</p>
        <p>• Space Invaders • Pac-Man • Donkey Kong • Tetris • Super Mario Bros • Sonic The Hedgehog • Street Fighter II</p>
      </div>

      <!-- Donkey Kong Playable Game -->
      <div class="game-container">
        <h3>Play Donkey Kong!</h3>
        <iframe src="https://archive.org/embed/arcade_dkong" 
                width="640" height="480" 
                frameborder="0" 
                webkitallowfullscreen="true" 
                mozallowfullscreen="true" 
                allowfullscreen 
                style="margin-top: 20px; width: 100%; max-width: 640px; height: 480px;">
        </iframe>
        <p style="margin-top: 10px; font-size: 0.7rem;">(Click inside the game to start playing. Controls: Arrow keys + Ctrl)</p>
      </div>

      <!-- Tetris Playable Game -->
      <div class="game-container">
        <h3>Play Tetris!</h3>
        <iframe src="https://archive.org/embed/tetris_gameboy" 
                width="640" height="480" 
                frameborder="0" 
                webkitallowfullscreen="true" 
                mozallowfullscreen="true" 
                allowfullscreen 
                style="margin-top: 20px; width: 100%; max-width: 640px; height: 480px;">
        </iframe>
        <p style="margin-top: 10px; font-size: 0.7rem;">(Click inside the game to start playing. Controls: Arrow keys)</p>
      </div>
    </section>

    <section id="highscores">
      <h2>HIGH SCORES</h2>
      <div class="game-container">
        <p>Top players this week:</p>
        <p>1. NINJA - 1,250,400 pts (Pac-Man)</p>
        <p>2. SK8R - 985,200 pts (Space Invaders)</p>
        <p>3. BEAST - 876,500 pts (Donkey Kong)</p>
      </div>
    </section>

    <section id="consoles">
      <h2>RETRO CONSOLES</h2>
      <div class="game-container">
        <p>Our museum features:</p>
        <p>• Atari 2600 • NES • Sega Genesis • SNES • Game Boy • PlayStation • Nintendo 64</p>
      </div>
    </section>

    <section id="about">
      <h2>ABOUT US</h2>
      <div class="game-container">
        <p>Founded in 2023, Retro Game Hub is dedicated to preserving gaming history and introducing classic games to new generations.</p>
        <p>Visit our physical location in San Francisco or play our online emulators!</p>
      </div>
    </section>
  </main>

  <script>
    const retroNav = document.getElementById('retroNav');
    window.addEventListener('scroll', function() {
      if (window.scrollY > 50) {
        retroNav.classList.add('scrolled');
      } else {
        retroNav.classList.remove('scrolled');
      }
    });

    const sections = document.querySelectorAll('section');
    const navLinks = document.querySelectorAll('.nav-link');
    window.addEventListener('scroll', function() {
      let current = '';
      sections.forEach(section => {
        const sectionTop = section.offsetTop;
        if (window.scrollY >= sectionTop - 100) {
          current = section.getAttribute('id');
        }
      });
      navLinks.forEach(link => {
        link.classList.remove('active');
        if (link.getAttribute('href') === `#${current}`) {
          link.classList.add('active');
        }
      });
    });
  </script>
</body>
</html>

