# netzeroninja.github.io
GetOut Rewards site
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GetOut Rewards — The Financial Backbone of Adventure</title>
<meta name="description" content="Turn everyday spending into fuel for the lifestyle you love. GetOut Rewards is the first financial platform built by outdoor people, for outdoor people.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Source+Sans+3:ital,wght@0,300;0,400;0,600;0,700;0,900&family=Playfair+Display:ital,wght@0,700;0,800;0,900;1,700&display=swap" rel="stylesheet">
<style>
*, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

:root {
  --deep-olive: #36362B;
  --charcoal: #4A4A4A;
  --bronze: #8B7355;
  --sage: #5C7A3D;
  --cream: #F5F1EB;
  --warm-white: #FAF8F5;
  --dark-bg: #1A1A15;
  --gold-accent: #C4A265;
  --forest-dark: #2A2E1F;
}

html { scroll-behavior: smooth; }

body {
  font-family: 'Source Sans 3', 'Helvetica Neue', Arial, sans-serif;
  color: var(--charcoal);
  background: var(--warm-white);
  overflow-x: hidden;
  -webkit-font-smoothing: antialiased;
}

nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 1000;
  padding: 0 2rem; height: 72px;
  display: flex; align-items: center; justify-content: space-between;
  transition: background 0.4s, box-shadow 0.4s, backdrop-filter 0.4s;
}
nav.scrolled {
  background: rgba(26, 26, 21, 0.92);
  backdrop-filter: blur(20px);
  box-shadow: 0 2px 40px rgba(0,0,0,0.15);
}
.nav-logo {
  font-family: 'Source Sans 3', sans-serif; font-weight: 900;
  font-size: 1.5rem; letter-spacing: 3px; color: var(--cream);
  text-decoration: none; text-transform: uppercase;
}
.nav-logo span { color: var(--gold-accent); }
.nav-links {
  display: flex; gap: 2rem; list-style: none; align-items: center;
}
.nav-links a {
  color: var(--cream); text-decoration: none; font-weight: 600;
  font-size: 0.85rem; letter-spacing: 1.5px; text-transform: uppercase;
  opacity: 0.85; transition: opacity 0.3s;
}
.nav-links a:hover { opacity: 1; }
.nav-cta {
  background: var(--bronze) !important; color: var(--cream) !important;
  padding: 10px 24px !important; border-radius: 4px;
  opacity: 1 !important; transition: background 0.3s !important;
}
.nav-cta:hover { background: var(--gold-accent) !important; }
.mobile-toggle {
  display: none; background: none; border: none; cursor: pointer; padding: 8px;
}
.mobile-toggle span {
  display: block; width: 24px; height: 2px; background: var(--cream); margin: 5px 0; transition: 0.3s;
}

