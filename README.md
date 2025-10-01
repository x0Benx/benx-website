<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>BenX Portfolio</title>

  <!-- Sleek Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@1,500&display=swap" rel="stylesheet">

  <style>
    /* Global styles */
    body {
      margin: 0;
      font-family: 'Playfair Display', serif;
      font-style: italic;
      background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
      color: #fff;
      line-height: 1.6;
      overflow-x: hidden;
    }

    /* Header Sidebar */
    header {
      position: fixed;
      top: 0;
      right: 0;
      height: 100%;
      width: 200px;
      background: rgba(255, 255, 255, 0.08);
      backdrop-filter: blur(12px);
      border-left: 1px solid rgba(255, 255, 255, 0.2);
      padding: 2rem 1rem;
      text-align: center;
    }

    header .logo img {
      width: 70px;
      margin-bottom: 1rem;
    }

    header h1 {
      margin: 0;
      font-size: 1.8rem;
      color: #fff;
    }

    nav {
      margin-top: 2rem;
      display: flex;
      flex-direction: column;
      gap: 1.5rem;
    }

    nav a {
      color: #fff;
      text-decoration: none;
      font-weight: bold;
      transition: color 0.3s;
    }

    nav a:hover {
      color: #87CEEB;
    }

    /* Content wrapper */
    main {
      margin-right: 220px;
      padding: 3rem 2rem;
    }

    section {
      margin-bottom: 4rem;
    }

    section h2 {
      font-size: 2rem;
      margin-bottom: 1.2rem;
      color: #87CEEB;
    }

    /* Liquid glass project cards */
    .projects {
      display: flex;
      flex-wrap: wrap;
      gap: 30px;
      justify-content: flex-start;
    }

    .project-card {
      background: rgba(255, 255, 255, 0.08);
      backdrop-filter: blur(15px);
      border-radius: 15px;
      padding: 2rem;
      flex: 1 1 300px;
      min-height: 180px;
      transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .project-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 8px 25px rgba(0, 0, 0, 0.3);
    }

    .project-card h3 {
      margin-top: 0;
      color: #fff;
      font-size: 1.5rem;
    }

    .project-card a {
      display: inline-block;
      margin-top: 1rem;
      padding: 0.6rem 1.2rem;
      border-radius: 8px;
      background: rgba(135, 206, 235, 0.2);
      color: #87CEEB;
      font-weight: bold;
      text-decoration: none;
      transition: background 0.3s ease, color 0.3s ease;
    }

    .project-card a:hover {
      background: #87CEEB;
      color: #000;
    }

    /* Updates section */
    #updates {
      margin-bottom: 4rem;
    }

    .updates-container {
      background: rgba(255, 255, 255, 0.08);
      backdrop-filter: blur(15px);
      border-radius: 15px;
      padding: 1.5rem;
      min-height: 300px;
      box-shadow: 0 8px 25px rgba(0, 0, 0, 0.2);
    }

    /* Contact links */
    a {
      color: #87CEEB;
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 2rem;
      border-top: 1px solid rgba(255, 255, 255, 0.2);
      color: rgba(255, 255, 255, 0.7);
    }
  </style>
</head>
<body>
  <!-- Right Sidebar Header -->
  <header>
    <div class="logo">
      <img src="https://upload.wikimedia.org/wikipedia/commons/1/1b/Bat_icon.svg" alt="Logo">
    </div>
    <h1>BenX</h1>
    <nav>
      <a href="#about">About</a>
      <a href="#projects">Top Projects</a>
      <a href="#updates">Updates</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <!-- Main content -->
  <main>
    <section id="about">
      <h2>About</h2>
      <p>Exploring the elegance of Web3 with creativity and depth. This space is dedicated to sharing insights, ideas, and breakthroughs across the Web3 landscape — from blockchain development to decentralized applications, innovation meets design here.</p>
    </section>

    <section id="projects">
      <h2>Top Projects</h2>
      <div class="projects">
        <div class="project-card">
          <h3>Antix</h3>
          <p>Decentralized innovation from Antix.</p>
          <a href="https://antix.in" target="_blank">View Project</a>
        </div>
        <div class="project-card">
          <h3>Pulse</h3>
          <p>On Alphabot, powered by Boost.</p>
          <a href="#" target="_blank">View Project</a>
        </div>
        <div class="project-card">
          <h3>Play AI</h3>
          <p>AI-powered tools on Kaito Yaps.</p>
          <a href="#" target="_blank">View Project</a>
        </div>
        <div class="project-card">
          <h3>Veera</h3>
          <p>The Veera browser experience.</p>
          <a href="https://veerabrowser.com" target="_blank">View Project</a>
        </div>
        <div class="project-card">
          <h3>XO Market</h3>
          <p>The conviction market platform.</p>
          <a href="#" target="_blank">View Project</a>
        </div>
        <div class="project-card">
          <h3>Airaa</h3>
          <p>Innovating at Airaa.</p>
          <a href="https://airaa.com" target="_blank">View Project</a>
        </div>
        <div class="project-card">
          <h3>Boost S2</h3>
          <p>Season Two campaign on Pulse.</p>
          <a href="#" target="_blank">View Project</a>
        </div>
        <div class="project-card">
          <h3>Rayls</h3>
          <p>Decentralized systems by Rayls Labs.</p>
          <a href="https://raylslabs.com" target="_blank">View Project</a>
        </div>
        <div class="project-card">
          <h3>VeloraDEX</h3>
          <p>A next-gen decentralized exchange.</p>
          <a href="#" target="_blank">View Project</a>
        </div>
        <div class="project-card">
          <h3>Lumiterra</h3>
          <p>Immersive Web3 gaming experiences.</p>
          <a href="#" target="_blank">View Project</a>
        </div>
      </div>
    </section>

    <!-- Latest Updates (Twitter Feed) -->
    <section id="updates">
      <h2>Latest Updates</h2>
      <div class="updates-container">
        <a class="twitter-timeline" 
           href="https://twitter.com/0xcosmicx?ref_src=twsrc%5Etfw"
           data-theme="dark"
           data-chrome="transparent nofooter noborders"
           data-tweet-limit="5">
           Tweets by @0xcosmicx
        </a>
      </div>
      <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
    </section>

    <section id="contact">
      <h2>Contact</h2>
      <p>Email: <a href="mailto:Avpbwoa2001@gmail.com">Avpbwoa2001@gmail.com</a></p>
      <p>X (Twitter): <a href="https://x.com/0xcosmicx" target="_blank">@0xcosmicx</a></p>
      <p>GitHub: <a href="https://github.com/x0benX" target="_blank">x0benX</a></p>
    </section>
  </main>

  <!-- Footer -->
  <footer>
    <p>© 2025 BenX | Liquid Glass Portfolio</p>
  </footer>

  <script>
    console.log("✨ Welcome to BenX Liquid Glass Portfolio ✨");
  </script>
</body>
</html>
