<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>Arghya Samanta — Video Editor</title>
<link href="https://fonts.googleapis.com/css2?family=Instrument+Sans:wght@400;500;600;700&family=Instrument+Serif:ital@0;1&display=swap" rel="stylesheet">
<style>
:root{--bg:#080a0f;--tx:#f0f4ff;--mu:#8a9bb8;--bl:#3b82f6;--bb:#60a5fa;--head:'Instrument Sans',system-ui,sans-serif;--body:'Instrument Serif',Georgia,serif;--disp:'Instrument Serif',Georgia,serif;box-sizing:border-box}
html{scroll-behavior:smooth;scroll-padding-top:env(safe-area-inset-top,0px)}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
body{background:var(--bg);color:var(--tx);font-family:var(--body);overflow-x:hidden}
body::before{content:'';position:fixed;inset:0;pointer-events:none;z-index:-1;background:radial-gradient(42% 36% at 18% 12%,rgba(37,70,220,.6),transparent 72%),radial-gradient(46% 40% at 88% 32%,rgba(70,110,255,.5),transparent 72%),radial-gradient(52% 44% at 52% 85%,rgba(20,40,170,.55),transparent 72%),#02030a}
body::after{content:'';position:fixed;inset:0;pointer-events:none;z-index:-1;opacity:.22;background-image:url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='220' height='220'><filter id='n'><feTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='2' stitchTiles='stitch'/><feColorMatrix values='0 0 0 0 1 0 0 0 0 1 0 0 0 0 1 0 0 0 1.6 -.3'/></filter><rect width='100%' height='100%' filter='url(%23n)'/></svg>")}
section{position:relative;z-index:1}
/* glass */
.glass{background:rgba(255,255,255,.05);-webkit-backdrop-filter:blur(10px);backdrop-filter:blur(10px);border:1px solid rgba(255,255,255,.12);box-shadow:inset 0 1px 0 rgba(255,255,255,.25),inset 0 -1px 0 rgba(255,255,255,.05),inset 0 0 18px rgba(255,255,255,.05),0 10px 40px rgba(0,0,0,.45)}
.btn{position:relative;isolation:isolate;display:inline-flex;align-items:center;gap:8px;font:600 14px var(--head);color:#fff;text-decoration:none;padding:15px 32px;border-radius:50px;border:0;cursor:pointer;background:rgba(255,255,255,.04);box-shadow:0 0 6px rgba(0,0,0,.1),0 2px 8px rgba(0,0,0,.3),inset 3px 3px .5px -3.5px rgba(255,255,255,.2),inset -3px -3px .5px -3.5px rgba(255,255,255,.85),inset 1px 1px 1px -.5px rgba(255,255,255,.6),inset -1px -1px 1px -.5px rgba(255,255,255,.6),inset 0 0 6px 6px rgba(255,255,255,.1),0 0 16px rgba(59,130,246,.25);transition:transform .3s}
.btn::before{content:'';position:absolute;inset:0;z-index:-1;border-radius:inherit;-webkit-backdrop-filter:blur(6px);backdrop-filter:blur(6px)}
.btn:hover{transform:scale(1.06)}
.btn.blue{background:rgba(59,130,246,.35)}
.tags .glass,.links .glass{-webkit-backdrop-filter:none;backdrop-filter:none}
nav{position:fixed;top:calc(16px + env(safe-area-inset-top,0px));left:50%;transform:translateX(-50%);z-index:100;display:flex;gap:2px;padding:6px;border-radius:50px}
nav a{font:600 11px var(--head);text-transform:uppercase;letter-spacing:.12em;color:var(--mu);text-decoration:none;padding:8px 16px;border-radius:50px;transition:.25s}
nav a.on{color:#fff;background:rgba(59,130,246,.22);box-shadow:0 0 16px rgba(59,130,246,.25)}
/* hero */
#home{min-height:100vh;display:flex;flex-direction:column;justify-content:center;align-items:center;text-align:center;padding:120px 24px 80px}
.badge{font:600 11px var(--head);letter-spacing:.15em;text-transform:uppercase;color:var(--bb);padding:8px 18px;border-radius:50px;margin-bottom:28px}
h1{font:400 clamp(66px,14vw,160px)/.88 var(--disp);letter-spacing:-.02em;margin-bottom:24px}
h1 span{display:block}
h1 span+span{font-style:italic;color:transparent;background:linear-gradient(135deg,#60a5fa,#93c5fd 40%,#3b82f6);-webkit-background-clip:text;background-clip:text;filter:drop-shadow(0 0 30px rgba(59,130,246,.55))}
.desc{font-size:19px;color:var(--mu);max-width:540px;line-height:1.7;margin-bottom:40px}
.stats{display:flex;border-radius:18px;margin-bottom:40px;overflow:hidden}
.stat{padding:18px 30px;text-align:center}
.stat+.stat{border-left:1px solid rgba(255,255,255,.08)}
.stat b{display:block;font:400 38px var(--disp);color:var(--bb);text-shadow:0 0 20px rgba(96,165,250,.6)}
.stat i{font:600 10px var(--head);letter-spacing:.12em;text-transform:uppercase;color:var(--mu);font-style:normal}
.row{display:flex;gap:12px;flex-wrap:wrap;justify-content:center}
/* about */
.wrap{max-width:1100px;margin:0 auto;padding:90px 24px}
.lab{display:inline-block;font:600 11px var(--head);letter-spacing:.15em;text-transform:uppercase;color:var(--bl);padding:6px 14px;border-radius:50px;margin-bottom:28px}
.about{display:grid;grid-template-columns:1fr 1fr;gap:56px;align-items:center}
.vid{aspect-ratio:16/9;border-radius:16px;overflow:hidden;background:#0e1118}
.vid+.vid{margin-top:16px}
.vid iframe{width:100%;height:100%;border:0}
h2{font:400 clamp(42px,6.5vw,76px)/1 var(--disp);letter-spacing:-.015em;margin-bottom:22px}
h2 em{font-style:italic;color:transparent;background:linear-gradient(135deg,#60a5fa,#3b82f6);-webkit-background-clip:text;background-clip:text}
.about p{font-size:17px;line-height:1.75;color:var(--mu);margin-bottom:18px}
.tags{display:flex;flex-wrap:wrap;gap:8px;margin-top:26px}
.tags span{font:500 12px var(--head);color:var(--mu);padding:6px 14px;border-radius:8px}
/* wheel */
#work .wrap{padding-bottom:30px}
.sub{font-size:17px;color:var(--mu);max-width:500px}
#stage{position:relative;height:88vh;min-height:520px;overflow:hidden;user-select:none;-webkit-user-select:none;cursor:grab;touch-action:pan-x;outline:none}
#stage:active{cursor:grabbing}
#wheel{position:absolute;top:50%;left:50%;transform-style:preserve-3d}
.card{position:absolute;will-change:transform;backface-visibility:hidden;-webkit-backface-visibility:hidden;cursor:pointer}
.face{position:relative;display:block;width:100%;height:100%;border-radius:12px;overflow:hidden;background:#0e1118;border:1px solid rgba(255,255,255,.14);box-shadow:0 10px 24px -14px rgba(59,130,246,.5)}
.face img{width:100%;height:100%;object-fit:cover;display:block;pointer-events:none}
.face .go{position:absolute;right:10px;bottom:10px;font:500 11px var(--head);padding:5px 12px;border-radius:50px;color:#fff}
.ov{pointer-events:none;position:absolute;inset:0}
.face .go{-webkit-backdrop-filter:none;backdrop-filter:none;background:rgba(10,14,30,.65)}
body::before,body::after{transform:translateZ(0)}
#wlabel,#wtitle{position:absolute;pointer-events:none;font-family:var(--disp);font-weight:400;letter-spacing:-.02em}
#wlabel{inset:0;display:grid;place-items:center;text-align:center;color:var(--tx)}
#wtitle{top:50%;left:6%;transform:translateY(-50%);opacity:0;max-width:22%}
#widx{position:absolute;top:6%;right:3%;list-style:none;text-align:right;font-family:var(--head);line-height:1.8;color:var(--mu)}
#widx button{all:unset;cursor:pointer;transition:color .2s}
#widx button.on{color:#fff;font-weight:600}
.hint{text-align:center;font:500 12px var(--head);color:var(--mu);letter-spacing:.1em;text-transform:uppercase;padding-bottom:20px}
@media(max-width:700px){.about{grid-template-columns:1fr}.stats{flex-direction:column}.stat+.stat{border-left:0;border-top:1px solid rgba(255,255,255,.08)}#wtitle{left:50%;top:auto;bottom:5%;transform:translateX(-50%);text-align:center;max-width:90%}#widx{display:none}nav a{padding:8px 11px}}
/* ending */
#end{position:relative;z-index:1;background:radial-gradient(ellipse 90% 40% at 50% 100%,rgba(200,215,255,.9) 0,rgba(70,110,255,.55) 35%,transparent 72%),radial-gradient(45% 30% at 15% 20%,rgba(37,70,220,.5),transparent 70%),#02030a}
#end::before{content:'';position:absolute;inset:0;pointer-events:none;opacity:.25;background-image:url("data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='220' height='220'><filter id='n'><feTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='2' stitchTiles='stitch'/><feColorMatrix values='0 0 0 0 1 0 0 0 0 1 0 0 0 0 1 0 0 0 1.6 -.3'/></filter><rect width='100%' height='100%' filter='url(%23n)'/></svg>")}
#reveal{height:230vh;position:relative}
#reveal .in{position:sticky;top:0;height:100vh;display:flex;align-items:center;justify-content:center;padding:24px}
#rt{font:400 clamp(40px,8vw,104px)/1.02 var(--disp);letter-spacing:-.02em;text-align:center;max-width:980px}
#rt span{opacity:.12;will-change:opacity}
.contact{position:relative;max-width:760px;margin:0 auto;padding:0 20px 110px}
.cc{border-radius:28px;padding:52px 32px;text-align:center}
.cc h2{margin-bottom:12px}
.cc p{font-size:18px;color:#c3cfe6;max-width:480px;margin:0 auto 34px}
.links{display:flex;gap:10px;flex-wrap:wrap;justify-content:center;margin-bottom:34px}
.links a{font:500 13px var(--head);color:#e8eeff;text-decoration:none;padding:11px 18px;border-radius:12px;transition:.25s}
.links a:hover{transform:translateY(-3px);color:#fff}
footer{position:relative;z-index:1;text-align:center;padding:22px;font:12px var(--head);color:#111;background:#fff;letter-spacing:.05em}
/* modal */
#modal{position:fixed;inset:0;z-index:1000;background:rgba(0,0,0,.85);-webkit-backdrop-filter:blur(16px);backdrop-filter:blur(16px);display:flex;align-items:center;justify-content:center;opacity:0;visibility:hidden;pointer-events:none;transition:opacity .3s,visibility .3s}
#modal.open{opacity:1;visibility:visible;pointer-events:all}
.mb{width:92vw;max-width:960px;border-radius:20px;overflow:hidden}
.mh{display:flex;justify-content:space-between;align-items:center;padding:14px 18px;font:600 15px var(--head);border-bottom:1px solid rgba(255,255,255,.1)}
.mh button{all:unset;cursor:pointer;width:32px;height:32px;text-align:center;border-radius:8px;background:rgba(255,255,255,.08)}
.mv{aspect-ratio:16/9;background:#000}.mv iframe{width:100%;height:100%;border:0}
</style>
</head>
<body>
<svg width="0" height="0" style="position:absolute"><defs><filter id="lg" x="0" y="0" width="100%" height="100%" color-interpolation-filters="sRGB"><feTurbulence type="fractalNoise" baseFrequency="0.05" numOctaves="1" seed="1" result="t"/><feGaussianBlur in="t" stdDeviation="2" result="b"/><feDisplacementMap in="SourceGraphic" in2="b" scale="70" xChannelSelector="R" yChannelSelector="B" result="d"/><feGaussianBlur in="d" stdDeviation="4"/></filter></defs></svg>

<nav class="glass"><a href="#home" class="on">Home</a><a href="#about">About</a><a href="#work">Work</a><a href="#end">Contact</a></nav>

<section id="home">
  <div class="badge glass">Premium Video Editor</div>
  <h1><span>Arghya</span><span>Samanta</span></h1>
  <p class="desc">High-end video editor with 2 years of hands-on agency experience — specializing in dynamic, high-retention content from cinematic real estate to viral medical reels.</p>
  <div class="stats glass"><div class="stat"><b>30+</b><i>Clients</i></div><div class="stat"><b>84.3K</b><i>Subscribers</i></div><div class="stat"><b>61.2M</b><i>Total Views</i></div></div>
  <div class="row"><a href="#work" class="btn blue">▶ View Work</a><a href="#end" class="btn">Get in Touch</a></div>
</section>

<section id="about"><div class="wrap">
  <span class="lab glass">About</span>
  <div class="about">
    <div><div class="vid glass"><iframe src="https://drive.google.com/file/d/1hTg2OXfRVEecAwfc-qntyRnXT5HIZ3m7/preview" allow="autoplay" loading="lazy" title="Arghya Samanta"></iframe></div><div class="vid glass"><iframe src="https://drive.google.com/file/d/12lZlO3zvHG5wTu0uUrsm9qH6eCMKPZpV/preview" allow="autoplay" loading="lazy" title="Intro Video"></iframe></div></div>
    <div>
      <h2>Crafting Stories<br><em>Frame by Frame</em></h2>
      <p>I’m a video editor with 2 years of hands-on agency experience, specializing in dynamic, high-retention content creation. My work spans cinematic real estate, medical education, viral social content, and long-form podcasts.</p>
      <p>I blend technical precision with creative pacing — motion graphics, color science, and storytelling instincts to produce content that doesn’t just look good, but performs.</p>
      <div class="tags"><span class="glass">Premiere Pro</span><span class="glass">Photoshop</span><span class="glass">CapCut PC</span><span class="glass">Topaz AI</span><span class="glass">After Motion</span><span class="glass">Alight Motion</span><span class="glass">Color Grading</span><span class="glass">Motion Graphics</span><span class="glass">Podcasts</span><span class="glass">Short-Form Reels</span></div>
    </div>
  </div>
</div></section>

<section id="work">
  <div class="wrap"><span class="lab glass">Portfolio</span><h2>Selected <em>Work</em></h2><p class="sub">Scroll, drag or use the index to turn the wheel. Tap the front card to play.</p></div>
  <div id="stage" tabindex="0" aria-label="Works wheel">
    <div id="wheel"></div>
    <div id="wlabel">Works ’26</div>
    <div id="wtitle"></div>
    <ol id="widx"></ol>
  </div>
  <div class="hint">↑ ↓ keys also work</div>
</section>

<div id="end">
  <section id="reveal"><div class="in"><p id="rt"></p></div></section>
  <section id="contact" class="contact">
    <div class="cc glass">
      <h2>Let’s Create<br><em>Something Great</em></h2>
      <p>Available for long-term collaborations, project-based work, and brand partnerships.</p>
      <div class="links">
        <a class="glass" href="mailto:apsediting120@gmail.com">apsediting120@gmail.com</a>
        <a class="glass" href="tel:+917318805018">+91 73188 05018</a>
        <a class="glass" href="https://framefolio.in/apsvisuallab" target="_blank" rel="noopener">Portfolio</a>
        <a class="glass" href="https://youtube.com/@aps_editor_1m" target="_blank" rel="noopener">YouTube</a>
        <a class="glass" href="https://linkedin.com/in/aps-editor-37212640a" target="_blank" rel="noopener">LinkedIn</a>
      </div>
      <a class="btn blue" href="mailto:apsediting120@gmail.com">Send Message →</a>
    </div>
  </section>
</div>
<footer>© 2026 Arghya Samanta · Video Editor · India</footer>

<div id="modal"><div class="mb glass"><div class="mh"><span id="mt">Video</span><button id="mx">✕</button></div><div class="mv"><iframe id="mf" allow="autoplay; fullscreen" title="Video"></iframe></div></div></div>

<script>
const W=[["Podcast Reel Edit","1XfwntyIalFjDB-9f6VRitjPIn6zOPkfZ"],["Edit 01","1rG0MwZm6ZSvZgmFLF8KavUqFzL5N68R7"],["Edit 02","1ht9m2GOuS4zPuluuQQZ2fj7UfrQrtM0m"],["Edit 03","1NPCJ2ABPDlioOmtDX8a7Pj_wpp6v5sLr"]];
const $=s=>document.querySelector(s),cl=(v,a,b)=>Math.min(b,Math.max(a,v)),rad=d=>d*Math.PI/180;
const stage=$('#stage'),wheel=$('#wheel'),lab=$('#wlabel'),ttl=$('#wtitle'),ix=$('#widx');
const n=W.length,last=n-1,src=id=>`https://drive.google.com/file/d/${id}/preview`;
wheel.innerHTML=W.map((w,i)=>`<div class="card" data-i="${i}"><span class="face"><img src="https://drive.google.com/thumbnail?id=${w[1]}&sz=w800" alt="${w[0]}" decoding="async" draggable="false"><span class="ov"></span><span class="go glass">▶ Play</span></span></div>`).join('');
ix.innerHTML=W.map((w,i)=>`<li><button data-i="${i}">${w[0]}</button></li>`).join('');
const cards=[...wheel.children],btns=[...ix.querySelectorAll('button')];
const STEP=40,DRUM=2.22,LENS=2.7,RING=1.14,BOW=1.82,CULL=1.6,EASE=.12,RATIO=1.78;
let turn=0,target=0,active=0,M={},settle,drag=null,moved=0;
const reduced=matchMedia('(prefers-reduced-motion: reduce)').matches;
function size(){const w=stage.clientWidth,h=stage.clientHeight;
  const cw=Math.min(h*.38*RATIO,w*(w<700?.64:.34)),ch=cw/RATIO;
  M={cw,ch,drumR:ch*DRUM,ringR:ch*RING,bow:ch*BOW,rs:cl((2*Math.PI*ch*RING/n)*.82/cw,.16,1),fs:ch*.124};
  stage.style.perspective=ch*LENS+'px';
  cards.forEach(c=>{c.style.cssText+=`;width:${cw}px;height:${ch}px;margin-left:${-cw/2}px;margin-top:${-ch/2}px`});
  lab.style.fontSize=ttl.style.fontSize=M.fs+'px';ix.style.fontSize=ch*.04+'px';}
new ResizeObserver(()=>{size();kick()}).observe(stage);size();
const to=v=>{target=cl(v,0,last+1);kick()};
let raf=0;const kick=()=>{if(!raf)raf=requestAnimationFrame(draw)};
let lt=0;
function draw(ts){raf=0;const dt=lt?Math.min((ts-lt)/16.667,3):1;lt=ts;
  const gap=target-turn;if(Math.abs(gap)<.0005)turn=target;else turn+=gap*(reduced?1:1-Math.pow(1-EASE,dt));
  const m=cl(turn,0,1),pos=Math.max(0,turn-1);
  wheel.style.transform=`translateZ(${-m*M.drumR}px)`;
  cards.forEach((c,i)=>{const d=i-pos,dd=d*STEP;
    c.style.transform=`translateX(${-m*M.bow*(1-Math.cos(rad(dd)))}px) rotateZ(${(1-m)*d*(360/n)}deg) translateY(${-(1-m)*M.ringR}px) rotateX(${m*dd}deg) translateZ(${m*M.drumR}px)`;
    c.style.opacity=m>.5&&Math.abs(d)>CULL?0:1;c.style.zIndex=Math.round(100-Math.abs(d)*2);
    c.firstElementChild.style.transform=`scale(${M.rs+(1-M.rs)*m})`;});
  lab.style.opacity=1-m;ttl.style.opacity=m;
  const near=cl(Math.round(pos),0,last);
  if(near!==active){active=near;ttl.textContent=W[active][0];btns.forEach((b,i)=>b.classList.toggle('on',i===active));}
  if(turn!==target)kick();else lt=0;}
ttl.textContent=W[0][0];btns[0].classList.add('on');kick();
stage.addEventListener('wheel',e=>{const nx=target+e.deltaY/900;if(nx>0&&nx<last+1)e.preventDefault();to(nx);
  clearTimeout(settle);settle=setTimeout(()=>to(Math.round(target)),140);},{passive:false});
stage.addEventListener('pointerdown',e=>{drag=e.clientY;moved=0});
addEventListener('pointermove',e=>{if(drag===null)return;moved+=Math.abs(drag-e.clientY);to(target+(drag-e.clientY)/420);drag=e.clientY});
addEventListener('pointerup',()=>{if(drag===null)return;drag=null;if(target>1)to(Math.round(target))});
stage.addEventListener('keydown',e=>{if(e.key==='ArrowDown')to(Math.round(target)+1);else if(e.key==='ArrowUp')to(Math.round(target)-1);else return;e.preventDefault()});
stage.addEventListener('click',e=>{if(moved>8)return;const c=e.target.closest('.card'),b=e.target.closest('#widx button');
  if(b)return to(+b.dataset.i+1);
  if(c){const i=+c.dataset.i;if(i===active&&turn>.9)openM(W[i]);else to(i+1);}});
/* modal */
function openM(w){$('#mf').src=src(w[1]);$('#mt').textContent=w[0];$('#modal').classList.add('open')}
function closeM(){$('#modal').classList.remove('open');$('#mf').src=''}
$('#mx').onclick=closeM;$('#modal').onclick=e=>{if(e.target.id==='modal')closeM()};addEventListener('keydown',e=>{if(e.key==='Escape')closeM()});
/* text reveal */
const words="Great work isn’t made alone. Let’s build something people can’t stop watching.".split(' ');
$('#rt').innerHTML=words.map(w=>`<span>${w}</span>`).join(' ');
const ws=[...document.querySelectorAll('#rt span')],rv=$('#reveal');
let lp=-1;function rev(){const r=rv.getBoundingClientRect(),p=cl(-r.top/(r.height-innerHeight),0,1);if(p===lp)return;lp=p;
  ws.forEach((s,i)=>{const st=i/ws.length*.85;s.style.opacity=.12+.88*cl((p-st)/.12,0,1)});}
let tk=0;addEventListener('scroll',()=>{if(!tk)tk=requestAnimationFrame(()=>{tk=0;nv();rev()})},{passive:true});rev();
/* nav */
const secs=['home','about','work','end'].map(id=>document.getElementById(id)),links=[...document.querySelectorAll('nav a')];let cur='';
function nv(){let c='home';secs.forEach(s=>{if(scrollY>=s.offsetTop-200)c=s.id});if(c===cur)return;cur=c;links.forEach(a=>a.classList.toggle('on',a.getAttribute('href')==='#'+c))}
</script>
</body>
</html>