/* HERO */
.hero {
  position: relative; min-height: 100vh;
  display: flex; align-items: center; justify-content: center;
  background: var(--dark-bg); overflow: hidden;
}
.hero-bg {
  position: absolute; inset: 0;
  background: linear-gradient(135deg, rgba(26,26,21,0.95) 0%, rgba(42,46,31,0.7) 40%, rgba(92,122,61,0.3) 100%);
  z-index: 1;
}
.hero-texture {
  position: absolute; inset: 0; opacity: 0.08; z-index: 1;
  background-image:
    radial-gradient(circle at 20% 80%, var(--sage) 0%, transparent 50%),
    radial-gradient(circle at 80% 20%, var(--bronze) 0%, transparent 50%),
    radial-gradient(circle at 60% 60%, var(--gold-accent) 0%, transparent 40%);
}
.topo-lines {
  position: absolute; inset: 0; z-index: 1; opacity: 0.04;
  background-size: 400px 400px;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400' viewBox='0 0 400 400'%3E%3Cpath d='M0 200 Q100 150 200 200 Q300 250 400 200' fill='none' stroke='%23C4A265' stroke-width='1'/%3E%3Cpath d='M0 220 Q100 170 200 220 Q300 270 400 220' fill='none' stroke='%23C4A265' stroke-width='1'/%3E%3Cpath d='M0 240 Q100 190 200 240 Q300 290 400 240' fill='none' stroke='%23C4A265' stroke-width='1'/%3E%3Cpath d='M0 100 Q150 50 250 100 Q350 150 400 100' fill='none' stroke='%23C4A265' stroke-width='1'/%3E%3Cpath d='M0 120 Q150 70 250 120 Q350 170 400 120' fill='none' stroke='%23C4A265' stroke-width='1'/%3E%3Cpath d='M0 300 Q80 260 200 300 Q320 340 400 300' fill='none' stroke='%23C4A265' stroke-width='1'/%3E%3Cpath d='M0 320 Q80 280 200 320 Q320 360 400 320' fill='none' stroke='%23C4A265' stroke-width='1'/%3E%3C/svg%3E");
}
.hero-content {
  position: relative; z-index: 2; text-align: center;
  max-width: 860px; padding: 2rem;
  animation: fadeUp 1.2s ease-out;
}
@keyframes fadeUp {
  from { opacity: 0; transform: translateY(40px); }
  to { opacity: 1; transform: translateY(0); }
}
.hero-badge {
  display: inline-block; border: 1px solid var(--gold-accent);
  color: var(--gold-accent); font-size: 0.7rem; font-weight: 700;
  letter-spacing: 3px; text-transform: uppercase;
  padding: 8px 24px; margin-bottom: 2rem;
  animation: fadeUp 1.2s ease-out 0.2s both;
}
.hero h1 {
  font-family: 'Playfair Display', serif; font-weight: 900;
  font-size: clamp(2.8rem, 7vw, 5.5rem); color: var(--cream);
  line-height: 1.05; margin-bottom: 1.5rem;
  animation: fadeUp 1.2s ease-out 0.4s both;
}
.hero h1 em { font-style: italic; color: var(--gold-accent); }
.hero-sub {
  font-size: clamp(1rem, 2vw, 1.25rem); color: rgba(245,241,235,0.75);
  line-height: 1.7; max-width: 620px; margin: 0 auto 2.5rem; font-weight: 300;
  animation: fadeUp 1.2s ease-out 0.6s both;
}
.hero-actions {
  display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap;
  animation: fadeUp 1.2s ease-out 0.8s both;
}
.btn-primary {
  background: var(--bronze); color: var(--cream); padding: 16px 40px;
  font-size: 0.85rem; font-weight: 700; letter-spacing: 2px;
  text-transform: uppercase; border: none; cursor: pointer;
  text-decoration: none; transition: all 0.3s;
}
.btn-primary:hover {
  background: var(--gold-accent); transform: translateY(-2px);
  box-shadow: 0 8px 30px rgba(196,162,101,0.3);
}
.btn-outline {
  background: transparent; color: var(--cream); padding: 16px 40px;
  font-size: 0.85rem; font-weight: 700; letter-spacing: 2px;
  text-transform: uppercase; border: 1px solid rgba(245,241,235,0.3);
  cursor: pointer; text-decoration: none; transition: all 0.3s;
}
.btn-outline:hover { border-color: var(--gold-accent); color: var(--gold-accent); }
.scroll-indicator {
  position: absolute; bottom: 2rem; left: 50%; transform: translateX(-50%);
  z-index: 2; animation: float 3s ease-in-out infinite;
}
.scroll-indicator svg { width: 24px; height: 24px; stroke: var(--gold-accent); opacity: 0.5; }
@keyframes float {
  0%, 100% { transform: translateX(-50%) translateY(0); }
  50% { transform: translateX(-50%) translateY(10px); }
}

/* STATS */
.stats-bar { background: var(--deep-olive); padding: 3rem 2rem; }
.stats-grid {
  max-width: 900px; margin: 0 auto;
  display: grid; grid-template-columns: repeat(3, 1fr);
  gap: 2rem; text-align: center;
}
.stat-item h3 {
  font-family: 'Playfair Display', serif; font-size: 2.5rem;
  font-weight: 800; color: var(--gold-accent); margin-bottom: 0.3rem;
}
.stat-item p {
  color: rgba(245,241,235,0.6); font-size: 0.8rem;
  font-weight: 600; letter-spacing: 1.5px; text-transform: uppercase;
}

