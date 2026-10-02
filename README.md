
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#08090d">
<meta name="description" content="The personal universe of Biraja Prasad Jena — Liskun. Still becoming, never pretending.">
<title>LISKUN — A World of My Own</title>

<style>
:root {
  --bg: #08090d;
  --panel: #101219;
  --panel2: #151822;
  --text: #f2f0eb;
  --muted: #9195a3;
  --line: rgba(255,255,255,.10);
  --accent: #c5b5ff;
  --accent2: #91d9e9;
  --radius: 22px;
}

* { box-sizing: border-box; margin: 0; padding: 0; }

html { scroll-behavior: smooth; scroll-padding-top: 85px; }

body {
  background: var(--bg);
  color: var(--text);
  font-family: Inter, -apple-system, BlinkMacSystemFont, "Segoe UI",
               sans-serif;
  line-height: 1.65;
  overflow-x: hidden;
}

body::before {
  content: "";
  position: fixed;
  inset: 0;
  pointer-events: none;
  z-index: -1;
  background:
    radial-gradient(ellipse at 15% 10%, rgba(125,100,220,.12), transparent 40%),
    radial-gradient(ellipse at 90% 50%, rgba(63,148,170,.07), transparent 38%);
}

button, input { font: inherit; }
button, a { -webkit-tap-highlight-color: transparent; }
a { color: inherit; text-decoration: none; }
button { color: inherit; }
::selection { background: var(--accent); color: #08090d; }

#stars {
  position: fixed;
  inset: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
  pointer-events: none;
}

.noise {
  position: fixed;
  inset: 0;
  pointer-events: none;
  z-index: 20;
  opacity: .025;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 180 180' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.7'/%3E%3C/svg%3E");
}

/* MUSIC AT THE TOP */
.music-top {
  position: relative;
  z-index: 30;
  padding: 12px 5%;
  border-bottom: 1px solid var(--line);
  background: rgba(8,9,13,.88);
  backdrop-filter: blur(18px);
}

.music-inner {
  max-width: 1100px;
  margin: auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 16px;
}

.music-label {
  display: flex;
  align-items: center;
  gap: 10px;
  min-width: 0;
}

.music-disc {
  width: 37px;
  height: 37px;
  border-radius: 50%;
  display: grid;
  place-items: center;
  flex-shrink: 0;
  background: linear-gradient(135deg, #29243e, #101b29);
  border: 1px solid rgba(197,181,255,.35);
  color: var(--accent);
  animation: spin 7s linear infinite;
  animation-play-state: paused;
}

.music-disc.playing { animation-play-state: running; }

@keyframes spin { to { transform: rotate(360deg); } }

.music-meta { min-width: 0; }

.music-meta strong {
  display: block;
  font-size: 11px;
  letter-spacing: 1.8px;
}

.music-meta span {
  display: block;
  color: var(--muted);
  font-size: 11px;
}

audio { width: min(270px, 52vw); height: 36px; }

/* NAVIGATION */
.nav {
  position: sticky;
  top: 0;
  z-index: 25;
  border-bottom: 1px solid var(--line);
  background: rgba(8,9,13,.78);
  backdrop-filter: blur(18px);
}

.nav-inner {
  max-width: 1100px;
  margin: auto;
  padding: 13px 5%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
}

.brand {
  font-size: 14px;
  letter-spacing: 3px;
  font-weight: 800;
}

.brand span { color: var(--accent); }

.nav-links {
  display: flex;
  gap: 23px;
  color: var(--muted);
  font-size: 12px;
}

.nav-links a:hover { color: var(--text); }

main, footer {
  width: min(100% - 40px, 1000px);
  margin-inline: auto;
}

section { padding: 100px 0; }

.eyebrow {
  font-size: 10px;
  text-transform: uppercase;
  letter-spacing: 3px;
  color: var(--accent);
  margin-bottom: 16px;
}

.section-heading {
  font-size: clamp(30px, 5vw, 46px);
  line-height: 1.15;
  letter-spacing: -1.8px;
  margin-bottom: 16px;
  font-weight: 600;
}

.section-intro {
  color: var(--muted);
  max-width: 530px;
  font-size: 14px;
}

.line { height: 1px; background: var(--line); }

/* HERO */
.hero {
  min-height: 79vh;
  padding: 100px 0 85px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  position: relative;
}

.status {
  display: inline-flex;
  align-items: center;
  gap: 9px;
  align-self: flex-start;
  border: 1px solid var(--line);
  background: rgba(255,255,255,.025);
  border-radius: 50px;
  padding: 7px 12px;
  color: #c2c4cf;
  font-size: 11px;
  margin-bottom: 30px;
}

.status-dot {
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: #9be2bd;
  box-shadow: 0 0 12px #9be2bd;
}

.hero h1 {
  font-size: clamp(53px, 11vw, 110px);
  letter-spacing: -.075em;
  line-height: .95;
  font-weight: 750;
  max-width: 900px;
}

.hero h1 .outline {
  color: transparent;
  -webkit-text-stroke: 1px rgba(242,240,235,.75);
}

.hero-description {
  margin-top: 27px;
  max-width: 450px;
  color: #a6a9b5;
  font-size: 15px;
}

.motto {
  margin-top: 28px;
  font-size: 13px;
  color: #d9d1f5;
  letter-spacing: .5px;
}

.hero-bottom {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 18px;
  margin-top: 58px;
}

.button {
  border: 1px solid var(--line);
  background: #f0edf8;
  color: #11121a;
  border-radius: 50px;
  padding: 12px 19px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  font-size: 12px;
  cursor: pointer;
  transition: .25s ease;
}

.button:hover { transform: translateY(-3px); background: white; }

.button.secondary {
  background: transparent;
  color: var(--text);
}

.hero-time {
  color: var(--muted);
  font-size: 11px;
  letter-spacing: 1px;
}

/* GENERAL CARDS */
.grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 14px;
  margin-top: 32px;
}

