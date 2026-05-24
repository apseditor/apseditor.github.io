<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Arghya Samanta | Video Editor</title>

  <!-- Fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;600&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">

  <style>

    *{
      margin:0;
      padding:0;
      box-sizing:border-box;
      scroll-behavior:smooth;
    }

    body{
      font-family:'Inter',sans-serif;
      background:#050505;
      color:#fff;
      overflow-x:hidden;
    }

    /* GRID BACKGROUND */

    body::before{
      content:'';
      position:fixed;
      inset:0;
      background:
      linear-gradient(rgba(255,255,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255,255,255,0.03) 1px, transparent 1px);
      background-size:50px 50px;
      z-index:-2;
    }

    body::after{
      content:'';
      position:fixed;
      width:600px;
      height:600px;
      background:radial-gradient(circle,#2563ff55 0%,transparent 70%);
      top:-200px;
      right:-150px;
      z-index:-1;
      filter:blur(40px);
    }

    section{
      padding:100px 10%;
    }

    h1,h2{
      font-family:'Cormorant Garamond',serif;
    }

    /* HERO */

    .hero{
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      position:relative;
    }

    .hero-content{
      max-width:700px;
    }

    .tag{
      border:1px solid #2563ff;
      display:inline-block;
      padding:10px 20px;
      color:#6ea3ff;
      letter-spacing:4px;
      margin-bottom:40px;
      font-size:13px;
      text-transform:uppercase;
      box-shadow:0 0 20px #2563ff33;
    }

    .hero h1{
      font-size:90px;
      line-height:0.9;
      font-weight:600;
    }

    .hero h1 span{
      color:#ffffff18;
      display:block;
      font-style:italic;
    }

    .hero p{
      margin-top:40px;
      max-width:600px;
      color:#8f8f8f;
      line-height:1.9;
      font-size:17px;
    }

    .buttons{
      margin-top:50px;
      display:flex;
      gap:20px;
      flex-wrap:wrap;
    }

    .btn{
      padding:18px 35px;
      border:1px solid #2563ff;
      background:transparent;
      color:#6ea3ff;
      text-decoration:none;
      transition:0.4s;
      letter-spacing:2px;
    }

    .btn:hover{
      background:#2563ff;
      color:#fff;
      box-shadow:0 0 30px #2563ff88;
      transform:translateY(-3px);
    }

    .btn.secondary{
      border:1px solid #333;
      color:#aaa;
    }

    /* ABOUT */

    .about{
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:60px;
      align-items:center;
    }

    .about img{
      width:100%;
      border-radius:20px;
      box-shadow:0 0 40px #2563ff22;
    }

    .section-title{
      font-size:60px;
      margin-bottom:20px;
    }

    .about p{
      color:#a1a1a1;
      line-height:1.9;
      margin-bottom:30px;
    }

    .stats{
      display:flex;
      gap:40px;
      flex-wrap:wrap;
    }

    .stat h3{
      color:#6ea3ff;
      font-size:32px;
      margin-bottom:5px;
    }

    .stat span{
      color:#777;
      font-size:14px;
      letter-spacing:1px;
    }

    /* SKILLS */

    .skills-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
      gap:25px;
      margin-top:50px;
    }

    .skill-card{
      background:#0c0c0c;
      border:1px solid #1c1c1c;
      padding:30px;
      border-radius:20px;
      transition:0.4s;
    }

    .skill-card:hover{
      transform:translateY(-5px);
      border-color:#2563ff;
      box-shadow:0 0 30px #2563ff22;
    }

    .skill-card h3{
      margin-bottom:10px;
    }

    .skill-card p{
      color:#888;
      line-height:1.7;
    }

    /* PORTFOLIO */

    .portfolio-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
      gap:30px;
      margin-top:50px;
    }

    .video-card{
      background:#0b0b0b;
      border-radius:20px;
      overflow:hidden;
      border:1px solid #1a1a1a;
      transition:0.4s;
    }

    .video-card:hover{
      transform:translateY(-6px);
      box-shadow:0 0 35px #2563ff22;
    }

    .video-card iframe{
      width:100%;
      height:250px;
      border:none;
    }

    .video-info{
      padding:25px;
    }

    .video-info h3{
      margin-bottom:10px;
    }

    .video-info p{
      color:#8b8b8b;
      line-height:1.7;
    }

    /* CONTACT */

    .contact{
      text-align:center;
    }

    .contact p{
      color:#9b9b9b;
      margin:20px auto 40px;
      max-width:600px;
      line-height:1.8;
    }

    footer{
      padding:30px;
      text-align:center;
      color:#666;
      border-top:1px solid #111;
    }

    /* RESPONSIVE */

    @media(max-width:900px){

      .hero h1{
        font-size:60px;
      }

      .about{
        grid-template-columns:1fr;
      }

      .section-title{
        font-size:45px;
      }

    }

  </style>