/* SECTIONS */
section { padding: 6rem 2rem; }
.section-label {
  font-size: 0.7rem; font-weight: 700; letter-spacing: 3px;
  text-transform: uppercase; color: var(--bronze); margin-bottom: 1rem;
}
.section-title {
  font-family: 'Playfair Display', serif; font-size: clamp(2rem, 4vw, 3rem);
  font-weight: 800; color: var(--deep-olive); line-height: 1.15; margin-bottom: 1.5rem;
}
.section-desc {
  font-size: 1.1rem; color: var(--charcoal); line-height: 1.7;
  max-width: 640px; font-weight: 300;
}

/* STORY */
.story { background: var(--warm-white); }
.story-inner {
  max-width: 1100px; margin: 0 auto;
  display: grid; grid-template-columns: 1fr 1fr;
  gap: 4rem; align-items: center;
}
.story-visual {
  position: relative; height: 520px; background: var(--deep-olive); overflow: hidden;
}
.story-visual-inner {
  position: absolute; inset: 2rem; border: 1px solid var(--bronze);
  display: flex; flex-direction: column; justify-content: center;
  align-items: center; padding: 3rem; text-align: center;
}
.story-visual-inner .brand-mark {
  font-family: 'Source Sans 3', sans-serif; font-weight: 900;
  font-size: 3rem; letter-spacing: 6px; color: var(--cream);
  text-transform: uppercase; margin-bottom: 0.75rem;
}
.story-visual-inner .brand-mark span { color: var(--gold-accent); }
.story-visual-inner .brand-tagline {
  font-family: 'Playfair Display', serif; font-style: italic;
  font-size: 1rem; color: var(--bronze); margin-bottom: 1.5rem;
}
.story-visual-inner .brand-location {
  font-size: 0.7rem; letter-spacing: 2px; text-transform: uppercase;
  color: rgba(245,241,235,0.4); font-weight: 600;
}
.story-quote {
  font-family: 'Playfair Display', serif; font-size: 1.4rem;
  font-style: italic; color: var(--deep-olive); line-height: 1.5;
  margin-top: 2rem; padding-left: 1.5rem; border-left: 3px solid var(--bronze);
}
.story-quote-attr {
  margin-top: 0.75rem; font-family: 'Source Sans 3', sans-serif;
  font-style: normal; font-size: 0.8rem; font-weight: 600;
  letter-spacing: 1px; text-transform: uppercase; color: var(--bronze);
}

/* VISION */
.vision {
  background: var(--dark-bg); position: relative; overflow: hidden;
}
.vision .topo-bg {
  position: absolute; inset: 0; opacity: 0.03;
  background-size: 400px 400px;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400' viewBox='0 0 400 400'%3E%3Cpath d='M0 200 Q100 150 200 200 Q300 250 400 200' fill='none' stroke='%23C4A265' stroke-width='1'/%3E%3Cpath d='M0 220 Q100 170 200 220 Q300 270 400 220' fill='none' stroke='%23C4A265' stroke-width='1'/%3E%3Cpath d='M0 240 Q100 190 200 240 Q300 290 400 240' fill='none' stroke='%23C4A265' stroke-width='1'/%3E%3C/svg%3E");
}
.vision-inner {
  max-width: 800px; margin: 0 auto; text-align: center;
  position: relative; z-index: 1;
}
.vision .section-label { color: var(--gold-accent); }
.vision .section-title { color: var(--cream); }
.vision .section-desc { color: rgba(245,241,235,0.65); margin: 0 auto; text-align: center; }
.vision-pillars {
  display: grid; grid-template-columns: repeat(2, 1fr);
  gap: 1.5rem; margin-top: 3.5rem; text-align: left;
}
.vision-pillar {
  padding: 2rem;
  background: rgba(245,241,235,0.04);
  border: 1px solid rgba(196,162,101,0.1);
  transition: all 0.3s;
}
.vision-pillar:hover {
  border-color: rgba(196,162,101,0.25);
  background: rgba(245,241,235,0.06);
}
.vision-pillar h3 {
  font-family: 'Playfair Display', serif; font-size: 1.15rem;
  font-weight: 800; color: var(--cream); margin-bottom: 0.6rem;
}
.vision-pillar p {
  font-size: 0.9rem; color: rgba(245,241,235,0.55);
  line-height: 1.6; font-weight: 300;
}

