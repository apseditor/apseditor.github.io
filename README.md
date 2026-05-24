<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Arghya Samanta — Video Editor</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Instrument+Sans:wght@400;500;600;700&family=Instrument+Serif:ital@0;1&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #080a0f;
    --surface: rgba(255,255,255,0.04);
    --surface-hover: rgba(255,255,255,0.08);
    --border: rgba(255,255,255,0.08);
    --border-glow: rgba(59,130,246,0.3);
    --text-primary: #f0f4ff;
    --text-secondary: #8a9bb8;
    --blue: #3b82f6;
    --blue-glow: rgba(59,130,246,0.15);
    --blue-bright: #60a5fa;
    --white: #ffffff;
    --gray: #1a1f2e;
    --font-head: 'Instrument Sans', sans-serif;
    --font-body: 'Instrument Serif', serif;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text-primary);
    font-family: var(--font-body);
    overflow-x: hidden;
    cursor: none;
  }

  /* Custom cursor */
  .cursor {
    position: fixed;
    width: 8px; height: 8px;
    background: var(--blue);
    border-radius: 50%;
    pointer-events: none;
    z-index: 9999;
    transform: translate(-50%,-50%);
    transition: transform 0.1s, width 0.2s, height 0.2s;
    box-shadow: 0 0 12px var(--blue), 0 0 24px var(--blue-glow);
  }
  .cursor-ring {
    position: fixed;
    width: 32px; height: 32px;
    border: 1px solid rgba(59,130,246,0.5);
    border-radius: 50%;
    pointer-events: none;
    z-index: 9998;
    transform: translate(-50%,-50%);
    transition: transform 0.15s ease, width 0.3s, height 0.3s, opacity 0.3s;
  }

  /* Grid Background */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(59,130,246,0.06) 1px, transparent 1px),
      linear-gradient(90deg, rgba(59,130,246,0.06) 1px, transparent 1px);
    background-size: 60px 60px;
    pointer-events: none;
    z-index: 0;
  }

  /* Radial glow at center */
  body::after {
    content: '';
    position: fixed;
    top: 0; left: 50%;
    transform: translateX(-50%);
    width: 800px; height: 600px;
    background: radial-gradient(ellipse at center top, rgba(59,130,246,0.08) 0%, transparent 70%);
    pointer-events: none;
    z-index: 0;
  }

  /* NAV */
  nav {
    position: fixed;
    top: 24px;
    left: 50%;
    transform: translateX(-50%);
    z-index: 100;
    display: flex;
    align-items: center;
    gap: 4px;
    padding: 6px 8px;
    background: rgba(8,10,15,0.7);
    backdrop-filter: blur(20px) saturate(180%);
    -webkit-backdrop-filter: blur(20px) saturate(180%);
    border: 1px solid var(--border);
    border-radius: 50px;
    box-shadow: 0 0 0 1px rgba(59,130,246,0.1), 0 8px 32px rgba(0,0,0,0.4);
  }

  nav a {
    font-family: var(--font-head);
    font-size: 13px;
    font-weight: 500;
    color: var(--text-secondary);
    text-decoration: none;
    padding: 8px 18px;
    border-radius: 50px;
    transition: all 0.25s ease;
    letter-spacing: 0.02em;
  }
  nav a:hover { color: var(--text-primary); background: var(--surface); }
  nav a.active {
    color: var(--white);
    background: rgba(59,130,246,0.15);
    border: 1px solid rgba(59,130,246,0.25);
    box-shadow: 0 0 16px rgba(59,130,246,0.15);
  }

  section { position: relative; z-index: 1; }

  /* HERO */
  #home {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 120px 24px 80px;
  }

  .hero-badge {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    font-family: var(--font-head);
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--blue-bright);
    background: rgba(59,130,246,0.1);
    border: 1px solid rgba(59,130,246,0.2);
    border-radius: 50px;
    padding: 8px 18px;
    margin-bottom: 32px;
    box-shadow: 0 0 20px rgba(59,130,246,0.1);
    animation: fadeUp 0.8s ease both;
  }

  .hero-badge::before {
    content: '';
    width: 6px; height: 6px;
    background: var(--blue);
    border-radius: 50%;
    box-shadow: 0 0 8px var(--blue);
    animation: pulse 2s infinite;
  }

  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.4; }
  }

  h1.hero-name {
    font-family: var(--font-head);
    font-size: clamp(56px, 10vw, 110px);
    font-weight: 700;
    line-height: 0.95;
    letter-spacing: -0.03em;
    margin-bottom: 24px;
    animation: fadeUp 0.8s 0.1s ease both;
  }

  h1.hero-name .line1 {
    display: block;
    color: var(--white);
    text-shadow:
      0 0 40px rgba(255,255,255,0.15),
      0 0 80px rgba(255,255,255,0.05);
  }

  h1.hero-name .line2 {
    display: block;
    color: transparent;
    background: linear-gradient(135deg, #60a5fa 0%, #93c5fd 40%, #3b82f6 100%);
    -webkit-background-clip: text;
    background-clip: text;
    filter: drop-shadow(0 0 30px rgba(59,130,246,0.5));
    animation: glowPulse 3s ease-in-out infinite;
  }

  @keyframes glowPulse {
    0%, 100% { filter: drop-shadow(0 0 30px rgba(59,130,246,0.5)); }
    50% { filter: drop-shadow(0 0 50px rgba(59,130,246,0.8)); }
  }

  .hero-desc {
    font-family: var(--font-body);
    font-size: clamp(16px, 2vw, 19px);
    color: var(--text-secondary);
    max-width: 540px;
    line-height: 1.7;
    margin: 0 auto 48px;
    animation: fadeUp 0.8s 0.2s ease both;
  }

  .hero-stats {
    display: flex;
    gap: 1px;
    background: var(--border);
    border: 1px solid var(--border);
    border-radius: 16px;
    overflow: hidden;
    margin-bottom: 48px;
    backdrop-filter: blur(12px);
    box-shadow: 0 0 40px rgba(59,130,246,0.05);
    animation: fadeUp 0.8s 0.3s ease both;
  }

  .stat {
    flex: 1;
    padding: 20px 32px;
    background: var(--surface);
    text-align: center;
    transition: background 0.3s;
  }
  .stat:hover { background: var(--surface-hover); }

  .stat-num {
    font-family: var(--font-head);
    font-size: 28px;
    font-weight: 700;
    color: var(--blue-bright);
    display: block;
    text-shadow: 0 0 20px rgba(96,165,250,0.6), 0 0 40px rgba(59,130,246,0.3);
    filter: brightness(1.1);
  }

  .stat-label {
    font-family: var(--font-head);
    font-size: 10px;
    font-weight: 600;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--text-secondary);
    margin-top: 4px;
    display: block;
  }

  .hero-btns {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
    justify-content: center;
    animation: fadeUp 0.8s 0.4s ease both;
  }

  .btn-primary {
    font-family: var(--font-head);
    font-size: 14px;
    font-weight: 600;
    color: var(--white);
    background: var(--blue);
    border: none;
    border-radius: 50px;
    padding: 14px 32px;
    cursor: pointer;
    text-decoration: none;
    display: inline-flex;
    align-items: center;
    gap: 8px;
    transition: all 0.3s ease;
    box-shadow: 0 0 30px rgba(59,130,246,0.4), 0 4px 20px rgba(59,130,246,0.3);
  }
  .btn-primary:hover {
    background: var(--blue-bright);
    box-shadow: 0 0 50px rgba(59,130,246,0.6), 0 4px 30px rgba(59,130,246,0.5);
    transform: translateY(-2px);
  }

  .btn-secondary {
    font-family: var(--font-head);
    font-size: 14px;
    font-weight: 600;
    color: var(--text-primary);
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 50px;
    padding: 14px 32px;
    cursor: pointer;
    text-decoration: none;
    display: inline-flex;
    align-items: center;
    gap: 8px;
    transition: all 0.3s ease;
    backdrop-filter: blur(12px);
  }
  .btn-secondary:hover {
    background: var(--surface-hover);
    border-color: rgba(59,130,246,0.4);
    box-shadow: 0 0 20px rgba(59,130,246,0.1);
    transform: translateY(-2px);
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* DIVIDER */
  .section-divider {
    display: flex;
    align-items: center;
    gap: 16px;
    margin-bottom: 64px;
  }
  .section-divider::before, .section-divider::after {
    content: '';
    flex: 1;
    height: 1px;
    background: linear-gradient(90deg, transparent, var(--border), transparent);
  }
  .section-label {
    font-family: var(--font-head);
    font-size: 11px;
    font-weight: 600;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--blue);
    padding: 6px 14px;
    border: 1px solid rgba(59,130,246,0.2);
    border-radius: 50px;
    background: rgba(59,130,246,0.07);
    box-shadow: 0 0 16px rgba(59,130,246,0.1);
  }

  /* SECTION WRAPPER */
  .section-wrap {
    max-width: 1100px;
    margin: 0 auto;
    padding: 100px 24px;
  }

  /* ABOUT */
  #about {
    background: linear-gradient(180deg, transparent 0%, rgba(59,130,246,0.03) 50%, transparent 100%);
  }

  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 64px;
    align-items: center;
  }

  .about-visual {
    position: relative;
  }

  /* ── UPDATED PROFILE IMAGE SECTION ── */
  .about-img-wrap {
    position: relative;
    border-radius: 16px;
    overflow: hidden;
    aspect-ratio: 16/9;
    border: 1px solid var(--border);
    box-shadow: 0 0 60px rgba(59,130,246,0.1), 0 0 0 1px rgba(59,130,246,0.05);
    background: #0e1118;
  }

  .about-img-wrap::before {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, rgba(59,130,246,0.1) 0%, transparent 60%);
    z-index: 1;
    pointer-events: none;
  }

  /* Use an iframe to embed the Drive file — most reliable cross-origin method */
  .about-img-wrap iframe {
    width: 100%;
    height: 100%;
    border: none;
    display: block;
  }

  /* Intro video below pfp */
  .intro-video-wrap {
    margin-top: 16px;
    border-radius: 12px;
    overflow: hidden;
    border: 1px solid var(--border);
    box-shadow: 0 0 30px rgba(59,130,246,0.08);
    aspect-ratio: 16/9;
    background: #0a0c12;
  }
  .intro-video-wrap iframe {
    width: 100%;
    height: 100%;
    border: none;
    display: block;
  }

  .about-text h2 {
    font-family: var(--font-head);
    font-size: clamp(32px, 4vw, 48px);
    font-weight: 700;
    line-height: 1.1;
    margin-bottom: 24px;
    letter-spacing: -0.02em;
  }

  .about-text h2 span {
    color: transparent;
    background: linear-gradient(135deg, #60a5fa, #3b82f6);
    -webkit-background-clip: text;
    background-clip: text;
    text-shadow: none;
    filter: drop-shadow(0 0 20px rgba(59,130,246,0.4));
  }

  .about-text p {
    font-family: var(--font-body);
    font-size: 17px;
    line-height: 1.75;
    color: var(--text-secondary);
    margin-bottom: 20px;
  }

  .skills-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: 32px;
  }

  .skill-tag {
    font-family: var(--font-head);
    font-size: 12px;
    font-weight: 500;
    color: var(--text-secondary);
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 6px 14px;
    transition: all 0.25s;
    backdrop-filter: blur(8px);
  }
  .skill-tag:hover {
    color: var(--blue-bright);
    border-color: rgba(59,130,246,0.3);
    background: rgba(59,130,246,0.07);
    box-shadow: 0 0 12px rgba(59,130,246,0.1);
  }

  /* WORK / PORTFOLIO */
  #work { }

  .work-tabs {
    display: flex;
    gap: 8px;
    margin-bottom: 48px;
    flex-wrap: wrap;
  }

  .tab-btn {
    font-family: var(--font-head);
    font-size: 13px;
    font-weight: 500;
    color: var(--text-secondary);
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    padding: 10px 20px;
    cursor: pointer;
    transition: all 0.25s;
    backdrop-filter: blur(8px);
  }
  .tab-btn:hover {
    color: var(--text-primary);
    border-color: rgba(59,130,246,0.3);
  }
  .tab-btn.active {
    color: var(--white);
    background: rgba(59,130,246,0.15);
    border-color: rgba(59,130,246,0.4);
    box-shadow: 0 0 20px rgba(59,130,246,0.1);
  }

  .video-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
    gap: 20px;
  }

  .video-card {
    position: relative;
    border-radius: 14px;
    overflow: hidden;
    background: var(--gray);
    border: 1px solid var(--border);
    transition: all 0.35s ease;
    cursor: pointer;
    box-shadow: 0 4px 24px rgba(0,0,0,0.3);
  }
  .video-card:hover {
    transform: translateY(-6px);
    border-color: rgba(59,130,246,0.4);
    box-shadow: 0 20px 60px rgba(0,0,0,0.4), 0 0 0 1px rgba(59,130,246,0.2), 0 0 40px rgba(59,130,246,0.08);
  }

  .video-thumb {
    position: relative;
    aspect-ratio: 16/9;
    background: #0e1118;
    overflow: hidden;
  }

  .video-thumb iframe {
    width: 100%;
    height: 100%;
    border: none;
    pointer-events: none;
  }

  .video-overlay {
    position: absolute;
    inset: 0;
    background: linear-gradient(to top, rgba(8,10,15,0.8) 0%, transparent 60%);
    display: flex;
    align-items: center;
    justify-content: center;
    opacity: 0;
    transition: opacity 0.3s;
  }

  .video-card:hover .video-overlay { opacity: 1; }

  .play-btn {
    width: 52px; height: 52px;
    background: rgba(59,130,246,0.9);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 0 30px rgba(59,130,246,0.5);
    transform: scale(0.8);
    transition: transform 0.3s;
  }
  .video-card:hover .play-btn { transform: scale(1); }

  .play-btn svg { fill: white; margin-left: 3px; }

  .video-info {
    padding: 16px 18px;
  }

  .video-cat {
    font-family: var(--font-head);
    font-size: 10px;
    font-weight: 600;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--blue);
    margin-bottom: 6px;
    display: block;
    text-shadow: 0 0 12px rgba(59,130,246,0.5);
  }

  .video-title {
    font-family: var(--font-head);
    font-size: 15px;
    font-weight: 600;
    color: var(--text-primary);
    line-height: 1.3;
  }

  /* Glass video modal */
  .modal-overlay {
    position: fixed;
    inset: 0;
    background: rgba(0,0,0,0.85);
    backdrop-filter: blur(16px);
    z-index: 1000;
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
    width: 90vw;
    max-width: 960px;
    background: rgba(10,12,20,0.9);
    border: 1px solid rgba(59,130,246,0.2);
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 0 100px rgba(59,130,246,0.15), 0 40px 80px rgba(0,0,0,0.6);
    transform: scale(0.95);
    transition: transform 0.3s;
  }
  .modal-overlay.open .modal-box { transform: scale(1); }

  .modal-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 16px 20px;
    border-bottom: 1px solid var(--border);
  }

  .modal-title {
    font-family: var(--font-head);
    font-size: 15px;
    font-weight: 600;
    color: var(--text-primary);
  }

  .modal-close {
    width: 32px; height: 32px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 8px;
    color: var(--text-secondary);
    font-size: 18px;
    cursor: pointer;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.2s;
    font-family: var(--font-head);
  }
  .modal-close:hover { color: white; background: var(--surface-hover); }

  .modal-video {
    aspect-ratio: 16/9;
    background: #000;
  }
  .modal-video iframe {
    width: 100%;
    height: 100%;
    border: none;
  }

  /* CONTACT */
  #contact {
    background: linear-gradient(180deg, transparent 0%, rgba(59,130,246,0.03) 50%, transparent 100%);
  }

  .contact-card {
    background: var(--surface);
    backdrop-filter: blur(20px);
    border: 1px solid var(--border);
    border-radius: 24px;
    padding: 60px;
    text-align: center;
    position: relative;
    overflow: hidden;
    box-shadow: 0 0 80px rgba(59,130,246,0.06), 0 0 0 1px rgba(59,130,246,0.05);
  }

  .contact-card::before {
    content: '';
    position: absolute;
    top: -1px; left: 20%; right: 20%;
    height: 1px;
    background: linear-gradient(90deg, transparent, rgba(59,130,246,0.5), transparent);
  }

  .contact-card h2 {
    font-family: var(--font-head);
    font-size: clamp(32px, 4vw, 52px);
    font-weight: 700;
    letter-spacing: -0.02em;
    margin-bottom: 16px;
  }

  .contact-card h2 span {
    color: transparent;
    background: linear-gradient(135deg, #60a5fa, #3b82f6);
    -webkit-background-clip: text;
    background-clip: text;
    filter: drop-shadow(0 0 20px rgba(59,130,246,0.5));
  }

  .contact-card p {
    font-family: var(--font-body);
    font-size: 18px;
    color: var(--text-secondary);
    margin-bottom: 48px;
    max-width: 500px;
    margin-left: auto;
    margin-right: auto;
  }

  .contact-links {
    display: flex;
    gap: 12px;
    justify-content: center;
    flex-wrap: wrap;
    margin-bottom: 48px;
  }

  .contact-link {
    font-family: var(--font-head);
    font-size: 13px;
    font-weight: 500;
    color: var(--text-secondary);
    text-decoration: none;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 12px 20px;
    display: flex;
    align-items: center;
    gap: 10px;
    transition: all 0.25s;
    backdrop-filter: blur(8px);
  }
  .contact-link:hover {
    color: var(--blue-bright);
    border-color: rgba(59,130,246,0.35);
    background: rgba(59,130,246,0.07);
    transform: translateY(-3px);
    box-shadow: 0 8px 24px rgba(59,130,246,0.1);
  }

  /* FOOTER */
  footer {
    position: relative;
    z-index: 1;
    border-top: 1px solid var(--border);
    padding: 32px 24px;
    text-align: center;
  }

  footer p {
    font-family: var(--font-head);
    font-size: 12px;
    color: var(--text-secondary);
    letter-spacing: 0.05em;
  }

  footer span {
    color: var(--blue);
    text-shadow: 0 0 8px rgba(59,130,246,0.4);
  }

  /* SCROLL FADE IN */
  .reveal {
    opacity: 0;
    transform: translateY(32px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .reveal.visible {
    opacity: 1;
    transform: translateY(0);
  }

  /* Responsive */
  @media (max-width: 768px) {
    .about-grid { grid-template-columns: 1fr; gap: 40px; }
    .hero-stats { flex-direction: column; gap: 0; }
    .contact-card { padding: 36px 24px; }
    .video-grid { grid-template-columns: 1fr; }
    h1.hero-name { font-size: 54px; }
  }

  /* Glass card accent */
  .glass-accent {
    position: relative;
    background: var(--surface);
    backdrop-filter: blur(12px);
    border: 1px solid var(--border);
    border-radius: 14px;
    overflow: hidden;
  }
  .glass-accent::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 1px;
    background: linear-gradient(90deg, transparent, rgba(255,255,255,0.08), transparent);
  }

  /* Section title */
  .section-title {
    font-family: var(--font-head);
    font-size: clamp(36px, 5vw, 60px);
    font-weight: 700;
    letter-spacing: -0.025em;
    line-height: 1.05;
    margin-bottom: 16px;
  }
  .section-title span {
    color: transparent;
    background: linear-gradient(135deg, #60a5fa, #3b82f6);
    -webkit-background-clip: text;
    background-clip: text;
    filter: drop-shadow(0 0 20px rgba(59,130,246,0.4));
  }

  .section-sub {
    font-family: var(--font-body);
    font-size: 17px;
    color: var(--text-secondary);
    margin-bottom: 56px;
    max-width: 500px;
  }

  /* Tab hidden/visible */
  .tab-content { display: none; }
  .tab-content.active { display: grid; }

  /* Video card clickable */
  .video-card-link {
    display: block;
    text-decoration: none;
    color: inherit;
  }
</style>
</head>
<body>

<div class="cursor" id="cursor"></div>
<div class="cursor-ring" id="cursorRing"></div>

<!-- NAV -->
<nav>
  <a href="#home" class="active">Home</a>
  <a href="#about">About</a>
  <a href="#work">Work</a>
  <a href="#contact">Contact</a>
</nav>

<!-- HERO -->
<section id="home">
  <div class="hero-badge">Premium Video Editor</div>
  <h1 class="hero-name">
    <span class="line1">Arghya</span>
    <span class="line2">Samanta</span>
  </h1>
  <p class="hero-desc">
    High-end video editor with 4 years of hands-on agency experience — specializing in dynamic, high-retention content from cinematic real estate to viral medical reels.
  </p>
  <div class="hero-stats">
    <div class="stat">
      <span class="stat-num">30+</span>
      <span class="stat-label">Clients</span>
    </div>
    <div class="stat">
      <span class="stat-num">81.5K</span>
      <span class="stat-label">Subscribers</span>
    </div>
    <div class="stat">
      <span class="stat-num">58.5M+</span>
      <span class="stat-label">Views</span>
    </div>
  </div>
  <div class="hero-btns">
    <a href="#work" class="btn-primary">
      <svg width="14" height="14" viewBox="0 0 24 24" fill="white"><polygon points="5,3 19,12 5,21"/></svg>
      View Work
    </a>
    <a href="#contact" class="btn-secondary">Get in Touch</a>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="section-wrap">
    <div class="section-divider reveal">
      <span class="section-label">About</span>
    </div>
    <div class="about-grid">
      <div class="about-visual reveal">

        <!-- ── PROFILE IMAGE: embedded via Google Drive iframe preview ── -->
        <div class="about-img-wrap">
          <iframe
            src="https://drive.google.com/file/d/1hTg2OXfRVEecAwfc-qntyRnXT5HIZ3m7/preview"
            allow="autoplay"
            title="Arghya Samanta">
          </iframe>
        </div>

        <!-- Intro video below photo -->
        <div class="intro-video-wrap">
          <iframe 
            src="https://drive.google.com/file/d/12lZlO3zvHG5wTu0uUrsm9qH6eCMKPZpV/preview"
            allow="autoplay"
            title="Intro Video">
          </iframe>
        </div>
      </div>
      <div class="about-text reveal">
        <h2>Crafting Stories<br><span>Frame by Frame</span></h2>
        <p>
          I'm a video editor with 4 years of hands-on agency experience, specializing in dynamic, high-retention content creation. My work spans cinematic real estate, medical education, viral social content, and long-form podcasts.
        </p>
        <p>
          I blend technical precision with creative pacing — bringing together motion graphics, color science, and storytelling instincts to produce content that doesn't just look good, but performs.
        </p>
        <div class="skills-grid">
          <span class="skill-tag">Adobe Premiere Pro</span>
          <span class="skill-tag">Adobe Photoshop</span>
          <span class="skill-tag">CapCut PC</span>
          <span class="skill-tag">Topaz AI</span>
          <span class="skill-tag">After Motion</span>
          <span class="skill-tag">Alight Motion</span>
          <span class="skill-tag">Color Grading</span>
          <span class="skill-tag">Motion Graphics</span>
          <span class="skill-tag">Podcast Production</span>
          <span class="skill-tag">Short-Form Reels</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- WORK -->
<section id="work">
  <div class="section-wrap">
    <div class="section-divider reveal">
      <span class="section-label">Portfolio</span>
    </div>
    <div class="reveal">
      <h2 class="section-title">Selected <span>Work</span></h2>
      <p class="section-sub">A curated collection of edits across medical, real estate, social, and podcast formats.</p>
    </div>

    <div class="work-tabs reveal">
      <button class="tab-btn active" onclick="switchTab('all', this)">All</button>
      <button class="tab-btn" onclick="switchTab('medical', this)">Medical</button>
      <button class="tab-btn" onclick="switchTab('realestate', this)">Real Estate</button>
      <button class="tab-btn" onclick="switchTab('podcast', this)">Podcast</button>
      <button class="tab-btn" onclick="switchTab('other', this)">Other</button>
    </div>

    <!-- ALL -->
    <div id="tab-all" class="tab-content video-grid active">
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/12ptrR7XBpbgoMoTmfMQH67693zIvHGcB/preview','Medical Edit 01')">
        <div class="video-thumb">
          <iframe src="https://drive.google.com/file/d/12ptrR7XBpbgoMoTmfMQH67693zIvHGcB/preview" title="Medical 01"></iframe>
          <div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div>
        </div>
        <div class="video-info"><span class="video-cat">Medical</span><div class="video-title">Medical Edit 01</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1Df-ISzAKITq5itUM8OnUR5-eacIj6kPg/preview','Medical Edit 02')">
        <div class="video-thumb">
          <iframe src="https://drive.google.com/file/d/1Df-ISzAKITq5itUM8OnUR5-eacIj6kPg/preview" title="Medical 02"></iframe>
          <div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div>
        </div>
        <div class="video-info"><span class="video-cat">Medical</span><div class="video-title">Medical Edit 02</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1Fh1mjjHSyDKMT3yKUdIzjnXV3s1ykqQa/preview','Medical Edit 03')">
        <div class="video-thumb">
          <iframe src="https://drive.google.com/file/d/1Fh1mjjHSyDKMT3yKUdIzjnXV3s1ykqQa/preview" title="Medical 03"></iframe>
          <div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div>
        </div>
        <div class="video-info"><span class="video-cat">Medical</span><div class="video-title">Medical Edit 03</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1r1DB0ENEdR6SForQ_zN8hWQLRevdaALz/preview','Medical Edit 04')">
        <div class="video-thumb">
          <iframe src="https://drive.google.com/file/d/1r1DB0ENEdR6SForQ_zN8hWQLRevdaALz/preview" title="Medical 04"></iframe>
          <div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div>
        </div>
        <div class="video-info"><span class="video-cat">Medical</span><div class="video-title">Medical Edit 04</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1J3a7sXH9Mp3inen2q6BmfouVw1gALdHd/preview','Real Estate Edit 01')">
        <div class="video-thumb">
          <iframe src="https://drive.google.com/file/d/1J3a7sXH9Mp3inen2q6BmfouVw1gALdHd/preview" title="Real Estate 01"></iframe>
          <div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div>
        </div>
        <div class="video-info"><span class="video-cat">Real Estate</span><div class="video-title">Real Estate Edit 01</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1YWQk4aYFgErMnVKe6QhYh74AEPXTfpEo/preview','Real Estate Edit 02')">
        <div class="video-thumb">
          <iframe src="https://drive.google.com/file/d/1YWQk4aYFgErMnVKe6QhYh74AEPXTfpEo/preview" title="Real Estate 02"></iframe>
          <div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div>
        </div>
        <div class="video-info"><span class="video-cat">Real Estate</span><div class="video-title">Real Estate Edit 02</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1BTVzmjPaMjegu0xYx9YUB5wpcUoCgFYX/preview','Real Estate Edit 03')">
        <div class="video-thumb">
          <iframe src="https://drive.google.com/file/d/1BTVzmjPaMjegu0xYx9YUB5wpcUoCgFYX/preview" title="Real Estate 03"></iframe>
          <div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div>
        </div>
        <div class="video-info"><span class="video-cat">Real Estate</span><div class="video-title">Real Estate Edit 03</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1XfwntyIalFjDB-9f6VRitjPIn6zOPkfZ/preview','Podcast Reel Edit')">
        <div class="video-thumb">
          <iframe src="https://drive.google.com/file/d/1XfwntyIalFjDB-9f6VRitjPIn6zOPkfZ/preview" title="Podcast"></iframe>
          <div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div>
        </div>
        <div class="video-info"><span class="video-cat">Podcast</span><div class="video-title">Podcast Reel Edit</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1W6h-oND23LMk7i1mx2LyCRSUYnv4j5ke/preview','Edit 01')">
        <div class="video-thumb">
          <iframe src="https://drive.google.com/file/d/1W6h-oND23LMk7i1mx2LyCRSUYnv4j5ke/preview" title="Other 01"></iframe>
          <div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div>
        </div>
        <div class="video-info"><span class="video-cat">Other</span><div class="video-title">Edit 01</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1EGmHAPFnQ57dXzP04mfwo2WNWvIHtcL0/preview','Edit 02')">
        <div class="video-thumb">
          <iframe src="https://drive.google.com/file/d/1EGmHAPFnQ57dXzP04mfwo2WNWvIHtcL0/preview" title="Other 02"></iframe>
          <div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div>
        </div>
        <div class="video-info"><span class="video-cat">Other</span><div class="video-title">Edit 02</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1Ng5_1mZxCAdrFmiH39N0hPeABTaiBo71/preview','Edit 03')">
        <div class="video-thumb">
          <iframe src="https://drive.google.com/file/d/1Ng5_1mZxCAdrFmiH39N0hPeABTaiBo71/preview" title="Other 03"></iframe>
          <div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div>
        </div>
        <div class="video-info"><span class="video-cat">Other</span><div class="video-title">Edit 03</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1KC2LRwLPBvCKhSHUfGBomb3-rsa6bSGn/preview','Edit 04')">
        <div class="video-thumb">
          <iframe src="https://drive.google.com/file/d/1KC2LRwLPBvCKhSHUfGBomb3-rsa6bSGn/preview" title="Other 04"></iframe>
          <div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div>
        </div>
        <div class="video-info"><span class="video-cat">Other</span><div class="video-title">Edit 04</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1bg88H4LIaVU94Ob0zNxEvSCIahPaVpVb/preview','Edit 05')">
        <div class="video-thumb">
          <iframe src="https://drive.google.com/file/d/1bg88H4LIaVU94Ob0zNxEvSCIahPaVpVb/preview" title="Other 05"></iframe>
          <div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div>
        </div>
        <div class="video-info"><span class="video-cat">Other</span><div class="video-title">Edit 05</div></div>
      </div>
    </div>

    <!-- MEDICAL -->
    <div id="tab-medical" class="tab-content video-grid">
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/12ptrR7XBpbgoMoTmfMQH67693zIvHGcB/preview','Medical Edit 01')">
        <div class="video-thumb"><iframe src="https://drive.google.com/file/d/12ptrR7XBpbgoMoTmfMQH67693zIvHGcB/preview" title="M1"></iframe><div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div></div>
        <div class="video-info"><span class="video-cat">Medical</span><div class="video-title">Medical Edit 01</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1Df-ISzAKITq5itUM8OnUR5-eacIj6kPg/preview','Medical Edit 02')">
        <div class="video-thumb"><iframe src="https://drive.google.com/file/d/1Df-ISzAKITq5itUM8OnUR5-eacIj6kPg/preview" title="M2"></iframe><div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div></div>
        <div class="video-info"><span class="video-cat">Medical</span><div class="video-title">Medical Edit 02</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1Fh1mjjHSyDKMT3yKUdIzjnXV3s1ykqQa/preview','Medical Edit 03')">
        <div class="video-thumb"><iframe src="https://drive.google.com/file/d/1Fh1mjjHSyDKMT3yKUdIzjnXV3s1ykqQa/preview" title="M3"></iframe><div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div></div>
        <div class="video-info"><span class="video-cat">Medical</span><div class="video-title">Medical Edit 03</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1r1DB0ENEdR6SForQ_zN8hWQLRevdaALz/preview','Medical Edit 04')">
        <div class="video-thumb"><iframe src="https://drive.google.com/file/d/1r1DB0ENEdR6SForQ_zN8hWQLRevdaALz/preview" title="M4"></iframe><div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div></div>
        <div class="video-info"><span class="video-cat">Medical</span><div class="video-title">Medical Edit 04</div></div>
      </div>
    </div>

    <!-- REAL ESTATE -->
    <div id="tab-realestate" class="tab-content video-grid">
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1J3a7sXH9Mp3inen2q6BmfouVw1gALdHd/preview','Real Estate Edit 01')">
        <div class="video-thumb"><iframe src="https://drive.google.com/file/d/1J3a7sXH9Mp3inen2q6BmfouVw1gALdHd/preview" title="RE1"></iframe><div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div></div>
        <div class="video-info"><span class="video-cat">Real Estate</span><div class="video-title">Real Estate Edit 01</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1YWQk4aYFgErMnVKe6QhYh74AEPXTfpEo/preview','Real Estate Edit 02')">
        <div class="video-thumb"><iframe src="https://drive.google.com/file/d/1YWQk4aYFgErMnVKe6QhYh74AEPXTfpEo/preview" title="RE2"></iframe><div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div></div>
        <div class="video-info"><span class="video-cat">Real Estate</span><div class="video-title">Real Estate Edit 02</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1BTVzmjPaMjegu0xYx9YUB5wpcUoCgFYX/preview','Real Estate Edit 03')">
        <div class="video-thumb"><iframe src="https://drive.google.com/file/d/1BTVzmjPaMjegu0xYx9YUB5wpcUoCgFYX/preview" title="RE3"></iframe><div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div></div>
        <div class="video-info"><span class="video-cat">Real Estate</span><div class="video-title">Real Estate Edit 03</div></div>
      </div>
    </div>

    <!-- PODCAST -->
    <div id="tab-podcast" class="tab-content video-grid">
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1XfwntyIalFjDB-9f6VRitjPIn6zOPkfZ/preview','Podcast Reel Edit')">
        <div class="video-thumb"><iframe src="https://drive.google.com/file/d/1XfwntyIalFjDB-9f6VRitjPIn6zOPkfZ/preview" title="Podcast"></iframe><div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div></div>
        <div class="video-info"><span class="video-cat">Podcast</span><div class="video-title">Podcast Reel Edit</div></div>
      </div>
    </div>

    <!-- OTHER -->
    <div id="tab-other" class="tab-content video-grid">
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1W6h-oND23LMk7i1mx2LyCRSUYnv4j5ke/preview','Edit 01')">
        <div class="video-thumb"><iframe src="https://drive.google.com/file/d/1W6h-oND23LMk7i1mx2LyCRSUYnv4j5ke/preview" title="O1"></iframe><div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div></div>
        <div class="video-info"><span class="video-cat">Other</span><div class="video-title">Edit 01</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1EGmHAPFnQ57dXzP04mfwo2WNWvIHtcL0/preview','Edit 02')">
        <div class="video-thumb"><iframe src="https://drive.google.com/file/d/1EGmHAPFnQ57dXzP04mfwo2WNWvIHtcL0/preview" title="O2"></iframe><div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div></div>
        <div class="video-info"><span class="video-cat">Other</span><div class="video-title">Edit 02</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1Ng5_1mZxCAdrFmiH39N0hPeABTaiBo71/preview','Edit 03')">
        <div class="video-thumb"><iframe src="https://drive.google.com/file/d/1Ng5_1mZxCAdrFmiH39N0hPeABTaiBo71/preview" title="O3"></iframe><div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div></div>
        <div class="video-info"><span class="video-cat">Other</span><div class="video-title">Edit 03</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1KC2LRwLPBvCKhSHUfGBomb3-rsa6bSGn/preview','Edit 04')">
        <div class="video-thumb"><iframe src="https://drive.google.com/file/d/1KC2LRwLPBvCKhSHUfGBomb3-rsa6bSGn/preview" title="O4"></iframe><div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div></div>
        <div class="video-info"><span class="video-cat">Other</span><div class="video-title">Edit 04</div></div>
      </div>
      <div class="video-card" onclick="openModal('https://drive.google.com/file/d/1bg88H4LIaVU94Ob0zNxEvSCIahPaVpVb/preview','Edit 05')">
        <div class="video-thumb"><iframe src="https://drive.google.com/file/d/1bg88H4LIaVU94Ob0zNxEvSCIahPaVpVb/preview" title="O5"></iframe><div class="video-overlay"><div class="play-btn"><svg width="18" height="18" viewBox="0 0 24 24"><polygon points="5,3 19,12 5,21"/></svg></div></div></div>
        <div class="video-info"><span class="video-cat">Other</span><div class="video-title">Edit 05</div></div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="section-wrap">
    <div class="section-divider reveal">
      <span class="section-label">Contact</span>
    </div>
    <div class="contact-card reveal">
      <h2>Let's Create<br><span>Something Great</span></h2>
      <p>Available for long-term collaborations, project-based work, and brand partnerships.</p>
      <div class="contact-links">
        <a href="mailto:apsediting120@gmail.com" class="contact-link">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="m22 7-8.97 5.7a1.94 1.94 0 0 1-2.06 0L2 7"/></svg>
          apsediting120@gmail.com
        </a>
        <a href="tel:+917318805018" class="contact-link">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07A19.5 19.5 0 0 1 4.69 12a19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 3.6 1.27h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/></svg>
          +91 73188 05018
        </a>
        <a href="https://framefolio.in/apsvisuallab" target="_blank" class="contact-link">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><path d="M12 2a14.5 14.5 0 0 0 0 20 14.5 14.5 0 0 0 0-20"/><path d="M2 12h20"/></svg>
          Portfolio
        </a>
        <a href="https://youtube.com/@aps_editor_1m" target="_blank" class="contact-link">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M22.54 6.42A2.78 2.78 0 0 0 20.6 4.46C18.88 4 12 4 12 4s-6.88 0-8.6.46A2.78 2.78 0 0 0 1.46 6.42 29 29 0 0 0 1 12a29 29 0 0 0 .46 5.58A2.78 2.78 0 0 0 3.4 19.54C5.12 20 12 20 12 20s6.88 0 8.6-.46a2.78 2.78 0 0 0 1.94-1.96A29 29 0 0 0 23 12a29 29 0 0 0-.46-5.58z"/><polygon points="9.75 15.02 15.5 12 9.75 8.98 9.75 15.02" fill="var(--bg)"/></svg>
          YouTube
        </a>
        <a href="https://linkedin.com/in/aps-editor-37212640a" target="_blank" class="contact-link">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
          LinkedIn
        </a>
      </div>
      <a href="mailto:apsediting120@gmail.com" class="btn-primary" style="display:inline-flex; margin: 0 auto;">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="white" stroke-width="2"><path d="m22 2-7 20-4-9-9-4z"/><path d="M22 2 11 13"/></svg>
        Send Message
      </a>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p>© 2026 <span>Arghya Samanta</span> · Video Editor · India</p>
</footer>

<!-- VIDEO MODAL -->
<div class="modal-overlay" id="videoModal" onclick="closeModal(event)">
  <div class="modal-box">
    <div class="modal-header">
      <span class="modal-title" id="modalTitle">Video</span>
      <button class="modal-close" onclick="closeModal()">✕</button>
    </div>
    <div class="modal-video">
      <iframe id="modalIframe" src="" allow="autoplay; fullscreen" title="Video Preview"></iframe>
    </div>
  </div>
</div>

<script>
  // Custom cursor
  const cursor = document.getElementById('cursor');
  const ring = document.getElementById('cursorRing');
  let mouseX = 0, mouseY = 0, ringX = 0, ringY = 0;

  document.addEventListener('mousemove', e => {
    mouseX = e.clientX; mouseY = e.clientY;
    cursor.style.left = mouseX + 'px';
    cursor.style.top = mouseY + 'px';
  });

  function animateRing() {
    ringX += (mouseX - ringX) * 0.15;
    ringY += (mouseY - ringY) * 0.15;
    ring.style.left = ringX + 'px';
    ring.style.top = ringY + 'px';
    requestAnimationFrame(animateRing);
  }
  animateRing();

  document.querySelectorAll('a, button, .video-card').forEach(el => {
    el.addEventListener('mouseenter', () => {
      cursor.style.width = '14px';
      cursor.style.height = '14px';
      ring.style.width = '48px';
      ring.style.height = '48px';
    });
    el.addEventListener('mouseleave', () => {
      cursor.style.width = '8px';
      cursor.style.height = '8px';
      ring.style.width = '32px';
      ring.style.height = '32px';
    });
  });

  // Nav active state
  const sections = document.querySelectorAll('section');
  const navLinks = document.querySelectorAll('nav a');

  window.addEventListener('scroll', () => {
    let current = '';
    sections.forEach(s => {
      if (window.scrollY >= s.offsetTop - 120) current = s.id;
    });
    navLinks.forEach(a => {
      a.classList.toggle('active', a.getAttribute('href') === '#' + current);
    });
  });

  // Reveal on scroll
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver(entries => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
        observer.unobserve(e.target);
      }
    });
  }, { threshold: 0.1 });
  reveals.forEach(r => observer.observe(r));

  // Tab switching
  function switchTab(tab, btn) {
    document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
    document.querySelectorAll('.tab-content').forEach(c => c.classList.remove('active'));
    btn.classList.add('active');
    document.getElementById('tab-' + tab).classList.add('active');
  }

  // Modal
  function openModal(src, title) {
    document.getElementById('modalIframe').src = src;
    document.getElementById('modalTitle').textContent = title;
    document.getElementById('videoModal').classList.add('open');
    document.body.style.overflow = 'hidden';
  }

  function closeModal(e) {
    if (!e || e.target === document.getElementById('videoModal') || e.target.classList.contains('modal-close')) {
      document.getElementById('videoModal').classList.remove('open');
      document.getElementById('modalIframe').src = '';
      document.body.style.overflow = '';
    }
  }

  document.addEventListener('keydown', e => {
    if (e.key === 'Escape') closeModal({ target: document.getElementById('videoModal') });
  });
</script>
</body>
</html>