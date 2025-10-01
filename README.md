<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Web3 Development</title>

  <!-- CSS goes here -->
  <style>
    body {
      margin: 0;
      font-family: 'Cinzel', serif;
      background: #000;
      color: #f1f1f1;
      line-height: 1.6;
    }

    header {
      background: #111;
      color: #f1f1f1;
      padding: 1rem;
      text-align: center;
      border-bottom: 3px solid #8b0000;
    }

    header .logo {
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    header .bat-logo {
      width: 60px;
      filter: invert(12%) sepia(94%) saturate(7429%) hue-rotate(350deg) brightness(91%) contrast(110%);
    }

    nav {
      margin-top: 0.5rem;
    }

    nav a {
      color: #ff0000;
      margin: 0 15px;
      text-decoration: none;
      font-weight: bold;
    }

    nav a:hover {
      text-shadow: 0 0 5px #ff0000;
    }

    section {
      padding: 3rem 1rem;
      max-width: 900px;
      margin: auto;
    }

    h2 {
      color: #ff0000;
      border-bottom: 2px solid #8b0000;
      padding-bottom: 0.5rem;
      margin-bottom: 1rem;
    }

    .projects {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
      justify-content: center;
    }

    .project-card {
      background: #111;
      border: 2px solid #8b0000;
      padding: 1rem;
      width: 250px;
      border-radius: 8px;
      text-align: center;
      transition: transform 0.2s;
    }

    .project-card:hover {
      transform: scale(1.05);
      box-shadow: 0 0 10px #ff0000;
    }

    footer {
      background: #111;
      color: #888;
      text-align: center;
      padding: 1rem;
      margin-top: 2rem;
      border-top: 3px solid #8b0000;
    }
  </style>
</head>
<body>
  <header>
    <div class="logo">
      <img src="https://upload.wikimedia.org/wikipedia/commons/1/1b/Bat_icon.svg" alt="Gothic Bat" class="bat-logo">
      <h1>BenX</h1>
    </div>
    <nav>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <section id="about">
    <h2>About</h2>
    <p>All things informative for Web3 development. Welcome to the shadows of innovation 🦇.</p>
  </section>

  <section id="projects">
    <h2>Projects & Portfolio</h2>
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

  <section id="contact">
    <h2>Contact</h2>
    <p>Email: <a href="mailto:Avpbwoa2001@gmail.com">Avpbwoa2001@gmail.com</a></p>
    <p>X: <a href="https://x.com/0xcosmicx" target="_blank">@0xcosmicx</a></p>
    <p>GitHub: <a href="https://github.com/x0benX" target="_blank">x0benX</a></p>
  </section>

  <footer>
    <p>© 2025 BenX | Crafted in the Gothic Web3 Realm</p>
  </footer>

  <!-- JavaScript goes here -->
  <script>
    console.log("Welcome to the Gothic Web3 realm of BenX 🦇");
  </script>
</body>
</html>