/* BUILDING */
.building { background: var(--cream); }
.building-inner { max-width: 900px; margin: 0 auto; }
.building-header { text-align: center; max-width: 650px; margin: 0 auto 3.5rem; }
.building-grid {
  display: grid; grid-template-columns: repeat(3, 1fr);
  gap: 2.5rem; text-align: center;
}
.building-icon {
  width: 56px; height: 56px; margin: 0 auto 1.25rem;
  display: flex; align-items: center; justify-content: center;
  border: 1px solid var(--bronze); border-radius: 50%;
}
.building-icon svg {
  width: 24px; height: 24px; stroke: var(--bronze);
  fill: none; stroke-width: 1.5;
}
.building-item h3 {
  font-weight: 700; font-size: 1rem; color: var(--deep-olive); margin-bottom: 0.6rem;
}
.building-item p {
  font-size: 0.9rem; color: var(--charcoal); line-height: 1.6; font-weight: 300;
}

/* CONSERVATION */
.conservation {
  background: var(--forest-dark); position: relative;
  overflow: hidden; text-align: center;
}
.conservation .topo-bg {
  position: absolute; inset: 0; opacity: 0.03;
  background-size: 400px 400px;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400' viewBox='0 0 400 400'%3E%3Cpath d='M0 200 Q100 150 200 200 Q300 250 400 200' fill='none' stroke='%235C7A3D' stroke-width='1'/%3E%3Cpath d='M0 220 Q100 170 200 220 Q300 270 400 220' fill='none' stroke='%235C7A3D' stroke-width='1'/%3E%3C/svg%3E");
}
.conservation-inner {
  position: relative; z-index: 1; max-width: 720px; margin: 0 auto;
}
.conservation .section-label { color: var(--sage); }
.conservation .section-title { color: var(--cream); margin-bottom: 1.5rem; }
.conservation .section-desc {
  color: rgba(245,241,235,0.7); max-width: 600px;
  margin: 0 auto 2.5rem; text-align: center;
}
.partner-logos {
  display: flex; gap: 2.5rem; justify-content: center;
  align-items: center; flex-wrap: wrap; margin-top: 3rem; opacity: 0.4;
}
.partner-logos span {
  font-size: 0.7rem; font-weight: 700; letter-spacing: 2px;
  text-transform: uppercase; color: var(--cream);
}

/* WAITLIST */
.waitlist {
  background: var(--deep-olive); text-align: center; padding: 7rem 2rem;
}
.waitlist-inner { max-width: 580px; margin: 0 auto; }
.waitlist .section-label { color: var(--gold-accent); }
.waitlist .section-title { color: var(--cream); margin-bottom: 1rem; }
.waitlist .section-desc {
  color: rgba(245,241,235,0.7); margin: 0 auto 2.5rem; text-align: center;
}
.waitlist-form { display: flex; gap: 0; max-width: 480px; margin: 0 auto; }
.waitlist-form input {
  flex: 1; padding: 16px 20px;
  font-family: 'Source Sans 3', sans-serif; font-size: 0.95rem;
  border: 1px solid rgba(196,162,101,0.3); border-right: none;
  background: rgba(245,241,235,0.06); color: var(--cream);
  outline: none; transition: border 0.3s;
}
.waitlist-form input::placeholder { color: rgba(245,241,235,0.35); }
.waitlist-form input:focus { border-color: var(--gold-accent); }
.waitlist-form button {
  padding: 16px 32px; background: var(--bronze); color: var(--cream);
  font-family: 'Source Sans 3', sans-serif; font-weight: 700;
  font-size: 0.8rem; letter-spacing: 2px; text-transform: uppercase;
  border: 1px solid var(--bronze); cursor: pointer;
  transition: all 0.3s; white-space: nowrap;
}
.waitlist-form button:hover { background: var(--gold-accent); border-color: var(--gold-accent); }
.waitlist-note { margin-top: 1rem; font-size: 0.75rem; color: rgba(245,241,235,0.35); }

