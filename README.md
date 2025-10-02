<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>BenX - Web3 Development</title>

  <!-- Gothic Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@700&display=swap" rel="stylesheet">

  <style>
    body {
      margin: 0;
      font-family: 'Cinzel Decorative', cursive;
      background: #0a0a0a;
      color: #f1f1f1;
      line-height: 1.6;
    }

    /* Header */
    header {
      background: rgba(15, 15, 15, 0.8);
      border-bottom: 2px solid rgba(255, 255, 255, 0.1);
      text-align: center;
      padding: 1rem;
      backdrop-filter: blur(10px);
      position: sticky;
      top: 0;
      z-index: 1000;
    }

    header .logo img {
      width: 70px;
      margin-bottom: 0.5rem;
      filter: invert(12%) sepia(94%) saturate(7429%) hue-rotate(350deg) brightness(91%) contrast(110%);
    }

    header h1 {
      margin: 0;
      font-size: 2.2rem;
      font-style: italic;
      color: #fff;
    }

    /* Sidebar toggle button */
    .menu-btn {
      position: fixed;
      top: 20px;
      right: 20px;
      background: rgba(255, 255, 255, 0.1);
      border: none;
      padding: 10px 15px;
      border-radius: 8px;
      color: #fff;
      font-size: 1rem;
      cursor: pointer;
      z-index: 1100;
      backdrop-filter: blur(8px);
    }

    /* Sidebar */
    nav {
      position: fixed;
      top: 0;
      right: -250px;
      width: 250px;
      height: 100%;
      background: rgba(20, 20, 20, 0.95);
      backdrop-filter: blur(12px);
      box-shadow: -2px 0 10px rgba(0,0,0,0.5);
      padding-top: 80px;
      transition: right 0.3s ease-in-out;
      z-index: 1050;
    }

    nav a {
      display: block;
      color: #87CEEB;
      text-decoration: none;
      padding: 12px 20px;
      font-weight: bold;
      font-style: italic;
    }

    nav a:hover {
      background: rgba(135, 206, 235, 0.2);
    }

    nav.active {
      right: 0;
    }

    /* Sections */
    section {
      padding: 3rem 1rem;
      max-width: 900px;
      margin: auto;
    }

    section h2 {
      color: #87CEEB;
      border-bottom: 2px solid rgba(255,255,255,0.1);
      margin-bottom: 1rem;
      font-style: italic;
    }

    /* Project cards */
    .projects {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: center;
    }

    .project-card {
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255,255,255,0.2);
      padding: 1rem;
      width: 260px;
      border-radius: 12px;
      text-align: center;
      transition: transform 0.2s, box-shadow 0.2s;
      backdrop-filter: blur(15px);
    }

    .project-card:hover {
      transform: scale(1.05);
      box-shadow: 0 0 15px rgba(135,206,235,0.5);
    }

    /* Twitter embed */
    .twitter-feed {
      text-align: center;
      margin-top: 2rem;
    }

    /* Footer */
    footer {
      background: rgba(15, 15, 15, 0.9);
      border-top: 2px solid rgba(255,255,255,0.1);
      text-align: center;
      padding: 1rem;
      color: #aaa;
      margin-top: 3rem;
      backdrop-filter: blur(8px);
    }
  </style>
</head>
<body>
  <!-- Header -->
  <header>
    <div class="logo">
      <img src="https://upload.wikimedia.org/wikipedia/commons/1/1b/Bat_icon.svg" alt="Gothic Bat">
    </div>
    <h1>BenX</h1>
  </header>

  <!-- Menu button -->
  <button class="menu-btn" onclick="toggleMenu()">☰ Menu</button>

  <!-- Sidebar menu -->
  <nav id="sidebar">
    <a href="#about">About</a>
    <a href="#projects">Projects</a>
    <a href="#contact">Contact</a>
  </nav>

  <!-- About -->
  <section id="about">
    <h2>About</h2>
    <p>
      This site is a hub for Web3 development insights. A place where ideas flow like liquid glass and 
      innovation takes on a Gothic edge 🦇. Here you'll find updates, experiments, and ongoing work 
      connected to the evolving Web3 ecosystem.
    </p>
  </section>

  <!-- Projects -->
  <section id="projects">
    <h2>Projects</h2>
    <div class="projects">
      <div class="project-card">
        <h3>Project One</h3>
        <p>A showcase of Web3 magic — coming soon.</p>
      </div>
      <div class="project-card">
        <h3>Project Two</h3>
        <p>Another masterpiece in progress...</p>
      </div>
    </div>
  </section>

  <!-- Contact -->
  <section id="contact">
    <h2>Contact</h2>
    <p>Email: <a href="mailto:Avpbwoa2001@gmail.com">Avpbwoa2001@gmail.com</a></p>
    <p>X (Twitter): <a href="https://x.com/0xcosmicx" target="_blank">@0xcosmicx</a></p>
    <p>GitHub: <a href="https://github.com/x0benX" target="_blank">x0benX</a></p>
  </section>

  <!-- Twitter Updates -->
  <section id="updates">
    <h2>Latest Updates</h2>
    <div class="twitter-feed">
      <a class="twitter-timeline" data-theme="dark" data-height="500" href="https://x.com/0xcosmicx">
        Tweets by 0xcosmicx
      </a>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <p>© 2025 BenX | Forged in the Gothic Web3 Realm</p>
  </footer>

  <!-- Scripts -->
  <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
  <script>
    function toggleMenu() {
      document.getElementById("sidebar").classList.toggle("active");
    }
  </script>
</body>
</html>
