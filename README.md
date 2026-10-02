# Biraja-Prasad-

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#f4eee4">
<meta name="description" content="A little corner of the internet belonging to Biraja Prasad Jena, known as Liskun. Still becoming, never pretending.">
<title>Liskun — Still Becoming 🌙</title>

<style>
:root{
  --bg:#f4eee4;
  --paper:#fffaf2;
  --cream:#e9dece;
  --ink:#403b35;
  --muted:#81776b;
  --accent:#9c8065;
  --accent2:#c4a88b;
  --line:#ded2c2;
  --shadow:0 16px 45px rgba(76,59,40,.08);
}
*{box-sizing:border-box}
html{scroll-behavior:smooth;scroll-padding-top:85px}
body{
  margin:0;
  color:var(--ink);
  background:
    radial-gradient(ellipse at 10% 5%,#fffdf8 0,transparent 36%),
    radial-gradient(ellipse at 95% 40%,#e8ddcf 0,transparent 38%),
    var(--bg);
  font-family:Georgia,"Times New Roman",serif;
  overflow-x:hidden;
}
button,input{font:inherit}
button,a{-webkit-tap-highlight-color:transparent}
a{color:inherit;text-decoration:none}
button{cursor:pointer}
::selection{background:#d8c2aa;color:#30271e}

#ambient{
  position:fixed;inset:0;
  overflow:hidden;pointer-events:none;
  z-index:0;
}
.spark{
  position:absolute;
  top:var(--top);left:var(--left);
  color:var(--star-color);
  font-size:var(--size);
  opacity:0;
  animation:twinkle var(--duration) var(--delay) infinite ease-in-out;
}
@keyframes twinkle{
  0%,100%{opacity:.12;transform:scale(.75)}
  50%{opacity:.7;transform:scale(1.2)}
}
.floating{
  position:fixed;
  bottom:-35px;left:var(--left);
  font-size:var(--size);
  opacity:0;
  color:#b8a18a;
  animation:floatUp var(--duration) linear forwards;
  pointer-events:none;
  z-index:2;
}
@keyframes floatUp{
  0%{transform:translateY(0) rotate(0);opacity:0}
  12%{opacity:.6}
  90%{opacity:.35}
  100%{transform:translateY(-110vh) rotate(40deg);opacity:0}
}
nav{
  position:sticky;top:0;z-index:20;
  display:flex;align-items:center;justify-content:space-between;
  gap:12px;padding:14px 5%;
  background:#f8f2e9eF;
  border-bottom:1px solid #e6dbcc;
  backdrop-filter:blur(14px);
}
.logo{font-size:1rem;letter-spacing:1px;white-space:nowrap}
.logo span{color:var(--accent)}
.navlinks{
  display:flex;gap:14px;overflow-x:auto;
  font:11px Arial,sans-serif;color:var(--muted);
}
.navlinks a{white-space:nowrap}
.navlinks a:hover{color:var(--ink)}
main,footer{position:relative;z-index:1}
section{padding:68px 6%;position:relative}
.hero{
  min-height:88vh;
  display:flex;flex-direction:column;
  align-items:center;justify-content:center;
  text-align:center;padding-top:70px;
}
.moon{font-size:2.5rem;animation:moonGlow 4s ease-in-out infinite}
@keyframes moonGlow{
  50%{filter:drop-shadow(0 0 15px #c6ae8b);transform:translateY(-4px)}
}
.eyebrow{
  font:10px Arial,sans-serif;
  text-transform:uppercase;letter-spacing:3px;
  color:var(--accent);
}
h1{
  margin:22px 0 12px;
  font-size:clamp(3.7rem,15vw,7.5rem);
  font-weight:normal;line-height:.95;
  letter-spacing:-3px;
}
h1 em{font-weight:normal;color:var(--accent)}
h2{
  margin:12px 0 18px;
  font-size:clamp(2rem,7vw,3.2rem);
  font-weight:normal;line-height:1.12;
}
h3{font-weight:normal}
p{line-height:1.85}
.hero p{max-width:480px}
.subtle{color:var(--muted)}
.small{font:11px Arial,sans-serif;color:var(--muted);line-height:1.7}
.section-head{text-align:center;max-width:650px;margin:0 auto 30px}
.section-head p{max-width:530px;margin-left:auto;margin-right:auto}
.rule{width:48px;height:1px;background:var(--accent2);margin:22px auto}
.button{
  display:inline-block;border:1px solid var(--accent);
  background:var(--ink);color:var(--paper);
  border-radius:40px;padding:13px 21px;
  font-size:12px;letter-spacing:.5px;
  transition:transform .2s,background .2s;
}
.button:hover{transform:translateY(-3px);background:#66584a}
.button.secondary{background:transparent;color:var(--ink);border-color:var(--line)}
.button.secondary:hover{background:var(--paper)}
.button-row{display:flex;justify-content:center;gap:10px;flex-wrap:wrap;margin-top:20px}
.card{
  background:#fffaf2d9;
  border:1px solid #fffdf7;
  border-radius:23px;padding:24px;
  box-shadow:var(--shadow);
}
.center{text-align:center}
.tag{
  display:inline-block;padding:7px 12px;margin:4px;
  border-radius:30px;background:#eee4d7;
  color:#66594b;font:11px Arial,sans-serif;
}
.grid2{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.tile{
  border:1px solid #e5d9c8;background:#fff9f0;
  border-radius:18px;padding:17px;
}
.tile .symbol{font-size:1.7rem}
.tile h3{margin:10px 0 6px;font-size:1.05rem}
.tile p{margin:0;font-size:.88rem}
.quote-card{
  max-width:640px;margin:auto;text-align:center;
  background:#eae0d2;border-radius:22px;padding:30px 22px;
}
.quote-mark{font-size:2.5rem;color:var(--accent2);line-height:1}
.quote-text{font-size:clamp(1.25rem,4vw,1.8rem);line-height:1.55}
.quote-author{font:10px Arial,sans-serif;letter-spacing:2px;text-transform:uppercase;color:var(--muted)}
.gallery{display:grid;grid-template-columns:repeat(2,minmax(0,1fr));gap:13px}
.photo-card{
  padding:8px 8px 12px;background:#fffdf8;
  border:1px solid #e9dfd1;border-radius:7px;
  box-shadow:0 8px 22px #5c473015;
}
.photo-card:nth-child(even){transform:rotate(1deg)}
.photo-card:nth-child(odd){transform:rotate(-1deg)}
.photo-card img{
  width:100%;aspect-ratio:3/4;object-fit:cover;
  background:#e7ddcf;display:block;cursor:pointer;
  border-radius:3px;
}
.photo-card figcaption{text-align:center;padding-top:10px;font-size:.83rem}
.placeholder{
  aspect-ratio:3/4;background:#e9dfd1;
  display:flex;flex-direction:column;
  align-items:center;justify-content:center;
  text-align:center;color:#8b7964;padding:10px;
}
.placeholder span{font-size:2rem}
.placeholder small{font:10px Arial,sans-serif;line-height:1.6}
.photo-tip{text-align:center;font:11px Arial,sans-serif;color:var(--muted);margin-top:20px}
.music-art{
  width:150px;height:150px;border-radius:50%;
  margin:0 auto 22px;display:grid;place-items:center;
  background:radial-gradient(circle,#fffaf2,#e1d1bd);
  font-size:3.5rem;border:1px solid #e4d5c1;
  box-shadow:0 0 0 9px #eee4d7;
}
audio{width:100%;margin:12px 0}
.progress-wrap{height:4px;background:#e1d4c4;border-radius:20px;overflow:hidden}
.progress-fill{height:100%;width:0;background:#94785c}
.music-times{display:flex;justify-content:space-between;font:10px Arial,sans-serif;color:var(--muted)}
.reveal-card{
  width:100%;min-height:145px;
  text-align:left;border:1px solid #e6d9c8;
  border-radius:18px;background:#fffaf2;
  padding:17px;color:var(--ink);
}
.reveal-card .reveal-icon{font-size:1.5rem;display:block;margin-bottom:10px}
.reveal-card .reveal-answer{display:none;font-size:.9rem;line-height:1.7}
.reveal-card.open .reveal-prompt{display:none}
.reveal-card.open .reveal-answer{display:block;animation:appear .35s}
@keyframes appear{from{opacity:0;transform:translateY(8px)}to{opacity:1;transform:translateY(0)}}
.journal-entry{padding:16px 0;border-bottom:1px solid var(--line)}
.journal-entry:last-child{border-bottom:0}
.journal-entry strong{font-weight:normal;color:var(--accent)}
.journal-entry p{margin:7px 0}
.input-row{display:flex;gap:8px;margin-top:15px}
.input-row input{
  flex:1;min-width:0;border:1px solid var(--line);
  background:#fffdf8;border-radius:12px;padding:12px;
  color:var(--ink);
}
.result{min-height:28px;color:var(--accent);font-size:.9rem}
.mini-game{
  background:#f0e6d8;border-radius:20px;padding:20px;text-align:center;
}
.game-button{
  width:56px;height:56px;border-radius:50%;
  border:1px solid #d8c5ad;background:#fffaf2;
  margin:5px;font-size:1.5rem;
}
.game-button.selected{background:#d5c1a8;transform:scale(.95)}
#secretNote{display:none}
#secretNote.show{display:block;animation:appear .5s}
footer{text-align:center;padding:45px 18px 55px;border-top:1px solid #e4d8c9;background:#eee5d9}
footer .moon{font-size:2rem}
#toast{
  position:fixed;bottom:18px;left:50%;transform:translateX(-50%);
  background:#403b35;color:#fffaf2;padding:12px 17px;
  border-radius:30px;font:12px Arial,sans-serif;
  display:none;z-index:1100;text-align:center;max-width:90%;
}
#lightbox{
  display:none;position:fixed;inset:0;z-index:1000;
  background:#28231feF;align-items:center;justify-content:center;padding:18px;
}
#lightbox.open{display:flex}
#lightbox img{max-width:100%;max-height:82vh;object-fit:contain;border-radius:10px}
#lightbox button{
  position:absolute;top:15px;right:15px;
  border:0;border-radius:50%;width:42px;height:42px;
  background:#fffaf2;color:var(--ink);font-size:1.4rem;
}
#topBtn{
  position:fixed;bottom:18px;right:15px;z-index:15;
  width:42px;height:42px;border-radius:50%;
  background:#fffaf2eF;border:1px solid var(--line);
  color:var(--ink);display:none;
}
.fade-in{opacity:0;transform:translateY(16px);transition:opacity .7s,transform .7s}
.fade-in.visible{opacity:1;transform:translateY(0)}
@media(min-width:700px){
  section{padding:90px 10%}
  .gallery{grid-template-columns:repeat(3,minmax(0,1fr));gap:20px}
  .grid2{grid-template-columns:repeat(3,minmax(0,1fr))}
  .reveal-grid{grid-template-columns:repeat(3,minmax(0,1fr))}
  .hero{min-height:90vh}
}
@media(max-width:380px){
  nav{padding:12px 4%}
  .navlinks{gap:9px;font-size:10px}
  .logo{font-size:.88rem}
  section{padding:55px 5%}
  .card{padding:18px}
  .grid2{gap:8px}
  .tile{padding:12px}
  .input-row{flex-direction:column}
}
@media(prefers-reduced-motion:reduce){
  *,*:before,*:after{animation:none!important;scroll-behavior:auto!important;transition:none!important}
  .fade-in{opacity:1;transform:none}
}
</style>
</head>

<body>
<div id="ambient" aria-hidden="true"></div>

<nav>
  <a class="logo" href="#home">LISKUN <span>✧</span></a>
  <div class="navlinks">
    <a href="#about">About</a>
    <a href="#vibe">My vibe</a>
    <a href="#quotes">Words</a>
    <a href="#gallery">Gallery</a>
    <a href="#secret">Secret</a>
  </div>
</nav>

<main>
<!-- 01 / HERO -->
<section class="hero" id="home">
  <div class="moon">☾</div>
  <p class="eyebrow">A small corner of the internet</p>
  <h1>Biraja<br><em>Prasad Jena.</em></h1>
  <p class="subtle">But you can call me <strong>Liskun.</strong></p>
  <div class="rule"></div>
  <p>Quiet outside, many thoughts inside.<br>Still becoming, never pretending.</p>
  <div class="button-row">
    <a class="button" href="#about">Get to know me ↗</a>
    <button class="button secondary" id="heroQuote">A thought for today ✧</button>
  </div>
  <p class="small" style="margin-top:45px">SCROLL SLOWLY · THERE'S NO RUSH</p>
</section>

<!-- 02 / ABOUT -->
<section id="about">
  <div class="section-head fade-in">
    <p class="eyebrow">A little introduction</p>
    <h2>Who is Liskun?</h2>
    <p class="subtle">Not a perfect story. Just a real person, figuring things out one day at a time.</p>
  </div>
  <div class="card fade-in">
    <p>Hey, I'm <strong>Biraja Prasad Jena</strong> — also known as Liskun. 🌙</p>
    <p>I'm someone who enjoys quiet moments, meaningful thoughts, music, gaming and the little things that make ordinary days memorable. I believe there is always something new to learn, something to improve and another version of ourselves waiting to grow.</p>
    <p>I'm still figuring life out, chasing my goals at my own pace, and learning that you don't need to have everything sorted out to move forward.</p>
    <p class="center"><em>“Still becoming, never pretending.”</em></p>
  </div>
  <div class="center" style="margin-top:22px">
    <span class="tag">🌙 Quiet thinker</span>
    <span class="tag">🎧 Music lover</span>
    <span class="tag">🎮 Gamer</span>
    <span class="tag">📚 Always learning</span>
    <span class="tag">✨ Work in progress</span>
  </div>
</section>

<!-- 03 / PERSONAL VIBE -->
<section id="vibe">
  <div class="section-head fade-in">
    <p class="eyebrow">Things I enjoy</p>
    <h2>My little universe.</h2>
    <p class="subtle">A few things that make up my everyday world.</p>
  </div>
  <div class="grid2 fade-in">
    <div class="tile">
      <div class="symbol">🎧</div>
      <h3>Music</h3>
      <p>Some feelings are easier to understand when there's a song playing in the background.</p>
    </div>
    <div class="tile">
      <div class="symbol">🌌</div>
      <h3>Deep thoughts</h3>
      <p>Thinking about life, people, time and the little lessons hidden in ordinary moments.</p>
    </div>
    <div class="tile">
      <div class="symbol">🎮</div>
      <h3>Gaming</h3>
      <p>A little competition, a little fun, and a good way to enjoy some free time.</p>
    </div>
    <div class="tile">
      <div class="symbol">📚</div>
      <h3>College life</h3>
      <p>Learning new things, collecting experiences and growing beyond the classroom.</p>
    </div>
    <div class="tile">
      <div class="symbol">📝</div>
      <h3>Words & quotes</h3>
      <p>Short lines that stay in your mind long after you've finished reading them.</p>
    </div>
    <div class="tile">
      <div class="symbol">🌱</div>
      <h3>Personal growth</h3>
      <p>Small steps count, even when nobody else can see the progress.</p>
    </div>
  </div>
</section>

<!-- 04 / QUOTES -->
<section id="quotes">
  <div class="section-head fade-in">
    <p class="eyebrow">A thought to keep</p>
    <h2>Words for the quiet moments.</h2>
    <p class="subtle">Tap the button whenever you want a different thought.</p>
  </div>
  <div class="quote-card fade-in">
    <div class="quote-mark">“</div>
    <p class="quote-text" id="quoteText">You don't need to have your whole life figured out to take the next small step.</p>
    <p class="quote-author" id="quoteAuthor">A LITTLE REMINDER</p>
    <button class="button secondary" id="nextQuote">Another thought ↗</button>
    <button class="button secondary" id="copyQuote">Copy quote</button>
    <p class="small" id="quoteStatus" aria-live="polite"></p>
  </div>
  <div class="grid2" style="margin-top:20px">
    <div class="tile"><h3>On life</h3><p>Life doesn't always move at the speed you want. Keep going at the pace you can.</p></div>
    <div class="tile"><h3>On people</h3><p>Be kind, keep your boundaries, and let actions tell you what words cannot.</p></div>
    <div class="tile"><h3>On growth</h3><p>You can be proud of how far you've come and still want to grow further.</p></div>
    <div class="tile"><h3>On peace</h3><p>Not every situation needs a reaction. Sometimes peace is enough.</p></div>
  </div>
</section>

<!-- 05 / PHOTO GALLERY -->
<section id="gallery">
  <div class="section-head fade-in">
    <p class="eyebrow">A few frames from my world</p>
    <h2>Little memories.</h2>
    <p class="subtle">A place for photos that mean something to me.</p>
  </div>
  <div class="gallery fade-in">
    <!-- Replace photo1.jpg, photo2.jpg etc. with your own image filenames. -->
    <figure class="photo-card">
      <div class="placeholder"><span>☾</span><small>YOUR PHOTO 01<br>Replace with photo1.jpg</small></div>
      <figcaption>A moment worth keeping.</figcaption>
    </figure>
    <figure class="photo-card">
      <div class="placeholder"><span>✧</span><small>YOUR PHOTO 02<br>Replace with photo2.jpg</small></div>
      <figcaption>Just being myself.</figcaption>
    </figure>
    <figure class="photo-card">
      <div class="placeholder"><span>🌿</span><small>YOUR PHOTO 03<br>Replace with photo3.jpg</small></div>
      <figcaption>A little piece of life.</figcaption>
    </figure>
    <figure class="photo-card">
      <div class="placeholder"><span>☁</span><small>YOUR PHOTO 04<br>Replace with photo4.jpg</small></div>
      <figcaption>Somewhere in between.</figcaption>
    </figure>
    <figure class="photo-card">
      <div class="placeholder"><span>🌙</span><small>YOUR PHOTO 05<br>Replace with photo5.jpg</small></div>
      <figcaption>One for the memories.</figcaption>
    </figure>
    <figure class="photo-card">
      <div class="placeholder"><span>♡</span><small>YOUR PHOTO 06<br>Replace with photo6.jpg</small></div>
      <figcaption>More chapters to come.</figcaption>
    </figure>
  </div>
  <p class="photo-tip">Tip: Upload your pictures to the same GitHub folder and use the instructions below the code to display them.</p>
</section>

<!-- 06 / MUSIC -->
<section id="music">
  <div class="section-head fade-in">
    <p class="eyebrow">Press play, take a breath</p>
    <h2>My mood, in music.</h2>
  </div>
  <div class="card center fade-in" style="max-width:500px;margin:auto">
    <div class="music-art">♫</div>
    <p class="eyebrow">NOW PLAYING</p>
    <h3 id="trackTitle">Your favourite song</h3>
    <p class="small">Add a song you love and make this corner yours.</p>
    <!-- Add a legally usable audio file named song.mp3 to your repository. -->
    <audio id="audioPlayer" controls preload="metadata">
      <source src="song.mp3" type="audio/mpeg">
      Your browser does not support audio playback.
    </audio>
    <div class="music-times"><span id="elapsed">0:00</span><span id="duration">0:00</span></div>
    <div class="progress-wrap"><div class="progress-fill" id="musicProgress"></div></div>
    <p class="small">Music starts only when you press play.</p>
  </div>
</section>

<!-- 07 / LITTLE THINGS -->
<section id="little-things">
  <div class="section-head fade-in">
    <p class="eyebrow">Tap to uncover</p>
    <h2>A few things I believe.</h2>
  </div>
  <div class="grid2 reveal-grid fade-in">
    <button class="reveal-card">
      <span class="reveal-icon">🌱</span>
      <strong class="reveal-prompt">Something I remind myself</strong>
      <span class="reveal-answer">Growth can be quiet. Not every improvement needs an audience.</span>
    </button>
    <button class="reveal-card">
      <span class="reveal-icon">🕊️</span>
      <strong class="reveal-prompt">Something worth protecting</strong>
      <span class="reveal-answer">Your peace, your self-respect, and your ability to be kind without losing yourself.</span>
    </button>
    <button class="reveal-card">
      <span class="reveal-icon">🌙</span>
      <strong class="reveal-prompt">Something about me</strong>
      <span class="reveal-answer">I may not say everything out loud, but I enjoy thinking deeply about the things that matter to me.</span>
    </button>
    <button class="reveal-card">
      <span class="reveal-icon">🧭</span>
      <strong class="reveal-prompt">A lesson I'm learning</strong>
      <span class="reveal-answer">Not knowing every answer doesn't mean you're going nowhere. Keep learning and adjusting.</span>
    </button>
    <button class="reveal-card">
      <span class="reveal-icon">☁</span>
      <strong class="reveal-prompt">A gentle reminder</strong>
      <span class="reveal-answer">You are allowed to rest without feeling guilty for not being productive every moment.</span>
    </button>
    <button class="reveal-card">
      <span class="reveal-icon">✨</span>
      <strong class="reveal-prompt">My personal motto</strong>
      <span class="reveal-answer">Still becoming, never pretending. I'd rather grow honestly than act like I've already arrived.</span>
    </button>
  </div>
</section>

<!-- 08 / MINI JOURNAL -->
<section id="journal">
  <div class="section-head fade-in">
    <p class="eyebrow">Notes to myself</p>
    <h2>Little journal.</h2>
    <p class="subtle">Thoughts worth remembering. These are sample entries you can edit directly in the HTML.</p>
  </div>
  <div class="card fade-in">
    <div class="journal-entry">
      <strong>NOTE 01 · KEEP GOING</strong>
      <p>You don't have to move fast. You just have to keep making choices that take you closer to the person you want to become.</p>
    </div>
    <div class="journal-entry">
      <strong>NOTE 02 · STAY GENUINE</strong>
      <p>It's okay if everyone doesn't understand you. Be willing to learn, but don't build your entire life around approval.</p>
    </div>
    <div class="journal-entry">
      <strong>NOTE 03 · MAKE ROOM FOR JOY</strong>
      <p>Take your goals seriously, but leave space for music, laughter, good conversations and simple moments.</p>
    </div>
  </div>
</section>

<!-- 09 / INTERACTIVE GAME -->
<section id="game">
  <div class="section-head fade-in">
    <p class="eyebrow">A tiny moment of fun</p>
    <h2>Choose a moon. 🌙</h2>
    <p class="subtle">Three moons, three small messages. Pick whichever one you like.</p>
  </div>
  <div class="mini-game fade-in">
    <button class="game-button" data-message="Keep moving at your own pace. Small steps are still steps." aria-label="Moon one">☾</button>
    <button class="game-button" data-message="You don't need to pretend to be someone else to belong." aria-label="Moon two">☽</button>
    <button class="game-button" data-message="Give yourself the same patience you give to people you care about." aria-label="Moon three">🌙</button>
    <p id="moonMessage" class="result">Choose your moon to reveal a message.</p>
  </div>
</section>

<!-- 10 / SECRET MESSAGE -->
<section id="secret">
  <div class="section-head fade-in">
    <p class="eyebrow">A little hidden corner</p>
    <h2>Something behind the stars.</h2>
    <p class="subtle">Curiosity brought you here. Tap below. ✧</p>
  </div>
  <div class="card center fade-in">
    <div style="font-size:2.5rem">✧ ☾ ✧</div>
    <button class="button" id="secretButton">Reveal the hidden note</button>
    <div id="secretNote">
      <div class="rule"></div>
      <p><strong>Hey, you. Yes, you. 🤍</strong></p>
      <p>If you're reading this, here's a small reminder: you don't need to have every part of your life figured out right now.</p>
      <p>Be honest about where you are, patient about where you're going, and proud of the effort nobody else sees.</p>
      <p>You're allowed to change your mind, learn from mistakes and begin again.</p>
      <p><em>Keep becoming. Keep being real. — Liskun 🌙</em></p>
    </div>
  </div>
</section>

<!-- 11 / FINAL -->
<section id="end">
  <div class="section-head fade-in">
    <p class="eyebrow">Before you leave</p>
    <h2>That's a little bit of me.</h2>
    <p class="subtle">Thanks for spending a moment in my corner of the internet.</p>
  </div>
  <div class="quote-card fade-in">
    <div class="moon">☾</div>
    <p class="quote-text">“I don't have to be finished to be proud of the journey.”</p>
    <div class="rule"></div>
    <p class="quote-author">BIRAJA PRASAD JENA · LISKUN</p>
    <p>Still becoming, never pretending.</p>
    <button class="button" id="leaveMessage">Leave with a little positivity ✧</button>
    <p id="goodbyeMessage" class="result"></p>
  </div>
</section>
</main>

<footer>
  <div class="moon">☾</div>
  <p><strong>Biraja Prasad Jena</strong></p>
  <p class="small">Known as Liskun · Still becoming, never pretending.</p>
  <p class="small">Made with a quiet mind and a little imagination.</p>
  <a href="#home" class="small">Back to the moon ↑</a>
</footer>

<button id="topBtn" aria-label="Back to top">↑</button>
<div id="toast" role="status" aria-live="polite"></div>

<div id="lightbox" role="dialog" aria-label="Expanded photograph">
  <button id="closeLightbox" aria-label="Close photo">×</button>
  <img id="lightboxImage" src="" alt="Expanded personal memory">
</div>

<script>
/* Gentle background stars */
(function createStars(){
  const ambient=document.getElementById("ambient");
  const symbols=["✧","·","✦","⋆","✳"];
  for(let i=0;i<48;i++){
    const star=document.createElement("span");
    star.className="spark";
    star.textContent=symbols[Math.floor(Math.random()*symbols.length)];
    star.style.setProperty("--top",Math.random()*100+"%");
    star.style.setProperty("--left",Math.random()*100+"%");
    star.style.setProperty("--size",(7+Math.random()*12)+"px");
    star.style.setProperty("--duration",(3+Math.random()*5)+"s");
    star.style.setProperty("--delay",(-Math.random()*6)+"s");
    star.style.setProperty("--star-color",Math.random()>.5?"#aa9277":"#d0b99e");
    ambient.appendChild(star);
  }
})();

/* Floating symbols, with a gentle pace */
const reducedMotion=window.matchMedia("(prefers-reduced-motion: reduce)").matches;
if(!reducedMotion){
  setInterval(()=>{
    const symbol=document.createElement("span");
    symbol.className="floating";
    symbol.textContent=["✧","♡","⋆","☾","·"][Math.floor(Math.random()*5)];
    symbol.style.setProperty("--left",Math.random()*100+"%");
    symbol.style.setProperty("--size",(12+Math.random()*15)+"px");
    symbol.style.setProperty("--duration",(9+Math.random()*7)+"s");
    document.body.appendChild(symbol);
    setTimeout(()=>symbol.remove(),17000);
  },1600);
}

/* Random thoughtful quotes */
const quotes=[
  ["You don't need to have your whole life figured out to take the next small step.","A LITTLE REMINDER"],
  ["Be kind, but remember that boundaries are a form of self-respect.","ON PEOPLE"],
  ["A quiet season can still be a season of growth.","ON GROWTH"],
  ["Not every thought needs to become a worry. Let some things pass.","ON PEACE"],
  ["You can start again without explaining your entire story to everyone.","ON BEGINNINGS"],
  ["Make a life you enjoy living, not just one that looks impressive.","ON LIFE"],
  ["You are allowed to be a work in progress and still appreciate yourself.","ON SELF-WORTH"],
  ["Consistency is often quieter than motivation, but it carries you further.","ON GOALS"],
  ["Protect your peace without losing your kindness.","ON BALANCE"],
  ["Be genuine. The right people won't need you to pretend.","ON BEING REAL"],
  ["Some answers arrive when you give yourself time to breathe.","ON PATIENCE"],
  ["Keep your heart kind and your eyes open.","A THOUGHT TO KEEP"],
  ["Small steps still count on the days when progress feels invisible.","ON PROGRESS"],
  ["You can be grateful for today and still dream of tomorrow.","ON DREAMS"],
  ["Not every ending is a failure; some endings make room for change.","ON CHANGE"]
];
let currentQuote=-1;

function showRandomQuote(){
  let next;
  do{next=Math.floor(Math.random()*quotes.length)}while(next===currentQuote&&quotes.length>1);
  currentQuote=next;
  document.getElementById("quoteText").textContent=quotes[next][0];
  document.getElementById("quoteAuthor").textContent=quotes[next][1];
  document.getElementById("quoteStatus").textContent="";
}
document.getElementById("nextQuote").addEventListener("click",showRandomQuote);
document.getElementById("heroQuote").addEventListener("click",()=>{
  showRandomQuote();
  document.getElementById("quotes").scrollIntoView({behavior:reducedMotion?"auto":"smooth"});
});

function showToast(message){
  const toast=document.getElementById("toast");
  toast.textContent=message;
  toast.style.display="block";
  clearTimeout(showToast.timer);
  showToast.timer=setTimeout(()=>toast.style.display="none",2400);
}

document.getElementById("copyQuote").addEventListener("click",async()=>{
  const text=document.getElementById("quoteText").textContent;
  try{
    await navigator.clipboard.writeText("“"+text+"”");
    document.getElementById("quoteStatus").textContent="Quote copied ✧";
  }catch(e){
    document.getElementById("quoteStatus").textContent="Select and copy the quote manually.";
  }
});

/* Tap-to-reveal cards */
document.querySelectorAll(".reveal-card").forEach(card=>{
  card.addEventListener("click",()=>card.classList.toggle("open"));
});

/* Three little moons */
document.querySelectorAll(".game-button").forEach(button=>{
  button.addEventListener("click",()=>{
    document.querySelectorAll(".game-button").forEach(b=>b.classList.remove("selected"));
    button.classList.add("selected");
    document.getElementById("moonMessage").textContent=button.dataset.message;
  });
});

/* Secret note */
document.getElementById("secretButton").addEventListener("click",()=>{
  const note=document.getElementById("secretNote");
  const open=note.classList.toggle("show");
  document.getElementById("secretButton").textContent=open?"Hide the hidden note":"Reveal the hidden note";
});

/* Music timer */
const audio=document.getElementById("audioPlayer");
function formatTime(seconds){
  if(!Number.isFinite(seconds)||seconds<0)return "0:00";
  return Math.floor(seconds/60)+":"+String(Math.floor(seconds%60)).padStart(2,"0");
}
function updateMusic(){
  document.getElementById("elapsed").textContent=formatTime(audio.currentTime);
  document.getElementById("duration").textContent=formatTime(audio.duration);
  const percent=Number.isFinite(audio.duration)&&audio.duration>0?(audio.currentTime/audio.duration)*100:0;
  document.getElementById("musicProgress").style.width=percent+"%";
}
audio.addEventListener("timeupdate",updateMusic);
audio.addEventListener("loadedmetadata",updateMusic);
audio.addEventListener("durationchange",updateMusic);

/* Photo placeholders become real photos when files are supplied */
const photoNames=["photo1.jpg","photo2.jpg","photo3.jpg","photo4.jpg","photo5.jpg","photo6.jpg"];
document.querySelectorAll(".photo-card").forEach((figure,index)=>{
  const name=photoNames[index];
  const img=new Image();
  img.onload=()=>{
    const placeholder=figure.querySelector(".placeholder");
    const photo=document.createElement("img");
    photo.src=name;
    photo.alt="Personal photograph "+(index+1);
    photo.loading="lazy";
    placeholder.replaceWith(photo);
    photo.addEventListener("click",()=>openLightbox(photo));
  };
  img.onerror=()=>{};
  img.src=name;
});

function openLightbox(img){
  document.getElementById("lightboxImage").src=img.src;
  document.getElementById("lightbox").classList.add("open");
}
function closeLightbox(){
  document.getElementById("lightbox").classList.remove("open");
  document.getElementById("lightboxImage").src="";
}
document.getElementById("closeLightbox").addEventListener("click",closeLightbox);
document.getElementById("lightbox").addEventListener("click",e=>{
  if(e.target.id==="lightbox")closeLightbox();
});
document.addEventListener("keydown",e=>{
  if(e.key==="Escape")closeLightbox();
});

/* Gentle reveal on scroll */
const fadeElements=document.querySelectorAll(".fade-in");
if("IntersectionObserver" in window&&!reducedMotion){
  const observer=new IntersectionObserver(entries=>{
    entries.forEach(entry=>{
      if(entry.isIntersecting){
        entry.target.classList.add("visible");
        observer.unobserve(entry.target);
      }
    });
  },{threshold:.12});
  fadeElements.forEach(el=>observer.observe(el));
}else{
  fadeElements.forEach(el=>el.classList.add("visible"));
}

/* Back-to-top button */
const topBtn=document.getElementById("topBtn");
window.addEventListener("scroll",()=>{
  topBtn.style.display=window.scrollY>500?"block":"none";
},{passive:true});
topBtn.addEventListener("click",()=>window.scrollTo({top:0,behavior:reducedMotion?"auto":"smooth"}));

/* Final message */
const goodbyeMessages=[
  "Take care of yourself. You're doing better than you think. 🌙",
  "May your next chapter bring learning, laughter and peace. ✧",
  "Keep being genuine. Keep becoming. — Liskun 🤍",
  "One step at a time. There's no need to rush your whole life."
];
document.getElementById("leaveMessage").addEventListener("click",()=>{
  document.getElementById("goodbyeMessage").textContent=
    goodbyeMessages[Math.floor(Math.random()*goodbyeMessages.length)];
});
</script>
</body>
</html>
