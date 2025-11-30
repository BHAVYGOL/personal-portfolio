<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Bhavy Gol — Portfolio</title>

  <!-- Fonts & Icons -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
  <!-- Font Awesome (icons) -->
  <script src="https://kit.fontawesome.com/a076d05399.js" crossorigin="anonymous"></script>
  <!-- Lucide (optional vector icons) -->
  <script src="https://unpkg.com/lucide@0.248.0/dist/lucide.min.js"></script>

  <style>
    /* ---------- Root / base ---------- */
    :root{
      --bg1: #7b2ff7; /* purple */
      --bg2: #00c6ff; /* blue */
      --bg3: #ff6ec4; /* pink */
      --glass: rgba(255,255,255,0.06);
      --card-transparent: rgba(255,255,255,0.12);
      --muted: rgba(255,255,255,0.85);
      --accent-dark: #0b1220;
      --max-width: 1200px;
    }

    *{box-sizing:border-box}
    html,body{height:100%;}
    body{
      margin:0;
      font-family: 'Poppins', system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      color:white;
      background: linear-gradient(120deg, var(--bg1), var(--bg2), var(--bg3));
      background-size: 400% 400%;
      animation: bgShift 14s ease infinite;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.45;
      overflow-y: auto;
      scroll-behavior: smooth;
    }

    @keyframes bgShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    a{color:inherit;text-decoration:none}
    img{max-width:100%;display:block}

    /* ---------- Container ---------- */
    .site-wrap{
      max-width: var(--max-width);
      margin: 0 auto;
      padding: 28px;
    }

    /* ---------- Header & Nav ---------- */
    header{
      position:sticky;
      top:0;
      z-index:1200;
      background: linear-gradient(180deg, rgba(0,0,0,0.18), rgba(255,255,255,0.02));
      backdrop-filter: blur(8px);
      border-bottom: 1px solid rgba(255,255,255,0.06);
    }

    .nav-inner{
      max-width: var(--max-width);
      margin: 0 auto;
      display:flex;
      align-items:center;
      justify-content:space-between;
      gap:18px;
      padding:12px 22px;
    }

    .brand{
      display:flex;align-items:center;gap:12px;
    }
    .logo{
      width:48px;height:48px;border-radius:12px;
      display:grid;place-items:center;font-weight:800;
      background: linear-gradient(135deg, rgba(255,255,255,0.12), rgba(255,255,255,0.02));
      box-shadow: 0 8px 24px rgba(0,0,0,0.25);
      font-size:18px;
    }
    .brand .txt{font-weight:700;letter-spacing:0.2px}
    .brand .sub{font-size:12px;color:rgba(255,255,255,0.8)}

    nav.primary{
      display:flex;gap:10px;align-items:center;
    }
    nav.primary a{
      padding:8px 12px;border-radius:8px;font-weight:600;color:var(--muted);transition:all .18s ease;
    }
    nav.primary a:hover{ background: rgba(255,255,255,0.03); transform:translateY(-3px); color:#fff; }

    /* ---------- Hero ---------- */
    .hero{
      padding:84px 0 48px;
      display:flex;
      gap:30px;
      align-items:center;
      justify-content:space-between;
    }

    .hero-left{ flex:1; min-width:420px; max-width:760px; }
    .hero-right{ width:320px; min-width:220px; display:grid; place-items:center; }

    .typewriter{
      font-size:56px;
      font-weight:800;
      line-height:1;
      white-space:nowrap;
      overflow:hidden;
      border-right:4px solid rgba(255,255,255,0.9);
      width:0;
      animation: typing 3.2s steps(26) forwards, blink 0.9s steps(1) infinite;
    }
    @keyframes typing{ from { width:0 } to { width:460px } }
    @keyframes blink{ 50% { border-color: transparent } }

    .hero p.lead{ margin-top:12px; font-size:18px; color:rgba(255,255,255,0.9) }

    .cta-row{ margin-top:20px; display:flex; gap:12px; align-items:center; flex-wrap:wrap }
    .btn{
      padding:10px 16px; border-radius:12px; font-weight:700; cursor:pointer;
      background: linear-gradient(90deg, rgba(255,255,255,0.14), rgba(255,255,255,0.06));
      border:1px solid rgba(255,255,255,0.06); color:var(--accent-dark);
      transition: transform .16s ease, box-shadow .16s ease;
    }
    .btn:hover{ transform: translateY(-4px); box-shadow: 0 12px 30px rgba(0,0,0,0.28) }
    .btn-light{ background:linear-gradient(90deg,#ffffffAA,#ffffff88); color:#05060a }

    .avatar{
      width:220px; height:220px; border-radius:18px;
      background: linear-gradient(135deg, rgba(255,255,255,0.08), rgba(255,255,255,0.02));
      display:grid; place-items:center; border:1px solid rgba(255,255,255,0.04);
      box-shadow: 0 14px 40px rgba(0,0,0,0.3);
    }
    .avatar .initials{ font-size:46px; font-weight:900 }

    /* ---------- Sections ---------- */
    section{ padding:56px 0; }
    .section-title{ display:flex; align-items:center; gap:12px; margin-bottom:18px; font-size:22px; font-weight:700 }
    .section-sub{ color: rgba(255,255,255,0.88); margin-bottom:18px; }

    /* ---------- Grid & Cards ---------- */
    .grid{ display:grid; grid-template-columns: repeat(3, 1fr); gap:20px; align-items:stretch; }
    .card{
      padding:18px;
      border-radius:14px;
      background: linear-gradient(180deg, rgba(255,255,255,0.04), rgba(255,255,255,0.02));
      border:1px solid rgba(255,255,255,0.04);
      box-shadow: 0 10px 30px rgba(0,0,0,0.25);
      transition: transform .28s cubic-bezier(.2,.9,.3,1), box-shadow .28s ease, filter .28s ease;
      position:relative;
      overflow:hidden;
    }
    .card .icon{
      width:60px;height:60px;border-radius:12px;display:grid;place-items:center;
      background: rgba(255,255,255,0.03); font-size:26px;
      margin-bottom:10px;
    }
    .card h3{ margin:0 0 8px; font-size:18px; }
    .card p{ margin:0; color: rgba(255,255,255,0.88); font-size:14px; }

    /* Glow effect */
    .card::before{
      content:"";
      position:absolute; inset: -40% -40% auto -40%; height:180%;
      background: radial-gradient(circle at 10% 10%, rgba(255,255,255,0.06), transparent 10%),
                  radial-gradient(circle at 90% 90%, rgba(255,255,255,0.03), transparent 12%);
      opacity:0; transition: opacity .35s ease;
      pointer-events:none;
    }
    .card:hover{ transform: translateY(-12px) scale(1.03); box-shadow: 0 30px 80px rgba(0,0,0,0.46); }
    .card:hover::before{ opacity:1; filter: blur(8px); }

    /* Tag list */
    .tags{ display:flex; gap:8px; flex-wrap:wrap; margin-top:12px }
    .tag{ padding:6px 10px; border-radius:999px; background:rgba(255,255,255,0.04); font-size:13px; color: rgba(255,255,255,0.9) }

    /* Skills layout */
    .skills-grid{ display:flex; gap:18px; flex-wrap:wrap; justify-content:center; align-items:stretch; }
    .skill{
      width:240px;
      padding:14px;border-radius:12px; background: linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0.01));
      border:1px solid rgba(255,255,255,0.04);
      text-align:left;
    }
    .skill h4{ margin:0 0 8px; font-size:16px }
    .bar{
      width:100%; height:10px; background: rgba(255,255,255,0.06); border-radius:999px; overflow:hidden;
    }
    .bar > i{ display:block; height:100%; background: linear-gradient(90deg,#fff6,#fff2); border-radius:999px; }

    /* Contact */
    .contact-grid{ display:flex; gap:20px; align-items:start; justify-content:space-between; }
    .contact-card{
      flex:1; min-width:360px; padding:18px; border-radius:12px;
      background: linear-gradient(180deg, rgba(255,255,255,0.03), rgba(255,255,255,0.01));
      border:1px solid rgba(255,255,255,0.04);
    }
    .contact-card label{ display:block; font-size:13px; color:rgba(255,255,255,0.85); margin-bottom:6px; }
    .contact-card input, .contact-card textarea{
      width:100%; padding:10px;border-radius:8px;border:1px solid rgba(255,255,255,0.06);
      background: rgba(0,0,0,0.08); color:var(--muted);
    }

    /* ---------- Small helpers & animations ---------- */
    .fade-up{ opacity:0; transform:translateY(18px); animation: fadeUp 700ms forwards; }
    .delay-1{ animation-delay:120ms } .delay-2{ animation-delay:260ms } .delay-3{ animation-delay:420ms }

    @keyframes fadeUp { to { opacity:1; transform:none } }

    /* Responsive */
    @media (max-width:1100px){
      .hero{ flex-direction:column; align-items:flex-start; gap:18px; padding-top:36px }
      .hero-right{ width:100%; display:flex; justify-content:center }
      .grid{ grid-template-columns: repeat(2, 1fr) }
      .contact-grid{ flex-direction:column }
    }
    @media (max-width:640px){
      .grid{ grid-template-columns: 1fr }
      nav.primary{ display:none } /* keep it simple for mobile */
      .typewriter{ font-size:36px; animation: typing 3.2s steps(16) forwards; width:320px }
      .site-wrap{ padding:16px }
      .hero-left{ min-width:unset; max-width:unset }
    }
  </style>
</head>
<body>

  <!-- HEADER / NAV -->
  <header role="banner">
    <div class="nav-inner">
      <div class="brand" aria-hidden="false">
        <div class="logo">BG</div>
        <div>
          <div class="txt">Bhavy Gol</div>
          <div class="sub">Web & Software Developer</div>
        </div>
      </div>

      <nav class="primary" role="navigation" aria-label="Main navigation">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#skills">Skills</a>
        <a href="#projects">Projects</a>
        <a href="#contact">Contact</a>
      </nav>
    </div>
  </header>

  <main class="site-wrap" id="top">

    <!-- HERO -->
    <section id="home" class="hero" aria-label="Introduction">
      <div class="hero-left fade-up delay-1">
        <div class="typewriter" aria-hidden="false">Bhavy Gol</div>
        <p class="lead">I design embedded solutions & web experiences — combining firmware, IoT, and frontend to ship real products.</p>

        <div class="cta-row">
          <a class="btn btn-light" href="#projects">See Projects</a>
          <a class="btn" href="#contact">Contact Me</a>
          <a class="btn" href="#" onclick="openResume();return false;">Resume</a>
        </div>

        <p style="margin-top:12px;color:rgba(255,255,255,0.9)">Email: <a href="mailto:bhavygol@gmail.com" style="color:#fff;font-weight:700">bhavygol@gmail.com</a></p>
      </div>

      <div class="hero-right fade-up delay-2" aria-hidden="true">
        <div class="avatar">
          <!-- Replace with your image: <img src="your-photo.jpg" alt="Bhavy Gol"> -->
          <div class="initials">BG</div>
        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about" class="fade-up delay-2" aria-labelledby="about-title">
      <h2 id="about-title" class="section-title">About</h2>
      <p class="section-sub">Hello — I'm Bhavy. I specialise in firmware (C/C++), front-end web (HTML/CSS/JavaScript) and small IoT systems. I enjoy turning hardware ideas into reliable products.</p>

      <div style="display:flex;gap:20px;align-items:flex-start;flex-wrap:wrap;">
        <div style="flex:1;min-width:320px;">
          <p style="color:rgba(255,255,255,0.9)">Replace this with a short paragraph about your education, interests, or experience — for example, where you studied, notable projects, or what you enjoy building.</p>
        </div>

        <div style="width:320px;">
          <div class="card">
            <h3 style="margin-bottom:8px">Quick Links</h3>
            <div style="display:flex;flex-direction:column;gap:8px;margin-top:10px">
              <a class="btn" href="#" onclick="openResume();return false;">Download Resume</a>
              <a class="btn" href="#" target="_blank">GitHub</a>
              <a class="btn" href="#" target="_blank">LinkedIn</a>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- SKILLS -->
    <section id="skills" class="fade-up delay-3" aria-labelledby="skills-title">
      <h2 id="skills-title" class="section-title">Skills</h2>
      <p class="section-sub">Languages, tools and embedded experience.</p>

      <div class="skills-grid">
        <div class="skill glow-card fade-up delay-1" style="animation-delay:140ms;">
          <h4>C</h4>
          <div class="bar" aria-hidden="true"><i style="width:86%"></i></div>
          <p style="margin-top:10px;color:rgba(255,255,255,0.9)">Systems programming and microcontroller firmware.</p>
        </div>

        <div class="skill glow-card fade-up delay-2" style="animation-delay:220ms;">
          <h4>C++</h4>
          <div class="bar" aria-hidden="true"><i style="width:78%"></i></div>
          <p style="margin-top:10px;color:rgba(255,255,255,0.9)">Embedded C++ & higher-level application logic.</p>
        </div>

        <div class="skill glow-card fade-up delay-3" style="animation-delay:300ms;">
          <h4>JavaScript</h4>
          <div class="bar" aria-hidden="true"><i style="width:74%"></i></div>
          <p style="margin-top:10px;color:rgba(255,255,255,0.9)">Frontend, small web apps, UI interactions.</p>
        </div>

        <div class="skill glow-card fade-up delay-3" style="animation-delay:380ms; display:flex; gap:12px; align-items:center;">
          <div style="width:58px;height:58px;border-radius:10px;background:rgba(255,255,255,0.03);display:grid;place-items:center">
            <!-- Python (snake-like) svg -->
            <svg width="36" height="36" viewBox="0 0 24 24" fill="none" aria-hidden="true" xmlns="http://www.w3.org/2000/svg">
              <path d="M6 3c1.5 0 3 1 3 2.5V6h-4C4.7 6 4 6.7 4 7.5V9c0 .8.7 1.5 1.5 1.5H10c1.1 0 2 .9 2 2v1.5C12 15.9 10.9 17 9.5 17H7v1.5C7 19.9 8.1 21 9.5 21H12" stroke="#fff" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/>
              <path d="M18 21c-1.5 0-3-1-3-2.5V18h4c1.3 0 2-.7 2-1.5V15c0-.8-.7-1.5-1.5-1.5H14c-1.1 0-2-.9-2-2V9.5C12 6.1 13.1 5 14.5 5H17V3.5C17 2.1 16 1 14.5 1H12" stroke="#fff" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
          </div>

          <div style="flex:1">
            <h4>Python (tools & scripting)</h4>
            <div class="bar" aria-hidden="true"><i style="width:56%"></i></div>
            <p style="margin-top:10px;color:rgba(255,255,255,0.9)">Scripting, quick prototypes, data tools.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- PROJECTS -->
    <section id="projects" class="fade-up delay-2" aria-labelledby="projects-title">
      <h2 id="projects-title" class="section-title">Projects</h2>
      <p class="section-sub">Selected projects — embedded, web and IoT.</p>

      <div class="grid" role="list" aria-label="Projects list">
        <!-- Track Race -->
        <article class="card glow-card fade-up delay-1" role="article">
          <div class="icon" aria-hidden="true"><span style="font-size:22px">🏁</span></div>
          <h3>Track Race</h3>
          <p>A timed race-tracking system for model cars with lap counting, live display and analytics (microcontroller + web dashboard).</p>
          <div class="tags" aria-hidden="true">
            <span class="tag">C</span>
            <span class="tag">Embedded</span>
            <span class="tag">Realtime</span>
          </div>
          <div style="margin-top:12px;">
            <a class="btn" href="#" target="_blank">View Repo</a>
            <a class="btn" href="#" style="margin-left:8px">Demo</a>
          </div>
        </article>

        <!-- Home Automation -->
        <article class="card glow-card fade-up delay-2">
          <div class="icon" aria-hidden="true"><span style="font-size:22px">🏠</span></div>
          <h3>Home Automation</h3>
          <p>Smart home control system using sensors, relays and scheduling. Mobile UI + MQTT connectivity for reliable remote control.</p>
          <div class="tags">
            <span class="tag">C++</span>
            <span class="tag">IoT</span>
            <span class="tag">MQTT</span>
          </div>
          <div style="margin-top:12px;">
            <a class="btn" href="#" target="_blank">View Repo</a>
          </div>
        </article>

        <!-- SWILLS Web Developer -->
        <article class="card glow-card fade-up delay-3">
          <div class="icon" aria-hidden="true"><i class="fas fa-globe"></i></div>
          <h3>SWILLS Website</h3>
          <p>Responsive, modern website for a small business. Built with clean HTML/CSS and JavaScript for interactive elements.</p>
          <div class="tags">
            <span class="tag">HTML</span>
            <span class="tag">CSS</span>
            <span class="tag">JavaScript</span>
          </div>
          <div style="margin-top:12px;">
            <a class="btn" href="#" target="_blank">Live Site</a>
            <a class="btn" href="#" style="margin-left:8px">Source</a>
          </div>
        </article>

        <!-- Do You Know? -->
        <article class="card glow-card fade-up delay-3">
          <div class="icon" aria-hidden="true"><i class="fas fa-question-circle"></i></div>
          <h3>Do You Know?</h3>
          <p>Interactive knowledge quiz that tests users on topics with instant feedback and score tracking. Fun, educational web app.</p>
          <div class="tags">
            <span class="tag">JavaScript</span>
            <span class="tag">Web App</span>
            <span class="tag">UX</span>
          </div>
          <div style="margin-top:12px;">
            <a class="btn" href="#" target="_blank">Try Demo</a>
            <a class="btn" href="#" style="margin-left:8px">Source</a>
          </div>
        </article>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="fade-up delay-2" aria-labelledby="contact-title">
      <h2 id="contact-title" class="section-title">Contact</h2>
      <p class="section-sub">Want to collaborate? Send a message or email me directly.</p>

      <div class="contact-grid">
        <form class="contact-card" id="contactForm" aria-label="Contact form">
          <h3 style="margin-top:0">Message me</h3>
          <label for="name">Your name</label>
          <input id="name" name="name" type="text" placeholder="Your name" required>

          <label for="email" style="margin-top:10px">Your email</label>
          <input id="email" name="email" type="email" placeholder="you@example.com" required>

          <label for="message" style="margin-top:10px">Message</label>
          <textarea id="message" name="message" rows="5" placeholder="Tell me about the project..." required></textarea>

          <div style="margin-top:12px;display:flex;gap:10px;flex-wrap:wrap">
            <button class="btn btn-light" type="submit">Send message</button>
            <a class="btn" href="mailto:bhavygol@gmail.com">Email directly</a>
          </div>
        </form>

        <aside class="contact-card" aria-label="Contact details">
          <div style="margin-bottom:12px">
            <strong>Email</strong>
            <div style="color:rgba(255,255,255,0.9);margin-top:6px">bhavygol@gmail.com</div>
          </div>

          <div style="margin-bottom:12px">
            <strong>Location</strong>
            <div style="color:rgba(255,255,255,0.9);margin-top:6px">India (city)</div>
          </div>

          <div>
            <strong>Find me</strong>
            <div style="margin-top:8px; display:flex; gap:8px; flex-wrap:wrap">
              <a class="btn" href="#" target="_blank"><i class="fab fa-github" aria-hidden="true"></i> GitHub</a>
              <a class="btn" href="#" target="_blank"><i class="fab fa-linkedin" aria-hidden="true"></i> LinkedIn</a>
            </div>
          </div>
        </aside>
      </div>
    </section>

    <footer style="margin-top:40px;text-align:center;color:rgba(255,255,255,0.85);padding:24px 0">
      © <span id="yr"></span> Bhavy Gol — Built with ❤️
    </footer>

  </main>

  <script>
    // initialize lucide icons (if available)
    if (typeof lucide !== "undefined" && lucide.createIcons) {
      lucide.createIcons();
    }

    // set year in footer
    document.getElementById('yr').textContent = new Date().getFullYear();

    // Smooth reveal on scroll (simple, lightweight)
    const revealElems = document.querySelectorAll('.fade-up');
    const revealObserver = new IntersectionObserver((entries)=>{
      entries.forEach(entry=>{
        if(entry.isIntersecting){
          entry.target.style.opacity = 1;
          entry.target.style.transform = 'none';
          entry.target.style.animation = (entry.target.classList.contains('delay-1') ? 'none' : 'none');
        }
      });
    }, { threshold: 0.12 });
    revealElems.forEach(el => revealObserver.observe(el));

    // Contact form: open mail client by default (client-side fallback)
    const form = document.getElementById('contactForm');
    form.addEventListener('submit', function(e){
      e.preventDefault();
      const name = encodeURIComponent(document.getElementById('name').value.trim());
      const email = encodeURIComponent(document.getElementById('email').value.trim());
      const message = encodeURIComponent(document.getElementById('message').value.trim());
      const subject = encodeURIComponent('Portfolio message from ' + (name || 'Visitor'));
      const body = encodeURIComponent('Name: ' + (name || '') + '\nEmail: ' + (email || '') + '\n\n' + (message || ''));
      window.location.href = `mailto:bhavygol@gmail.com?subject=${subject}&body=${body}`;
    });

    // Resume placeholder function (replace with your resume url)
    function openResume(){
      // Replace '#' with a real resume URL or file path
      window.open('#', '_blank');
    }

    // Small accessibility: keyboard-friendly skip to content
    // Add focus outline for keyboard users
    document.addEventListener('keydown', function(e){
      if(e.key === 'Tab') document.body.classList.add('show-focus');
    });
  </script>
</body>
</html>
# personal-portfolio