.card {
  background: linear-gradient(145deg, rgba(255,255,255,.045), rgba(255,255,255,.015));
  border: 1px solid var(--line);
  border-radius: var(--radius);
  padding: 24px;
  transition: border-color .25s, transform .25s;
}

.card:hover {
  border-color: rgba(197,181,255,.4);
  transform: translateY(-3px);
}

.card-number {
  font-size: 11px;
  color: var(--accent);
  letter-spacing: 2px;
  margin-bottom: 28px;
}

.card h3 { font-size: 18px; font-weight: 550; margin-bottom: 8px; }
.card p { color: var(--muted); font-size: 13px; }

/* INTERACTIVE CONSTELLATION */
.constellation {
  margin-top: 35px;
  border: 1px solid var(--line);
  border-radius: var(--radius);
  padding: 25px;
  background: radial-gradient(ellipse at center, rgba(120,105,190,.12), transparent 75%);
}

.constellation-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
  flex-wrap: wrap;
  margin-bottom: 15px;
}

.constellation-top p { font-size: 12px; color: var(--muted); }

.star-map {
  min-height: 190px;
  position: relative;
  overflow: hidden;
  border-radius: 15px;
}

.star-map svg {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  opacity: .45;
}

.constellation-star {
  position: absolute;
  transform: translate(-50%, -50%);
  border: 1px solid rgba(197,181,255,.3);
  background: #151425;
  width: 43px;
  height: 43px;
  border-radius: 50%;
  display: grid;
  place-items: center;
  color: var(--accent);
  cursor: pointer;
  box-shadow: 0 0 24px rgba(197,181,255,.08);
  transition: .25s;
}

.constellation-star:hover, .constellation-star:focus-visible {
  background: var(--accent);
  color: #090a10;
  box-shadow: 0 0 28px rgba(197,181,255,.4);
  transform: translate(-50%, -50%) scale(1.12);
}

.star-label {
  position: absolute;
  font-size: 10px;
  color: #c2c0ce;
  white-space: nowrap;
  pointer-events: none;
}

.star-result {
  min-height: 65px;
  border-top: 1px solid var(--line);
  margin-top: 12px;
  padding-top: 17px;
}

.star-result strong { font-size: 14px; }
.star-result p { color: var(--muted); font-size: 12px; margin-top: 3px; }

/* THOUGHTS */
.quote-box {
  margin-top: 32px;
  padding: clamp(25px, 6vw, 48px);
  border: 1px solid var(--line);
  border-radius: var(--radius);
  background: linear-gradient(130deg, rgba(197,181,255,.09), rgba(145,217,233,.025));
}

