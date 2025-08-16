 <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta http-equiv="X-UA-Compatible" content="IE=edge" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Happy Birthday — Mazharul Islam Udoy</title>
  <meta name="color-scheme" content="light" />
  <style>
    :root{
      --pink:#ffd7ea;           /* light pink */
      --lpink:#fff0f7;          /* softer light pink */
      --text:#1e1e1e;
      --accent:#ff4da6;
      --balloon1:#ff6b6b;       /* coral */
      --balloon2:#6bc5ff;       /* sky */
      --gold:#ffd166;           /* warm gold */
      --bg-dark:#0a0a0a;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0; font-family: ui-rounded, system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial, "Noto Sans";
      color:var(--text); background:var(--bg-dark); overflow:hidden; -webkit-font-smoothing:antialiased; text-rendering:optimizeLegibility;
    }

    /* Utility */
    [data-step]{ display:none }
    body.step-1 [data-step="1"], body.step-2 [data-step="2"], body.step-3 [data-step="3"]{ display:block }
    [hidden]{display:none !important}
    .center{ position:absolute; inset:0; display:flex; align-items:center; justify-content:center; flex-direction:column; gap:16px; padding:24px; text-align:center }
    button{ border:0; padding:16px 28px; font-weight:800; letter-spacing:.3px; font-size:clamp(16px,4vw,22px); border-radius:999px; cursor:pointer;
      background: linear-gradient(135deg,#ff9ec9,#ff3f89 60%, #b50059); color:#fff; box-shadow:0 12px 28px rgba(255,63,137,.35);
      transition: transform .18s ease, box-shadow .25s ease, filter .25s ease;
    }
    button:hover{ transform: translateY(-1px); filter:saturate(1.05) }
    button:active{ transform: translateY(1px) scale(.99) }

    /* STEP 1 — Welcome (Canvas particles from four sides toward center) */
    .step-1{ background: radial-gradient(60vw 60vw at 50% -10%, rgba(255,255,255,.06), transparent), var(--bg-dark); }
    .hero{ position:absolute; inset:0; display:grid; place-items:center; pointer-events:none }
    #welcomeCanvas{ width:100%; height:100%; display:block; }
    .title{ position:absolute; top:8%; left:50%; transform:translateX(-50%); color:#fff; font-weight:900; letter-spacing:.6px; text-align:center;
      text-shadow:0 4px 26px rgba(0,0,0,.45); font-size: clamp(22px,6vw,44px); pointer-events:none }

    /* STEP 2 — Celebration */
    .step-2{ background: linear-gradient(180deg, var(--lpink), var(--pink)); }
    .congratz{ position:absolute; top:14px; left:50%; transform:translateX(-50%); text-align:center; font-weight:900; letter-spacing:1px;
      font-size:clamp(22px,7vw,56px); color:transparent; background:conic-gradient(from 180deg, #ff7ecb, #ffc93d, #7ef9ff, #9cff6a, #ff7ecb);
      -webkit-background-clip:text; background-clip:text; filter: drop-shadow(0 6px 16px rgba(0,0,0,.08));
      animation: popIn .9s ease both, hue 6s linear infinite;
    }
    @keyframes popIn{ from{ opacity:0; transform:translateX(-50%) translateY(-12px) scale(.96);} to{opacity:1; transform:translateX(-50%) translateY(0) scale(1);} }
    @keyframes hue{ to{ filter: hue-rotate(360deg) drop-shadow(0 6px 16px rgba(0,0,0,.1)); } }

    .petals{ position:absolute; inset:0; pointer-events:none; overflow:hidden }
    .petal{ position:absolute; top:-10vh; font-size:clamp(16px, 4vw, 26px); will-change:transform; opacity:.95; user-select:none;
      animation: petalFall linear var(--dur) var(--delay) infinite; }
    @keyframes petalFall{ 0%{ transform: translateY(-12vh) translateX(0) rotate(0deg)} 100%{ transform: translateY(120vh) translateX(var(--shift, 0)) rotate(360deg)} }

    .balloon{ position:absolute; top:-40vh; width:clamp(64px, 22vw, 128px); height:clamp(84px, 30vw, 168px); border-radius:50% 50% 48% 48%/60% 60% 40% 40%;
      display:flex; align-items:center; justify-content:center; color:#fff; font-weight:900; text-shadow:0 2px 12px rgba(0,0,0,.25);
      font-size: clamp(24px, 9vw, 56px); box-shadow: inset 0 -18px 28px rgba(0,0,0,.12); opacity:0;
      animation: dropIn 1.8s cubic-bezier(.2,.85,.2,1.1) forwards; }
    .balloon::after{ content:""; position:absolute; bottom:-26px; left:50%; transform:translateX(-50%); width:2px; height:56vh; background:rgba(0,0,0,.15) }
    .b1{ left:20%; background: radial-gradient(50% 60% at 30% 20%, rgba(255,255,255,.7), transparent 60%), var(--balloon1); animation-delay: .8s }
    .b2{ right:20%; background: radial-gradient(50% 60% at 30% 20%, rgba(255,255,255,.7), transparent 60%), var(--balloon2); animation-delay: 1.2s }
    @keyframes dropIn{ from{ transform:translateY(-60vh) scale(.95); opacity:0 } to{ transform:translateY(18vh) scale(1); opacity:1 } }

    /* STEP 3 — Cake & Candles */
    .step-3{ background: radial-gradient(80vw 80vw at 50% -10%, rgba(255,255,255,.35), rgba(255,255,255,0)), linear-gradient(180deg,#ffeef6,#ffd7ea); }
    .cake-wrap{ position:absolute; inset:0; display:grid; place-items:center; }
    .cake{ position:relative; width:min(86vw, 520px); height:min(60vw, 360px); cursor:pointer }
    .plate{ position:absolute; bottom:0; left:50%; transform:translateX(-50%); width:100%; height:24px; border-radius:999px; background:linear-gradient(180deg,#fff,#dedede); box-shadow:0 18px 28px rgba(0,0,0,.12) }
    .layer{ position:absolute; left:50%; transform:translateX(-50%); width:84%; border-radius:24px; background:#ffb6d9; box-shadow: inset 0 -12px 0 #ff8cc6 }
    .layer.t1{ bottom:24px; height:80px }
    .layer.t2{ bottom:94px; width:70%; height:68px }
    .layer.t3{ bottom:152px; width:54%; height:56px }
    .drip{ position:absolute; top:0; left:0; right:0; height:22px; background:#ff87c3; border-radius:24px 24px 10px 10px }

    .candles{ position:absolute; bottom: 220px; left:50%; transform:translateX(-50%); display:flex; gap:clamp(6px, 1.2vw, 12px) }
    .candle{ width:clamp(10px,2.2vw,14px); height:clamp(58px,10.5vw,74px); background:#fff; border-radius:6px; position:relative; box-shadow: inset 0 -10px 0 #ffd1ea }
    .candle::before{ content:""; position:absolute; inset:0; background: repeating-linear-gradient(45deg, #ffc1e1 0 6px, #ffffff 6px 12px); border-radius:6px; opacity:.85 }
    .flame{ position:absolute; top:-18px; left:50%; transform:translateX(-50%); width:clamp(10px,2vw,14px); height:clamp(16px,3vw,20px); border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
      background: radial-gradient(50% 60% at 50% 40%, #fff 0 20%, #ffd25a 40%, #ff8300 80%); filter: drop-shadow(0 2px 8px rgba(255,131,0,.6));
      animation: flicker .18s infinite alternate; transform-origin: 50% 100% }
    @keyframes flicker{ from{ transform:translateX(-50%) scale(1)} to{ transform:translateX(-50%) scale(1.06)} }

    /* Blow-out animation */
    .smoke{ position:absolute; top:-10px; left:50%; transform:translateX(-50%); width:6px; height:6px; border-radius:50%; background: radial-gradient(circle, rgba(200,200,200,.7), rgba(200,200,200,0)); opacity:0 }
    .blown .flame{ opacity:0; animation:none }
    .blown .smoke{ animation: puff 1.2s ease-out forwards }
    @keyframes puff{ 0%{ opacity:0; transform:translate(-50%,0) scale(.6) } 50%{ opacity:.8; transform:translate(-50%,-24px) scale(1) } 100%{ opacity:0; transform:translate(-50%,-46px) scale(1.2) } }

    /* Messages */
    .messages{ position:absolute; left:50%; bottom:8%; transform:translateX(-50%); width:min(92vw, 780px); text-align:center }
    .messages p, .messages h2{ margin:10px 0; opacity:0; transform:translateY(8px); transition: .6s ease; font-weight:700; line-height:1.35 }
    .messages h2{ font-size:clamp(22px,6vw,34px); color:#b3005d }
    .messages p{ font-size:clamp(16px,4.2vw,22px) }
    .messages .show{ opacity:1; transform:translateY(0) }

    /* Hints (small helper) */
    .hint{ position:absolute; bottom:10px; width:100%; text-align:center; font-size:12px; opacity:.55; color:#333 }

    /* Respect reduced motion */
    @media (prefers-reduced-motion: reduce){
      *{ animation-duration:.001ms !important; animation-iteration-count:1 !important; transition-duration:.001ms !important; scroll-behavior:auto !important }
    }

    /* Mobile tweaks */
    @media (max-width:420px){ .congratz{ top:8px } .balloon{ font-size:12vw } .candles{ bottom:46vw } }
  </style>
</head>
<body class="step-1">

  <!-- STEP 1: Welcome -->
  <section class="step-1" data-step="1">
    <div class="hero"><canvas id="welcomeCanvas" aria-label="Reddish particles flowing towards center" role="img"></canvas></div>
    <div class="title">Welcome, Sir Mazharul Islam Udoy 🎉</div>
    <div class="center">
      <button id="startBtn" aria-label="Go to Step 2">Sir Click Me</button>
      <div class="hint">Step 1 · Welcome animation → Click the button</div>
    </div>
  </section>

  <!-- STEP 2: Celebration -->
  <section class="step-2" data-step="2">
    <div class="congratz" aria-live="polite">Congratulations!</div>
    <div class="petals" id="petals" aria-hidden="true"></div>
    <div class="balloon b1" id="balloon2" aria-label="Balloon with number 2"><b>2</b></div>
    <div class="balloon b2" id="balloon8" aria-label="Balloon with number 8"><b>8</b></div>
    <div class="center" style="bottom:8%; top:auto">
      <div class="hint">Step 2 · Petals & balloons · Auto-next after 5s</div>
    </div>
  </section>

  <!-- STEP 3: Cake & Message -->
  <section class="step-3" data-step="3">
    <div class="cake-wrap">
      <div class="cake" id="cake" role="button" tabindex="0" aria-label="Blow the candles by clicking">
        <div class="plate"></div>
        <div class="layer t3"><div class="drip"></div></div>
        <div class="layer t2"><div class="drip"></div></div>
        <div class="layer t1"><div class="drip"></div></div>
        <div class="candles" id="candles"></div>
      </div>
      <div class="messages" id="messages">
        <h2 id="m1">Many Many Happy Birthday Sir</h2>
        <p id="m2">My Allah live you long and long, and bless you every moment of your life.</p>
        <p id="m3">Thank you sir</p>
        <p id="m4">Many many wishes for 28</p>
      </div>
      <div class="hint">Step 3 · Click the cake to blow the candles & reveal messages</div>
    </div>
  </section>

  <noscript style="position:fixed;inset:0;background:#fff;color:#000;padding:20px;z-index:9999;">
    Please enable JavaScript to view the full birthday experience.
  </noscript>

<script type="module">
  // ====== Helpers ======
  const rand = (min, max) => Math.random() * (max - min) + min;

  // ====== STEP 1: Canvas particles from all four sides toward center ======
  (function welcomeParticles(){
    const cvs = document.getElementById('welcomeCanvas');
    const ctx = cvs.getContext('2d');
    let w, h, dpr, running = true;
    const particles = [];

    function resize(){
      dpr = Math.max(1, Math.min(2, window.devicePixelRatio || 1));
      w = cvs.clientWidth; h = cvs.clientHeight;
      cvs.width = Math.floor(w * dpr); cvs.height = Math.floor(h * dpr);
      ctx.setTransform(dpr,0,0,dpr,0,0);
    }
    window.addEventListener('resize', resize, { passive:true }); resize();

    function spawn(){
      const side = Math.floor(Math.random()*4); // 0=top 1=right 2=bottom 3=left
      let x,y,vx,vy;
      const speed = rand(60, 120)/100; // .6 - 1.2 px/frame
      const cx = w/2, cy = h/2;
      if(side===0){ x = rand(0,w); y = -10; }
      if(side===1){ x = w+10; y = rand(0,h); }
      if(side===2){ x = rand(0,w); y = h+10; }
      if(side===3){ x = -10; y = rand(0,h); }
      const ang = Math.atan2(cy - y, cx - x);
      vx = Math.cos(ang) * speed; vy = Math.sin(ang) * speed;
      particles.push({ x, y, vx, vy, r: rand(2,5), life: 0, max: rand(180,300), hue: rand(350, 10+360) });
    }

    function draw(){
      if(!document.body.classList.contains('step-1')) { running = false; return; }
      ctx.clearRect(0,0,w,h);
      // soft vignette glow
      const g = ctx.createRadialGradient(w/2,h/2,0,w/2,h/2,Math.max(w,h)/1.2);
      g.addColorStop(0,'rgba(255,80,110,.08)'); g.addColorStop(1,'rgba(0,0,0,0)');
      ctx.fillStyle=g; ctx.fillRect(0,0,w,h);

      for(let i=particles.length-1;i>=0;i--){
        const p = particles[i];
        p.x += p.vx; p.y += p.vy; p.life++;
        // slight inward acceleration
        const cx=w/2, cy=h/2; const ang=Math.atan2(cy-p.y, cx-p.x); p.vx += Math.cos(ang)*0.002; p.vy += Math.sin(ang)*0.002;
        // draw glow
        ctx.beginPath();
        const grd = ctx.createRadialGradient(p.x,p.y,0,p.x,p.y,p.r*3);
        grd.addColorStop(0,`hsla(${p.hue%360},85%,60%,.9)`);
        grd.addColorStop(1,`hsla(${p.hue%360},85%,50%,0)`);
        ctx.fillStyle = grd; ctx.arc(p.x,p.y,p.r*3,0,Math.PI*2); ctx.fill();
        if(p.life>p.max) particles.splice(i,1);
      }
      for(let i=0;i<8;i++) if(particles.length<320) spawn();
      if(running) requestAnimationFrame(draw);
    }
    draw();
  })();

  // ====== STEP 2: Petals + Balloons + Auto advance ======
  function makePetals(){
    const wrap = document.getElementById('petals');
    wrap.innerHTML = '';
    const total = 30;
    const glyphs = ['❀','✿','🌸','🌷','✾','❁'];
    for(let i=0;i<total;i++){
      const f = document.createElement('div'); f.className='petal'; f.textContent = glyphs[Math.floor(Math.random()*glyphs.length)];
      f.style.left = rand(0,100)+'vw';
      f.style.setProperty('--dur', rand(4.5, 8.5)+'s');
      f.style.setProperty('--delay', rand(-2, 1)+'s');
      f.style.setProperty('--shift', (Math.random()<.5?'-':'')+rand(10, 80)+'px');
      f.style.filter = `hue-rotate(${Math.floor(rand(0,360))}deg)`;
      wrap.appendChild(f);
    }
  }

  // ====== STEP 3: Candles ======
  function makeCandles(){
    const wrap = document.getElementById('candles');
    wrap.innerHTML = '';
    const total = 8; // adjust if needed
    for(let i=0;i<total;i++){
      const c = document.createElement('div'); c.className='candle';
      const flame = document.createElement('div'); flame.className='flame';
      const smoke = document.createElement('div'); smoke.className='smoke';
      c.appendChild(flame); c.appendChild(smoke); wrap.appendChild(c);
    }
  }

  // ====== Navigation & Timing ======
  const startBtn = document.getElementById('startBtn');
  startBtn.addEventListener('click', () => {
    document.body.className = 'step-2';
    makePetals();
    // Delay balloon appearance a bit for drama
    setTimeout(() => { document.getElementById('balloon2').style.opacity = '1'; }, 200);
    setTimeout(() => { document.getElementById('balloon8').style.opacity = '1'; }, 600);
    // Auto transition to Step 3 after 5 seconds
    setTimeout(() => { document.body.className = 'step-3'; makeCandles(); }, 5000);
  }, { once:true });

  // Step 3 interactivity — blow candles then sequentially reveal wishes
  const cake = document.getElementById('cake');
  const showSeq = () => {
    const ids = ['m1','m2','m3','m4'];
    ids.forEach((id, idx) => setTimeout(() => document.getElementById(id).classList.add('show'), 400 + idx*900));
  }
  cake.addEventListener('click', () => {
    document.body.classList.add('blown');
    showSeq();
  }, { once:true });
  cake.addEventListener('keydown', (e)=>{ if(e.key==='Enter' || e.key===' ') { e.preventDefault(); cake.click(); } });

  // ====== Lightweight Self-Tests (run manually) ======
  // Run by opening with #test in the URL or calling window.__runBirthdayTests() in console
  function __runBirthdayTests(){
    const log = (...a)=>console.log('%c[test]', 'font-weight:bold;color:#b50059', ...a);
    const assert = (cond, msg)=>{ if(!cond){ console.error('[fail]', msg); } else { log('[pass]', msg); } };

    assert(document.body.classList.contains('step-1'), 'Initial step is Step 1');
    assert(document.getElementById('welcomeCanvas'), 'Welcome canvas exists');
    assert(document.getElementById('startBtn'), 'Start button exists');

    // simulate click and then timed checks
    document.getElementById('startBtn').click();
    setTimeout(()=>{
      assert(document.body.classList.contains('step-2'), 'After click, Step 2 is active');
      assert(document.getElementById('petals').children.length>0, 'Petals generated');
    }, 200);

    setTimeout(()=>{
      assert(document.body.classList.contains('step-3'), 'Auto advanced to Step 3 after ~5s');
      // Click cake
      document.getElementById('cake').click();
    }, 5200);

    setTimeout(()=>{
      ['m1','m2','m3','m4'].forEach(id=>assert(document.getElementById(id).classList.contains('show'), `${id} message revealed`));
      log('All tests scheduled complete.');
    }, 7000);
  }
  window.__runBirthdayTests = __runBirthdayTests;
  if(location.hash === '#test') setTimeout(__runBirthdayTests, 100);
</script>
</body>
</html>
