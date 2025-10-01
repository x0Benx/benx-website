<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Web3 Development</title>

  <!-- Gothic Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@700&display=swap" rel="stylesheet">

  <style>
    /* Global styles */
    body {
      margin: 0;
      font-family: 'Cinzel Decorative', cursive;
      background-color: #000;
      color: #f1f1f1;
      line-height: 1.6;
    }

    /* Header */
    header {
      background: #111;
      border-bottom: 3px solid #8b0000;
      text-align: center;
      padding: 1rem;
    }

    header .logo img {
      width: 80px;
      margin-bottom: 0.5rem;
      filter: invert(12%) sepia(94%) saturate(7429%) hue-rotate(350deg) brightness(91%) contrast(110%);
    }

    header h1 {
      margin: 0;
      color: #ff0000;
      font-size: 2.5rem;
    }

    nav {
      margin-top: 0.5rem;
    }

    nav a {
      color: #ff0000;
      text-decoration: none;
      margin: 0 15px;
      font-weight: bold;
    }

    nav a:hover {
      text-shadow: 0 0 8px #ff0000;
    }

    /* Sections */
    section {
      padding: 3rem 1rem;
      max-width: 900px;
      margin: auto;
    }

    section h2 {
      color: #ff0000;
      border-bottom: 2px solid #8b0000;
      margin-bottom: 1rem;
    }

    /* Projects */
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
      width: 260px;
      border-radius: 6px;
      text-align: center;
      transition: transform 0.2s, box-shadow 0.2s;
    }

    .project-card:hover {
      transform: scale(1.05);
      box-shadow: 0 0 15px #ff0000;
    }

    /* Contact Links */
    a {
      color: #ff0000;
    }

    a:hover {
      text-shadow: 0 0 5px #ff0000;
    }

    /* Footer */
    footer {
      background: #111;
      border-top: 3px solid #8b0000;
      text-align: center;
      padding: 1rem;
      color: #777;
      margin-top: 3rem;
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
    <nav>
      <a href="#about">About</a>
      <a href="#projects">Projects</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <!-- About Section -->
  <section id="about">
    <h2>About</h2>
    <p>All things informative for Web3 development. Enter the shadows of innovation 🦇.</p>
  </section>

  <!-- Projects Section -->
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

  <!-- Contact Section -->
  <section id="contact">
    <h2>Contact</h2>
    <p>Email: <a href="mailto:Avpbwoa2001@gmail.com">Avpbwoa2001@gmail.com</a></p>
    <p>X (Twitter): <a href="https://x.com/0xcosmicx" target="_blank">@0xcosmicx</a></p>
    <p>GitHub: <a href="https://github.com/x0benX" target="_blank">x0benX</a></p>
  </section>

  <!-- Footer -->
  <footer>
    <p>© 2025 BenX | Forged in the Gothic Web3 Realm</p>
  </footer>

  <!-- JavaScript -->
  <script>
    console.log("🦇 Welcome to the Gothic Web3 realm of BenX 🔥");
  </script>
</body>
</html>