.quote-mark { font-family: Georgia, serif; font-size: 55px; color: var(--accent); line-height: 1; }

#quoteText {
  font-family: Georgia, "Times New Roman", serif;
  font-size: clamp(22px, 4vw, 35px);
  line-height: 1.4;
  letter-spacing: -.6px;
  margin: 15px 0 22px;
}

.quote-bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 15px;
}

/* PHOTO GALLERY - NO CAPTIONS */
.gallery {
  margin-top: 32px;
  display: grid;
  grid-template-columns: repeat(3, minmax(0,1fr));
  gap: 12px;
}

.photo {
  position: relative;
  aspect-ratio: 4 / 5;
  overflow: hidden;
  border: 1px solid var(--line);
  border-radius: 16px;
  background: linear-gradient(145deg, #191b28, #0d1017);
  cursor: zoom-in;
}

.photo img {
  width: 100%;
  height: 100%;
  display: block;
  object-fit: cover;
  transition: transform .5s, opacity .4s;
}

.photo:hover img { transform: scale(1.045); }

.photo.empty::after {
  content: "＋";
  position: absolute;
  inset: 0;
  display: grid;
  place-items: center;
  color: rgba(197,181,255,.55);
  font-size: 32px;
  pointer-events: none;
}

/* MODAL */
.modal {
  position: fixed;
  inset: 0;
  z-index: 60;
  display: none;
  align-items: center;
  justify-content: center;
  padding: 22px;
  background: rgba(0,0,0,.88);
  backdrop-filter: blur(12px);
}

.modal.open { display: flex; }

.modal img {
  max-width: min(100%, 850px);
  max-height: 82vh;
  object-fit: contain;
  border-radius: 12px;
}

.modal-close {
  position: absolute;
  top: 18px;
  right: 20px;
  border: 1px solid var(--line);
  background: #171820;
  border-radius: 50%;
  width: 43px;
  height: 43px;
  font-size: 20px;
  cursor: pointer;
}

/* TERMINAL */
.terminal {
  margin-top: 32px;
  border: 1px solid rgba(145,217,233,.22);
  border-radius: 17px;
  overflow: hidden;
  background: #0b0e13;
  font-family: "SFMono-Regular", Consolas, monospace;
}

.terminal-head {
  padding: 13px 17px;
  background: #11151c;
  border-bottom: 1px solid var(--line);
  font-size: 11px;
  color: #a7a9b4;
  display: flex;
  align-items: center;
  gap: 7px;
}

.terminal-head i {
  display: block;
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: #77758b;
}

.terminal-body { padding: 20px; font-size: 12px; }
.terminal-output { min-height: 120px; white-space: pre-wrap; color: #b7c9c8; }
.terminal-form { display: flex; gap: 8px; align-items: center; margin-top: 14px; }
.terminal-form label { color: #a7baff; }
.terminal-form input {
  min-width: 0;
  flex: 1;
  border: 0;
  outline: 0;
  color: #e8e8ee;
  background: transparent;
  font-family: inherit;
  font-size: 12px;
}
.terminal-form button {
  background: transparent;
  border: 1px solid var(--line);
  border-radius: 7px;
  padding: 6px 10px;
  font-size: 11px;
  cursor: pointer;
}

/* SECRET */
.secret-card {
  margin-top: 32px;
  text-align: center;
  padding: 38px 24px;
  background: linear-gradient(145deg, rgba(197,181,255,.08), rgba(255,255,255,.015));
  border: 1px solid var(--line);
  border-radius: var(--radius);
}

.lock-icon { font-size: 30px; margin-bottom: 14px; }
.secret-card p { color: var(--muted); font-size: 13px; margin: 8px auto 20px; max-width: 400px; }

.secret-message {
  display: none;
  margin-top: 24px;
  padding-top: 20px;
  border-top: 1px solid var(--line);
  font-family: Georgia, serif;
  font-size: 20px;
  color: #ded5ff;
}

.secret-message.show { display: block; animation: appear .6s ease; }

@keyframes appear {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}

footer {
  padding: 35px 0 42px;
  border-top: 1px solid var(--line);
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 15px;
  flex-wrap: wrap;
}

.footer-brand { font-size: 13px; letter-spacing: 2px; font-weight: 700; }
footer p { font-size: 11px; color: var(--muted); }

.reveal { opacity: 0; transform: translateY(18px); transition: opacity .7s, transform .7s; }
.reveal.visible { opacity: 1; transform: translateY(0); }

#toast {
  position: fixed;
  bottom: 22px;
  left: 50%;
  transform: translate(-50%, 15px);
  z-index: 80;
  background: #f0edf8;
  color: #11121a;
  padding: 11px 17px;
  border-radius: 50px;
  font-size: 12px;
  opacity: 0;
  pointer-events: none;
  transition: .25s;
  width: max-content;
  max-width: calc(100% - 30px);
  text-align: center;
}

#toast.show { opacity: 1; transform: translate(-50%, 0); }

@media (max-width: 650px) {
  .music-inner { align-items: flex-start; flex-direction: column; gap: 9px; }
  audio { width: 100%; }
  .nav-inner { padding-block: 12px; }
  .nav-links { gap: 13px; font-size: 11px; }
  .nav-links a:nth-child(2) { display: none; }
  main, footer { width: calc(100% - 32px); }
  section { padding: 73px 0; }
  .hero { min-height: 74vh; padding: 80px 0 55px; }
  .hero h1 { font-size: clamp(51px, 14vw, 78px); }
  .hero-description { font-size: 14px; }
  .grid { grid-template-columns: 1fr; }
  .card { padding: 21px; }
  .card-number { margin-bottom: 18px; }
  .gallery { grid-template-columns: repeat(2, minmax(0,1fr)); gap: 9px; }
  .photo { border-radius: 12px; }
  .constellation { padding: 15px; }
  .star-map { min-height: 185px; }
  .constellation-star { width: 38px; height: 38px; }
  .terminal-body { padding: 14px; }
  .terminal-form { flex-wrap: wrap; }
}

@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after {
    scroll-behavior: auto !important;
    animation-duration: .01ms !important;
    transition-duration: .01ms !important;
  }
}
</style>
</head>

<body>
<canvas id="stars" aria-hidden="true"></canvas>
<div class="noise" aria-hidden="true"></div>

<!-- MUSIC PLAYER IS AT THE TOP -->
<div class="music-top" id="topMusic">
  <div class="music-inner">
    <div class="music-label">
      <div class="music-disc" id="musicDisc">♫</div>
      <div class="music-meta">
        <strong>A LITTLE SOUNDTRACK</strong>
        <span id="musicStatus">Your corner of the universe</span>
      </div>
    </div>
    <audio id="audioPlayer" controls preload="metadata">
      <source src="song.mp3" type="audio/mpeg">
      Your browser does not support audio playback.
    </audio>
  </div>
</div>

<nav class="nav">
  <div class="nav-inner">
    <a class="brand" href="#home">LISKUN<span>.</span></a>
    <div class="nav-links">
      <a href="#about">About</a>
      <a href="#thoughts">Thoughts</a>
      <a href="#gallery">Gallery</a>
      <a href="#terminal">Explore</a>
    </div>
  </div>
</nav>

<main>
  <!-- HERO -->
  <section class="hero" id="home">
    <div class="status"><span class="status-dot"></span> A WORK IN PROGRESS</div>
    <p class="eyebrow">A DIGITAL SPACE BY BIRAJA PRASAD JENA</p>
    <h1>NOT HERE<br>TO BE <span class="outline">EVERYONE.</span></h1>
    <p class="hero-description">
      Just a human collecting experiences, learning things, asking questions,
      and figuring life out one day at a time.
    </p>
    <p class="motto">“Still becoming, never pretending.”</p>

    <div class="hero-bottom">
      <div style="display:flex;gap:10px;flex-wrap:wrap">
        <a class="button" href="#about">Explore my world ↘</a>
        <button class="button secondary" id="surpriseBtn">Surprise me ✦</button>
      </div>
      <div class="hero-time" id="liveClock">LOCAL TIME · --:--:--</div>
    </div>
  </section>

  <div class="line"></div>

  <!-- ABOUT -->
  <section id="about" class="reveal">
    <p class="eyebrow">01 / A LITTLE ABOUT ME</p>
    <h2 class="section-heading">A person, not a perfect bio.</h2>
    <p class="section-intro">
      I'm Biraja Prasad Jena. Most people know me as Liskun.
      This is a small space for the things I enjoy, the things I think about,
      and the person I'm slowly becoming.
    </p>

    <div class="grid">
      <article class="card">
        <div class="card-number">01 — THE MIND</div>
        <h3>Always curious.</h3>
        <p>I like learning how things work, exploring ideas, and finding something interesting in ordinary moments.</p>
      </article>
      <article class="card">
        <div class="card-number">02 — THE VIBE</div>
        <h3>Quietly evolving.</h3>
        <p>Not everything needs an announcement. Some of the best changes happen away from the spotlight.</p>
      </article>
      <article class="card">
        <div class="card-number">03 — THE INTERESTS</div>
        <h3>Different little worlds.</h3>
        <p>Music, gaming, technology, college life, meaningful conversations, and thoughts that appear at midnight.</p>
      </article>
      <article class="card">
        <div class="card-number">04 — THE DIRECTION</div>
        <h3>More to become.</h3>
        <p>Learning new skills, making progress, and building a future that feels like my own.</p>
      </article>
    </div>
  </section>

  <div class="line"></div>

  <!-- INTERACTIVE CONSTELLATION -->
  <section id="universe" class="reveal">
    <p class="eyebrow">02 / FIND YOUR WAY</p>
    <h2 class="section-heading">A few stars from my universe.</h2>
    <p class="section-intro">Tap any star. Each one reveals a different side of this little world.</p>

    <div class="constellation">
      <div class="constellation-top">
        <p>✦ INTERACTIVE CONSTELLATION</p>
        <p>Choose a star to explore</p>
      </div>

      <div class="star-map">
        <svg viewBox="0 0 600 220" preserveAspectRatio="none" aria-hidden="true">
          <g stroke="#bcb0f7" stroke-width="1" fill="none">
            <path d="M70 135 L190 60 L300 125 L430 50 L530 145"/>
            <path d="M190 60 L220 175 L300 125"/>
            <path d="M300 125 L390 180 L530 145"/>
          </g>
        </svg>

        <button class="constellation-star" style="left:12%;top:61%" data-star="0" aria-label="Explore curiosity">✦</button>
        <span class="star-label" style="left:5%;top:76%">Curiosity</span>

        <button class="constellation-star" style="left:32%;top:27%" data-star="1" aria-label="Explore music">✧</button>
        <span class="star-label" style="left:29%;top:10%">Music</span>

        <button class="constellation-star" style="left:50%;top:56%" data-star="2" aria-label="Explore dreams">✦</button>
        <span class="star-label" style="left:46%;top:72%">Dreams</span>

        <button class="constellation-star" style="left:72%;top:23%" data-star="3" aria-label="Explore growth">✧</button>
        <span class="star-label" style="left:68%;top:7%">Growth</span>

        <button class="constellation-star" style="left:89%;top:65%" data-star="4" aria-label="Explore the unknown">✦</button>
        <span class="star-label" style="left:78%;top:81%">The unknown</span>
      </div>

      <div class="star-result" aria-live="polite">
        <strong id="starTitle">A universe waiting to be explored.</strong>
        <p id="starDescription">Choose a star above and see where it takes you.</p>
      </div>
    </div>
  </section>

  <div class="line"></div>

  <!-- THOUGHTS -->
  <section id="thoughts" class="reveal">
    <p class="eyebrow">03 / THOUGHTS AFTER DARK</p>
    <h2 class="section-heading">Words worth keeping.</h2>
    <p class="section-intro">A little reminder that life doesn't need to be figured out all at once.</p>

    <div class="quote-box">
      <div class="quote-mark">“</div>
      <p id="quoteText">You don't need to have everything figured out to take the next step.</p>
      <div class="quote-bottom">
        <p style="font-size:11px;color:var(--muted)">A NOTE TO SELF</p>
        <button class="button secondary" id="newQuote">Another thought ↗</button>
      </div>
    </div>
  </section>

  <div class="line"></div>

  <!-- GALLERY WITHOUT CAPTIONS -->
  <section id="gallery" class="reveal">
    <p class="eyebrow">04 / FRAGMENTS OF LIFE</p>
    <h2 class="section-heading">A few frames.</h2>
    <p class="section-intro">Some moments speak better without words.</p>

    <div class="gallery">
      <button class="photo empty" aria-label="Photo 1"><img src="photo1.jpg" alt="" loading="lazy"></button>
      <button class="photo empty" aria-label="Photo 2"><img src="photo2.jpg" alt="" loading="lazy"></button>
      <button class="photo empty" aria-label="Photo 3"><img src="photo3.jpg" alt="" loading="lazy"></button>
      <button class="photo empty" aria-label="Photo 4"><img src="photo4.jpg" alt="" loading="lazy"></button>
      <button class="photo empty" aria-label="Photo 5"><img src="photo5.jpg" alt="" loading="lazy"></button>
      <button class="photo empty" aria-label="Photo 6"><img src="photo6.jpg" alt="" loading="lazy"></button>
    </div>
  </section>

  <div class="line"></div>

  <!-- TERMINAL -->
  <section id="terminal" class="reveal">
    <p class="eyebrow">05 / THE BACK ROOM</p>
    <h2 class="section-heading">Curiosity looks good on you.</h2>
    <p class="section-intro">A tiny terminal. Type <code>help</code> to see what you can discover.</p>

    <div class="terminal">
      <div class="terminal-head"><i></i><i></i><i></i> &nbsp; liskun://explorer</div>
      <div class="terminal-body">
        <div class="terminal-output" id="terminalOutput" aria-live="polite">Welcome, explorer.
This is a tiny corner of my digital world.
Type "help" to begin.</div>
        <form class="terminal-form" id="terminalForm">
          <label for="terminalInput">visitor@liskun:~$</label>
          <input id="terminalInput" autocomplete="off" spellcheck="false" placeholder="type a command..." aria-label="Terminal command">
          <button type="submit">ENTER ↵</button>
        </form>
      </div>
    </div>
  </section>

  <div class="line"></div>

  <!-- SECRET MESSAGE -->
  <section id="secret" class="reveal">
    <p class="eyebrow">06 / NOT EVERYTHING IS ON DISPLAY</p>
    <h2 class="section-heading">Some things are hidden in plain sight.</h2>
    <p class="section-intro">A little extra for people who make it all the way down here.</p>

    <div class="secret-card">
      <div class="lock-icon" id="lockIcon">⌘</div>
      <h3 style="font-size:20px;font-weight:550">One last little secret.</h3>
      <p>No complicated password. Just a reminder worth hearing.</p>
      <button class="button" id="unlockBtn">Reveal the message ✦</button>
      <div class="secret-message" id="secretMessage">
        You're allowed to be a work in progress.<br>
        Keep learning. Keep your curiosity.<br>
        Your story is still being written.
      </div>
    </div>
  </section>
</main>

<footer>
  <div>
    <div class="footer-brand">LISKUN<span style="color:var(--accent)">.</span></div>
    <p style="margin-top:6px">Biraja Prasad Jena · Made of midnight thoughts.</p>
  </div>
  <p>Still becoming, never pretending. © <span id="year"></span></p>
  <button class="button secondary" id="topBtn">Back to top ↑</button>
</footer>

<div class="modal" id="imageModal" role="dialog" aria-modal="true" aria-label="Expanded photograph">
  <button class="modal-close" id="modalClose" aria-label="Close image">×</button>
  <img id="expandedImage" src="" alt="Expanded photograph">
</div>

<div id="toast" role="status" aria-live="polite"></div>

<script>
/* STARFIELD */
const canvas = document.getElementById("stars");
const ctx = canvas.getContext("2d");
let stars = [];
let canvasWidth = 0;
let canvasHeight = 0;

function makeStars() {
  const dpr = Math.min(window.devicePixelRatio || 1, 2);
  canvasWidth = window.innerWidth;
  canvasHeight = window.innerHeight;
  canvas.width = canvasWidth * dpr;
  canvas.height = canvasHeight * dpr;
  ctx.setTransform(dpr, 0, 0, dpr, 0, 0);

  const count = Math.min(160, Math.floor(canvasWidth / 5));
  stars = Array.from({ length: count }, () => ({
    x: Math.random() * canvasWidth,
    y: Math.random() * canvasHeight,
    r: Math.random() * 1.3 + .2,
    a: Math.random() * .6 + .15,
    speed: Math.random() * .009 + .002,
    phase: Math.random() * Math.PI * 2
  }));
}

let frame = 0;
function drawStars() {
  ctx.clearRect(0, 0, canvasWidth, canvasHeight);
  frame++;
  stars.forEach(s => {
    const alpha = s.a * (.65 + .35 * Math.sin(frame * s.speed + s.phase));
    ctx.beginPath();
    ctx.arc(s.x, s.y, s.r, 0, Math.PI * 2);
    ctx.fillStyle = `rgba(218,213,255,${alpha})`;
    ctx.fill();
  });
  requestAnimationFrame(drawStars);
}

makeStars();
drawStars();
window.addEventListener("resize", makeStars);

/* LIVE CLOCK */
function updateClock() {
  const now = new Date();
  document.getElementById("liveClock").textContent =
    "LOCAL TIME · " + now.toLocaleTimeString([], {
      hour: "2-digit", minute: "2-digit", second: "2-digit"
    });
}
updateClock();
setInterval(updateClock, 1000);
document.getElementById("year").textContent = new Date().getFullYear();

/* MUSIC PLAYER */
const audioPlayer = document.getElementById("audioPlayer");
const musicDisc = document.getElementById("musicDisc");
const musicStatus = document.getElementById("musicStatus");

audioPlayer.addEventListener("play", () => {
  musicDisc.classList.add("playing");
  musicStatus.textContent = "Now playing · your soundtrack";
});

audioPlayer.addEventListener("pause", () => {
  musicDisc.classList.remove("playing");
  musicStatus.textContent = "Your corner of the universe";
});

audioPlayer.addEventListener("error", () => {
  musicStatus.textContent = "Add song.mp3 to activate your soundtrack";
});

/* CONSTELLATION */
const starData = [
  {
    title: "Curiosity",
    description: "There is always something new to learn, even in the smallest things."
  },
  {
    title: "Music",
    description: "Sometimes a song can say what a whole conversation cannot."
  },
  {
    title: "Dreams",
    description: "Big plans are built from small steps taken when nobody is watching."
  },
  {
    title: "Growth",
    description: "Becoming a better version of yourself is a journey, not a deadline."
  },
  {
    title: "The unknown",
    description: "Not knowing everything yet is part of what makes life interesting."
  }
];

document.querySelectorAll(".constellation-star").forEach(button => {
  button.addEventListener("click", () => {
    const data = starData[Number(button.dataset.star)];
    document.getElementById("starTitle").textContent = data.title;
    document.getElementById("starDescription").textContent = data.description;
    document.querySelectorAll(".constellation-star").forEach(b => b.style.background = "");
    button.style.background = "rgba(197,181,255,.18)";
  });
});

/* RANDOM THOUGHTS */
const quotes = [
  "You don't need to have everything figured out to take the next step.",
  "A quiet season can still be a season of growth.",
  "Become someone your future self will thank you for.",
  "Not every chapter needs an audience.",
  "Some of the best things take time, patience, and a little courage.",
  "You are allowed to change your mind as you learn more about life.",
  "Make a life that feels good from the inside, too.",
  "Progress is still progress, even when nobody notices."
];

let lastQuote = -1;
document.getElementById("newQuote").addEventListener("click", () => {
  let next;
  do {
    next = Math.floor(Math.random() * quotes.length);
  } while (next === lastQuote && quotes.length > 1);
  lastQuote = next;
  const el = document.getElementById("quoteText");
  el.style.opacity = "0";
  setTimeout(() => {
    el.textContent = quotes[next];
    el.style.opacity = "1";
  }, 180);
});

/* TERMINAL */
const terminalForm = document.getElementById("terminalForm");
const terminalInput = document.getElementById("terminalInput");
const terminalOutput = document.getElementById("terminalOutput");

const commands = {
  help: `AVAILABLE COMMANDS

about    — who is Liskun?
motto    — a personal reminder
interests — what I enjoy
quote    — a random thought
time     — current local time
clear    — clear this terminal
secret   — a little message
hello    — say hello`,

  about: `NAME: Biraja Prasad Jena
ALSO KNOWN AS: Liskun
STATUS: Still learning.
DIRECTION: Becoming, one day at a time.`,

  motto: `"Still becoming, never pretending."`,

  interests: `Music.
Gaming.
Technology.
College life.
Deep thoughts.
Learning new things.`,

  secret: `Psst...
You found a little corner of the internet.
Stay curious, explorer. ✦`,

  hello: `Hey, visitor.
Thanks for exploring my little corner of the internet.`
};

terminalForm.addEventListener("submit", event => {
  event.preventDefault();
  const command = terminalInput.value.trim().toLowerCase();
  if (!command) return;

  if (command === "clear") {
    terminalOutput.textContent = "";
  } else if (command === "quote") {
    terminalOutput.textContent = quotes[Math.floor(Math.random() * quotes.length)];
  } else if (command === "time") {
    terminalOutput.textContent = new Date().toLocaleString();
  } else if (commands[command]) {
    terminalOutput.textContent = commands[command];
  } else {
    terminalOutput.textContent =
      `Command not found: "${command}"\nType "help" to see available commands.`;
  }

  terminalInput.value = "";
});

/* HIDDEN MESSAGE */
document.getElementById("unlockBtn").addEventListener("click", () => {
  const message = document.getElementById("secretMessage");
  const button = document.getElementById("unlockBtn");
  const icon = document.getElementById("lockIcon");
  const isOpen = message.classList.toggle("show");

  icon.textContent = isOpen ? "✦" : "⌘";
  button.textContent = isOpen ? "Hide the message ↑" : "Reveal the message ✦";
});

/* SURPRISE BUTTON */
const surpriseMessages = [
  "Plot twist: you're exactly where your next chapter begins.",
  "A little reminder: keep going at your own pace.",
  "Somewhere, someone is glad you exist. Be kind to yourself, too.",
  "Your future is built by the little things you do today.",
  "Congratulations. You have officially discovered a random thought."
];

let toastTimer;
function showToast(message) {
  const toast = document.getElementById("toast");
  toast.textContent = message;
  toast.classList.add("show");
  clearTimeout(toastTimer);
  toastTimer = setTimeout(() => toast.classList.remove("show"), 3000);
}

document.getElementById("surpriseBtn").addEventListener("click", () => {
  showToast(surpriseMessages[Math.floor(Math.random() * surpriseMessages.length)]);
});

/* PHOTO GALLERY: EMPTY PHOTOS ARE HIDDEN */
document.querySelectorAll(".photo").forEach(photo => {
  const img = photo.querySelector("img");

  img.addEventListener("load", () => {
    photo.classList.remove("empty");
  });

  img.addEventListener("error", () => {
    photo.classList.add("empty");
    img.style.display = "none";
  });

  if (img.complete && img.naturalWidth > 0) {
    photo.classList.remove("empty");
  } else if (img.complete && img.naturalWidth === 0) {
    img.style.display = "none";
  }

  photo.addEventListener("click", () => {
    if (img.style.display === "none" || !img.naturalWidth) {
      showToast("Add your photo file to the website folder first.");
      return;
    }
    document.getElementById("expandedImage").src = img.src;
    document.getElementById("imageModal").classList.add("open");
  });
});

/* CLOSE IMAGE VIEWER */
const imageModal = document.getElementById("imageModal");

function closeModal() {
  imageModal.classList.remove("open");
  document.getElementById("expandedImage").src = "";
}

document.getElementById("modalClose").addEventListener("click", closeModal);
imageModal.addEventListener("click", event => {
  if (event.target === imageModal) closeModal();
});
document.addEventListener("keydown", event => {
  if (event.key === "Escape") closeModal();
});

/* BACK TO TOP */
document.getElementById("topBtn").addEventListener("click", () => {
  window.scrollTo({ top: 0, behavior: "smooth" });
});

/* SCROLL REVEALS */
const revealObserver = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      entry.target.classList.add("visible");
      revealObserver.unobserve(entry.target);
    }
  });
}, { threshold: .08 });

document.querySelectorAll(".reveal").forEach(el => revealObserver.observe(el));
</script>
</body>
</html>
