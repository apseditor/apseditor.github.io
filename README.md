<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>APS Editor — Premium Video Editor</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@300;400;500;600&family=DM+Mono:wght@300;400&display=swap" rel="stylesheet">
<style>
  :root {
    --white: #f0eeea;
    --gray-light: #888;
    --gray-mid: #444;
    --black: #0a0a0a;
    --glow-blue: #4a9eff;
  }
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body {
    background: var(--black);
    color: var(--white);
    font-family: "DM Mono", monospace;
    font-weight: 300;
    overflow-x: hidden;
    cursor: none;
  }
  .cursor {
    position: fixed; width: 8px; height: 8px;
    background: var(--glow-blue); border-radius: 50%;
    pointer-events: none; z-index: 9999;
    transform: translate(-50%, -50%);
    box-shadow: 0 0 12px var(--glow-blue), 0 0 24px var(--glow-blue);
    transition: transform 0.1s ease;
  }
  .cursor-ring {
    position: fixed; width: 32px; height: 32px;
    border: 1px solid rgba(74,158,255,0.4); border-radius: 50%;
    pointer-events: none; z-index: 9998;
    transform: translate(-50%, -50%); transition: all 0.18s ease;
  }
  body::before {
    content: ""; position: fixed; inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.04'/%3E%3C/svg%3E");
    pointer-events: none; z-index: 1000; opacity: 0.4;
  }
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 500;
    display: flex; justify-content: space-between; align-items: center;
    padding: 28px 60px;
    border-bottom: 1px solid rgba(255,255,255,0.04);
    backdrop-filter: blur(12px); background: rgba(10,10,10,0.8);
  }
  .nav-logo {
    font-family: "Cormorant Garamond", serif; font-size: 1rem;
    font-weight: 500; letter-spacing: 0.15em; color: var(--white); text-decoration: none;
  }
  .nav-links { display: flex; gap: 40px; list-style: none; }
  .nav-links a {
    color: var(--gray-light); text-decoration: none; font-size: 0.6rem;
    letter-spacing: 0.2em; text-transform: uppercase; transition: color 0.3s; cursor: none;
  }
  .nav-links a:hover { color: var(--white); }

  /* HERO */
  .hero {
    min-height: 100vh; display: flex; align-items: center;
    padding: 140px 60px 80px; position: relative; overflow: hidden;
  }
  .hero-bg {
    position: absolute; inset: 0;
    background: radial-gradient(ellipse 60% 50% at 70% 50%, rgba(74,158,255,0.05) 0%, transparent 70%),
                radial-gradient(ellipse 40% 60% at 20% 80%, rgba(74,158,255,0.03) 0%, transparent 60%);
  }
  .hero-grid {
    position: absolute; inset: 0;
    background-image: linear-gradient(rgba(255,255,255,0.018) 1px, transparent 1px),
                      linear-gradient(90deg, rgba(255,255,255,0.018) 1px, transparent 1px);
    background-size: 80px 80px;
    mask-image: radial-gradient(ellipse 80% 80% at 50% 50%, black 0%, transparent 100%);
  }
  .hero-content { position: relative; z-index: 2; max-width: 900px; }
  .hero-tag {
    display: inline-block; font-size: 0.58rem; letter-spacing: 0.3em;
    text-transform: uppercase; color: var(--glow-blue);
    border: 1px solid rgba(74,158,255,0.3); padding: 6px 16px; margin-bottom: 40px;
    opacity: 0; animation: fadeUp 0.8s ease 0.2s forwards;
  }
  h1 {
    font-family: "Cormorant Garamond", serif;
    font-size: clamp(4rem, 10vw, 9rem); font-weight: 300;
    line-height: 0.92; letter-spacing: -0.02em; margin-bottom: 40px;
    opacity: 0; animation: fadeUp 0.8s ease 0.4s forwards;
  }
  .glow-name { display: block; color: var(--white); text-shadow: 0 0 60px rgba(74,158,255,0.25); }
  .thin-line { display: block; color: var(--gray-mid); font-weight: 300; font-style: italic; }
  .hero-desc {
    max-width: 460px;