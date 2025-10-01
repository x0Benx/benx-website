<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>BenX Portfolio</title>

  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@1,500&display=swap" rel="stylesheet">

  <!-- Twitter widgets script (in head so embed can initialize early) -->
  <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

  <style>
    :root{
      --sidebar-width: 200px;
      --sidebar-collapsed: 60px;
      --accent: #87CEEB;
      --glass-bg: rgba(255,255,255,0.08);
      --transition: 300ms;
    }

    /* Reset & globals */
    *{box-sizing:border-box}
    body{
      margin:0;
      font-family:'Playfair Display', serif;
      font-style: italic;
      background: linear-gradient(135deg,#0f2027,#203a43,#2c5364);
      color:#fff;
      line-height:1.6;
      overflow-x:hidden;
      transition: background var(--transition);
    }

    /* Collapsible right sidebar */
    header {
      position: fixed;
      top: 0;
      right: 0;
      height: 100%;
      width: var(--sidebar-width);
      background: var(--glass-bg);
      backdrop-filter: blur(12px);
      border-left: 1px solid rgba(255,255,255,0.14);
      padding: 1.6rem 1rem;
      text-align: center;
      transition: width var(--transition) ease, transform var(--transition) ease;
      z-index: 40;
    }

    /* Collapsed state controlled by body.sidebar-collapsed */
    body.sidebar-collapsed header{
      width: var(--sidebar-collapsed);
    }

    header .logo img{
      width:70px;
      transition: width var(--transition);
    }
    body.sidebar-collapsed header .logo img{ width:46px; }

    header h1{
      margin:0.4rem 0 0;
      font-size:1.4rem;
      color:#fff;
      transition: opacity var(--transition);
    }
    body.sidebar-collapsed header h1{ opacity:0; pointer-events:none; }

    /* Toggle button sits on the left edge of the sidebar (so it floats over content) */
    #sidebar-toggle{
      position: absolute;
      left: calc(-1 * (36px));
      top: 18px;
      width:36px;
      height:36px;
      border-radius:8px;
      border:none;
      background: rgba(255,255,255,0.06);
      color:#fff;
      cursor:pointer;
      display:flex;
      align-items:center;
      justify-content:center;
      font-size:18px;
      backdrop-filter: blur(6px);
      box-shadow: 0 4px 12px rgba(0,0,0,0.35);
      transition: transform var(--transition);
      z-index: 45;
    }

    /* Nav */
    nav {
      margin-top: 2.2rem;
      display:flex;
      flex-direction:column;
      gap:1rem;
    }

    nav a{
      color:#fff;
      text-decoration:none;
      font-weight:bold;
      transition: opacity 150ms;
      white-space:nowrap;
    }
    /* hide nav text when collapsed */
    body.sidebar-collapsed nav a{ opacity:0; pointer-events:none; }

    /* Content wrapper */
    main{
      margin-right: calc(var(--sidebar-width) + 20px);
      padding: 3rem 2rem;
      transition: margin-right var(--transition) ease;
    }
    body.sidebar-collapsed main{
      margin-right: calc(var(--sidebar-collapsed) + 20px);
    }

    section{ margin-bottom: 3.2rem; }
    section h2{
      font-size:2rem;
      margin-bottom:1rem;
      color:var(--accent);
    }

    /* Projects grid */
    .projects{
      display:flex;
      flex-wrap:wrap;
      gap:24px;
      justify-content:flex-start;
    }

    .project-card{
      background: var(--glass-bg);
      backdrop-filter: blur(15px);
      border-radius:14px;
      padding:1.6rem;
      flex: 1 1 300px;
      min-height: 260px;
      transition: transform 260ms, box-shadow 260ms;
      text-align:center;
      display:flex;
      flex-direction:column;
      align-items:stretch;
    }
    .project-card:hover{
      transform: translateY(-8px);
      box-shadow: 0 12px 30px rgba(0,0,0,0.35);
    }

    .project-img{
      width:100%;
      height:140px;
      object-fit:contain;
      border-radius:10px;
      background: rgba(255,255,255,0.06);
      margin-bottom: 1rem;
      padding:10px;
      display:block;
    }

    .project-card h3{ margin:0 0 0.4rem; font-size:1.25rem; color:#fff; }
    .project-card p{ margin:0; color:rgba(255,255,255,0.9); flex:0 0 auto; }

    .project-actions{ margin-top:auto; display:flex; justify-content:center; }
    .project-card a{
      display:inline-block;
      margin-top:1rem;
      padding:0.5rem 1rem;
      border-radius:8px;
      background: rgba(135,206,235,0.14);
      color:var(--accent);
      font-weight:bold;
      text-decoration:none;
      transition: background 180ms,color 180ms;
    }
    .project-card a:hover{ background:var(--accent); color:#000; }

    /* Updates */
    .updates-container{
      background: var(--glass-bg);
      backdrop-filter: blur(15px);
      border-radius:14px;
      padding:1rem;
      min-height:280px;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
    }
    .updates-fallback{
      margin-top:0.6rem;
      color:rgba(255,255,255,0.85);
    }
    .updates-fallback a{ color:var(--accent); text-decoration:none; }

    /* Footer */
    footer{ text-align:center; padding:2rem; border-top:1px solid rgba(255,255,255,0.08); color:rgba(255,255,255,0.65); }

    /* Responsive tweaks */
    @media (max-width:900px){
      header{ position:fixed; bottom:0; right:0; top:auto; width:100%; height:auto; border-left:none; border-top:1px solid rgba(255,255,255,0.08); display:flex; justify-content:space-between; padding:0.6rem 1rem; align-items:center; }
      #sidebar-toggle{ left: 12px; top:8px; }
      body.sidebar-collapsed main{ margin-right: 20px; } /* don't reduce mobile margin-right too much */
      main{ margin-right:20px; padding:2rem 1rem; }
      nav{ flex-direction:row; gap: 12px; margin-top:0; }
    }
  </style>
</head>
<body>
  <!-- Right Sidebar Header (collapsible) -->
  <header>
    <button id="sidebar-toggle" title="Toggle menu" aria-label="Toggle menu">☰</button>

    <div class="logo" aria-hidden="false">
      <img src="https://upload.wikimedia.org/wikipedia/commons/1/1b/Bat_icon.svg" alt="BenX logo">
    </div>

    <h1>BenX</h1>

    <nav aria-label="Main navigation">
      <a href="#about">About</a>
      <a href="#projects">Top Projects</a>
      <a href="#updates">Updates</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <main>
    <section id="about">
      <h2>About</h2>
      <p>Exploring the elegance of Web3 with creativity and depth. This space is dedicated to sharing insights, ideas, and breakthroughs across the Web3 landscape — from blockchain development to decentralized applications, innovation meets design here.</p>
    </section>

    <section id="projects">
      <h2>Top Projects</h2>
      <div class="projects">

        <!-- Antix -->
        <div class="project-card">
          <img class="project-img" src="https://files.fm/f/ggunmg3uqr" alt="Antix logo"
               loading="lazy"
               onerror="this.onerror=null;this.src='https://via.placeholder.com/300x150?text=No+Image';">
          <h3>Antix</h3>
          <p>Decentralized innovation from Antix.</p>
          <div class="project-actions">
            <a href="https://antix.in" target="_blank" rel="noopener">View Project</a>
          </div>
        </div>

        <!-- Airaa -->
        <div class="project-card">
          <img class="project-img" src="https://files.fm/f/p9puusv3ts" alt="Airaa logo"
               loading="lazy"
               onerror="this.onerror=null;this.src='https://via.placeholder.com/300x150?text=No+Image';">
          <h3>Airaa</h3>
          <p>Innovating at Airaa.</p>
          <div class="project-actions">
            <a href="https://airaa.xyz" target="_blank" rel="noopener">View Project</a>
          </div>
        </div>

        <!-- Boost -->
        <div class="project-card">
          <img class="project-img" src="https://files.fm/f/3855j6kju9" alt="Boost logo"
               loading="lazy"
               onerror="this.onerror=null;this.src='https://via.placeholder.com/300x150?text=No+Image';">
          <h3>Boost S2</h3>
          <p>Season Two campaign on Pulse.</p>
          <div class="project-actions">
            <a href="https://www.alphabot.app/boost" target="_blank" rel="noopener">View Project</a>
          </div>
        </div>

        <!-- Lumiterra -->
        <div class="project-card">
          <img class="project-img" src="https://files.fm/f/4yd5th2ev8" alt="Lumiterra logo"
               loading="lazy"
               onerror="this.onerror=null;this.src='https://via.placeholder.com/300x150?text=No+Image';">
          <h3>Lumiterra</h3>
          <p>Immersive Web3 gaming experiences.</p>
          <div class="project-actions">
            <a href="https://lumiterra.net" target="_blank" rel="noopener">View Project</a>
          </div>
        </div>

        <!-- Play AI -->
        <div class="project-card">
          <img class="project-img" src="https://files.fm/f/mksw6qgnxm" alt="Play AI logo"
               loading="lazy"
               onerror="this.onerror=null;this.src='https://via.placeholder.com/300x150?text=No+Image';">
          <h3>Play AI</h3>
          <p>AI-powered tools on Kaito Yaps.</p>
          <div class="project-actions">
            <a href="https://yaps.kaito.ai/playai" target="_blank" rel="noopener">View Project</a>
          </div>
        </div>

        <!-- Rayls -->
        <div class="project-card">
          <img class="project-img" src="https://files.fm/f/ecwhxw6yjs" alt="Rayls logo"
               loading="lazy"
               onerror="this.onerror=null;this.src='https://via.placeholder.com/300x150?text=No+Image';">
          <h3>Rayls</h3>
          <p>Decentralized systems by Rayls Labs.</p>
          <div class="project-actions">
            <a href="https://raylslabs.com" target="_blank" rel="noopener">View Project</a>
          </div>
        </div>

        <!-- Veera -->
        <div class="project-card">
          <img class="project-img" src="https://files.fm/f/kpeny2ywts" alt="Veera logo"
               loading="lazy"
               onerror="this.onerror=null;this.src='https://via.placeholder.com/300x150?text=No+Image';">
          <h3>Veera</h3>
          <p>The Veera browser experience.</p>
          <div class="project-actions">
            <a href="https://veerabrowser.com" target="_blank" rel="noopener">View Project</a>
          </div>
        </div>

        <!-- VeloraDEX -->
        <div class="project-card">
          <img class="project-img" src="https://files.fm/f/m4ftayn8rx" alt="VeloraDEX logo"
               loading="lazy"
               onerror="this.onerror=null;this.src='https://via.placeholder.com/300x150?text=No+Image';">
          <h3>VeloraDEX</h3>
          <p>A next-gen decentralized exchange.</p>
          <div class="project-actions">
            <a href="https://cookie.fun" target="_blank" rel="noopener">View Project</a>
          </div>
        </div>

        <!-- XO Market -->
        <div class="project-card">
          <img class="project-img" src="https://files.fm/f/tsfmqxhhwx" alt="XO Market logo"
               loading="lazy"
               onerror="this.onerror=null;this.src='https://via.placeholder.com/300x150?text=No+Image';">
          <h3>XO Market</h3>
          <p>The conviction market platform.</p>
          <div class="project-actions">
            <a href="https://xo.market" target="_blank" rel="noopener">View Project</a>
          </div>
        </div>

        <!-- TenProtocol (no site provided) -->
        <div class="project-card">
          <img class="project-img" src="https://files.fm/f/5r6es9r7fh" alt="TenProtocol logo"
               loading="lazy"
               onerror="this.onerror=null;this.src='https://via.placeholder.com/300x150?text=No+Image';">
          <h3>TenProtocol</h3>
          <p>Protocol innovation in Web3.</p>
          <div class="project-actions">
            <a href="#" target="_blank" rel="noopener">View Project</a>
          </div>
        </div>

      </div>
    </section>

    <!-- Latest Updates (Twitter/X feed) -->
    <section id="updates">
      <h2>Latest Updates</h2>
      <div class="updates-container" aria-live="polite">
        <a class="twitter-timeline"
           href="https://x.com/0xcosmicx"
           data-theme="dark"
           data-chrome="transparent nofooter noborders"
           data-tweet-limit="5">
           Tweets by @0xcosmicx
        </a>

        <!-- Fallback if embed doesn't show (useful for local testing or blocked widgets) -->
        <div class="updates-fallback">
          If the feed doesn't appear here (adblocker or local file view may block it), view updates on
          <a href="https://x.com/0xcosmicx" target="_blank" rel="noopener">@0xcosmicx</a>.
        </div>
      </div>
    </section>

    <section id="contact">
      <h2>Contact</h2>
      <p>Email: <a href="mailto:Avpbwoa2001@gmail.com">Avpbwoa2001@gmail.com</a></p>
      <p>X (Twitter): <a href="https://x.com/0xcosmicx" target="_blank">@0xcosmicx</a></p>
      <p>GitHub: <a href="https://github.com/x0benX" target="_blank">x0benX</a></p>
    </section>

  </main>

  <footer>
    <p>© 2025 BenX | Liquid Glass Portfolio</p>
  </footer>

  <script>
    // Sidebar toggle
    (function(){
      const toggle = document.getElementById('sidebar-toggle');
      toggle.addEventListener('click', () => {
        document.body.classList.toggle('sidebar-collapsed');
        // save preference
        try { localStorage.setItem('benx.sidebarCollapsed', document.body.classList.contains('sidebar-collapsed')); } catch(e){}
      });

      // persist state between page loads
      try {
        const saved = localStorage.getItem('benx.sidebarCollapsed');
        if (saved === 'true') document.body.classList.add('sidebar-collapsed');
      } catch(e){}

      // small accessibility: toggle with "m" key (optional)
      document.addEventListener('keydown', (ev) => {
        if (ev.key === 'm' && !ev.metaKey && !ev.ctrlKey && !ev.altKey) {
          document.body.classList.toggle('sidebar-collapsed');
        }
      });
    })();
  </script>
</body>
</html>