/* FOOTER */
footer { background: var(--dark-bg); padding: 3rem 2rem 2rem; }
.footer-inner { max-width: 900px; margin: 0 auto; text-align: center; }
.footer-brand { margin-bottom: 1.5rem; }
.footer-brand .nav-logo { display: inline-block; margin-bottom: 0.75rem; font-size: 1.2rem; }
.footer-brand p {
  font-size: 0.85rem; color: rgba(245,241,235,0.4); font-weight: 300;
  max-width: 400px; margin: 0 auto; line-height: 1.6;
}
.footer-links {
  display: flex; justify-content: center; gap: 2rem; margin: 1.5rem 0;
}
.footer-links a {
  color: rgba(245,241,235,0.5); text-decoration: none; font-size: 0.8rem;
  font-weight: 600; letter-spacing: 1px; text-transform: uppercase;
  transition: color 0.3s;
}
.footer-links a:hover { color: var(--gold-accent); }
.footer-divider {
  width: 60px; height: 1px; background: rgba(196,162,101,0.2); margin: 1.5rem auto;
}
.footer-bottom p { font-size: 0.7rem; color: rgba(245,241,235,0.25); line-height: 1.6; }

/* ANIMATIONS */
.reveal {
  opacity: 0; transform: translateY(30px);
  transition: all 0.8s cubic-bezier(0.16, 1, 0.3, 1);
}
.reveal.visible { opacity: 1; transform: translateY(0); }

/* RESPONSIVE */
@media (max-width: 768px) {
  nav { padding: 0 1.25rem; }
  .nav-links {
    display: none; position: fixed; top: 72px; left: 0; right: 0; bottom: 0;
    background: rgba(26,26,21,0.98); flex-direction: column;
    justify-content: center; align-items: center; gap: 2rem;
  }
  .nav-links.open { display: flex; }
  .mobile-toggle { display: block; }
  .story-inner { grid-template-columns: 1fr; }
  .story-visual { height: 280px; }
  .vision-pillars { grid-template-columns: 1fr; }
  .building-grid { grid-template-columns: 1fr; gap: 2rem; }
  .stats-grid { grid-template-columns: 1fr; gap: 1.5rem; }
  .waitlist-form { flex-direction: column; }
  .waitlist-form input { border-right: 1px solid rgba(196,162,101,0.3); border-bottom: none; }
  .hero h1 { font-size: clamp(2.2rem, 8vw, 3.5rem); }
  section { padding: 4rem 1.25rem; }
  .partner-logos { gap: 1.5rem; }
}
</style>
</head>
<body>

<nav id="navbar">
  <a href="#" class="nav-logo">GET<span>OUT</span></a>
  <ul class="nav-links" id="navLinks">
    <li><a href="#story">Our Story</a></li>
    <li><a href="#vision">The Vision</a></li>
    <li><a href="#conservation">Conservation</a></li>
    <li><a href="#waitlist" class="nav-cta">Join Waitlist</a></li>
  </ul>
  <button class="mobile-toggle" id="mobileToggle" aria-label="Menu">
    <span></span><span></span><span></span>
  </button>
</nav>

<section class="hero" id="hero">
  <div class="hero-bg"></div>
  <div class="hero-texture"></div>
  <div class="topo-lines"></div>
  <div class="hero-content">
    <div class="hero-badge">Coming Soon</div>
    <h1>Turn Every Dollar Into <em>Fuel for the Wild</em></h1>
    <p class="hero-sub">The first rewards ecosystem built by outdoor people, for outdoor people. Your groceries, gas, and everyday spending now have a purpose&mdash;to get you back outside.</p>
    <div class="hero-actions">
      <a href="#waitlist" class="btn-primary">Join the Waitlist</a>
      <a href="#story" class="btn-outline">Our Story</a>
    </div>
  </div>
  <div class="scroll-indicator">
    <svg viewBox="0 0 24 24" fill="none" stroke-width="2" stroke-linecap="round">
      <path d="M12 5v14M5 12l7 7 7-7"/>
    </svg>
  </div>
</section>

<div class="stats-bar">
  <div class="stats-grid">
    <div class="stat-item reveal"><h3>$1.2T</h3><p>Outdoor Economy</p></div>
    <div class="stat-item reveal"><h3>160M</h3><p>Active Participants</p></div>
    <div class="stat-item reveal"><h3>2.3%</h3><p>of U.S. GDP</p></div>
  </div>
