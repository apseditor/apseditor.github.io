<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Arghya Samanta — Premium Video Editor</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Instrument+Sans:wght@400;500;600;700&family=Instrument+Serif:ital@0;1&display=swap" rel="stylesheet" />
<style>
  /* ── Reset & Variables ── */
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

  :root {
    --bg: #080a10;
    --grid: rgba(255,255,255,0.045);
    --white: #f5f7ff;
    --gray-1: #9ba3b8;
    --gray-2: #3a3f52;
    --blue-glow: #4f8ef7;
    --blue-soft: #2563eb;
    --glass-bg: rgba(255,255,255,0.04);
    --glass-border: rgba(255,255,255,0.09);
    --glass-hover: rgba(255,255,255,0.07);
    --font-head: 'Instrument Sans', sans-serif;
    --font-body: 'Instrument Serif', serif;
  }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--white);
    font-family: var(--font-body);
    overflow-x: hidden;
    line-height: 1.6;
  }

  /* ── Grid Background ── */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(var(--grid) 1px, transparent 1px),
      linear-gradient(90deg, var(--grid) 1px, transparent 1px);
    background-size: 64px 64px;
    pointer-events: none;
    z-index: 0;
  }

  /* Radial glow at top */
  body::after {
    content: '';
    position: fixed;
    top: -200px;
    left: 50%;
    transform: translateX(-50%);
    width: 900px;
    height: 600px;
    background: radial-gradient(ellipse at center, rgba(79,142,247,0.12) 0%, transparent 70%);
    pointer-events: none;
    z-index: 0;
  }

  /* ── Nav ── */
  nav {
    position: fixed;
    top: 20px;
    left: 50%;
    transform: translateX(-50%);
    z-index: 100;
    display: flex;
    align-items: center;
    gap: 2px;
    background: rgba(10,12,20,0.65);
    border: 1px solid var(--glass-border);
    border-radius: 60px;
    padding: 8px 12px;
    backdrop-filter: blur(24px);
    -webkit-backdrop-filter: blur(24px);
  }

  nav a {
    font-family: var(--font-head);
    font-size: 0.78rem;
    font-weight: 500;
    letter-spacing: 0.04em;
    color: var(--gray-1);
    text-decoration: none;
    padding: 6px 16px;
    border-radius: 40px;
    transition: color 0.2s, background 0.2s;
  }

  nav a:hover, nav a.active {
    color: var(--white);
    background: rgba(255,255,255,0.07);
  }

  /* ── Utility ── */
  .container {
    max-width: 1100px;
    margin: 0 auto;
    padding: 0 32px;
    position: relative;
    z-index: 1;
  }

  section { padding: 100px 0; }

  .label {
    font-family: var(--font-head);
    font-size: 0.7rem;
    font-weight: 600;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--blue-glow);
    text-shadow: 0 0 18px rgba(79,142,247,0.7), 0 0 40px rgba(79,142,247,0.3);
    margin-bottom: 16px;
    display: block;
  }

  h1, h2, h3 { font-family: var(--font-head); font-weight: 700; }

  h1 {
    font-size: clamp(3rem, 8vw, 6rem);
    line-height: 1.0;
    letter-spacing: -0.03em;
    color: var(--white);
    text-shadow: 0 0 80px rgba(79,142,247,0.15);
  }

  h2 {
    font-size: clamp(1.8rem, 4vw, 2.8rem);
    letter-spacing: -0.02em;
    color: var(--white);
    text-shadow: 0 0 40px rgba(79,142,247,0.2);
  }

  /* ── Glass Card ── */
  .glass {
    background: var(--glass-bg);
    border: 1px solid var(--glass-border);
    border-radius: 20px;
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);
    transition: background 0.3s, border-color 0.3s, transform 0.3s;
  }

  .glass:hover {
    background: var(--glass-hover);
    border-color: rgba(79,142,247,0.2);
    transform: translateY(-2px);
  }

  /* ── HERO ── */
  #hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    padding-top: 120px;
  }

  .hero-inner {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: center;
  }

  .hero-text .name-accent {
    background: linear-gradient(135deg, #fff 30%, var(--blue-glow));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    filter: drop-shadow(0 0 30px rgba(79,142,247,0.4));
  }

  .hero-text p {
    margin-top: 20px;
    font-size: 1.1rem;
    color: var(--gray-1);
    max-width: 420px;
    line-height: 1.75;
  }

  .hero-cta {
    display: flex;
    gap: 12px;
    margin-top: 36px;
    flex-wrap: wrap;
  }

  .btn {
    font-family: var(--font-head);
    font-size: 0.85rem;
    font-weight: 600;
    letter-spacing: 0.04em;
    padding: 12px 28px;
    border-radius: 50px;
    text-decoration: none;
    transition: all 0.25s;
    cursor: pointer;
    border: none;
    display: inline-flex;
    align-items: center;
    gap: 8px;
  }

  .btn-primary {
    background: var(--blue-glow);
    color: #fff;
    box-shadow: 0 0 30px rgba(79,142,247,0.4), 0 4px 20px rgba(0,0,0,0.4);
  }

  .btn-primary:hover {
    box-shadow: 0 0 50px rgba(79,142,247,0.6), 0 4px 30px rgba(0,0,0,0.5);
    transform: translateY(-2px);
  }

  .btn-secondary {
    background: var(--glass-bg);
    color: var(--white);
    border: 1px solid var(--glass-border);
    backdrop-filter: blur(12px);
  }

  .btn-secondary:hover {
    background: var(--glass-hover);
    border-color: rgba(79,142,247,0.3);
  }

  /* Stats row */
  .stats-row {
    display: flex;
    gap: 32px;
    margin-top: 48px;
  }

  .stat {
    display: flex;
    flex-direction: column;
    gap: 2px;
  }

  .stat-num {
    font-family: var(--font-head);
    font-size: 1.8rem;
    font-weight: 700;
    color: var(--blue-glow);
    text-shadow: 0 0 20px rgba(79,142,247,0.6), 0 0 60px rgba(79,142,247,0.2);
    line-height: 1;
  }

  .stat-label {
    font-family: var(--font-head);
    font-size: 0.65rem;
    font-weight: 600;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--gray-1);
  }

  .stat-divider {
    width: 1px;
    background: var(--gray-2);
    align-self: stretch;
  }

  /* Profile card */
  .profile-card {
    position: relative;
    padding: 4px;
    border-radius: 24px;
    background: linear-gradient(135deg, rgba(79,142,247,0.3), rgba(255,255,255,0.05), rgba(79,142,247,0.1));
  }

  .profile-card-inner {
    border-radius: 20px;
    overflow: hidden;
    position: relative;
  }

  .profile-card img {
    width: 100%;
    height: 480px;
    object-fit: cover;
    display: block;
    border-radius: 20px;
  }

  .profile-card::before {
    content: '';
    position: absolute;
    inset: -1px;
    border-radius: 25px;
    background: linear-gradient(135deg, rgba(79,142,247,0.5), transparent 50%, rgba(79,142,247,0.2));
    z-index: -1;
    filter: blur(20px);
    opacity: 0.6;
  }

  /* Intro video tag inside hero */
  .intro-video-wrap {
    margin-top: 20px;
    border-radius: 14px;
    overflow: hidden;
    border: 1px solid var(--glass-border);
    box-shadow: 0 0 40px rgba(79,142,247,0.08);
  }

  .intro-video-wrap iframe {
    width: 100%;
    height: 200px;
    border: none;
    display: block;
  }

  /* ── About ── */
  #about .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 48px;
    align-items: start;
  }

  .about-text p {
    color: var(--gray-1);
    margin-bottom: 16px;
    font-size: 1.05rem;
  }

  .skills-list {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 24px;
  }

  .skill-tag {
    font-family: var(--font-head);
    font-size: 0.75rem;
    font-weight: 500;
    color: var(--gray-1);
    background: var(--glass-bg);
    border: 1px solid var(--glass-border);
    border-radius: 6px;
    padding: 5px 12px;
    transition: all 0.2s;
  }

  .skill-tag:hover {
    color: var(--blue-glow);
    border-color: rgba(79,142,247,0.3);
    text-shadow: 0 0 12px rgba(79,142,247,0.5);
  }

  .about-right { display: flex; flex-direction: column; gap: 16px; }

  .info-card {
    padding: 20px 24px;
    border-radius: 16px;
  }

  .info-card-label {
    font-family: var(--font-head);
    font-size: 0.65rem;
    font-weight: 600;
    letter-spacing: 0.16em;
    text-transform: uppercase;
    color: var(--blue-glow);
    text-shadow: 0 0 12px rgba(79,142,247,0.6);
    margin-bottom: 6px;
  }

  .info-card-value {
    font-family: var(--font-head);
    font-size: 0.95rem;
    color: var(--white);
  }

  /* ── Portfolio ── */
  .section-header {
    display: flex;
    align-items: flex-end;
    justify-content: space-between;
    margin-bottom: 48px;
  }

  .portfolio-cats {
    display: flex;
    gap: 8px;
    margin-bottom: 40px;
    flex-wrap: wrap;
  }

  .cat-btn {
    font-family: var(--font-head);
    font-size: 0.78rem;
    font-weight: 600;
    letter-spacing: 0.06em;
    padding: 8px 20px;
    border-radius: 50px;
    border: 1px solid var(--glass-border);
    background: transparent;
    color: var(--gray-1);
    cursor: pointer;
    transition: all 0.2s;
  }

  .cat-btn:hover, .cat-btn.active {
    background: rgba(79,142,247,0.1);
    border-color: rgba(79,142,247,0.4);
    color: var(--blue-glow);
    text-shadow: 0 0 10px rgba(79,142,247,0.5);
  }

  .video-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
  }

  .video-card {
    border-radius: 16px;
    overflow: hidden;
    cursor: pointer;
    position: relative;
  }

  .video-card iframe {
    width: 100%;
    height: 200px;
    border: none;
    display: block;
    pointer-events: none;
  }

  .video-card-info {
    padding: 14px 16px;
  }

  .video-card-title {
    font-family: var(--font-head);
    font-size: 0.85rem;
    font-weight: 600;
    color: var(--white);
    margin-bottom: 4px;
  }

  .video-card-cat {
    font-family: var(--font-head);
    font-size: 0.7rem;
    font-weight: 500;
    color: var(--blue-glow);
    letter-spacing: 0.1em;
    text-transform: uppercase;
    text-shadow: 0 0 10px rgba(79,142,247,0.5);
  }

  /* Click overlay to open modal */
  .video-overlay {
    position: absolute;
    inset: 0;
    z-index: 2;
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    transition: opacity 0.25s;
    background: rgba(0,0,0,0.4);
    border-radius: 16px 16px 0 0;
  }

  .video-card:hover .video-overlay { opacity: 1; }

  .play-btn-lg {
    width: 52px;
    height: 52px;
    background: rgba(79,142,247,0.85);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 0 30px rgba(79,142,247,0.6);
    backdrop-filter: blur(8px);
  }

  .play-btn-lg svg { width: 20px; height: 20px; fill: #fff; margin-left: 3px; }

  /* ── Modal ── */
  .modal-overlay {
    position: fixed;
    inset: 0;
    z-index: 999;
    background: rgba(0,0,0,0.85);
    backdrop-filter: blur(20px);
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    pointer-events: none;
    transition: opacity 0.3s;
  }

  .modal-overlay.open {
    opacity: 1;
    pointer-events: all;
  }

  .modal-box {
    width: 90%;
    max-width: 900px;
    border-radius: 20px;
    overflow: hidden;
    position: relative;
    transform: scale(0.94);
    transition: transform 0.3s;
  }

  .modal-overlay.open .modal-box { transform: scale(1); }

  .modal-box iframe {
    width: 100%;
    height: 500px;
    border: none;
    display: block;
  }

  .modal-close {
    position: absolute;
    top: 14px;
    right: 14px;
    width: 34px;
    height: 34px;
    border-radius: 50%;
    background: rgba(0,0,0,0.6);
    border: 1px solid var(--glass-border);
    color: var(--white);
    font-size: 18px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    z-index: 10;
    backdrop-filter: blur(8px);
    line-height: 1;
    transition: background 0.2s;
  }

  .modal-close:hover { background: rgba(79,142,247,0.3); }

  /* ── Contact ── */
  #contact .contact-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 40px;
    align-items: start;
  }

  .contact-info h2 { margin-bottom: 16px; }

  .contact-info p {
    color: var(--gray-1);
    margin-bottom: 32px;
    font-size: 1.05rem;
  }

  .contact-links { display: flex; flex-direction: column; gap: 12px; }

  .contact-link {
    display: flex;
    align-items: center;
    gap: 14px;
    padding: 16px 20px;
    border-radius: 14px;
    text-decoration: none;
    transition: all 0.2s;
  }

  .contact-link:hover {
    border-color: rgba(79,142,247,0.3) !important;
    transform: translateX(4px);
  }

  .contact-link-icon {
    width: 36px;
    height: 36px;
    border-radius: 8px;
    background: rgba(79,142,247,0.12);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
  }

  .contact-link-icon svg { width: 18px; height: 18px; }

  .contact-link-text { flex: 1; }

  .contact-link-label {
    font-family: var(--font-head);
    font-size: 0.68rem;
    font-weight: 600;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--gray-1);
    margin-bottom: 2px;
  }

  .contact-link-value {
    font-family: var(--font-head);
    font-size: 0.9rem;
    font-weight: 500;
    color: var(--white);
  }

  .contact-form { display: flex; flex-direction: column; gap: 14px; }

  .form-group { display: flex; flex-direction: column; gap: 6px; }

  .form-label {
    font-family: var(--font-head);
    font-size: 0.72rem;
    font-weight: 600;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: var(--gray-1);
  }

  .form-input, .form-textarea {
    background: var(--glass-bg);
    border: 1px solid var(--glass-border);
    border-radius: 10px;
    color: var(--white);
    font-family: var(--font-head);
    font-size: 0.9rem;
    padding: 12px 16px;
    outline: none;
    transition: border-color 0.2s, box-shadow 0.2s;
    resize: none;
  }

  .form-input:focus, .form-textarea:focus {
    border-color: rgba(79,142,247,0.5);
    box-shadow: 0 0 0 3px rgba(79,142,247,0.1);
  }

  .form-input::placeholder, .form-textarea::placeholder { color: var(--gray-2); }

  /* ── Footer ── */
  footer {
    border-top: 1px solid var(--glass-border);
    padding: 32px 0;
    position: relative;
    z-index: 1;
  }

  .footer-inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .footer-brand {
    font-family: var(--font-head);
    font-size: 0.85rem;
    font-weight: 700;
    color: var(--white);
    letter-spacing: 0.04em;
  }

  .footer-copy {
    font-family: var(--font-head);
    font-size: 0.75rem;
    color: var(--gray-1);
  }

  /* ── Scroll animations ── */
  .fade-in {
    opacity: 0;
    transform: translateY(28px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }

  .fade-in.visible {
    opacity: 1;
    transform: none;
  }

  .fade-in:nth-child(2) { transition-delay: 0.1s; }
  .fade-in:nth-child(3) { transition-delay: 0.2s; }
  .fade-in:nth-child(4) { transition-delay: 0.3s; }

  /* ── Responsive ── */
  @media (max-width: 768px) {
    .hero-inner { grid-template-columns: 1fr; gap: 48px; }
    .profile-card img { height: 300px; }
    #about .about-grid { grid-template-columns: 1fr; }
    #contact .contact-grid { grid-template-columns: 1fr; }
    .video-grid { grid-template-columns: 1fr; }
    .section-header { flex-direction: column; align-items: flex-start; gap: 12px; }
    nav { width: calc(100% - 32px); justify-content: center; }
  }

  @media (max-width: 500px) {
    .video-grid { grid-template-columns: 1fr; }
    h1 { font-size: 2.4rem; }
    .stats-row { gap: 16px; }
    .stat-num { font-size: 1.4rem; }
  }
</style>
</head>
<body>

<!-- Nav -->
<nav>
  <a href="#hero" class="active">Home</a>
  <a href="#about">About</a>
  <a href="#portfolio">Work</a>
  <a href="#contact">Contact</a>
</nav>

<!-- ── HERO ── -->
<section id="hero">
  <div class="container">
    <div class="hero-inner">
      <div class="hero-text">
        <span class="label">Premium Video Editor</span>
        <h1><span class="name-accent">Arghya<br>Samanta</span></h1>
        <p>High-end freelance video editor with 4 years of hands-on agency experience. Specializing in dynamic, high-retention content — from cinematic real estate to viral medical reels.</p>

        <div class="stats-row">
          <div class="stat">
            <span class="stat-num">30+</span>
            <span class="stat-label">Clients</span>
          </div>
          <div class="stat-divider"></div>
          <div class="stat">
            <span class="stat-num">81.2K</span>
            <span class="stat-label">Subscribers</span>
          </div>
          <div class="stat-divider"></div>
          <div class="stat">
            <span class="stat-num">58.5M</span>
            <span class="stat-label">Views</span>
          </div>
        </div>

        <div class="hero-cta">
          <a href="#portfolio" class="btn btn-primary">
            <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><polygon points="5 3 19 12 5 21 5 3"/></svg>
            View Work
          </a>
          <a href="#contact" class="btn btn-secondary">Get in Touch</a>
        </div>
      </div>

      <div>
        <div class="profile-card">
          <div class="profile-card-inner">
            <img src="file_000000000acc71fa9a9c5a95b3308284.png" alt="Arghya Samanta" onerror="this.style.display='none'; this.nextElementSibling.style.display='flex';" />
            <!-- Fallback if image path doesn't resolve in artifact -->
            <div style="display:none; width:100%; height:480px; background:linear-gradient(135deg,#16102f,#1a1f35); align-items:center; justify-content:center; flex-direction:column; gap:12px; border-radius:20px;">
              <div style="width:80px;height:80px;border-radius:50%;background:rgba(79,142,247,0.15);border:2px solid rgba(79,142,247,0.3);display:flex;align-items:center;justify-content:center;">
                <svg width="36" height="36" fill="none" stroke="rgba(79,142,247,0.7)" stroke-width="1.5" viewBox="0 0 24 24"><circle cx="12" cy="8" r="4"/><path d="M4 20c0-4 3.6-7 8-7s8 3 8 7"/></svg>
              </div>
              <span style="font-family:var(--font-head);color:var(--gray-1);font-size:0.85rem;">Arghya Samanta</span>
            </div>
          </div>
        </div>

        <!-- Intro video below photo -->
        <div class="intro-video-wrap" style="margin-top:16px;">
          <iframe src="https://drive.google.com/file/d/12lZlO3zvHG5wTu0uUrsm9qH6eCMKPZpV/preview" allowfullscreen allow="autoplay"></iframe>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ── ABOUT ── -->
<section id="about">
  <div class="container">
    <div class="about-grid">
      <div class="about-text fade-in">
        <span class="label">Who I Am</span>
        <h2 style="margin-bottom:24px;">Crafting Stories<br><em style="font-family:var(--font-body);font-style:italic;color:var(--gray-1);">Frame by Frame</em></h2>
        <p>I'm a premium freelance video editor based in India, with 4 years of hands-on experience across agencies and independent clients. I specialize in blending technical precision with creative pacing.</p>
        <p>From high-retention YouTube shorts to cinematic real estate walkthroughs — every cut I make is intentional. My workflow spans Adobe Premiere Pro, After Effects, CapCut, Topaz AI, and more.</p>
        <p>Currently a Class 12 student who built a 81K+ YouTube channel from scratch with 58.5M+ views.</p>

        <div class="skills-list">
          <span class="skill-tag">Adobe Premiere Pro</span>
          <span class="skill-tag">Adobe Photoshop</span>
          <span class="skill-tag">After Motion</span>
          <span class="skill-tag">Alight Motion</span>
          <span class="skill-tag">CapCut PC</span>
          <span class="skill-tag">Topaz AI</span>
          <span class="skill-tag">Color Grading</span>
          <span class="skill-tag">Motion Graphics</span>
          <span class="skill-tag">Podcast Production</span>
          <span class="skill-tag">VFX Compositing</span>
        </div>
      </div>

      <div class="about-right fade-in">
        <div class="glass info-card">
          <div class="info-card-label">Specialty</div>
          <div class="info-card-value">High-Retention Shorts & Teasers</div>
        </div>
        <div class="glass info-card">
          <div class="info-card-label">Focus Areas</div>
          <div class="info-card-value">Medical · Real Estate · Podcasts · Motion Graphics</div>
        </div>
        <div class="glass info-card">
          <div class="info-card-label">Portfolio</div>
          <div class="info-card-value"><a href="https://framefolio.in/apsvisuallab" target="_blank" style="color:var(--blue-glow);text-decoration:none;text-shadow:0 0 12px rgba(79,142,247,0.5);">framefolio.in/apsvisuallab</a></div>
        </div>
        <div class="glass info-card">
          <div class="info-card-label">YouTube</div>
          <div class="info-card-value"><a href="https://youtube.com/@aps_editor_1m" target="_blank" style="color:var(--blue-glow);text-decoration:none;text-shadow:0 0 12px rgba(79,142,247,0.5);">@aps_editor_1m</a></div>
        </div>
        <div class="glass info-card">
          <div class="info-card-label">Location</div>
          <div class="info-card-value">India</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ── PORTFOLIO ── -->
<section id="portfolio">
  <div class="container">
    <div class="section-header fade-in">
      <div>
        <span class="label">Selected Work</span>
        <h2>Portfolio</h2>
      </div>
    </div>

    <div class="portfolio-cats">
      <button class="cat-btn active" onclick="filterCat('all', this)">All</button>
      <button class="cat-btn" onclick="filterCat('medical', this)">Medical</button>
      <button class="cat-btn" onclick="filterCat('realestate', this)">Real Estate</button>
      <button class="cat-btn" onclick="filterCat('podcast', this)">Podcast</button>
      <button class="cat-btn" onclick="filterCat('other', this)">Other</button>
    </div>

    <div class="video-grid" id="videoGrid">

      <!-- Medical -->
      <div class="glass video-card fade-in" data-cat="medical" onclick="openModal('https://drive.google.com/file/d/12ptrR7XBpbgoMoTmfMQH67693zIvHGcB/preview')">
        <div class="video-overlay"><div class="play-btn-lg"><svg viewBox="0 0 24 24"><polygon points="5 3 19 12 5 21 5 3"/></svg></div></div>
        <iframe src="https://drive.google.com/file/d/12ptrR7XBpbgoMoTmfMQH67693zIvHGcB/preview" allowfullscreen tabindex="-1"></iframe>
        <div class="video-card-info">
          <div class="video-card-title">Medical Content Edit #1</div>
          <div class="video-card-cat">Medical</div>
        </div>
      </div>

      <div class="glass video-card fade-in" data-cat="medical" onclick="openModal('https://drive.google.com/file/d/1Df-ISzAKITq5itUM8OnUR5-eacIj6kPg/preview')">
        <div class="video-overlay"><div class="play-btn-lg"><svg viewBox="0 0 24 24"><polygon points="5 3 19 12 5 21 5 3"/></svg></div></div>
        <iframe src="https://drive.google.com/file/d/1Df-ISzAKITq5itUM8OnUR5-eacIj6kPg/preview" allowfullscreen tabindex="-1"></iframe>
        <div class="video-card-info">
          <div class="video-card-title">Medical Content Edit #2</div>
          <div class="video-card-cat">Medical</div>
        </div>
      </div>

      <div class="glass video-card fade-in" data-cat="medical" onclick="openModal('https://drive.google.com/file/d/1Fh1mjjHSyDKMT3yKUdIzjnXV3s1ykqQa/preview')">
        <div class="video-overlay"><div class="play-btn-lg"><svg viewBox="0 0 24 24"><polygon points="5 3 19 12 5 21 5 3"/></svg></div></div>
        <iframe src="https://drive.google.com/file/d/1Fh1mjjHSyDKMT3yKUdIzjnXV3s1ykqQa/preview" allowfullscreen tabindex="-1"></iframe>
        <div class="video-card-info">
          <div class="video-card-title">Medical Content Edit #3</div>
          <div class="video-card-cat">Medical</div>
        </div>
      </div>

      <div class="glass video-card fade-in" data-cat="medical" onclick="openModal('https://drive.google.com/file/d/1r1DB0ENEdR6SForQ_zN8hWQLRevdaALz/preview')">
        <div class="video-overlay"><div class="play-btn-lg"><svg viewBox="0 0 24 24"><polygon points="5 3 19 12 5 21 5 3"/></svg></div></div>
        <iframe src="https://drive.google.com/file/d/1r1DB0ENEdR6SForQ_zN8hWQLRevdaALz/preview" allowfullscreen tabindex="-1"></iframe>
        <div class="video-card-info">
          <div class="video-card-title">Medical Content Edit #4</div>
          <div class="video-card-cat">Medical</div>
        </div>
      </div>

      <!-- Real Estate -->
      <div class="glass video-card fade-in" data-cat="realestate" onclick="openModal('https://drive.google.com/file/d/1J3a7sXH9Mp3inen2q6BmfouVw1gALdHd/preview')">
        <div class="video-overlay"><div class="play-btn-lg"><svg viewBox="0 0 24 24"><polygon points="5 3 19 12 5 21 5 3"/></svg></div></div>
        <iframe src="https://drive.google.com/file/d/1J3a7sXH9Mp3inen2q6BmfouVw1gALdHd/preview" allowfullscreen tabindex="-1"></iframe>
        <div class="video-card-info">
          <div class="video-card-title">Real Estate Showcase #1</div>
          <div class="video-card-cat">Real Estate</div>
        </div>
      </div>

      <div class="glass video-card fade-in" data-cat="realestate" onclick="openModal('https://drive.google.com/file/d/1YWQk4aYFgErMnVKe6QhYh74AEPXTfpEo/preview')">
        <div class="video-overlay"><div class="play-btn-lg"><svg viewBox="0 0 24 24"><polygon points="5 3 19 12 5 21 5 3"/></svg></div></div>
        <iframe src="https://drive.google.com/file/d/1YWQk4aYFgErMnVKe6QhYh74AEPXTfpEo/preview" allowfullscreen tabindex="-1"></iframe>
        <div class="video-card-info">
          <div class="video-card-title">Real Estate Showcase #2</div>
          <div class="video-card-cat">Real Estate</div>
        </div>
      </div>

      <div class="glass video-card fade-in" data-cat="realestate" onclick="openModal('https://drive.google.com/file/d/1BTVzmjPaMjegu0xYx9YUB5wpcUoCgFYX/preview')">
        <div class="video-overlay"><div class="play-btn-lg"><svg viewBox="0 0 24 24"><polygon points="5 3 19 12 5 21 5 3"/></svg></div></div>
        <iframe src="https://drive.google.com/file/d/1BTVzmjPaMjegu0xYx9YUB5wpcUoCgFYX/preview" allowfullscreen tabindex="-1"></iframe>
        <div class="video-card-info">
          <div class="video-card-title">Real Estate Showcase #3</div>
          <div class="video-card-cat">Real Estate</div>
        </div>
      </div>

      <!-- Podcast -->
      <div class="glass video-card fade-in" data-cat="podcast" onclick="openModal('https://drive.google.com/file/d/1XfwntyIalFjDB-9f6VRitjPIn6zOPkfZ/preview')">
        <div class="video-overlay"><div class="play-btn-lg"><svg viewBox="0 0 24 24"><polygon points="5 3 19 12 5 21 5 3"/></svg></div></div>
        <iframe src="https://drive.google.com/file/d/1XfwntyIalFjDB-9f6VRitjPIn6zOPkfZ/preview" allowfullscreen tabindex="-1"></iframe>
        <div class="video-card-info">
          <div class="video-card-title">Podcast Reel Edit</div>
          <div class="video-card-cat">Podcast</div>
        </div>
      </div>

      <!-- Other -->
      <div class="glass video-card fade-in" data-cat="other" onclick="openModal('https://drive.google.com/file/d/1W6h-oND23LMk7i1mx2LyCRSUYnv4j5ke/preview')">
        <div class="video-overlay"><div class="play-btn-lg"><svg viewBox="0 0 24 24"><polygon points="5 3 19 12 5 21 5 3"/></svg></div></div>
        <iframe src="https://drive.google.com/file/d/1W6h-oND23LMk7i1mx2LyCRSUYnv4j5ke/preview" allowfullscreen tabindex="-1"></iframe>
        <div class="video-card-info">
          <div class="video-card-title">Creative Edit #1</div>
          <div class="video-card-cat">Other</div>
        </div>
      </div>

      <div class="glass video-card fade-in" data-cat="other" onclick="openModal('https://drive.google.com/file/d/1EGmHAPFnQ57dXzP04mfwo2WNWvIHtcL0/preview')">
        <div class="video-overlay"><div class="play-btn-lg"><svg viewBox="0 0 24 24"><polygon points="5 3 19 12 5 21 5 3"/></svg></div></div>
        <iframe src="https://drive.google.com/file/d/1EGmHAPFnQ57dXzP04mfwo2WNWvIHtcL0/preview" allowfullscreen tabindex="-1"></iframe>
        <div class="video-card-info">
          <div class="video-card-title">Creative Edit #2</div>
          <div class="video-card-cat">Other</div>
        </div>
      </div>

      <div class="glass video-card fade-in" data-cat="other" onclick="openModal('https://drive.google.com/file/d/1Ng5_1mZxCAdrFmiH39N0hPeABTaiBo71/preview')">
        <div class="video-overlay"><div class="play-btn-lg"><svg viewBox="0 0 24 24"><polygon points="5 3 19 12 5 21 5 3"/></svg></div></div>
        <iframe src="https://drive.google.com/file/d/1Ng5_1mZxCAdrFmiH39N0hPeABTaiBo71/preview" allowfullscreen tabindex="-1"></iframe>
        <div class="video-card-info">
          <div class="video-card-title">Creative Edit #3</div>
          <div class="video-card-cat">Other</div>
        </div>
      </div>

      <div class="glass video-card fade-in" data-cat="other" onclick="openModal('https://drive.google.com/file/d/1KC2LRwLPBvCKhSHUfGBomb3-rsa6bSGn/preview')">
        <div class="video-overlay"><div class="play-btn-lg"><svg viewBox="0 0 24 24"><polygon points="5 3 19 12 5 21 5 3"/></svg></div></div>
        <iframe src="https://drive.google.com/file/d/1KC2LRwLPBvCKhSHUfGBomb3-rsa6bSGn/preview" allowfullscreen tabindex="-1"></iframe>
        <div class="video-card-info">
          <div class="video-card-title">Creative Edit #4</div>
          <div class="video-card-cat">Other</div>
        </div>
      </div>

      <div class="glass video-card fade-in" data-cat="other" onclick="openModal('https://drive.google.com/file/d/1bg88H4LIaVU94Ob0zNxEvSCIahPaVpVb/preview')">
        <div class="video-overlay"><div class="play-btn-lg"><svg viewBox="0 0 24 24"><polygon points="5 3 19 12 5 21 5 3"/></svg></div></div>
        <iframe src="https://drive.google.com/file/d/1bg88H4LIaVU94Ob0zNxEvSCIahPaVpVb/preview" allowfullscreen tabindex="-1"></iframe>
        <div class="video-card-info">
          <div class="video-card-title">Creative Edit #5</div>
          <div class="video-card-cat">Other</div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- ── CONTACT ── -->
<section id="contact">
  <div class="container">
    <div style="text-align:center; margin-bottom: 64px;" class="fade-in">
      <span class="label">Let's Work Together</span>
      <h2>Ready to Create<br><em style="font-family:var(--font-body);font-style:italic;color:var(--gray-1);">Something Remarkable?</em></h2>
    </div>

    <div class="contact-grid">
      <div class="contact-info fade-in">
        <p>Whether it's a viral reel, a cinematic real estate video, or a full podcast edit — I'm ready to bring your vision to life with precision and creativity.</p>

        <div class="contact-links">
          <a href="mailto:apsediting120@gmail.com" class="glass contact-link">
            <div class="contact-link-icon">
              <svg fill="none" stroke="var(--blue-glow)" stroke-width="1.5" viewBox="0 0 24 24"><path d="M3 8l9 6 9-6M3 8v10a1 1 0 001 1h16a1 1 0 001-1V8M3 8a1 1 0 011-1h16a1 1 0 011 1"/></svg>
            </div>
            <div class="contact-link-text">
              <div class="contact-link-label">Email</div>
              <div class="contact-link-value">apsediting120@gmail.com</div>
            </div>
          </a>

          <a href="tel:+917318805018" class="glass contact-link">
            <div class="contact-link-icon">
              <svg fill="none" stroke="var(--blue-glow)" stroke-width="1.5" viewBox="0 0 24 24"><path d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/></svg>
            </div>
            <div class="contact-link-text">
              <div class="contact-link-label">Phone</div>
              <div class="contact-link-value">+91 73188 05018</div>
            </div>
          </a>

          <a href="https://framefolio.in/apsvisuallab" target="_blank" class="glass contact-link">
            <div class="contact-link-icon">
              <svg fill="none" stroke="var(--blue-glow)" stroke-width="1.5" viewBox="0 0 24 24"><path d="M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019-9"/></svg>
            </div>
            <div class="contact-link-text">
              <div class="contact-link-label">Portfolio</div>
              <div class="contact-link-value">framefolio.in/apsvisuallab</div>
            </div>
          </a>

          <a href="https://linkedin.com/in/aps-editor-37212640a" target="_blank" class="glass contact-link">
            <div class="contact-link-icon">
              <svg fill="var(--blue-glow)" viewBox="0 0 24 24"><path d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6zM2 9h4v12H2zm2-4a2 2 0 110 4 2 2 0 010-4z"/></svg>
            </div>
            <div class="contact-link-text">
              <div class="contact-link-label">LinkedIn</div>
              <div class="contact-link-value">aps-editor-37212640a</div>
            </div>
          </a>
        </div>
      </div>

      <div class="glass fade-in" style="padding: 32px; border-radius: 20px;">
        <h3 style="font-family:var(--font-head);font-size:1.1rem;margin-bottom:24px;color:var(--white);">Send a Message</h3>
        <div class="contact-form">
          <div class="form-group">
            <label class="form-label">Your Name</label>
            <input type="text" class="form-input" placeholder="John Doe" />
          </div>
          <div class="form-group">
            <label class="form-label">Email</label>
            <input type="email" class="form-input" placeholder="hello@example.com" />
          </div>
          <div class="form-group">
            <label class="form-label">Project Type</label>
            <input type="text" class="form-input" placeholder="Medical Reel, Real Estate, Podcast..." />
          </div>
          <div class="form-group">
            <label class="form-label">Message</label>
            <textarea class="form-textarea" rows="4" placeholder="Tell me about your project..."></textarea>
          </div>
          <a href="mailto:apsediting120@gmail.com" class="btn btn-primary" style="justify-content:center;margin-top:4px;">
            Send Message
          </a>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ── Footer ── -->
<footer>
  <div class="container">
    <div class="footer-inner">
      <span class="footer-brand">AP — Arghya Samanta</span>
      <span class="footer-copy">© 2026 · Premium Video Editor · India</span>
    </div>
  </div>
</footer>

<!-- ── Modal ── -->
<div class="modal-overlay" id="modal" onclick="closeModal(event)">
  <div class="modal-box glass">
    <button class="modal-close" onclick="closeModal()">✕</button>
    <iframe id="modalIframe" src="" allowfullscreen allow="autoplay"></iframe>
  </div>
</div>

<script>
  /* ── Modal ── */
  function openModal(src) {
    document.getElementById('modalIframe').src = src + '&autoplay=1';
    document.getElementById('modal').classList.add('open');
    document.body.style.overflow = 'hidden';
  }

  function closeModal(e) {
    if (e && e.target !== document.getElementById('modal')) return;
    document.getElementById('modal').classList.remove('open');
    document.getElementById('modalIframe').src = '';
    document.body.style.overflow = '';
  }

  document.addEventListener('keydown', e => { if (e.key === 'Escape') closeModal(); });

  /* ── Category filter ── */
  function filterCat(cat, btn) {
    document.querySelectorAll('.cat-btn').forEach(b => b.classList.remove('active'));
    btn.classList.add('active');
    document.querySelectorAll('.video-card').forEach(card => {
      card.style.display = (cat === 'all' || card.dataset.cat === cat) ? '' : 'none';
    });
  }

  /* ── Scroll fade-in ── */
  const observer = new IntersectionObserver(entries => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.1 });

  document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));

  /* ── Active nav on scroll ── */
  const sections = document.querySelectorAll('section[id]');
  const navLinks = document.querySelectorAll('nav a');

  window.addEventListener('scroll', () => {
    let cur = '';
    sections.forEach(s => {
      if (window.scrollY >= s.offsetTop - 160) cur = s.id;
    });
    navLinks.forEach(a => {
      a.classList.toggle('active', a.getAttribute('href') === '#' + cur);
    });
  });
</script>
</body>
</html>