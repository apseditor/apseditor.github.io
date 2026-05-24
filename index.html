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
    aspect-ratio: 16 / 9;
    height: auto;
    object-fit: cover;
    object-position: center top;
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
        <p>High-end video editor with 4 years of hands-on agency experience. Specializing in dynamic, high-retention content — from cinematic real estate to viral medical reels.</p>

        <div class="stats-row">
          <div class="stat">
            <span class="stat-num">30+</span>
            <span class="stat-label">Clients</span>
          </div>
          <div class="stat-divider"></div>
          <div class="stat">
            <span class="stat-num">81.5K</span>
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
            <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAABogAAAOtCAIAAAA95HBeAABhWmNhQlgAAGFaanVtYgAAAB5qdW1kYzJwYQARABCAAACqADibcQNjMnBhAAAAYTRqdW1iAAAAR2p1bWRjMm1hABEAEIAAAKoAOJtxA3VybjpjMnBhOmE4OWUyMmMxLTFmNWEtNDJhMS1hZTBhLTg5ZWVlMTFlZjk2YgAAABf9anVtYgAAAClqdW1kYzJhcwARABCAAACqADibcQNjMnBhLmFzc2VydGlvbnMAAAAJ0Wp1bWIAAAA7anVtZEDLDDK7ikidpwsq1vR/Q2kTYzJwYS5pY29uAAAAABhjMnNo8Flb3NB5zi4Cuo4XBQgNFgAAABdiZmRiAGltYWdlL3N2Zyt4bWwAAAAJd2JpZGI8c3ZnIHdpZHRoPSI3MTYiIGhlaWdodD0iNzE2IiB2aWV3Qm94PSIwIDAgNzE2IDcxNiIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggZD0iTTUwOC43NDkgMzE3LjM5OUM1MTYuNzc3IDI4Ny4zMTQgNTA4Ljk5MSAyNTMuODg0IDQ4NS4zODkgMjMwLjI4MkM0NjEuNzg4IDIwNi42ODEgNDI4LjM2IDE5OC44OTUgMzk4LjI3MyAyMDYuOTIzQzM3Ni4yMzEgMTg0LjkyOCAzNDMuMzkgMTc0Ljk1NiAzMTEuMTQ4IDE4My41OTZDMjc4LjkwNiAxOTIuMjM0IDI1NS40NSAyMTcuMjkyIDI0Ny4zNiAyNDcuMzYxQzIxNy4yOTEgMjU1LjQ1MSAxOTIuMjMzIDI3OC45MSAxODMuNTk1IDMxMS4xNDlDMTc0Ljk1NyAzNDMuMzkxIDE4NC45MjcgMzc2LjIzMiAyMDYuOTI0IDM5OC4yNzRDMTk4Ljg5NiA0MjguMzU5IDIwNi42ODMgNDYxLjc4OSAyMzAuMjg0IDQ4NS4zOTFDMjUzLjg4NSA1MDguOTkyIDI4Ny4zMTMgNTE2Ljc3OSAzMTcuNDAxIDUwOC43NUMzMzkuNDQyIDUzMC43NDUgMzcyLjI4NiA1NDAuNzE3IDQwNC41MjUgNTMyLjA3OUM0MzYuNzY3IDUyMy40NDEgNDYwLjIyMyA0OTguMzg0IDQ2OC4zMTMgNDY4LjMxNUM0OTguMzgzIDQ2MC4yMjQgNTIzLjQ0IDQzNi43NjYgNTMyLjA3OCA0MDQuNTI2QzU0MC43MTYgMzcyLjI4NSA1MzAuNzQ3IDMzOS40NDMgNTA4Ljc0OSAzMTcuNDAyVjMxNy4zOTlaTTQ3MC44OTkgMjQ0Ljc3NkM0ODYuODkyIDI2MC43NyA0OTMuNDg4IDI4Mi42MDEgNDkwLjY4NyAzMDMuNDEyTDQxNS41NzcgMjYwLjA0NkM0MTIuNDExIDI1OC4yMTggNDA4LjUwOSAyNTguMjE4IDQwNS4zNDUgMjYwLjA0NkwzMTcuNDAxIDMxMC44MlYyNzcuNTI2QzMxNy40MDEgMjc1LjE5MSAzMTguNjUyIDI3My4wMDUgMzIwLjY3NiAyNzEuODM3TDM4Ny42NDQgMjMzLjE3NEM0MTQuMTc4IDIxOC4zNTMgNDQ4LjM0NiAyMjIuMjIzIDQ3MC45MDEgMjQ0Ljc3Nkg0NzAuODk5Wk0zNTcuODM3IDMxMS4xNDRMMzk4LjI3NSAzMzQuNDkxVjM4MS4xODVMMzU3LjgzNyA0MDQuNTMyTDMxNy4zOTggMzgxLjE4NVYzMzQuNDkxTDM1Ny44MzcgMzExLjE0NFpNMjY0Ljc3NiAyNjkuNjkzQzI2NS4yMDcgMjM5LjMwNSAyODUuNjQ0IDIxMS42NDkgMzE2LjQ1MyAyMDMuMzkzQzMzOC4zIDE5Ny41NCAzNjAuNTA1IDIwMi43NDQgMzc3LjEyNyAyMTUuNTczTDMwMi4wMTQgMjU4LjkzN0MyOTguODQ4IDI2MC43NjQgMjk2Ljg5OCAyNjQuMTQ0IDI5Ni44OTggMjY3Ljc5OFYzNjkuMzQ2TDI2OC4wNjUgMzUyLjY5OUMyNjYuMDQzIDM1MS41MzEgMjY0Ljc3NiAzNDkuMzUzIDI2NC43NzYgMzQ3LjAxN1YyNjkuNjkxVjI2OS42OTNaTTIwMy4zOTEgMzE2LjQ1NEMyMDkuMjQ0IDI5NC42MDggMjI0Ljg1NCAyNzcuOTc4IDI0NC4yNzYgMjY5Ljk5OVYzNTYuNzNDMjQ0LjI3NiAzNjAuMzg0IDI0Ni4yMjYgMzYzLjc2MyAyNDkuMzkyIDM2NS41OTFMMzM3LjMzNyA0MTYuMzY1TDMwOC41MDMgNDMzLjAxM0MzMDYuNDgxIDQzNC4xODEgMzAzLjk2MSA0MzQuMTg4IDMwMS45MzkgNDMzLjAyTDIzNC45NzEgMzk0LjM1N0MyMDguODY4IDM3OC43ODkgMTk1LjEzOCAzNDcuMjYxIDIwMy4zOTEgMzE2LjQ1NFpNMjQ0Ljc3NSA0NzAuOUMyMjguNzgxIDQ1NC45MDYgMjIyLjE4NiA0MzMuMDc1IDIyNC45ODYgNDEyLjI2NEwzMDAuMDk2IDQ1NS42M0MzMDMuMjYzIDQ1Ny40NTcgMzA3LjE2NCA0NTcuNDU3IDMxMC4zMjggNDU1LjYzTDM5OC4yNzMgNDA0Ljg1NlY0MzguMTQ5QzM5OC4yNzMgNDQwLjQ4NSAzOTcuMDIyIDQ0Mi42NzEgMzk0Ljk5NyA0NDMuODM5TDMyOC4wMjkgNDgyLjUwMkMzMDEuNDk1IDQ5Ny4zMjIgMjY3LjMyNyA0OTMuNDUyIDI0NC43NzIgNDcwLjlIMjQ0Ljc3NVpNNDUwLjg5NyA0NDUuOTgyQzQ1MC40NjYgNDc2LjM3MSA0MzAuMDI5IDUwNC4wMjcgMzk5LjIyIDUxMi4yODNDMzc3LjM3MyA1MTguMTM2IDM1NS4xNjggNTEyLjkzMiAzMzguNTQ3IDUwMC4xMDJMNDEzLjY1OSA0NTYuNzM4QzQxNi44MjYgNDU0LjkxMSA0MTguNzc1IDQ1MS41MzIgNDE4Ljc3NSA0NDcuODc3VjM0Ni4zMjlMNDQ3LjYwOSAzNjIuOTc3QzQ0OS42MzEgMzY0LjE0NSA0NTAuODk3IDM2Ni4zMjMgNDUwLjg5NyAzNjguNjU5VjQ0NS45ODVWNDQ1Ljk4MlpNNTEyLjI4MiAzOTkuMjIxQzUwNi40MjkgNDIxLjA2OCA0OTAuODE5IDQzNy42OTcgNDcxLjM5NyA0NDUuNjc2VjM1OC45NDZDNDcxLjM5NyAzNTUuMjkyIDQ2OS40NDggMzUxLjkxMiA0NjYuMjgxIDM1MC4wODVMMzc4LjMzNiAyOTkuMzExTDQwNy4xNyAyODIuNjYzQzQwOS4xOTIgMjgxLjQ5NSA0MTEuNzEyIDI4MS40ODcgNDEzLjczNCAyODIuNjU1TDQ4MC43MDIgMzIxLjMxOEM1MDYuODA1IDMzNi44ODcgNTIwLjUzNiAzNjguNDE1IDUxMi4yODIgMzk5LjIyMVoiIGZpbGw9ImJsYWNrIi8+Cjwvc3ZnPgoAAAF+anVtYgAAAEFqdW1kY2JvcgARABCAAACqADibcRNjMnBhLmFjdGlvbnMudjIAAAAAGGMyc2jyyAOMi9KBQFwtodZSyQFlAAABNWNib3KhZ2FjdGlvbnODpGZhY3Rpb25sYzJwYS5jcmVhdGVkZHdoZW7AdDIwMjYtMDUtMjNUMDA6MDA6MDBabXNvZnR3YXJlQWdlbnSiZG5hbWVpZ3B0LWltYWdlZ3ZlcnNpb25jMi4wcWRpZ2l0YWxTb3VyY2VUeXBleEZodHRwOi8vY3YuaXB0Yy5vcmcvbmV3c2NvZGVzL2RpZ2l0YWxzb3VyY2V0eXBlL3RyYWluZWRBbGdvcml0aG1pY01lZGlhomZhY3Rpb25uYzJwYS5jb252ZXJ0ZWRkd2hlbsB0MjAyNi0wNS0yM1QwMDowMDowMFqiZmFjdGlvbngYYzJwYS53YXRlcm1hcmtlZC51bmJvdW5kZHdoZW7AdDIwMjYtMDUtMjNUMDA6MDA6MDBaAAALump1bWIAAABJanVtZGNib3IAEQAQgAAAqgA4m3ETYzJwYS5jZXJ0aWZpY2F0ZS1zdGF0dXMAAAAAGGMyc2hBU1O7e/tHgFz/0a0DSMECAAALaWNib3KhaG9jc3BWYWxzgnkFhE1JSUVIZ29CQUtDQ0JCY3dnZ1FUQmdrckJnRUZCUWN3QVFFRWdnUUVNSUlFQURDQm9xSVdCQlJRV1FYMVg1UW0xMXJOcTI0Skt5MW1FUlQwK2hnUE1qQXlOakExTWpJeU1qQXdNelphTUhjd2RUQk5NQWtHQlNzT0F3SWFCUUFFRkQ1TWZJNVFDNGRzY3hXK3IyNlg2aER1bENESkJCVERzeVNXTkpPaFdlcFNHR3VlRitDcHV0YXdUQUlVVXBRbEI0RzFhb2I1TXhkNGNOYU9yZTlpR2tHQUFCZ1BNakF5TmpBMU1qSXlNakF3TXpaYW9CRVlEekl3TWpZd05USTVNakl3TURNMldqQUtCZ2dxaGtqT1BRUURBZ05JQURCRkFpRUFqOGhBTjF5TitpQk9ObjdUUWxVcnNTeUpZb0tDbmozdm1wLzAxS3FwbmRRQ0lIc0tYMFB6SEFzbU42bGsvVkZ2c3M1V1J5ay9ZZm5OeTFQdGZwam9oWW5Pb0lJREFUQ0NBdjB3Z2dMNU1JSUNmcUFEQWdFQ0FoUnVSWk42NnQ0MmNSbnVmTmF6eUpDRFE2UHMyakFLQmdncWhrak9QUVFEQXpDQnB6RUxNQWtHQTFVRUJoTUNWVk14RVRBUEJnTlZCQWdNQ0U1bGR5QlpiM0pyTVJFd0R3WURWUVFIREFoT1pYY2dXVzl5YXpFVE1CRUdBMVVFQ2d3S1ZISjFabThnU1c1akxqRVVNQklHQTFVRUN3d0xRMEVnUkdsMmFYTnBiMjR4R2pBWUJna3Foa2lHOXcwQkNRRVdDMk5oUUhSeWRXWnZMbUZwTVNzd0tRWURWUVFERENKVWNuVm1ieUJETWxCQklFTnNZV2x0SUZOcFoyNXBibWNnUTBFZ0tESXdNalVwTUI0WERUSTJNRFV4T0RBd01ETXlNbG9YRFRJMk1EWXhOekF3TURNeU1sb3dnYVV4Q3pBSkJnTlZCQVlUQWxWVE1SRXdEd1lEVlFRSURBaE9aWGNnV1c5eWF6RVJNQThHQTFVRUJ3d0lUbVYzSUZsdmNtc3hFekFSQmdOVkJBb01DbFJ5ZFdadklFbHVZeTR4RkRBU0JnTlZCQXNNQzBOQklFUnBkbWx6YVc5dU1Sb3dHQVlKS29aSWh2Y05BUWtCRmd0allVQjBjblZtYnk1aGFURXBNQ2NHQTFVRUF3d2dWSEoxWm04Z1F6SlFRU0JQUTFOUUlGSmxjM0J2Ym1SbGNpQW9NakF5TlNrd1dUQVRCZ2NxaGtqT1BRSUJCZ2dxaGtqT1BRTUJCd05DQUFUZC9Sa2I1aFpxM2JxRmp2d1VPbXpjdjJ5U0dnTDk1Y2htVTRPdHJ2RXI0bExVdCs1ZHIxQ0VneElMekNycTFZbTdtMy9QT0VPUjQzOGwvRjY4UHBkRW80R0hNSUdFTUIwR0ExVWREZ1FXQkJSUVdRWDFYNVFtMTFyTnEyNEpLeTFtRVJUMCtqQWZCZ05WSFNNRUdEQVdnQlREc3lTV05KT2hXZXBTR0d1ZUYrQ3B1dGF3VERBTUJnTlZIUk1CQWY4RUFqQUFNQTRHQTFVZER3RUIvd1FFQXdJSGdEQVRCZ05WSFNVRUREQUtCZ2dyQmdFRkJRY0RDVEFQQmdrckJnRUZCUWN3QVFVRUFnVUFNQW9HQ0NxR1NNNDlCQU1EQTJrQU1HWUNNUUNmRjhMZmZvdTJEZC9yY1NjWGluRDE2cFc0UlhsM2hXblpCdUVXMGExYjlJREhBdmdtVjhjNHVFVWt6eVlvcE8wQ01RRGhvK0VWUGRZRGxCc0hHUXBjaXczOS83enBkZFhPTTUzYStaMEdwYkhsQlJyR3BCcXNDNUZVazkwNHo1WFluSWs9eQXMTUlJRVZBb0JBS0NDQkUwd2dnUkpCZ2tyQmdFRkJRY3dBUUVFZ2dRNk1JSUVOakNCb3FJV0JCVEwySTQyaWlFUmN5eTU3NG9hbzJxZXZGTk1RQmdQTWpBeU5qQTFNakl5TWpBd016ZGFNSGN3ZFRCTk1Ba0dCU3NPQXdJYUJRQUVGSUFnOWJ6aUpPbHR2Tlp2eGhjcFpYd2t5UEg5QkJRRDFWK3Zmb1BsQkIxWmdDZEtOUDlGL2V0SmVBSVVNT2loOEtXSlFtdlN1WUpJUjVrWjNCWTNBc3VBQUJnUE1qQXlOakExTWpJeU1qQXdNemRhb0JFWUR6SXdNall3TlRJNU1qSXdNRE0zV2pBS0JnZ3Foa2pPUFFRREF3Tm9BREJsQWpFQS9La25ETU0zZ3VHcDlPNGVZZkdUWFlRME0rZUY3bGJjUVgvSUdCaDhtYTJ5eW9DVlhSMWc2N3c4dm13YTZQdzRBakFDK1FHNnNaM2t4alBycC93QWhKQXBEYkxna2E1WG1YVW5KazVoc3pBU1NrMWYyb2xRakNyNlhVUkcreTJPT09TZ2dnTVhNSUlERXpDQ0F3OHdnZ0tWb0FNQ0FRSUNGQVBRZlRTU2JWY1pjTWJZRkpCTWM4WFQ1WnZnTUFvR0NDcUdTTTQ5QkFNRE1JR29NUXN3Q1FZRFZRUUdFd0pWVXpFUk1BOEdBMVVFQ0F3SVRtVjNJRmx2Y21zeEVUQVBCZ05WQkFjTUNFNWxkeUJaYjNKck1STXdFUVlEVlFRS0RBcFVjblZtYnlCSmJtTXVNUlF3RWdZRFZRUUxEQXREUVNCRWFYWnBjMmx2YmpFYU1CZ0dDU3FHU0liM0RRRUpBUllMWTJGQWRISjFabTh1WVdreExEQXFCZ05WQkFNTUkxUnlkV1p2SUVNeVVFRWdVbTl2ZENCRFFTQW9NakF5TlN3Z1JVTkRJRkF6T0RRcE1CNFhEVEkyTURVeE1USXpOREl5TlZvWERUTTJNRFV3T0RJek5ESXlOVm93Z1o0eEN6QUpCZ05WQkFZVEFsVlRNUkV3RHdZRFZRUUlEQWhPWlhjZ1dXOXlhekVSTUE4R0ExVUVCd3dJVG1WM0lGbHZjbXN4RXpBUkJnTlZCQW9NQ2xSeWRXWnZJRWx1WXk0eEZEQVNCZ05WQkFzTUMwTkJJRVJwZG1semFXOXVNUm93R0FZSktvWklodmNOQVFrQkZndGpZVUIwY25WbWJ5NWhhVEVpTUNBR0ExVUVBd3daVkhKMVptOGdVbTl2ZENCUFExTlFJRkpsYzNCdmJtUmxjakIyTUJBR0J5cUdTTTQ5QWdFR0JTdUJCQUFpQTJJQUJHTDMxMnlnb0xYaHJOdkloaUxaeVhMTWU1ajRMSU1EaHJoMHdObFphTDlhV1Buc01WZVVFY1NCUVV1c29uL0pWaVhESSs3YVd5T3BzV3JLVm51cVcwcVhrOVFvNjN2cnlUZGszejlTYVJpbTYySkhOR1FKbkxzQ0lWaUNKN2tkT2FPQmh6Q0JoREFkQmdOVkhRNEVGZ1FVeTlpT05vb2hFWE1zdWUrS0dxTnFucnhUVEVBd0h3WURWUjBqQkJnd0ZvQVVBOVZmcjM2RDVRUWRXWUFuU2pUL1JmM3JTWGd3REFZRFZSMFRBUUgvQkFJd0FEQU9CZ05WSFE4QkFmOEVCQU1DQjRBd0V3WURWUjBsQkF3d0NnWUlLd1lCQlFVSEF3a3dEd1lKS3dZQkJRVUhNQUVGQkFJRkFEQUtCZ2dxaGtqT1BRUURBd05vQURCbEFqRUE3ZTBmaS9mTHpNNFRVOE42OUJyUXpBd1BHZ1RweERwV2hUV2FLcjRIaWJKR21WNUovTFdHNVZUV1VqckdhY2Q4QWpBWEdDVGEzdy9GZk1HVmlkUzFjZFRLckNuaEE2aUlxeTgzOE9sQi9sdCtHZU1TYnEydzZ2UVMza3oxc0ZFanh4Zz0AAADDanVtYgAAAEBqdW1kY2JvcgARABCAAACqADibcRNjMnBhLmhhc2guZGF0YQAAAAAYYzJzaFezSb7g+xH/+VAJJ5+IEYgAAAB7Y2JvcqVqZXhjbHVzaW9uc4GiZXN0YXJ0GCFmbGVuZ3RoGWFmZG5hbWVuanVtYmYgbWFuaWZlc3RjYWxnZnNoYTI1NmRoYXNoWCA0FqoUoF67r9Zu6sk/OqSNXb5XJfE3q+9SQ9ea9v7DqGNwYWRIAAAAAAAAAAAAAAMaanVtYgAAACdqdW1kYzJjbAARABCAAACqADibcQNjMnBhLmNsYWltLnYyAAAAAutjYm9ypmppbnN0YW5jZUlEeCx4bXA6aWlkOjUyNDgwZjBhLWM2ZmMtNGE2NS05NGRjLWM3ODJhZWFiZmYzY3RjbGFpbV9nZW5lcmF0b3JfaW5mb6RkbmFtZXgYT3BlbkFJIE1lZGlhIFNlcnZpY2UgQVBJZGljb26iY3VybHgkc2VsZiNqdW1iZj1jMnBhLmFzc2VydGlvbnMvYzJwYS5pY29uZGhhc2hYIG73uPdywyi7e+5i3woJqOKl1JJQ46Y6vhAo+5QUIXDVa3NwZWNWZXJzaW9uZTIuMi4wd29yZy5jb250ZW50YXV0aC5jMnBhX3JzZjAuNzkuMmlzaWduYXR1cmV4TXNlbGYjanVtYmY9L2MycGEvdXJuOmMycGE6YTg5ZTIyYzEtMWY1YS00MmExLWFlMGEtODllZWUxMWVmOTZiL2MycGEuc2lnbmF0dXJlcmNyZWF0ZWRfYXNzZXJ0aW9uc4SiY3VybHgkc2VsZiNqdW1iZj1jMnBhLmFzc2VydGlvbnMvYzJwYS5pY29uZGhhc2hYIG73uPdywyi7e+5i3woJqOKl1JJQ46Y6vhAo+5QUIXDVomN1cmx4KnNlbGYjanVtYmY9YzJwYS5hc3NlcnRpb25zL2MycGEuYWN0aW9ucy52MmRoYXNoWCAQkXa6GkVLJI5wd7kjX1OM9cbZJS/rzjm4qMO7Q1dJp6JjdXJseDJzZWxmI2p1bWJmPWMycGEuYXNzZXJ0aW9ucy9jMnBhLmNlcnRpZmljYXRlLXN0YXR1c2RoYXNoWCBUWFQF/w0EcCM4+wL3S9SIu7NLyV5jX348LNOfR4aTm6JjdXJseClzZWxmI2p1bWJmPWMycGEuYXNzZXJ0aW9ucy9jMnBhLmhhc2guZGF0YWRoYXNoWCCrpO4Z3HR5we5IqPtfl08/Lh6C+zS3O0V8XB2RTPeWhmhkYzp0aXRsZWlpbWFnZS5wbmdjYWxnZnNoYTI1NgAARc5qdW1iAAAAKGp1bWRjMmNzABEAEIAAAKoAOJtxA2MycGEuc2lnbmF0dXJlAAAARZ5jYm9y0oRZB1WiASYYIYJZA3IwggNuMIIC86ADAgECAhRSlCUHgbVqhvkzF3hw1o6t72IaQTAKBggqhkjOPQQDAzCBpzELMAkGA1UEBhMCVVMxETAPBgNVBAgMCE5ldyBZb3JrMREwDwYDVQQHDAhOZXcgWW9yazETMBEGA1UECgwKVHJ1Zm8gSW5jLjEUMBIGA1UECwwLQ0EgRGl2aXNpb24xGjAYBgkqhkiG9w0BCQEWC2NhQHRydWZvLmFpMSswKQYDVQQDDCJUcnVmbyBDMlBBIENsYWltIFNpZ25pbmcgQ0EgKDIwMjUpMB4XDTI2MDMyMzAyNTMwMloXDTI3MDMyNDAyNTMwMlowRzELMAkGA1UEBhMCVVMxGTAXBgNVBAoMEE9wZW5BSSBPcENvLCBMTEMxHTAbBgNVBAMMFE9wZW5BSSBNZWRpYSBTZXJ2aWNlMFkwEwYHKoZIzj0CAQYIKoZIzj0DAQcDQgAESqpE4gX/lrlPP8VsGeRutoYh53nozkzdKRVw+xuJZ8KNdAGRc/Mm9S9+4LWgcZYRYzNOJ1ZhjWl8ijimS/0qb6OCAVowggFWMB8GA1UdIwQYMBaAFMOzJJY0k6FZ6lIYa54X4Km61rBMMB0GA1UdDgQWBBQKd12L3lQTzn/zDzdxWsmHk1kx2DAMBgNVHRMBAf8EAjAAMA4GA1UdDwEB/wQEAwIGwDAfBgNVHSUEGDAWBgorBgEEAYPoXgIBBggrBgEFBQcDJDAlBgNVHSAEHjAcMAwGCisGAQQBg+heAQEwDAYKKwYBBAGD6DwBATBeBggrBgEFBQcBAQRSMFAwIQYIKwYBBQUHMAGGFWh0dHBzOi8vb2NzcC50cnVmby5haTArBggrBgEFBQcwAoYfaHR0cHM6Ly9jYS50cnVmby5haS9jMnBhLWNhLmNydDAzBgkrBgEEAYPoXgQEJgwkMDE5YmM0MDMtNWNkNy03NjY5LWFmZTYtZmRiMTcxNzdkNDI4MBkGCSsGAQQBg+heAwQMBgorBgEEAYPoXgMKMAoGCCqGSM49BAMDA2kAMGYCMQD/5oFiNWv70TfsT9gQvQqMqQ+mBNdWbS3qZxvVvolX750qrwd9eyqWWlGaoojvpc8CMQCtgDZrZ+hERAeVrM0BhL3tW8vdHVmLeIcDzg5lKxX7dJ+7xR2q0PF+uOzAiEt2FThZA9cwggPTMIIDWKADAgECAhQw6KHwpYlCa9K5gkhHmRncFjcCyzAKBggqhkjOPQQDAzCBqDELMAkGA1UEBhMCVVMxETAPBgNVBAgMCE5ldyBZb3JrMREwDwYDVQQHDAhOZXcgWW9yazETMBEGA1UECgwKVHJ1Zm8gSW5jLjEUMBIGA1UECwwLQ0EgRGl2aXNpb24xGjAYBgkqhkiG9w0BCQEWC2NhQHRydWZvLmFpMSwwKgYDVQQDDCNUcnVmbyBDMlBBIFJvb3QgQ0EgKDIwMjUsIEVDQyBQMzg0KTAeFw0yNjAyMDEwOTE1MThaFw0zMTAyMDIwOTE1MThaMIGnMQswCQYDVQQGEwJVUzERMA8GA1UECAwITmV3IFlvcmsxETAPBgNVBAcMCE5ldyBZb3JrMRMwEQYDVQQKDApUcnVmbyBJbmMuMRQwEgYDVQQLDAtDQSBEaXZpc2lvbjEaMBgGCSqGSIb3DQEJARYLY2FAdHJ1Zm8uYWkxKzApBgNVBAMMIlRydWZvIEMyUEEgQ2xhaW0gU2lnbmluZyBDQSAoMjAyNSkwdjAQBgcqhkjOPQIBBgUrgQQAIgNiAAT6nePm+iap9anW9g1vYcU48uYz6gX4CUK6t39puP/+hjrZp+dtJ/xCm6C8vvOu7I0CEplsz+LiuPpZ4dKhD9LrTR+MFpTlkk9Lx+fuvwrhuDUk4YFoGhEQNuEIGUfsqn6jggFAMIIBPDAdBgNVHQ4EFgQUw7MkljSToVnqUhhrnhfgqbrWsEwwHwYDVR0jBBgwFoAUA9Vfr36D5QQdWYAnSjT/Rf3rSXgwEgYDVR0TAQH/BAgwBgEB/wIBADAOBgNVHQ8BAf8EBAMCAQYwKQYDVR0lBCIwIAYKKwYBBAGD6F4CAQYIKwYBBQUHAyQGCCsGAQUFBwMEMEsGA1UdIAREMEIwDAYKKwYBBAGD6F4BATAyBgorBgEEAYPoPAEBMCQwIgYIKwYBBQUHAgEWFmh0dHBzOi8vdHJ1Zm8uYWkvY3BjcHMwXgYIKwYBBQUHAQEEUjBQMCEGCCsGAQUFBzABhhVodHRwczovL29jc3AudHJ1Zm8uYWkwKwYIKwYBBQUHMAKGH2h0dHBzOi8vY2EudHJ1Zm8uYWkvcm9vdC1jYS5jcnQwCgYIKoZIzj0EAwMDaQAwZgIxANUL/ipIu2RmAlZcGK/VHamYaH2+6PG4ur1AdDuswfgZPWOYLa6LB2X4geGqakrqZwIxAOtpNdTYxWmpTtGzLBYp1OCgrx77qUDJu5yH754Tq54tmfQ0BZRiuwuB6O0NuIz0tKNnc2lnVHN0MqFpdHN0VG9rZW5zgaFjdmFsWRSLMIIUhwYJKoZIhvcNAQcCoIIUeDCCFHQCAQExDzANBglghkgBZQMEAgEFADCBhwYLKoZIhvcNAQkQAQSgeAR2MHQCAQEGCisGAQQBg78wAQEwMTANBglghkgBZQMEAgEFAAQgxs455oCjS41mMPoPXAOHqqYS65Jmk2DdDzbpV/opJf0CCBxGVM8q0xUaGBYyMDI2MDUyMzIwNDAwNi44NDI2NjZaMAOAAQECCQCgtCMe6s2G2KCCEGYwggT2MIIDXqADAgECAhRh20YoMoqMjUoGt7/+YOMCbD9xtzANBgkqhkiG9w0BAQsFADB7MQswCQYDVQQGEwJVUzELMAkGA1UECAwCQ0ExFjAUBgNVBAcMDVNhbiBGcmFuY2lzY28xGTAXBgNVBAoMEE9wZW5BSSBPcENvLCBMTEMxDDAKBgNVBAsMA1RTQTEeMBwGA1UEAwwVT3BlbkFJIFRTQSBJc3N1aW5nIENBMB4XDTI2MDQwODE3NDYyNloXDTM3MDcwOTE3NDYyNlowdTELMAkGA1UEBhMCVVMxCzAJBgNVBAgMAkNBMRYwFAYDVQQHDA1TYW4gRnJhbmNpc2NvMRkwFwYDVQQKDBBPcGVuQUkgT3BDbywgTExDMQwwCgYDVQQLDANUU0ExGDAWBgNVBAMMD09wZW5BSSBUU0EgTGVhZjCCAaIwDQYJKoZIhvcNAQEBBQADggGPADCCAYoCggGBAOrKxa2U/fD9J5/HeKdhBMr/DilhKvuhiM1fqKKXnQ6JL4uRyB+8sJaQPQgcVYLBlo42ahWtiWnokNssRDKDqArNd+U16O6oZFv+uOCOnecCIKEowzXdpxA36SL3CU2XmrSEc8AufKlQRyigtPBpH/Cwhyl6Wf4PFBQ1QvnZaVIXSiA38mjMD/Ett4KWIBtLEQ5GElw9pBSGuEtFZjiiTk0nypW6dQzMTodqn3TDIBUFASRfDcR+XK7+HfMfC5XtAJHfPPWGmyoSXg7WDxzQ3cn6DchNw8mEWhhJLOQ4cxpgUrhM7sbzt7bY3WqpziC6XdbEXDUQZPIDIxFTP2KOZQURXXAr1MlrCYFFUugaV+1aRl3aXXacJXkQaINRpJiEdZFymFX/2ONDYrHtaWcnQbzFj/JqByuDSejhLRg0Drs5B69nvbSVHsgCsr1FZ81yAYiUX1VLBiytr+2l9CSvdwM+g4pkUY+RjAw5lkuwPa76BJmhPhiMPfC+FzahLvVjtQIDAQABo3gwdjAMBgNVHRMBAf8EAjAAMA4GA1UdDwEB/wQEAwIGwDAWBgNVHSUBAf8EDDAKBggrBgEFBQcDCDAdBgNVHQ4EFgQUpCdUgqKKgHs9xYbNP3DZwoOZUXgwHwYDVR0jBBgwFoAU8hTwsMcXVD0jQ4XcynPQcoA9uKgwDQYJKoZIhvcNAQELBQADggGBACD7JE9BwMC8mLIyEiAQjSCZSDUST8RGVn6nPj+2pSP5Kkg+4FGdH0VAeMG7g06TUMmbJ5Zo303O8vYc0nmr7+rBH9o/9ZhZCOZwzYn07keLqsvs/4x+FOFG2JHmnLge5DRG/2HSePh9ODnjUu0bX2boc8AAcjvkqKuOhhsqozch+Tvfe1xU2EzHaipLf89DdGAFgHOjydF3r4ep/bWxhGpuv4gqzpqhmquinoJIBww3xQJjUZfbUnxvHmfJaQhC1c/1+60bXouQ4uAIeTwuGxODap6l6CVBj4UQAe3kGMGgOo3+nVJQGu+H3uFkzVX5ISDftinvnydu0bo0RqtKIk/nYhV33UUj3WEtwjEpj8S5fnkCBqu0V9TB7M8dBuFce2VJsBnrTaukxydATqa0tY/PfMO0Q6d2014wY+6oF641KHRkq1o141svOj5OCmHWME1Dm/9OLsYhuT46LCAZVzB1ao5kS6LQCdEW16BnJkFtZ/gDcHa4JSZW+ZEmJ8NLSTCCBX4wggNmoAMCAQICFASNBMrGxQvF2hmwvPFOEZWl6rwZMA0GCSqGSIb3DQEBCwUAMHgxCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJDQTEWMBQGA1UEBwwNU2FuIEZyYW5jaXNjbzEZMBcGA1UECgwQT3BlbkFJIE9wQ28sIExMQzEMMAoGA1UECwwDVFNBMRswGQYDVQQDDBJPcGVuQUkgVFNBIFJvb3QgQ0EwIBcNMjYwNDA4MTc0NjI2WhgPMjEyNjA0MDkxNzQ2MjZaMHsxCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJDQTEWMBQGA1UEBwwNU2FuIEZyYW5jaXNjbzEZMBcGA1UECgwQT3BlbkFJIE9wQ28sIExMQzEMMAoGA1UECwwDVFNBMR4wHAYDVQQDDBVPcGVuQUkgVFNBIElzc3VpbmcgQ0EwggGiMA0GCSqGSIb3DQEBAQUAA4IBjwAwggGKAoIBgQCJvNS54sihC75hu948ZGZ+p76cbRDTqTAHJjwE9OBrIDnflTTtqaJlCEjbN4Yyg47MCkqgwPM0bKDAmM0rn6X0y3zZDybefslNou9jW5Hm9lmo0gH6TvnZOCtaDs1gWpiBmKjXU8bjGdYuSKxDVwnplPJH+WxFihVgt/euL16iNU6FOIVpnzSd0E3YQz3NNG38Y5P803C7Suh26GpOZkmg7fz4GL7vmhe3qHes77c4zLnUKjPEdg/WQBF3y/7HXRctQNPeizzAGNZAFEGZy5Q/LH0Aa1L8nspQtwlHRRXhBSNV+rFPb1SYlfR9uvho4SIcetyKkUOLFbYuEkOxYhygvsokji7vv6TRTei4PzHPJj3FAFDq8tkkIGTt1XOeLnB4qt5WPAX51ICi6K2v9vuoo1zLaKtE2zB38sQ0dGtVbcaH+/IyPJ5xDkUT9+xQD/v+1gQxJrvQxE1h4kLbr8Mrbl8rGRvm4rDvjVxEzR/Ac32Poum9bYK8JWWECDBp7RUCAwEAAaN7MHkwEgYDVR0TAQH/BAgwBgEB/wIBADAOBgNVHQ8BAf8EBAMCAQYwEwYDVR0lBAwwCgYIKwYBBQUHAwgwHQYDVR0OBBYEFPIU8LDHF1Q9I0OF3Mpz0HKAPbioMB8GA1UdIwQYMBaAFFjCQKA8R3YrqOZuqJGWjpbIt9nkMA0GCSqGSIb3DQEBCwUAA4ICAQCS7Ddc3mzrZNquoREJMHKu3HII9Tu8D3o91sbhL/aDM33oH1dAGE5Mmapr1JnZFIvba9ZM+MrQWTPToaA4XCOIRCT7h+H2kwYnvKHtTF9nXf81qzHS7HsR1EBDN0/ChBucumTID7CiHX6aNvjh0IKzUEOy4FW9gJTIWVJOSnTeXcdFWJu3+jCqO9xHvNUuLLk4GGMseVq33VWtPULfiAPP8Wj+cwDUWrfeJAKXkcDnZ/7cpgrzpUYRs1EcfxLPja9f4xjIuEDGveP51ktx0GRd5WTCS8Bed9E9x1ueFc97/ZSU5wFLCFHa+2T0qxHwNZTx9r5+Kw7dspo9UN1Qw5Zkjm2rDHOfKAY7BHfQl+1vRU+xMy5fRuuDtqlhH7zXgq74gG/C42kVMOZtfDpEkisGmC2v3DTBvqUqSOeHyN44DLUEDDPK44RQcPGyHkvejU/2kRncX4X68ebR18qn7rSf9iF4KYHw43BYdwEQhqQ6S5eDRujawmp2yakSyyEcD0W+ZbGghi6AvFlLTZtDH22014Tg/PDVyGGQDUOOE2qdw/EhPIRdBv471tgjOUULXx1xDfoy/aCAlUS1TwDlw3T94k6Hcob08FEBhx4IvdS1KzVsBhCSpDtrap26/cA7B5x2wgzVGDl/SdrjlBw+UAhq10ziiWGd7+vPxcNAbnB6ODCCBeYwggPOoAMCAQICFBNQO2yJjPAkAzMsj/dPjvt9guwbMA0GCSqGSIb3DQEBCwUAMHgxCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJDQTEWMBQGA1UEBwwNU2FuIEZyYW5jaXNjbzEZMBcGA1UECgwQT3BlbkFJIE9wQ28sIExMQzEMMAoGA1UECwwDVFNBMRswGQYDVQQDDBJPcGVuQUkgVFNBIFJvb3QgQ0EwIBcNMjYwNDA4MTc0NjI1WhgPMjEyNjA0MDkxNzQ2MjVaMHgxCzAJBgNVBAYTAlVTMQswCQYDVQQIDAJDQTEWMBQGA1UEBwwNU2FuIEZyYW5jaXNjbzEZMBcGA1UECgwQT3BlbkFJIE9wQ28sIExMQzEMMAoGA1UECwwDVFNBMRswGQYDVQQDDBJPcGVuQUkgVFNBIFJvb3QgQ0EwggIiMA0GCSqGSIb3DQEBAQUAA4ICDwAwggIKAoICAQD2kunSFLqtnuEarHWoVhvYqrGzapJflnn1krcULST4v8Aar2C+wZrNeZrcbJr+NprBmBakP+QsnbqlpVBzswrC+RrzxEkveL3S7LznP/Sb0RoP8qBhoiyJJcpRBhEX+SUQnNLGL/SJxEESDv4mHtNtNc3suzVgQKiFUb727pCY8SrYnXoQa2rZLtlj8+UUXCnFhiLBihxozes4nqlQllsjQ/s4/0J8OzqhUS8lyUjcMf9Qcu7wfKF3zRhvgWHzP79u6NIbsaYINuRrMvv+d6hem1zd3TGQTI5l/xaBy0HOKDFTyhhDzkgEbn3WZBazKRDktC46t1RaclZX86hqfR7v5mEf3WXIDkgJSZkydPAKoszdkwBTrCO9goUgse++7R2hdwDuOkYzop7sr+kGMWa0Zm+yiZOgfpUODyHOQfhe8I7pzbnA1TNdeNDQJzHPUDBycx0e2mrCwJPPrdwPZIf2+whOiHb1Pu//kiyZdy4L9gbcmLadCQM6/fQaCcePX1rpfkgNCSu1HoqDGwTyWxU8LBADr5GinUG3UmjRDREaGb+wwNpPYL3uKarth41xXCiMjYijJRRjRdgF/Hthj2xGVDsYXMmwgq+DyLEjPxyfGlvuotdUtSpTrruF26b6l57shIly83pAyRa2hVhHW/EkYTmiTN7Yxqgi8p6/W0wsywIDAQABo2YwZDASBgNVHRMBAf8ECDAGAQH/AgEBMA4GA1UdDwEB/wQEAwIBBjAdBgNVHQ4EFgQUWMJAoDxHdiuo5m6okZaOlsi32eQwHwYDVR0jBBgwFoAUWMJAoDxHdiuo5m6okZaOlsi32eQwDQYJKoZIhvcNAQELBQADggIBAFj4gZEMmPJsYf7Ihh3WW4Qdpta+uKZdDF1Jy7ihKc0tnbhY+fCEiT08+G/Vah+0KqJVkvBngZletVQM+5pGgOMCUQBTwA4DwYhX3u+CVX7j9H0Y6w8m/IP/IajBrN7bG5OrGc3QMHYYOpOdzqpnAw05Gi6AdN9t8H4Tdi/p6lBBizg9bOXgPu4v22RUNl4RvmJFttEhtIA8jBjr2pzWSqnVVGVba9FYfsBJh+vrS1+SDDuU15qG9qFZzkfwOKzDsH8DdGTRwFI7obF7KGvhDmmX+AIYDCgXOyf/rqQQnvdly6D06rm9lM5E4pixCkho7lWpIaVgj/7K1n3Re4YgnA7zqHjQxtpALsiBBQtcYqgqwftW5xh5B44Rr+zl29Nw/kbMY6hk8Tzpr6VkvF6/hQgtHrDO47nTpBHXUrtwi4ad+y6/CvbSVSsjQitDXOyhgmE/z3HtsPeX6eTLwjz8rHe3ttwgwUzpibIPsi9/w36SZJwItYTezJb9ibBLtUN90umthv0Z2S2fvQDuwLRHViN8SBWRDk4PZ4kge2IIwcleVfH2BsZRI1dv74e+FCBGeb6UArHIICidlYqIJlUFZlLvGH/ZS7qoWhTpwiytnwvDXELzofUnZHlxjApanv25+UV5B3Ae4WoDtTeWjlj9Rb9UJYyDAz0P2SYzI9BYd6a4MYIDaDCCA2QCAQEwgZMwezELMAkGA1UEBhMCVVMxCzAJBgNVBAgMAkNBMRYwFAYDVQQHDA1TYW4gRnJhbmNpc2NvMRkwFwYDVQQKDBBPcGVuQUkgT3BDbywgTExDMQwwCgYDVQQLDANUU0ExHjAcBgNVBAMMFU9wZW5BSSBUU0EgSXNzdWluZyBDQQIUYdtGKDKKjI1KBre//mDjAmw/cbcwDQYJYIZIAWUDBAIBBQCgggElMBoGCSqGSIb3DQEJAzENBgsqhkiG9w0BCRABBDAvBgkqhkiG9w0BCQQxIgQglSzMCrNDXezGhOXkjid7MNGygsP0TYL8Hwdb7DEnHRYwgdUGCyqGSIb3DQEJEAIvMYHFMIHCMIG/MIG8BCC9T7mykEyBNmeIbu9B4W3+BNkiB52/W5JK0KLEYEYiejCBlzB/pH0wezELMAkGA1UEBhMCVVMxCzAJBgNVBAgMAkNBMRYwFAYDVQQHDA1TYW4gRnJhbmNpc2NvMRkwFwYDVQQKDBBPcGVuQUkgT3BDbywgTExDMQwwCgYDVQQLDANUU0ExHjAcBgNVBAMMFU9wZW5BSSBUU0EgSXNzdWluZyBDQQIUYdtGKDKKjI1KBre//mDjAmw/cbcwDQYJKoZIhvcNAQELBQAEggGAsF/qcUEWv99sBW5SP4ng49/lTazdMZCAqzFjDLyVLkpC0uMjjzss+m+0S+wjD3xI1aHGQtwovaJ7voi9OvwQMtXy0V1J25LJxx04xdB+lm9GpqnpXLk5tWw5ynLQ6TNyiaZ4KV3Hhkz0r/nRlt2wkguVskih28jXADXqs0vhFwUOrJRPQyULTd2ksIO5XMDSzbP4Payek6m55wHtoNtX0DGb9yUISseRSK9xvpQR2BJbZk0oXvBjl/YTwuqDeyLNGsREZrwlKMljFSotc1ZyPGmwXJavsAQgIuKqeB1g6x6L8mWgTWTrkIH662xoYwRZfNNrrGbgiN0gp27Yfn83Hw/jHtq3PcphL1Qxt9eno/s4wvMGtNmy6ngiBTJrnD6WcvLHUgRqlPgv/XfqQCvgpKZG5BMKnn8FrNvhcZ/wR1hF6Txl8wbu//x8SsTAV09uVJJaPG1QmsmB0Mf+m3GETE2FBfx/vQuARAzTcSBraJCQ04xrzyz4URcPSZq1hrHKZXJWYWxzoWhvY3NwVmFsc4FZBCIwggQeCgEAoIIEFzCCBBMGCSsGAQUFBzABAQSCBAQwggQAMIGiohYEFFBZBfVflCbXWs2rbgkrLWYRFPT6GA8yMDI2MDUyMjIyMDAzNlowdzB1ME0wCQYFKw4DAhoFAAQUPkx8jlALh2xzFb6vbpfqEO6UIMkEFMOzJJY0k6FZ6lIYa54X4Km61rBMAhRSlCUHgbVqhvkzF3hw1o6t72IaQYAAGA8yMDI2MDUyMjIyMDAzNlqgERgPMjAyNjA1MjkyMjAwMzZaMAoGCCqGSM49BAMCA0gAMEUCIQCPyEA3XI36IE42ftNCVSuxLIligoKePe+an/TUqqmd1AIgewpfQ/McCyY3qWT9UW+yzlZHKT9h+c3LU+1+mOiFic6gggMBMIIC/TCCAvkwggJ+oAMCAQICFG5Fk3rq3jZxGe581rPIkINDo+zaMAoGCCqGSM49BAMDMIGnMQswCQYDVQQGEwJVUzERMA8GA1UECAwITmV3IFlvcmsxETAPBgNVBAcMCE5ldyBZb3JrMRMwEQYDVQQKDApUcnVmbyBJbmMuMRQwEgYDVQQLDAtDQSBEaXZpc2lvbjEaMBgGCSqGSIb3DQEJARYLY2FAdHJ1Zm8uYWkxKzApBgNVBAMMIlRydWZvIEMyUEEgQ2xhaW0gU2lnbmluZyBDQSAoMjAyNSkwHhcNMjYwNTE4MDAwMzIyWhcNMjYwNjE3MDAwMzIyWjCBpTELMAkGA1UEBhMCVVMxETAPBgNVBAgMCE5ldyBZb3JrMREwDwYDVQQHDAhOZXcgWW9yazETMBEGA1UECgwKVHJ1Zm8gSW5jLjEUMBIGA1UECwwLQ0EgRGl2aXNpb24xGjAYBgkqhkiG9w0BCQEWC2NhQHRydWZvLmFpMSkwJwYDVQQDDCBUcnVmbyBDMlBBIE9DU1AgUmVzcG9uZGVyICgyMDI1KTBZMBMGByqGSM49AgEGCCqGSM49AwEHA0IABN39GRvmFmrduoWO/BQ6bNy/bJIaAv3lyGZTg62u8SviUtS37l2vUISDEgvMKurVibubf884Q5HjfyX8Xrw+l0SjgYcwgYQwHQYDVR0OBBYEFFBZBfVflCbXWs2rbgkrLWYRFPT6MB8GA1UdIwQYMBaAFMOzJJY0k6FZ6lIYa54X4Km61rBMMAwGA1UdEwEB/wQCMAAwDgYDVR0PAQH/BAQDAgeAMBMGA1UdJQQMMAoGCCsGAQUFBwMJMA8GCSsGAQUFBzABBQQCBQAwCgYIKoZIzj0EAwMDaQAwZgIxAJ8Xwt9+i7YN3+txJxeKcPXqlbhFeXeFadkG4RbRrVv0gMcC+CZXxzi4RSTPJiik7QIxAOGj4RU91gOUGwcZClyLDf3/vOl11c4zndr5nQalseUFGsakGqwLkVST3TjPldiciWNwYWRZJRQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA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