</div>

<section class="story" id="story">
  <div class="story-inner">
    <div class="story-visual reveal">
      <div class="story-visual-inner">
        <div class="brand-mark">GET<span>OUT</span></div>
        <div class="brand-tagline">Life's an adventure.</div>
        <div class="brand-location">Golden, Colorado &middot; Est. 2025</div>
      </div>
    </div>
    <div class="story-text">
      <div class="section-label reveal">Our Story</div>
      <h2 class="section-title reveal">A Culture-Driven Economy Deserves a Financial Identity of Its Own</h2>
      <p class="section-desc reveal">Outdoor recreation isn't a niche. It's a $1.2 trillion engine powered by 160 million Americans who define themselves by what they do outside. Yet no financial product speaks their language, rewards their lifestyle, or gives back to the landscapes that make it all possible.</p>
      <p class="section-desc reveal" style="margin-top: 1rem;">We're building GetOut Rewards to change that&mdash;a platform where every swipe redirects value back into conservation, local outfitters, and the experiences that define who we are.</p>
      <blockquote class="story-quote reveal">
        We're not just issuing a card. We're building a new economic loop where passion becomes profit, loyalty becomes leverage, and spending becomes belonging.
        <div class="story-quote-attr">&mdash; GetOut Founders</div>
      </blockquote>
    </div>
  </div>
</section>

<section class="vision" id="vision">
  <div class="topo-bg"></div>
  <div class="vision-inner">
    <div class="section-label reveal">The Outdoor Rewards Network</div>
    <h2 class="section-title reveal">Four Pillars. One Ecosystem.</h2>
    <p class="section-desc reveal">We designed GetOut the way smart platforms work&mdash;not by squeezing users, but by participating in the value we help create.</p>
    <div class="vision-pillars">
      <div class="vision-pillar reveal">
        <h3>The Consumer</h3>
        <p>Adventurers whose identity is tied to mountains, rivers, and woods. GetOut finally gives them a financial identity that reflects who they are.</p>
      </div>
      <div class="vision-pillar reveal">
        <h3>Redemption Partners</h3>
        <p>Outfitters, guides, lodges, and specialty retailers. Everyday spending flows back into real gear and real experiences.</p>
      </div>
      <div class="vision-pillar reveal">
        <h3>Conservation Partners</h3>
        <p>The stewards of the wild become part of the financial loop. Every swipe becomes a small act of preservation.</p>
      </div>
      <div class="vision-pillar reveal">
        <h3>Everyday Merchants</h3>
        <p>Gas, grocery, travel, insurance&mdash;the everyday economy that fuels the outdoor one. Now, all that spending has a purpose.</p>
      </div>
    </div>
  </div>
</section>

<section class="building">
  <div class="building-inner">
    <div class="building-header">
      <div class="section-label reveal">What We're Building</div>
      <h2 class="section-title reveal">A Rewards Platform Unlike Anything Before It</h2>
      <p class="section-desc reveal" style="margin: 0 auto;">Credit cards that reward the entire outdoor lifestyle. Merchant tools that bring local businesses into the network. Conservation impact built into every transaction.</p>
    </div>
    <div class="building-grid">
      <div class="building-item reveal">
        <div class="building-icon">
          <svg viewBox="0 0 24 24"><rect x="2" y="5" width="20" height="14" rx="2"/><path d="M2 10h20"/></svg>
        </div>
        <h3>Rewards Cards</h3>
        <p>Premium and everyday cards designed around how outdoor enthusiasts actually spend&mdash;from gas and groceries to outfitters and guides.</p>
      </div>
      <div class="building-item reveal">
        <div class="building-icon">
          <svg viewBox="0 0 24 24"><path d="M12 2L2 7l10 5 10-5-10-5z"/><path d="M2 17l10 5 10-5"/><path d="M2 12l10 5 10-5"/></svg>
        </div>
        <h3>Merchant Network</h3>
        <p>Payment processing and loyalty tools for outdoor businesses&mdash;connecting merchants directly to the customers who live for what they sell.</p>
      </div>
      <div class="building-item reveal">
        <div class="building-icon">
          <svg viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><path d="M12 6v6l4 2"/></svg>
        </div>
        <h3>AI Offer Engine</h3>
        <p>Personalized, timely offers that know your season, your sport, and your next adventure&mdash;the right deal, right when it matters.</p>
      </div>
    </div>
  </div>
