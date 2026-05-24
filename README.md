<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Arghya Samanta</title>

<link rel="preconnect" href="https://fonts.googleapis.com">

<link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700;800&family=Space+Grotesk:wght@400;500;700&display=swap" rel="stylesheet">

<style>

*{
margin:0;
padding:0;
box-sizing:border-box;
scroll-behavior:smooth;
}

body{
background:#020202;
color:white;
font-family:'Outfit',sans-serif;
overflow-x:hidden;
}

/* GRID */

body::before{

content:'';

position:fixed;

inset:0;

background:
linear-gradient(rgba(255,255,255,0.03) 1px, transparent 1px),
linear-gradient(90deg, rgba(255,255,255,0.03) 1px, transparent 1px);

background-size:45px 45px;

z-index:-5;

}

/* BLUE GLOW */

.glow1{

position:fixed;

width:600px;
height:600px;

background:
radial-gradient(circle,#2563ff44 0%,transparent 70%);

top:-200px;
right:-100px;

filter:blur(120px);

z-index:-3;

}

.glow2{

position:fixed;

width:500px;
height:500px;

background:
radial-gradient(circle,#2563ff22 0%,transparent 70%);

bottom:-150px;
left:-100px;

filter:blur(120px);

z-index:-3;

}

section{
padding:120px 10%;
}

/* HERO */

.hero{

min-height:100vh;

display:flex;

align-items:center;

}

.hero-content{

max-width:800px;

}

.tag{

display:inline-block;

padding:12px 24px;

border:1px solid #2563ff;

border-radius:50px;

color:#76a8ff;

font-size:12px;

letter-spacing:4px;

margin-bottom:40px;

box-shadow:
0 0 25px #2563ff55;

}

.hero h1{

font-size:120px;

line-height:0.85;

font-family:'Space Grotesk',sans-serif;

font-weight:700;

letter-spacing:-7px;

}

.hero h1 span{

display:block;

color:#ffffff10;

font-style:italic;

}

.hero p{

margin-top:35px;

font-size:19px;

line-height:1.9;

color:#9f9f9f;

max-width:650px;

}

.buttons{

display:flex;

gap:20px;

margin-top:50px;

flex-wrap:wrap;

}

.btn{

padding:18px 34px;

border-radius:16px;

text-decoration:none;

color:#80adff;

border:1px solid #2563ff;

transition:0.4s;

background:#0a1220aa;

backdrop-filter:blur(20px);

box-shadow:
0 0 25px #2563ff22;

}

.btn:hover{

transform:translateY(-5px);

background:#2563ff;

color:white;

box-shadow:
0 0 40px #2563ff99;

}

.secondary{

border:1px solid #2b2b2b;

color:#aaa;

}

/* ABOUT */

.about{

display:grid;

grid-template-columns:1fr 1fr;

gap:70px;

align-items:center;

}

.about-image{

position:relative;

}

.about-image img{

width:100%;

aspect-ratio:16/9;

object-fit:cover;

border-radius:28px;

border:1px solid #1c1c1c;

box-shadow:
0 0 50px #2563ff22;

}

.about-image::after{

content:'';

position:absolute;

inset:0;

border-radius:28px;

background:
linear-gradient(to top,
rgba(0,0,0,0.6),
transparent);

}

.section-title{

font-size:68px;

font-family:'Space Grotesk',sans-serif;

margin-bottom:25px;

line-height:1;

}

.about p{

color:#9d9d9d;

line-height:1.9;

font-size:17px;

margin-bottom:25px;

}

.stats{

display:flex;

gap:40px;

flex-wrap:wrap;

margin-top:35px;

}

.stat h3{

font-size:42px;

color:#6ea3ff;

margin-bottom:8px;

}

.stat span{

color:#777;

font-size:14px;

}

/* PORTFOLIO */

.portfolio-grid{

display:grid;

grid-template-columns:repeat(auto-fit,minmax(320px,1fr));

gap:30px;

margin-top:60px;

}

.card{

background:#0a0a0a;

border:1px solid #1c1c1c;

border-radius:25px;

overflow:hidden;

transition:0.5s;

}

.card:hover{

transform:translateY(-8px);

border-color:#2563ff;

box-shadow:
0 0 50px #2563ff22;

}

.card img{

width:100%;

height:230px;

object-fit:cover;

}

.card-content{

padding:25px;

}

.card-content h3{

font-size:28px;

margin-bottom:12px;

}

.card-content p{

color:#8f8f8f;

line-height:1.8;

}

/* CONTACT */

.contact{

text-align:center;

}

.contact p{

max-width:700px;

margin:20px auto 40px;

color:#999;

line-height:1.9;

}

/* FOOTER */

footer{

padding:30px;

text-align:center;

color:#666;

border-top:1px solid #111;

}

/* RESPONSIVE */

@media(max-width:1000px){

.hero h1{

font-size:90px;

}

.about{

grid-template-columns:1fr;

}

.section-title{

font-size:52px;

}

}

@media(max-width:768px){

section{

padding:90px 7%;

}

.hero h1{

font-size:58px;

letter-spacing:-3px;

}

.section-title{

font-size:42px;

}

.hero p{

font-size:16px;

}

.buttons{

flex-direction:column;

}

.btn{

width:100%;

text-align:center;

}

}

</style>

</head>

<body>

<div class="glow1"></div>
<div class="glow2"></div>

<!-- AUDIO -->

<audio id="tap">
<source src="tap.mp3" type="audio/mp3">
</audio>

<audio id="scroll">
<source src="scroll.mp3" type="audio/mp3">
</audio>

<!-- HERO -->

<section class="hero">

<div class="hero-content">

<div class="tag">
AVAILABLE FOR COLLABORATIONS
</div>

<h1>
Arghya
Samanta
<span>Video Editor</span>
</h1>

<p>
Premium freelance video editor specializing in cinematic storytelling,
viral reels, motion graphics and luxury visual editing aesthetics.
</p>

<div class="buttons">

<a href="#portfolio" class="btn sound">
VIEW PORTFOLIO
</a>

<a href="#contact" class="btn secondary sound">
GET IN TOUCH
</a>

</div>

</div>

</section>

<!-- ABOUT -->

<section class="about">

<div class="about-image">

<!-- IMPORTANT -->
<!-- RENAME YOUR IMAGE EXACTLY -->

<img src="your-image.jpg" alt="Arghya Samanta">

</div>

<div>

<h2 class="section-title">
About Me
</h2>

<p>
High-end freelance video editor & visual specialist with 4 years of experience creating cinematic edits, viral reels, premium business content and engaging social media visuals.
</p>

<p>
Specialized in modern storytelling, transitions, color grading, sound design and high-retention editing systems.
</p>

<div class="stats">

<div class="stat">
<h3>4+</h3>
<span>Years Experience</span>
</div>

<div class="stat">
<h3>30+</h3>
<span>Clients Worked</span>
</div>

<div class="stat">
<h3>58M+</h3>
<span>Total Views</span>
</div>

</div>

</div>

</section>

<!-- PORTFOLIO -->

<section id="portfolio">

<h2 class="section-title">
Featured Work
</h2>

<div class="portfolio-grid">

<div class="card">

<img src="your-image.jpg">

<div class="card-content">

<h3>Cinematic Edit</h3>

<p>
High-retention cinematic editing with smooth transitions and luxury color grading.
</p>

</div>

</div>

<div class="card">

<img src="your-image.jpg">

<div class="card-content">

<h3>Social Media Reel</h3>

<p>
Modern premium reel editing optimized for engagement and audience retention.
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
Open for freelance collaborations, creator projects and premium editing work worldwide.
</p>

<div class="buttons" style="justify-content:center;">

<a href="https://instagram.com/" class="btn sound">
INSTAGRAM
</a>

<a href="mailto:yourmail@gmail.com" class="btn secondary sound">
EMAIL ME
</a>

</div>

</section>

<footer>

© 2026 Arghya Samanta — Premium Video Editor

</footer>

<script>

/* TAP SOUND */

const tap=document.getElementById('tap');

document.querySelectorAll('.sound').forEach(button=>{

button.addEventListener('click',()=>{

tap.volume=0.3;

tap.currentTime=0;

tap.play();

});

});

/* SCROLL SOUND */

const scroll=document.getElementById('scroll');

let isScrolling=false;

window.addEventListener('scroll',()=>{

if(!isScrolling){

scroll.volume=0.08;

scroll.currentTime=0;

scroll.play();

isScrolling=true;

setTimeout(()=>{

isScrolling=false;

},300);

}

});

/* FADE EFFECT */

const sections=document.querySelectorAll('section');

const observer=new IntersectionObserver(entries=>{

entries.forEach(entry=>{

if(entry.isIntersecting){

entry.target.style.opacity=1;

entry.target.style.transform='translateY(0px)';

}

});

});

sections.forEach(section=>{

section.style.opacity=0;

section.style.transform='translateY(60px)';

section.style.transition='1s ease';

observer.observe(section);

});

</script>

</body>

</html>