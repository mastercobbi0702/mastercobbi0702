<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Carlos — QA Automation Engineer & Product Developer</title>
<meta name="description" content="QA Automation Engineer en fintech y desarrollador de productos. Automatización end-to-end con Playwright y Python; apps móviles con React Native y Supabase." />
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@400;500;700&display=swap" rel="stylesheet" />
<style>
  :root{
    --bg:#0A0F16;
    --bg-elev:#111923;
    --bg-elev-2:#18222E;
    --bg-glass:rgba(17,25,35,.6);
    --border:#27313E;
    --border-soft:#1D2630;
    --text:#E8EFF6;
    --text-dim:#8896A4;
    --text-faint:#586472;
    --pass:#3FB950;
    --pass-deep:#238636;
    --pending:#E3B341;
    --fail:#FF6B5E;
    --accent:#58A6FF;
    --accent-2:#A371F7;
    --grad:linear-gradient(120deg,#3FB950,#58A6FF 55%,#A371F7);
    --mono:'JetBrains Mono',ui-monospace,monospace;
    --display:'Space Grotesk',system-ui,sans-serif;
    --body:'Inter',system-ui,sans-serif;
    --maxw:1120px;
  }
  *{box-sizing:border-box;margin:0;padding:0}
  html{scroll-behavior:smooth}
  body{background:var(--bg);color:var(--text);font-family:var(--body);line-height:1.6;-webkit-font-smoothing:antialiased;overflow-x:hidden}
  a{color:inherit;text-decoration:none}
  ::selection{background:var(--pass);color:#04130a}
  :focus-visible{outline:2px solid var(--accent);outline-offset:3px;border-radius:4px}
  .wrap{max-width:var(--maxw);margin:0 auto;padding:0 24px;position:relative;z-index:2}
  .grad-text{background:var(--grad);-webkit-background-clip:text;background-clip:text;-webkit-text-fill-color:transparent;color:transparent}

  /* ---------- NAV ---------- */
  nav{position:sticky;top:0;z-index:60;backdrop-filter:blur(12px);background:rgba(10,15,22,.7);border-bottom:1px solid var(--border-soft)}
  .nav-inner{display:flex;align-items:center;justify-content:space-between;height:62px}
  .brand{font-family:var(--mono);font-weight:700;font-size:15px;letter-spacing:-.02em;display:flex;align-items:center;gap:8px}
  .brand .dot{width:9px;height:9px;border-radius:50%;background:var(--pass);box-shadow:0 0 12px var(--pass);animation:pulse 2s ease-in-out infinite}
  @keyframes pulse{0%,100%{transform:scale(1);opacity:1}50%{transform:scale(1.25);opacity:.7}}
  .brand .tilde{color:var(--text-faint)}
  .nav-links{display:flex;gap:8px;font-family:var(--mono);font-size:13px}
  .nav-links a{color:var(--text-dim);padding:6px 12px;border-radius:7px;transition:color .15s,background .15s;position:relative}
  .nav-links a:hover{color:var(--text)}
  .nav-links a.active{color:var(--pass);background:rgba(63,185,80,.1)}
  .nav-links .hash{color:var(--text-faint)}
  .nav-cta{font-family:var(--mono);font-size:13px;padding:8px 16px;border:1px solid var(--pass);border-radius:8px;color:#eafbef;background:var(--pass-deep);transition:transform .12s,background .15s}
  .nav-cta:hover{transform:translateY(-2px);background:var(--pass)}
  @media(max-width:760px){.nav-links{display:none}.nav-cta{display:none}}

  /* ---------- HERO ---------- */
  header{position:relative;padding:84px 0 64px;overflow:hidden}
  #bg-canvas{position:absolute;inset:0;width:100%;height:100%;z-index:0;opacity:.55}
  header::after{content:"";position:absolute;inset:0;z-index:1;background:radial-gradient(ellipse 60% 50% at 70% 30%,transparent,var(--bg) 78%)}
  .hero-grid{display:grid;grid-template-columns:1.05fr .95fr;gap:48px;align-items:center}
  @media(max-width:900px){.hero-grid{grid-template-columns:1fr;gap:38px}}
  .status-chip{display:inline-flex;align-items:center;gap:9px;font-family:var(--mono);font-size:12.5px;color:var(--pass);background:rgba(63,185,80,.1);border:1px solid rgba(63,185,80,.3);padding:6px 14px;border-radius:30px;margin-bottom:24px}
  .status-chip .live{width:7px;height:7px;border-radius:50%;background:var(--pass);box-shadow:0 0 10px var(--pass);animation:pulse 1.6s ease-in-out infinite}
  h1{font-family:var(--display);font-weight:700;font-size:clamp(46px,8vw,82px);line-height:.98;letter-spacing:-.035em;margin-bottom:14px}
  .role{font-family:var(--mono);font-size:clamp(14px,2.2vw,17px);color:var(--text-dim);margin-bottom:26px;display:flex;flex-wrap:wrap;gap:6px 14px;align-items:center}
  .role .sep{color:var(--accent-2)}
  .tagline{font-family:var(--display);font-weight:500;font-size:clamp(20px,2.7vw,27px);line-height:1.32;max-width:30ch;margin-bottom:34px;color:#dde6ef}
  .tagline .brk{color:var(--fail)}
  .tagline .mk{color:var(--pass)}
  .cta-row{display:flex;gap:14px;flex-wrap:wrap}
  .btn{font-family:var(--mono);font-size:14px;font-weight:500;padding:13px 22px;border-radius:9px;border:1px solid var(--border);transition:transform .12s,border-color .15s,background .15s,box-shadow .15s;display:inline-flex;align-items:center;gap:9px;cursor:pointer}
  .btn:hover{transform:translateY(-2px)}
  .btn-primary{background:var(--pass-deep);border-color:var(--pass);color:#eafbef}
  .btn-primary:hover{background:var(--pass);box-shadow:0 10px 30px -10px var(--pass)}
  .btn-ghost{color:var(--text-dim);background:var(--bg-glass)}
  .btn-ghost:hover{border-color:var(--text-dim);color:var(--text)}

  /* ---------- TEST RUNNER ---------- */
  .runner{background:var(--bg-elev);border:1px solid var(--border);border-radius:14px;overflow:hidden;box-shadow:0 30px 70px -28px rgba(0,0,0,.8);position:relative}
  .runner::before{content:"";position:absolute;inset:0;border-radius:14px;padding:1px;background:linear-gradient(140deg,rgba(63,185,80,.4),transparent 40%,transparent 60%,rgba(163,113,247,.35));-webkit-mask:linear-gradient(#000 0 0) content-box,linear-gradient(#000 0 0);-webkit-mask-composite:xor;mask-composite:exclude;pointer-events:none}
  .runner-bar{display:flex;align-items:center;gap:14px;padding:12px 16px;border-bottom:1px solid var(--border-soft);background:var(--bg-elev-2)}
  .lights{display:flex;gap:7px}
  .lights i{width:11px;height:11px;border-radius:50%;display:block}
  .lights i:nth-child(1){background:#FF5F57}.lights i:nth-child(2){background:#FEBC2E}.lights i:nth-child(3){background:#28C840}
  .runner-title{font-family:var(--mono);font-size:12px;color:var(--text-faint)}
  .runner-body{font-family:var(--mono);font-size:13px;line-height:1.85;padding:18px 18px 8px;white-space:pre-wrap;min-height:300px}
  .ln{display:block;opacity:0}
  .ln.show{opacity:1;animation:lnIn .26s ease both}
  @keyframes lnIn{from{opacity:0;transform:translateY(4px)}to{opacity:1;transform:none}}
  .cmd .pr{color:var(--pass)}
  .suite .badge{background:var(--accent);color:#04101f;border-radius:4px;padding:1px 7px;font-weight:700;font-size:11px;margin-right:8px}
  .suite{color:var(--accent)}
  .ok{color:var(--text-dim)}.ok .chk{color:var(--pass);font-weight:700}
  .sum{color:var(--pass);font-weight:700}.dim{color:var(--text-faint)}
  .cursor{display:inline-block;width:8px;height:15px;background:var(--pass);vertical-align:-2px;margin-left:2px;animation:blink 1s steps(1) infinite}
  @keyframes blink{50%{opacity:0}}
  .runner-foot{padding:10px 18px 16px}
  .pbar{height:6px;border-radius:6px;background:var(--bg-elev-2);overflow:hidden}
  .pbar i{display:block;height:100%;width:0;background:linear-gradient(90deg,var(--pass),#56d364);border-radius:6px;transition:width 1.1s cubic-bezier(.6,0,.2,1)}
  .pbar-label{display:flex;justify-content:space-between;font-family:var(--mono);font-size:11px;color:var(--text-faint);margin-top:8px}

  /* ---------- METRICS ---------- */
  .metrics{padding:56px 0;border-top:1px solid var(--border-soft);border-bottom:1px solid var(--border-soft);background:linear-gradient(180deg,transparent,rgba(24,34,46,.25))}
  .metrics-grid{display:grid;grid-template-columns:repeat(3,1fr) 1.2fr;gap:18px}
  @media(max-width:860px){.metrics-grid{grid-template-columns:1fr 1fr}}
  .metric{background:var(--bg-elev);border:1px solid var(--border-soft);border-radius:13px;padding:22px 22px 20px;position:relative;overflow:hidden;transition:border-color .2s,transform .2s}
  .metric:hover{border-color:var(--border);transform:translateY(-3px)}
  .metric .num{font-family:var(--display);font-weight:700;font-size:clamp(34px,5vw,46px);line-height:1;letter-spacing:-.02em}
  .metric .lab{font-family:var(--mono);font-size:12px;color:var(--text-dim);margin-top:10px}
  .metric .spark{position:absolute;right:14px;top:16px;font-family:var(--mono);font-size:11px;color:var(--pass)}
  .metric.donut{display:flex;align-items:center;gap:18px}
  .ring-wrap{position:relative;width:92px;height:92px;flex-shrink:0}
  .ring-wrap svg{transform:rotate(-90deg)}
  .ring-bg{fill:none;stroke:var(--bg-elev-2);stroke-width:9}
  .ring-fg{fill:none;stroke:url(#ringGrad);stroke-width:9;stroke-linecap:round;stroke-dasharray:259.8;stroke-dashoffset:259.8;transition:stroke-dashoffset 1.4s cubic-bezier(.6,0,.2,1)}
  .ring-val{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;font-family:var(--display);font-weight:700;font-size:20px}
  .donut .meta .t{font-family:var(--mono);font-size:13px;color:var(--text)}
  .donut .meta .s{font-family:var(--mono);font-size:11.5px;color:var(--text-faint);margin-top:5px;line-height:1.5}

  /* ---------- SECTION SHELL ---------- */
  section{padding:74px 0;position:relative}
  .sec-label{font-family:var(--mono);font-size:13px;color:var(--text-faint);margin-bottom:10px}
  .sec-label b{color:var(--pass);font-weight:400}
  .sec-title{font-family:var(--display);font-weight:600;font-size:clamp(28px,4.2vw,40px);letter-spacing:-.025em;margin-bottom:34px;line-height:1.1}
  .reveal{opacity:0;transform:translateY(24px);transition:opacity .7s ease,transform .7s ease}
  .reveal.in{opacity:1;transform:none}

  /* ---------- ABOUT ---------- */
  .about-wrap{display:grid;grid-template-columns:1.5fr 1fr;gap:40px;align-items:start}
  @media(max-width:820px){.about-wrap{grid-template-columns:1fr;gap:28px}}
  .about-body{font-size:clamp(16px,2vw,18px);max-width:60ch;color:#ccd6df}
  .about-body strong{color:var(--text);font-weight:600}
  .about-body+.about-body{margin-top:16px}
  .about-card{background:var(--bg-elev);border:1px solid var(--border-soft);border-radius:13px;padding:22px;font-family:var(--mono);font-size:13px}
  .about-card .row{display:flex;justify-content:space-between;padding:9px 0;border-bottom:1px dashed var(--border-soft)}
  .about-card .row:last-child{border-bottom:none}
  .about-card .k{color:var(--text-faint)}
  .about-card .v{color:var(--text)}
  .about-card .v.g{color:var(--pass)}

  /* ---------- STACK ---------- */
  .stack-grid{display:grid;grid-template-columns:1fr 1fr;gap:20px}
  @media(max-width:760px){.stack-grid{grid-template-columns:1fr}}
  .stack-card{background:var(--bg-elev);border:1px solid var(--border-soft);border-radius:14px;padding:26px;transition:border-color .2s}
  .stack-card:hover{border-color:var(--border)}
  .stack-card h3{font-family:var(--mono);font-size:14px;font-weight:500;margin-bottom:4px}
  .stack-card .desc{font-family:var(--mono);font-size:12px;color:var(--text-faint);margin-bottom:20px}
  .stack-card.qa h3 .accent{color:var(--pass)}
  .stack-card.prod h3 .accent{color:var(--accent)}
  .skill{margin-bottom:14px}
  .skill:last-child{margin-bottom:0}
  .skill-top{display:flex;justify-content:space-between;font-family:var(--mono);font-size:12.5px;margin-bottom:6px}
  .skill-top .pct{color:var(--text-faint)}
  .skill-bar{height:7px;border-radius:6px;background:var(--bg-elev-2);overflow:hidden}
  .skill-bar i{display:block;height:100%;width:0;border-radius:6px;transition:width 1.2s cubic-bezier(.5,0,.2,1)}
  .qa .skill-bar i{background:linear-gradient(90deg,var(--pass-deep),var(--pass))}
  .prod .skill-bar i{background:linear-gradient(90deg,#1f6feb,var(--accent))}

  /* ---------- PROCESS ---------- */
  .flow{display:grid;grid-template-columns:repeat(4,1fr);gap:0;position:relative}
  @media(max-width:820px){.flow{grid-template-columns:1fr 1fr;gap:18px 0}}
  @media(max-width:480px){.flow{grid-template-columns:1fr}}
  .step{padding:24px 22px;position:relative}
  .step:not(:last-child)::after{content:"";position:absolute;right:0;top:38px;width:1px;height:calc(100% - 30px);background:var(--border-soft)}
  @media(max-width:820px){.step:not(:last-child)::after{display:none}}
  .step .n{font-family:var(--mono);font-size:13px;color:var(--pass);margin-bottom:14px;display:flex;align-items:center;gap:9px}
  .step .n .d{width:26px;height:26px;border-radius:8px;border:1px solid var(--border);display:flex;align-items:center;justify-content:center;color:var(--text);font-size:12px}
  .step h4{font-family:var(--display);font-weight:600;font-size:19px;margin-bottom:8px}
  .step p{font-size:14px;color:var(--text-dim)}

  /* ---------- PROJECTS ---------- */
  .filters{display:flex;gap:10px;margin-bottom:26px;flex-wrap:wrap}
  .filter{font-family:var(--mono);font-size:13px;padding:8px 16px;border-radius:20px;border:1px solid var(--border-soft);color:var(--text-dim);background:transparent;cursor:pointer;transition:all .15s}
  .filter:hover{border-color:var(--border);color:var(--text)}
  .filter.active{background:var(--text);color:var(--bg);border-color:var(--text)}
  .proj-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:18px}
  @media(max-width:900px){.proj-grid{grid-template-columns:1fr 1fr}}
  @media(max-width:620px){.proj-grid{grid-template-columns:1fr}}
  .card{background:var(--bg-elev);border:1px solid var(--border-soft);border-radius:14px;padding:22px;display:flex;flex-direction:column;transition:border-color .2s,box-shadow .2s,transform .35s cubic-bezier(.2,.6,.2,1);position:relative;transform-style:preserve-3d;will-change:transform}
  .card.hide{display:none}
  .card:hover{border-color:var(--border);box-shadow:0 24px 50px -28px rgba(0,0,0,.7)}
  .card .glow{position:absolute;inset:0;border-radius:14px;opacity:0;transition:opacity .25s;background:radial-gradient(380px circle at var(--mx,50%) var(--my,0%),rgba(88,166,255,.1),transparent 45%);pointer-events:none}
  .card:hover .glow{opacity:1}
  .card-top{display:flex;align-items:center;justify-content:space-between;margin-bottom:12px}
  .card-name{font-family:var(--mono);font-size:15px;font-weight:700}
  .status{font-family:var(--mono);font-size:11px;padding:3px 9px;border-radius:20px;display:inline-flex;align-items:center;gap:5px;white-space:nowrap}
  .status::before{content:"";width:6px;height:6px;border-radius:50%}
  .status.pass{color:var(--pass);background:rgba(63,185,80,.12)}.status.pass::before{background:var(--pass)}
  .status.run{color:var(--pending);background:rgba(227,179,65,.12)}.status.run::before{background:var(--pending);animation:blink 1.2s steps(1) infinite}
  .card-desc{font-size:14.5px;color:#bfc9d3;flex:1;margin-bottom:16px}
  .card-stack{display:flex;flex-wrap:wrap;gap:6px;margin-bottom:16px}
  .chip{font-family:var(--mono);font-size:11px;color:var(--text-dim);border:1px solid var(--border-soft);padding:3px 8px;border-radius:5px}
  .card-links{display:flex;gap:16px;font-family:var(--mono);font-size:13px}
  .card-links a{color:var(--accent);display:inline-flex;align-items:center;gap:6px;transition:opacity .15s}
  .card-links a:hover{opacity:.7}
  .card-links a.muted{color:var(--text-faint);cursor:default}
  .card-links svg{width:14px;height:14px}

  /* ---------- CONTACT ---------- */
  .contact{text-align:center;padding-bottom:48px}
  .contact .sec-title{margin-bottom:14px}
  .contact-sub{color:var(--text-dim);max-width:48ch;margin:0 auto 32px;font-size:16px}
  .contact-row{display:flex;gap:14px;justify-content:center;flex-wrap:wrap}
  .contact-glow{position:relative}
  .contact-glow::before{content:"";position:absolute;left:50%;top:-40px;transform:translateX(-50%);width:340px;height:200px;background:radial-gradient(closest-side,rgba(63,185,80,.18),transparent);filter:blur(20px);pointer-events:none;z-index:-1}

  footer{border-top:1px solid var(--border-soft);padding:28px 0;margin-top:20px}
  .foot-inner{display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:12px;font-family:var(--mono);font-size:12px;color:var(--text-faint)}
  .foot-inner .ok-pill{color:var(--pass)}

  @media (prefers-reduced-motion: reduce){
    *{animation:none !important;transition:none !important;scroll-behavior:auto}
    .ln{opacity:1}.cursor{display:none}
    .reveal{opacity:1;transform:none}
    .skill-bar i,.pbar i{transition:none}
    .ring-fg{transition:none}
  }
</style>
</head>
<body>

<nav>
  <div class="wrap nav-inner">
    <div class="brand"><span class="dot"></span>carlos<span class="tilde">~/</span>portfolio</div>
    <div class="nav-links" id="navlinks">
      <a href="#about"><span class="hash">#</span>sobre-mi</a>
      <a href="#stack"><span class="hash">#</span>stack</a>
      <a href="#proceso"><span class="hash">#</span>proceso</a>
      <a href="#proyectos"><span class="hash">#</span>proyectos</a>
    </div>
    <a class="nav-cta" href="#contacto">Contáctame</a>
  </div>
</nav>

<header id="top">
  <canvas id="bg-canvas"></canvas>
  <div class="wrap hero-grid">
    <div class="hero-text">
      <div class="status-chip"><span class="live"></span>Disponible para proyectos</div>
      <h1>Carlos</h1>
      <div class="role">QA Automation Engineer <span class="sep">·</span> Product Developer</div>
      <p class="tagline">Encuentro lo que <span class="brk">se rompe</span> y construyo lo que <span class="mk">funciona</span>.</p>
      <div class="cta-row">
        <a class="btn btn-primary" href="#proyectos">Ver proyectos &rarr;</a>
        <a class="btn btn-ghost" href="https://github.com/mastercobbi0702" target="_blank" rel="noopener">GitHub</a>
      </div>
    </div>

    <div class="runner" aria-hidden="true">
      <div class="runner-bar">
        <div class="lights"><i></i><i></i><i></i></div>
        <div class="runner-title">carlos.spec — passing</div>
      </div>
      <div class="runner-body" id="runner"></div>
      <div class="runner-foot">
        <div class="pbar"><i id="pbar"></i></div>
        <div class="pbar-label"><span>coverage</span><span id="pbar-pct">0%</span></div>
      </div>
    </div>
  </div>
</header>

<div class="metrics">
  <div class="wrap">
    <div class="metrics-grid">
      <div class="metric"><div class="spark">↗</div><div class="num" data-target="3" data-pad="2">00</div><div class="lab">repos públicos</div></div>
      <div class="metric"><div class="spark">↗</div><div class="num" data-target="5" data-pad="2">00</div><div class="lab">proyectos activos</div></div>
      <div class="metric"><div class="spark">↗</div><div class="num" data-target="2" data-pad="2">00</div><div class="lab">disciplinas: QA + Dev</div></div>
      <div class="metric donut">
        <div class="ring-wrap">
          <svg width="92" height="92" viewBox="0 0 92 92">
            <defs><linearGradient id="ringGrad" x1="0" y1="0" x2="1" y2="1"><stop offset="0" stop-color="#3FB950"/><stop offset="1" stop-color="#58A6FF"/></linearGradient></defs>
            <circle class="ring-bg" cx="46" cy="46" r="41.3"/>
            <circle class="ring-fg" id="ring" cx="46" cy="46" r="41.3"/>
          </svg>
          <div class="ring-val" id="ring-val">0%</div>
        </div>
        <div class="meta"><div class="t">test pass rate</div><div class="s">cada release sale<br/>verificado y sólido</div></div>
      </div>
    </div>
  </div>
</div>

<section id="about">
  <div class="wrap reveal">
    <div class="sec-label">// <b>sobre-mi</b></div>
    <h2 class="sec-title">Calidad de fintech,<br/>mentalidad de builder</h2>
    <div class="about-wrap">
      <div>
        <p class="about-body">Soy <strong>QA Automation Engineer en fintech</strong>, donde la calidad no es negociable: automatizo pruebas end-to-end para que cada release salga sólido y los bugs se queden en el pipeline, no en producción.</p>
        <p class="about-body">Fuera del trabajo construyo mis propios productos —<strong>apps móviles y tiendas online</strong>— de la idea al deploy. Uso la <strong>IA como acelerador, no como atajo</strong>: me mueve más rápido sin soltar el control de la calidad ni el entendimiento del código.</p>
      </div>
      <div class="about-card">
        <div class="row"><span class="k">rol</span><span class="v">QA + Producto</span></div>
        <div class="row"><span class="k">industria</span><span class="v">Fintech</span></div>
        <div class="row"><span class="k">lenguaje base</span><span class="v g">Python</span></div>
        <div class="row"><span class="k">ubicación</span><span class="v">México 🇲🇽</span></div>
        <div class="row"><span class="k">estado</span><span class="v g">● disponible</span></div>
      </div>
    </div>
  </div>
</section>

<section id="stack">
  <div class="wrap reveal">
    <div class="sec-label">// <b>stack</b></div>
    <h2 class="sec-title">Con qué trabajo</h2>
    <div class="stack-grid">
      <div class="stack-card qa">
        <h3>describe(<span class="accent">'QA &amp; Testing'</span>)</h3>
        <div class="desc">// automatización end-to-end</div>
        <div class="skill"><div class="skill-top"><span>Python</span><span class="pct">expert</span></div><div class="skill-bar"><i data-w="92"></i></div></div>
        <div class="skill"><div class="skill-top"><span>Playwright</span><span class="pct">advanced</span></div><div class="skill-bar"><i data-w="85"></i></div></div>
        <div class="skill"><div class="skill-top"><span>Selenium</span><span class="pct">advanced</span></div><div class="skill-bar"><i data-w="80"></i></div></div>
        <div class="skill"><div class="skill-top"><span>BDD / Pytest</span><span class="pct">solid</span></div><div class="skill-bar"><i data-w="78"></i></div></div>
      </div>
      <div class="stack-card prod">
        <h3>describe(<span class="accent">'Product'</span>)</h3>
        <div class="desc">// de la idea al deploy</div>
        <div class="skill"><div class="skill-top"><span>React Native</span><span class="pct">advanced</span></div><div class="skill-bar"><i data-w="82"></i></div></div>
        <div class="skill"><div class="skill-top"><span>JavaScript / React</span><span class="pct">advanced</span></div><div class="skill-bar"><i data-w="80"></i></div></div>
        <div class="skill"><div class="skill-top"><span>Supabase</span><span class="pct">solid</span></div><div class="skill-bar"><i data-w="75"></i></div></div>
        <div class="skill"><div class="skill-top"><span>HTML / CSS</span><span class="pct">solid</span></div><div class="skill-bar"><i data-w="78"></i></div></div>
      </div>
    </div>
  </div>
</section>

<section id="proceso">
  <div class="wrap reveal">
    <div class="sec-label">// <b>proceso</b></div>
    <h2 class="sec-title">Cómo llevo algo de cero a producción</h2>
    <div class="flow">
      <div class="step"><div class="n"><span class="d">01</span>analizar</div><h4>Entender</h4><p>Requerimientos, riesgos y casos borde antes de escribir una línea.</p></div>
      <div class="step"><div class="n"><span class="d">02</span>construir</div><h4>Automatizar</h4><p>Código de producto o suites de prueba limpias y mantenibles.</p></div>
      <div class="step"><div class="n"><span class="d">03</span>verificar</div><h4>Probar</h4><p>End-to-end, edge cases y regresión. Que falle aquí, no con el usuario.</p></div>
      <div class="step"><div class="n"><span class="d">04</span>entregar</div><h4>Deploy</h4><p>Release con confianza y observabilidad para iterar rápido.</p></div>
    </div>
  </div>
</section>

<section id="proyectos">
  <div class="wrap reveal">
    <div class="sec-label">// <b>proyectos</b></div>
    <h2 class="sec-title">En qué estoy trabajando</h2>
    <div class="filters" id="filters">
      <button class="filter active" data-f="all">Todos</button>
      <button class="filter" data-f="qa">QA &amp; Testing</button>
      <button class="filter" data-f="prod">Producto</button>
    </div>
    <div class="proj-grid" id="grid">

      <article class="card" data-cat="prod">
        <div class="glow"></div>
        <div class="card-top"><span class="card-name">MushiMushi2</span><span class="status run">in&nbsp;progress</span></div>
        <p class="card-desc">Plataforma social para la comunidad de crochet, en iOS y Android: descubre patrones, comparte proyectos y conecta con otras tejedoras.</p>
        <div class="card-stack"><span class="chip">React Native</span><span class="chip">Supabase</span><span class="chip">Cloudinary</span></div>
        <div class="card-links"><a class="muted">próximamente</a></div>
      </article>

      <article class="card" data-cat="prod">
        <div class="glow"></div>
        <div class="card-top"><span class="card-name">Saskesita Tiendita</span><span class="status pass">live</span></div>
        <p class="card-desc">Mi tienda online: catálogo, identidad de marca propia y operación de e-commerce de punta a punta.</p>
        <div class="card-stack"><span class="chip">E-commerce</span><span class="chip">Branding</span></div>
        <div class="card-links"><a href="#" target="_blank" rel="noopener">Visitar →</a></div>
      </article>

      <article class="card" data-cat="qa">
        <div class="glow"></div>
        <div class="card-top"><span class="card-name">qa-automation-bdd</span><span class="status pass">passing</span></div>
        <p class="card-desc">Suite de automatización con enfoque BDD: escenarios legibles que conectan negocio y pruebas técnicas.</p>
        <div class="card-stack"><span class="chip">Python</span><span class="chip">BDD</span></div>
        <div class="card-links"><a href="https://github.com/mastercobbi0702/qa-automation-bdd" target="_blank" rel="noopener"><svg viewBox="0 0 16 16" fill="currentColor"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.01 8.01 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>Código</a></div>
      </article>

      <article class="card" data-cat="qa">
        <div class="glow"></div>
        <div class="card-top"><span class="card-name">selenium_proyect</span><span class="status pass">passing</span></div>
        <p class="card-desc">Automatización de flujos web con Selenium para escenarios y aplicaciones legacy.</p>
        <div class="card-stack"><span class="chip">Python</span><span class="chip">Selenium</span></div>
        <div class="card-links"><a href="https://github.com/mastercobbi0702/selenium_proyect" target="_blank" rel="noopener"><svg viewBox="0 0 16 16" fill="currentColor"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.01 8.01 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>Código</a></div>
      </article>

      <article class="card" data-cat="qa">
        <div class="glow"></div>
        <div class="card-top"><span class="card-name">curso_playwright_30_dias</span><span class="status run">30&nbsp;días</span></div>
        <p class="card-desc">Reto personal de 30 días dominando Playwright: práctica diaria documentada, de lo básico a patrones avanzados.</p>
        <div class="card-stack"><span class="chip">Playwright</span><span class="chip">Python</span></div>
        <div class="card-links"><a href="https://github.com/mastercobbi0702/curso_playwright_30_dias" target="_blank" rel="noopener"><svg viewBox="0 0 16 16" fill="currentColor"><path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.01 8.01 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>Código</a></div>
      </article>

    </div>
  </div>
</section>

<section id="contacto" class="contact">
  <div class="wrap reveal contact-glow">
    <div class="sec-label" style="text-align:center">// <b>contacto</b></div>
    <h2 class="sec-title">Construyamos algo <span class="grad-text">que funcione</span></h2>
    <p class="contact-sub">¿Tienes un proyecto que necesita QA serio o desarrollo de producto? Hablemos.</p>
    <div class="contact-row">
      <a class="btn btn-primary" href="mailto:tu-correo@ejemplo.com">Escríbeme</a>
      <a class="btn btn-ghost" href="https://github.com/mastercobbi0702" target="_blank" rel="noopener">GitHub</a>
      <a class="btn btn-ghost" href="#" target="_blank" rel="noopener">LinkedIn</a>
    </div>
  </div>
</section>

<footer>
  <div class="wrap foot-inner">
    <span>© 2026 Carlos · QA &amp; Product</span>
    <span class="ok-pill">✓ all tests passed</span>
  </div>
</footer>

<script>
(function(){
  var reduce = window.matchMedia && window.matchMedia('(prefers-reduced-motion: reduce)').matches;

  /* ---------- TEST RUNNER ---------- */
  var runner = document.getElementById('runner');
  var lines = [
    {h:'<span class="cmd"><span class="pr">$</span> pytest carlos.py -v --who-am-i</span>'},
    {h:'<span class="dim">&nbsp;</span>'},
    {h:'<span class="suite"><span class="badge">PASS</span>tests/qa.py</span>'},
    {h:'<span class="ok"><span class="chk">  ✓</span> end-to-end con Playwright + Python</span>'},
    {h:'<span class="ok"><span class="chk">  ✓</span> suites BDD legibles y mantenibles</span>'},
    {h:'<span class="ok"><span class="chk">  ✓</span> Selenium para flujos legacy</span>'},
    {h:'<span class="dim">&nbsp;</span>'},
    {h:'<span class="suite"><span class="badge">PASS</span>tests/product.py</span>'},
    {h:'<span class="ok"><span class="chk">  ✓</span> apps móviles con React Native</span>'},
    {h:'<span class="ok"><span class="chk">  ✓</span> backend y auth con Supabase</span>'},
    {h:'<span class="dim">&nbsp;</span>'},
    {h:'<span class="suite"><span class="badge">PASS</span>tests/mindset.py</span>'},
    {h:'<span class="ok"><span class="chk">  ✓</span> IA como acelerador, no como atajo</span>'},
    {h:'<span class="dim">&nbsp;</span>'},
    {h:'<span class="sum">═══ 7 passed</span><span class="dim"> in 0.38s ═══</span>'}
  ];
  function finishBar(){
    var pb=document.getElementById('pbar'),pct=document.getElementById('pbar-pct');
    if(pb) pb.style.width='100%';
    if(pct){var n=0;var t=setInterval(function(){n+=4;if(n>=100){n=100;clearInterval(t);}pct.textContent=n+'%';},22);}
  }
  if(runner){
    if(reduce){
      runner.innerHTML = lines.map(function(l){return '<span class="ln show">'+l.h+'</span>';}).join('');
      var pbr=document.getElementById('pbar');if(pbr)pbr.style.width='100%';var pctr=document.getElementById('pbar-pct');if(pctr)pctr.textContent='100%';
    } else {
      runner.innerHTML = lines.map(function(l){return '<span class="ln">'+l.h+'</span>';}).join('') + '<span class="cursor"></span>';
      var els = runner.querySelectorAll('.ln'); var i=0;
      (function step(){
        if(i>=els.length){finishBar();return;}
        els[i].classList.add('show'); i++;
        var delay=(i===1)?400:(i<=2?240:150);
        setTimeout(step,delay);
      })();
    }
  }

  /* ---------- BACKGROUND CANVAS (pipeline graph) ---------- */
  var canvas=document.getElementById('bg-canvas');
  if(canvas && !reduce){
    var ctx=canvas.getContext('2d'),W,H,nodes=[],raf,pulses=[];
    var COLORS=['#3FB950','#58A6FF','#A371F7'];
    var DPR=Math.min(window.devicePixelRatio||1,2);
    function resize(){
      var r=canvas.parentElement.getBoundingClientRect();
      W=canvas.width=r.width*DPR; H=canvas.height=r.height*DPR;
      canvas.style.width=r.width+'px'; canvas.style.height=r.height+'px';
      build();
    }
    function build(){
      nodes=[]; var count=Math.min(46,Math.max(18,Math.floor(W*H/(46000*DPR))));
      for(var i=0;i<count;i++){
        nodes.push({x:Math.random()*W,y:Math.random()*H,vx:(Math.random()-.5)*.18*DPR,vy:(Math.random()-.5)*.18*DPR,r:(Math.random()*1.6+1)*DPR,c:COLORS[i%3]});
      }
    }
    function nearest(a){var out=[];var lim=(150*DPR)*(150*DPR);for(var j=0;j<nodes.length;j++){if(nodes[j]===a)continue;var dx=a.x-nodes[j].x,dy=a.y-nodes[j].y,d=dx*dx+dy*dy;if(d<lim)out.push({n:nodes[j],d:Math.sqrt(d)});}return out;}
    function draw(){
      ctx.clearRect(0,0,W,H);
      for(var i=0;i<nodes.length;i++){
        var n=nodes[i]; n.x+=n.vx; n.y+=n.vy;
        if(n.x<0||n.x>W)n.vx*=-1; if(n.y<0||n.y>H)n.vy*=-1;
        var near=nearest(n);
        for(var k=0;k<near.length;k++){
          var o=near[k]; var alpha=(1-o.d/(150*DPR))*.22;
          ctx.strokeStyle='rgba(120,150,180,'+alpha+')'; ctx.lineWidth=1*DPR;
          ctx.beginPath();ctx.moveTo(n.x,n.y);ctx.lineTo(o.n.x,o.n.y);ctx.stroke();
        }
      }
      for(var i2=0;i2<nodes.length;i2++){
        var nn=nodes[i2];
        ctx.beginPath();ctx.arc(nn.x,nn.y,nn.r,0,6.28);
        ctx.fillStyle=nn.c;ctx.globalAlpha=.85;ctx.fill();ctx.globalAlpha=1;
        ctx.beginPath();ctx.arc(nn.x,nn.y,nn.r*2.6,0,6.28);
        ctx.fillStyle=nn.c;ctx.globalAlpha=.08;ctx.fill();ctx.globalAlpha=1;
      }
      if(Math.random()<.04 && nodes.length>2){
        var a=nodes[Math.floor(Math.random()*nodes.length)];
        var nb=nearest(a); if(nb.length){pulses.push({a:a,b:nb[0].n,t:0});}
      }
      for(var p=pulses.length-1;p>=0;p--){
        var pu=pulses[p]; pu.t+=.025;
        if(pu.t>=1){pulses.splice(p,1);continue;}
        var px=pu.a.x+(pu.b.x-pu.a.x)*pu.t, py=pu.a.y+(pu.b.y-pu.a.y)*pu.t;
        ctx.beginPath();ctx.arc(px,py,2.4*DPR,0,6.28);
        ctx.fillStyle='#56d364';ctx.shadowBlur=10;ctx.shadowColor='#3FB950';ctx.fill();ctx.shadowBlur=0;
      }
      raf=requestAnimationFrame(draw);
    }
    resize(); draw();
    var rt; window.addEventListener('resize',function(){cancelAnimationFrame(raf);clearTimeout(rt);rt=setTimeout(function(){resize();draw();},180);});
  }

  /* ---------- INTERSECTION: reveals, counters, bars, donut ---------- */
  function animateCount(el){
    var target=+el.getAttribute('data-target'), pad=+(el.getAttribute('data-pad')||0);
    var dur=1100, start=performance.now();
    function fmt(v){return pad?String(v).padStart(pad,'0'):''+v;}
    if(reduce){el.textContent=fmt(target);return;}
    function tick(now){
      var p=Math.min((now-start)/dur,1); var val=Math.round(p*target);
      el.textContent=fmt(val);
      if(p<1)requestAnimationFrame(tick);
    }
    requestAnimationFrame(tick);
  }
  function fillRing(){
    var ring=document.getElementById('ring'), val=document.getElementById('ring-val');
    var C=259.8;
    if(reduce){if(ring)ring.style.strokeDashoffset=0;if(val)val.textContent='100%';return;}
    if(ring)ring.style.strokeDashoffset=0;
    var n=0,t=setInterval(function(){n+=4;if(n>=100){n=100;clearInterval(t);}if(val)val.textContent=n+'%';},22);
  }

  var io=new IntersectionObserver(function(entries){
    entries.forEach(function(e){
      if(!e.isIntersecting)return;
      var t=e.target;
      if(t.classList.contains('reveal'))t.classList.add('in');
      if(t.classList.contains('metrics-grid')){
        t.querySelectorAll('.num[data-target]').forEach(animateCount);
        fillRing();
      }
      if(t.classList.contains('stack-grid')){
        t.querySelectorAll('.skill-bar i').forEach(function(b){b.style.width=b.getAttribute('data-w')+'%';});
      }
      io.unobserve(t);
    });
  },{threshold:.25});

  document.querySelectorAll('.reveal').forEach(function(el){io.observe(el);});
  var mg=document.querySelector('.metrics-grid'); if(mg)io.observe(mg);
  var sg=document.querySelector('.stack-grid'); if(sg)io.observe(sg);

  /* ---------- SCROLL SPY ---------- */
  var spy=new IntersectionObserver(function(entries){
    entries.forEach(function(e){
      if(e.isIntersecting){
        var id=e.target.getAttribute('id');
        document.querySelectorAll('#navlinks a').forEach(function(a){
          a.classList.toggle('active',a.getAttribute('href')==='#'+id);
        });
      }
    });
  },{rootMargin:'-45% 0px -50% 0px'});
  ['about','stack','proceso','proyectos','contacto'].forEach(function(id){var s=document.getElementById(id);if(s)spy.observe(s);});

  /* ---------- PROJECT FILTERS ---------- */
  var filters=document.getElementById('filters');
  if(filters){
    filters.addEventListener('click',function(e){
      var b=e.target.closest('.filter'); if(!b)return;
      filters.querySelectorAll('.filter').forEach(function(f){f.classList.remove('active');});
      b.classList.add('active');
      var f=b.getAttribute('data-f');
      document.querySelectorAll('#grid .card').forEach(function(c){
        var show=(f==='all'||c.getAttribute('data-cat')===f);
        c.classList.toggle('hide',!show);
      });
    });
  }

  /* ---------- CARD TILT + GLOW ---------- */
  if(!reduce && window.matchMedia('(hover:hover)').matches){
    document.querySelectorAll('#grid .card').forEach(function(card){
      card.addEventListener('mousemove',function(ev){
        var r=card.getBoundingClientRect();
        var px=(ev.clientX-r.left)/r.width, py=(ev.clientY-r.top)/r.height;
        var rx=(py-.5)*-6, ry=(px-.5)*6;
        card.style.transform='perspective(800px) rotateX('+rx+'deg) rotateY('+ry+'deg) translateY(-3px)';
        card.style.setProperty('--mx',(px*100)+'%');
        card.style.setProperty('--my',(py*100)+'%');
      });
      card.addEventListener('mouseleave',function(){card.style.transform='';});
    });
  }
})();
</script>
</body>
</html>