</head>

<body>

  <!-- SOUND EFFECTS -->
  <audio id="tapSound" src="tap.mp3"></audio>

  <!-- HERO -->

  <section class="hero">

    <div class="hero-content">

      <div class="tag">
        Available For Collaborations
      </div>

      <h1>
        Arghya<br>
        Samanta
        <span>Video Editor</span>
      </h1>

      <p>
        Premium freelance video editor with 4 years of agency experience.
        Specializing in cinematic edits, high-retention content,
        reels, motion graphics, podcasts and viral short-form storytelling.
      </p>

      <div class="buttons">
        <a href="#portfolio" class="btn sound-btn">
          VIEW PORTFOLIO
        </a>

        <a href="#contact" class="btn secondary sound-btn">
          GET IN TOUCH
        </a>
      </div>

    </div>

  </section>

  <!-- ABOUT -->

  <section class="about">

    <img src="your-image.jpg" alt="Arghya Samanta">

    <div>

      <h2 class="section-title">
        About Me
      </h2>

      <p>
        High-end freelance video editor & visual specialist
        focused on cinematic storytelling, modern motion design,
        and high-retention editing styles.
      </p>

      <p>
        Worked with multiple agencies and creators,
        helping brands achieve premium visuals and stronger audience engagement.
      </p>

      <div class="stats">

        <div class="stat">
          <h3>4+</h3>
          <span>Years Experience</span>
        </div>

        <div class="stat">
          <h3>30+</h3>
          <span>Happy Clients</span>
        </div>

        <div class="stat">
          <h3>58M+</h3>
          <span>Total Views</span>
        </div>

      </div>

    </div>

  </section>

  <!-- SKILLS -->

  <section>

    <h2 class="section-title">
      Software & Expertise
    </h2>

    <div class="skills-grid">

      <div class="skill-card">
        <h3>Adobe Premiere Pro</h3>
        <p>Cinematic editing, transitions, pacing & storytelling.</p>
      </div>

      <div class="skill-card">
        <h3>After Effects</h3>
        <p>Motion graphics, VFX and modern animations.</p>
      </div>

      <div class="skill-card">
        <h3>Photoshop</h3>
        <p>Thumbnail design, manipulation and branding visuals.</p>
      </div>

      <div class="skill-card">
        <h3>Topaz AI</h3>
        <p>Upscaling, sharpening and premium enhancement workflow.</p>
      </div>

    </div>

  </section>

  <!-- PORTFOLIO -->

  <section id="portfolio">

    <h2 class="section-title">
      Featured Work
    </h2>

    <div class="portfolio-grid">

      <div class="video-card">

        <iframe
        src="https://drive.google.com/file/d/YOUR_VIDEO_ID/preview"
        allow="autoplay">
        </iframe>

        <div class="video-info">
          <h3>Cinematic Reel</h3>
          <p>
            High-retention editing with cinematic transitions and sound design.
          </p>
        </div>

      </div>

      <div class="video-card">

        <iframe
        src="https://drive.google.com/file/d/YOUR_VIDEO_ID/preview"
        allow="autoplay">
        </iframe>

        <div class="video-info">
          <h3>Podcast Edit</h3>
          <p>
            Professional podcast editing with smooth pacing and motion graphics.
          </p>
        </div>

      </div>

    </div>

  </section>

  <!-- CONTACT -->

  <section class="contact" id="contact">

    <h2 class="section-title">
      Let's Work Together
    </h2>

    <p>
      Open for freelance collaborations, agency work,
      commercial projects and long-term partnerships.
    </p>

    <div class="buttons" style="justify-content:center;">

      <a href="mailto:yourmail@gmail.com" class="btn sound-btn">
        EMAIL ME
      </a>

      <a href="https://instagram.com/" class="btn secondary sound-btn">
        INSTAGRAM
      </a>

    </div>

  </section>

  <footer>
    © 2026 Arghya Samanta — Premium Video Editor
  </footer>

  <script>

    // BUTTON SOUND

    const tap = document.getElementById('tapSound');

    document.querySelectorAll('.sound-btn').forEach(btn => {
      btn.addEventListener('click', () => {
        tap.currentTime = 0;
        tap.play();
      });
    });

    // SCROLL FADE ANIMATION

    const sections = document.querySelectorAll('section');

    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if(entry.isIntersecting){
          entry.target.style.opacity = 1;
          entry.target.style.transform = 'translateY(0)';
        }
      });
    });

    sections.forEach(section => {
      section.style.opacity = 0;
      section.style.transform = 'translateY(50px)';
      section.style.transition = '1s ease';
      observer.observe(section);
    });

  </script>

</body>
</html>