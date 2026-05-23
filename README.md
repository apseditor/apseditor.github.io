<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Arghya Samanta — Video Editor</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;500;600&family=DM+Mono:wght@300;400&display=swap" rel="stylesheet">
<style>
  :root {
    --white: #f0eeea;
    --gray-light: #888;
    --gray-mid: #444;
    --gray-dark: #1a1a1a;
    --black: #0a0a0a;
    --glow-blue: #4a9eff;
    --glow-white: rgba(255,255,255,0.08);
  }

  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--black);
    color: var(--white);
    font-family: 'DM Mono', monospace;
    font-weight: 300;
    overflow-x: hidden;
    cursor: none;
  }

  /* Custom cursor */
  .cursor {
    position: fixed;
    width: 8px; height: 8px;
    background: var(--glow-blue);
    border-radius: 50%;
    pointer-events: none;
    z-index: 9999;
    transform: translate(-50%, -50%);
    transition: transform 0.1s ease;
    box-shadow: 0 0 12px var(--glow-blue), 0 0 24px var(--glow-blue);
  }
  .cursor-ring {
    position: fixed;
    width: 32px; height: 32px;
    border: 1px solid rgba(74,158,255,0.4);
    border-radius: 50%;
    pointer-events: none;
    z-index: 9998;
    transform: translate(-50%, -50%);
    transition: all 0.18s ease;
  }

  /* Noise texture overlay */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none;
    z-index: 1000;
    opacity: 0.5;
  }

  /* NAV */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 28px 60px;
    border-bottom: 1px solid rgba(255,255,255,0.04);
    backdrop-filter: blur(12px);
    background: rgba(10,10,10,0.7);
  }

  .nav-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.1rem;
    font-weight: 500;
    letter-spacing: 0.1em;
    color: var(--white);
    text-decoration: none;
  }

  .nav-links {
    display: flex;
    gap: 40px;
    list-style: none;
  }

  .nav-links a {
    color: var(--gray-light);
    text-decoration: none;
    font-size: 0.65rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    transition: color 0.3s;
  }

  .nav-links a:hover { color: var(--white); }

  /* HERO */
  .hero {
    min-height: 100vh;
    display: flex;
    align-items: center;
    padding: 120px 60px 80px;
    position: relative;
    overflow: hidden;
  }

  .hero-bg {
    position: absolute;
    inset: 0;
    background: 
      radial-gradient(ellipse 60% 50% at 70% 50%, rgba(74,158,255,0.05) 0%, transparent 70%),
      radial-gradient(ellipse 40% 60% at 20% 80%, rgba(74,158,255,0.03) 0%, transparent 60%);
  }

  /* Animated grid lines */
  .hero-grid {
    position: absolute;
    inset: 0;
    background-image: 
      linear-gradient(rgba(255,255,255,0.02) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255,255,255,0.02) 1px, transparent 1px);
    background-size: 80px 80px;
    mask-image: radial-gradient(ellipse 80% 80% at 50% 50%, black 0%, transparent 100%);
  }

  .hero-content {
    position: relative;
    z-index: 2;
    max-width: 900px;
  }

  .hero-tag {
    display: inline-block;
    font-size: 0.6rem;
    letter-spacing: 0.3em;
    text-transform: uppercase;
    color: var(--glow-blue);
    border: 1px solid rgba(74,158,255,0.3);
    padding: 6px 16px;
    margin-bottom: 40px;
    opacity: 0;
    animation: fadeUp 0.8s ease 0.2s forwards;
  }

  h1 {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(4rem, 10vw, 9rem);
    font-weight: 300;
    line-height: 0.9;
    letter-spacing: -0.02em;
    margin-bottom: 40px;
    opacity: 0;
    animation: fadeUp 0.8s ease 0.4s forwards;
  }

  h1 .glow-name {
    display: block;
    color: var(--white);
    text-shadow: 0 0 60px rgba(74,158,255,0.3), 0 0 120px rgba(74,158,255,0.15);
  }

  h1 .thin-line {
    display: block;
    color: var(--gray-mid);
    font-weight: 300;
    font-style: italic;
  }

  .hero-desc {
    max-width: 480px;
    font-size: 0.75rem;
    line-height: 1.9;
    color: var(--gray-light);
    margin-bottom: 50px;
    opacity: 0;
    animation: fadeUp 0.8s ease 0.6s forwards;
  }

  .hero-cta {
    display: flex;
    gap: 20px;
    opacity: 0;
    animation: fadeUp 0.8s ease 0.8s forwards;
  }

  .btn-primary {
    display: inline-block;
    padding: 14px 36px;
    border: 1px solid rgba(74,158,255,0.5);
    color: var(--glow-blue);
    text-decoration: none;
    font-size: 0.65rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    position: relative;
    overflow: hidden;
    transition: all 0.3s;
    font-family: 'DM Mono', monospace;
    cursor: none;
  }

  .btn-primary::before {
    content: '';
    position: absolute;
    inset: 0;
    background: rgba(74,158,255,0.08);
    transform: translateX(-100%);
    transition: transform 0.3s ease;
  }

  .btn-primary:hover::before { transform: translateX(0); }
  .btn-primary:hover {
    box-shadow: 0 0 20px rgba(74,158,255,0.3), inset 0 0 20px rgba(74,158,255,0.05);
  }

  .btn-ghost {
    display: inline-block;
    padding: 14px 36px;
    border: 1px solid rgba(255,255,255,0.1);
    color: var(--gray-light);
    text-decoration: none;
    font-size: 0.65rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    transition: all 0.3s;
    font-family: 'DM Mono', monospace;
    cursor: none;
  }

  .btn-ghost:hover {
    border-color: rgba(255,255,255,0.3);
    color: var(--white);
  }

  /* STATS */
  .stats-bar {
    border-top: 1px solid rgba(255,255,255,0.05);
    border-bottom: 1px solid rgba(255,255,255,0.05);
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    padding: 0 60px;
  }

  .stat-item {
< truncated lines 254-595 >
    color: var(--glow-blue);
    margin-top: 12px;
    display: block;
  }

  .exp-bullets {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .exp-bullets li {
    font-size: 0.7rem;
    line-height: 1.8;
    color: var(--gray-light);
    padding-left: 20px;
    position: relative;
  }

  .exp-bullets li::before {
    content: '—';
    position: absolute;
    left: 0;
    color: var(--glow-blue);
    font-size: 0.6rem;
  }

  /* Responsive */
  @media (max-width: 768px) {
    nav { padding: 20px 24px; }
    .nav-links { display: none; }
    section { padding: 80px 24px; }
    .hero { padding: 100px 24px 60px; }
    .stats-bar { grid-template-columns: 1fr; padding: 0 24px; }
    .stat-item { border-right: none; border-bottom: 1px solid rgba(255,255,255,0.05); }
    .expertise-grid { grid-template-columns: 1fr; }
    .experience-block { grid-template-columns: 1fr; gap: 30px; }
    footer { padding: 24px; flex-direction: column; gap: 12px; }
    .divider { margin: 0 24px; }
  }
</style>
</head>
<body>

<div class="cursor" id="cursor"></div>
<div class="cursor-ring" id="cursorRing"></div>

<nav>
  <a href="#" class="nav-logo">APS EDITOR</a>
  <ul class="nav-links">
    <li><a href="#work">Work</a></li>
    <li><a href="#expertise">Expertise</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-bg"></div>
  <div class="hero-grid"></div>
  <div class="hero-content">
    <span class="hero-tag">Available for Collaborations</span>
    <h1>
      <span class="glow-name">Arghya</span>
      <span class="glow-name">Samanta</span>
      <span class="thin-line">Video Editor</span>
    </h1>
    <p class="hero-desc">
      Premium freelance video editor with 4 years of agency experience. Specializing in dynamic, high-retention content — from cinematic real estate to viral short-form.
    </p>
    <div class="hero-cta">
      <a href="#contact" class="btn-primary">Get in Touch</a>
      <a href="https://framefolio.in/apsvisuallab" target="_blank" class="btn-ghost">View Portfolio →</a>
    </div>
  </div>
</section>

<!-- MARQUEE -->
<div class="marquee-wrap">
  <div class="marquee-track">
    <span class="marquee-item">Adobe Premiere Pro <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Motion Graphics <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Color Grading <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Topaz AI <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">CapCut PC <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">After Motion <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Podcast Production <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Real Estate Edits <span class="marquee-dot">✦</span></span>
    <!-- duplicate for loop -->
    <span class="marquee-item">Adobe Premiere Pro <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Motion Graphics <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Color Grading <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Topaz AI <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">CapCut PC <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">After Motion <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Podcast Production <span class="marquee-dot">✦</span></span>
    <span class="marquee-item">Real Estate Edits <span class="marquee-dot">✦</span></span>
  </div>
</div>

<!-- STATS -->
<div class="stats-bar" id="stats">
  <div class="stat-item">
    <span class="stat-num">30+</span>
    <span class="stat-label">Happy Clients</span>
  </div>
  <div class="stat-item">
    <span class="stat-num">81.2K+</span>
    <span class="stat-label">YT Subscribers</span>
  </div>
  <div class="stat-item">
    <span class="stat-num">58.5M+</span>
    <span class="stat-label">Channel Views</span>
  </div>
</div>

<!-- EXPERIENCE -->
<section id="work">
  <div class="section-label">Experience</div>
  <h2 class="section-title">4 Years of<br>Premium Editing</h2>

  <div class="experience-block" data-animate>
    <div class="exp-meta">
      <div class="exp-role">Freelance Video Editor</div>
      <div class="exp-org">Various Agencies & Independent Clients</div>
      <span class="exp-years">4 Years</span>
    </div>
    <ul class="exp-bullets">
      <li>End-to-end editing workflows for real estate, medical content, business showcases, and high-energy podcasts.</li>
      <li>Integrated seamless motion graphics directly within the video editing process. Complex visual retouching and environmental compositing while maintaining strict biometric consistency.</li>
      <li>Cinematic color correction and grading — bringing a premium look to teasers, minimal edits, and short-form content.</li>
      <li>Edited highly engaging meme and viral content tailored for algorithms, significantly boosting client metrics.</li>
    </ul>
  </div>
</section>

<div class="divider"></div>

<!-- EXPERTISE -->
<section id="expertise">
  <div class="section-label">Expertise</div>
  <h2 class="section-title">What I Do<br>Best</h2>
  <div class="expertise-grid">
    <div class="expertise-card" data-animate>
      <span class="card-num">01</span>
      <div class="card-title">High-Retention Shorts & Teasers</div>
      <p class="card-desc">Fast-paced, algorithm-friendly edits utilizing dynamic subtitles, high-impact sound design, and Topaz AI upscaling for maximum viewer retention.</p>
    </div>
    <div class="expertise-card" data-animate>
      <span class="card-num">02</span>
      <div class="card-title">Cinematic Real Estate & Products</div>
      <p class="card-desc">Clean, minimalist edits relying on pristine cinematic color grading and smooth camera pacing to highlight property features and commercial goods.</p>
    </div>
    <div class="expertise-card" data-animate>
      <span class="card-num">03</span>
      <div class="card-title">Medical & Informative Content</div>
      <p class="card-desc">Clear, professional layouts for complex business and medical content, utilizing motion graphics to explain abstract concepts with precision and clarity.</p>
    </div>
    <div class="expertise-card" data-animate>
      <span class="card-num">04</span>
      <div class="card-title">Podcast Production</div>
      <p class="card-desc">Multi-cam syncing, seamless audio-video pacing, and engaging cutaways to retain audience attention throughout long-form formats.</p>
    </div>
  </div>
</section>

<!-- SOFTWARE -->
<section class="software-section">
  <div class="section-label">Core Stack</div>
  <h2 class="section-title" style="margin-bottom: 40px;">Software &<br>Tools</h2>
  <div class="software-list">
    <span class="software-tag" data-animate>Adobe Premiere Pro</span>
    <span class="software-tag" data-animate>Adobe Photoshop</span>
    <span class="software-tag" data-animate>CapCut PC</span>
    <span class="software-tag" data-animate>Topaz AI</span>
    <span class="software-tag" data-animate>After Motion</span>
    <span class="software-tag" data-animate>Alight Motion</span>
  </div>
</section>

<div class="divider"></div>

<!-- CONTACT -->
<section class="contact-section" id="contact">
  <div class="section-label">Let's Work Together</div>
  <h2 class="section-title" style="margin-bottom: 24px;">Ready to create<br>something premium?</h2>
  <a href="mailto:apsediting120@gmail.com" class="contact-email">apsediting120@gmail.com</a>
  <div class="contact-links">
    <a href="https://framefolio.in/apsvisuallab" class="contact-link" target="_blank">Portfolio</a>
    <a href="https://youtube.com/@aps_editor_1m" class="contact-link" target="_blank">YouTube</a>
    <a href="https://linkedin.com/in/aps-editor-37212640a" class="contact-link" target="_blank">LinkedIn</a>
  </div>
</section>

<footer>
  <span>© 2026 Arghya Samanta</span>
  <span>Premium Video Editor · India</span>
</footer>

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
    ringX += (mouseX - ringX) * 0.12;
    ringY += (mouseY - ringY) * 0.12;
    ring.style.left = ringX + 'px';
    ring.style.top = ringY + 'px';
    requestAnimationFrame(animateRing);
  }
  animateRing();

  // Cursor hover effects
  document.querySelectorAll('a, button, .expertise-card').forEach(el => {
    el.addEventListener('mouseenter', () => {
      cursor.style.transform = 'translate(-50%, -50%) scale(2.5)';
      ring.style.transform = 'translate(-50%, -50%) scale(1.5)';
      ring.style.borderColor = 'rgba(74,158,255,0.7)';
    });
    el.addEventListener('mouseleave', () => {
      cursor.style.transform = 'translate(-50%, -50%) scale(1)';
      ring.style.transform = 'translate(-50%, -50%) scale(1)';
      ring.style.borderColor = 'rgba(74,158,255,0.4)';
    });
  });

  // Scroll animations
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => {
          entry.target.classList.add('visible');
        }, i * 80);
      }
    });
  }, { threshold: 0.1 });

  document.querySelectorAll('.stat-item, .expertise-card, .experience-block, .software-tag').forEach(el => {
    observer.observe(el);
  });
</script>
</body>
</html>