</section>

<section class="conservation" id="conservation">
  <div class="topo-bg"></div>
  <div class="conservation-inner">
    <div class="section-label reveal">Conservation Impact</div>
    <h2 class="section-title reveal">Tech for the Good of the Wild</h2>
    <p class="section-desc reveal">Every transaction creates a micro-contribution to conservation. Through partnerships with America's leading conservation organizations, GetOut members don't just earn rewards&mdash;they protect the landscapes that make it all possible.</p>
    <a href="#waitlist" class="btn-primary reveal">Become a Founding Member</a>
    <div class="partner-logos reveal">
      <span>Strategic conservation partnerships &middot; Announcing soon</span>
    </div>
  </div>
</section>

<section class="waitlist" id="waitlist">
  <div class="waitlist-inner">
    <div class="section-label reveal">Launching 2026</div>
    <h2 class="section-title reveal">Be First on the Trail</h2>
    <p class="section-desc reveal">Join the founding member waitlist. Early members get priority access, exclusive rewards, and a voice in shaping the future of outdoor finance.</p>
    <form class="waitlist-form reveal" onsubmit="handleSubmit(event)">
      <input type="email" placeholder="Enter your email" required>
      <button type="submit">Get Out</button>
    </form>
    <p class="waitlist-note reveal">No spam. Just the call of the wild.</p>
  </div>
</section>

<footer>
  <div class="footer-inner">
    <div class="footer-brand">
      <a href="#" class="nav-logo">GET<span>OUT</span></a>
      <p>The first rewards ecosystem built by outdoor people, for outdoor people. Technology built to send people back outdoors.</p>
    </div>
    <div class="footer-links">
      <a href="#story">Our Story</a>
      <a href="#vision">Vision</a>
      <a href="#conservation">Conservation</a>
      <a href="mailto:info@getoutrewards.com">Contact</a>
    </div>
    <div class="footer-divider"></div>
    <div class="footer-bottom">
      <p>&copy; 2025 GetOut Rewards / Stone House LL &middot; Golden, Colorado</p>
      <p style="margin-top: 0.5rem;">Life's an adventure. <strong style="color: var(--gold-accent);">GetOut.</strong></p>
    </div>
  </div>
</footer>

<script>
const navbar = document.getElementById('navbar');
window.addEventListener('scroll', () => navbar.classList.toggle('scrolled', window.scrollY > 50));

const mobileToggle = document.getElementById('mobileToggle');
const navLinks = document.getElementById('navLinks');
mobileToggle.addEventListener('click', () => navLinks.classList.toggle('open'));
navLinks.querySelectorAll('a').forEach(link =>
  link.addEventListener('click', () => navLinks.classList.remove('open'))
);

const reveals = document.querySelectorAll('.reveal');
const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      const siblings = entry.target.parentElement.querySelectorAll('.reveal');
      let delay = 0;
      siblings.forEach((s, j) => { if (s === entry.target) delay = j * 100; });
      setTimeout(() => entry.target.classList.add('visible'), delay);
      observer.unobserve(entry.target);
    }
  });
}, { threshold: 0.15, rootMargin: '0px 0px -50px 0px' });
reveals.forEach(el => observer.observe(el));

function handleSubmit(e) {
  e.preventDefault();
  const input = e.target.querySelector('input');
  const btn = e.target.querySelector('button');
  btn.textContent = "You're In!";
  btn.style.background = '#5C7A3D';
  btn.style.borderColor = '#5C7A3D';
  input.value = '';
  input.placeholder = 'Welcome to the trail.';
  input.disabled = true;
  btn.disabled = true;
}

document.querySelectorAll('a[href^="#"]').forEach(anchor => {
  anchor.addEventListener('click', function(e) {
    e.preventDefault();
    const target = document.querySelector(this.getAttribute('href'));
    if (target) target.scrollIntoView({ behavior: 'smooth', block: 'start' });
  });
});
</script>

</body>
</html>
