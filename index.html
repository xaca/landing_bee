<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Hive — Pure gold, made by bees</title>
  <meta name="description" content="Hive No.01 — raw, single-origin wildflower honey. A scrollytelling prototype.">

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400..800;1,9..144,400..800&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

  <!-- Libraries (CDN, pinned versions) -->
  <script src="https://cdn.jsdelivr.net/npm/@tailwindcss/browser@4.1.13"></script>
  <script src="https://cdn.jsdelivr.net/npm/gsap@3.15.0/dist/gsap.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/gsap@3.15.0/dist/ScrollTrigger.min.js"></script>
  <script src="https://cdn.jsdelivr.net/npm/gsap@3.15.0/dist/MotionPathPlugin.min.js"></script>

  <style type="text/tailwindcss">
    @theme {
      --color-ink: #0b0906;
      --color-ink-2: #16110a;
      --color-honey: #f6b40e;
      --color-amber: #ff8a1f;
      --color-cream: #fff3d6;
      --font-sans: "Inter", system-ui, sans-serif;
      --font-display: "Fraunces", Georgia, serif;
    }
  </style>

  <style>
    :root { --bee: clamp(96px, 12vw, 170px); }
    html, body { background: #0b0906; }
    body { color: #fff3d6; overflow-x: hidden; -webkit-font-smoothing: antialiased; }
    section { position: relative; width: 100%; }
    .pin { height: 100vh; overflow: hidden; }

    .honeycomb {
      background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='56' height='100' viewBox='0 0 56 100'%3E%3Cpath d='M28 66L0 50L0 16L28 0L56 16L56 50L28 66L28 100' fill='none' stroke='%23f6b40e' stroke-opacity='0.09' stroke-width='1'/%3E%3C/svg%3E");
      -webkit-mask-image: radial-gradient(ellipse at 70% 50%, #000 10%, transparent 70%);
              mask-image: radial-gradient(ellipse at 70% 50%, #000 10%, transparent 70%);
    }
    .glow {
      position: absolute; border-radius: 50%; pointer-events: none;
      background: radial-gradient(circle, rgba(246,180,14,.32), rgba(255,138,31,.08) 45%, transparent 68%);
    }

    /* Split text */
    .line { display: block; overflow: hidden; padding-bottom: .12em; margin-bottom: -.12em; }
    .word-wrap { display: inline-block; white-space: nowrap; }
    .char { display: inline-block; will-change: transform; }

    /* Bee: track (scroll path) > intro > bank (tilt) > face (flip) > float (idle) > svg (wings) */
    #bee { position: fixed; left: 0; top: 0; width: var(--bee); aspect-ratio: 200 / 160; z-index: 40; pointer-events: none; visibility: hidden; will-change: transform; }
    #bee .bee-layer { position: absolute; inset: 0; }
    #bee svg { width: 100%; height: 100%; overflow: visible; filter: drop-shadow(0 12px 28px rgba(246,180,14,.35)); }
    .trail-dot { position: fixed; left: 0; top: 0; width: 7px; height: 7px; border-radius: 50%; background: #f6b40e; box-shadow: 0 0 12px #f6b40e; z-index: 39; pointer-events: none; opacity: 0; }

    /* Nav */
    #nav { transition: transform .45s cubic-bezier(.2,.8,.2,1); }
    #nav.nav-hidden { transform: translateY(-110%); }
    #progress { transform-origin: 0 50%; }

    /* Gallery */
    .gallery-track { display: flex; gap: clamp(16px, 3vw, 40px); width: max-content; padding: 0 8vw; }

    /* Anatomy */
    .anatomy-stage { position: absolute; left: 40%; top: 58%; width: 0; height: 0; }
    @media (min-width: 768px) { .anatomy-stage { left: 46%; top: 55%; } }
    .layer { position: absolute; left: 0; top: 0; width: min(50vw, 280px); translate: -50% -50%; }
    .layer svg { width: 100%; height: auto; display: block; overflow: visible; }
    .layer-label { position: absolute; left: calc(100% + 14px); top: 30%; white-space: nowrap; display: flex; align-items: center; gap: 10px; }
    .layer-label::before { content: ""; width: 28px; height: 1px; background: rgba(246,180,14,.6); }

    /* Process */
    .step-dot { position: absolute; top: .35rem; left: calc(1.25rem - 4rem - 7px); width: 16px; height: 16px; border-radius: 50%; background: #16110a; border: 2px solid rgba(255,243,214,.25); transition: all .4s ease; }
    @media (min-width: 768px) { .step-dot { left: calc(2rem - 6rem - 7px); } }
    .step.is-active .step-dot { background: #f6b40e; border-color: #f6b40e; box-shadow: 0 0 0 8px rgba(246,180,14,.15); }

    @media (prefers-reduced-motion: reduce) { #nav { transition: none; } }
  </style>
</head>

<body class="font-sans">

  <!-- Shared SVG definitions (jar + anatomy) -->
  <svg width="0" height="0" style="position:absolute" aria-hidden="true">
    <defs>
      <linearGradient id="g-honey" x1="0" y1="0" x2="1" y2="0">
        <stop offset="0" stop-color="#b85e00"/><stop offset=".35" stop-color="#f6b40e"/><stop offset=".6" stop-color="#ffd25a"/><stop offset="1" stop-color="#a85200"/>
      </linearGradient>
      <linearGradient id="g-glass" x1="0" y1="0" x2="1" y2="0">
        <stop offset="0" stop-color="#fff" stop-opacity=".2"/><stop offset=".2" stop-color="#fff" stop-opacity=".04"/><stop offset=".8" stop-color="#fff" stop-opacity=".02"/><stop offset="1" stop-color="#fff" stop-opacity=".16"/>
      </linearGradient>
      <linearGradient id="g-lid" x1="0" y1="0" x2="1" y2="0">
        <stop offset="0" stop-color="#6b3d00"/><stop offset=".4" stop-color="#e0a020"/><stop offset=".7" stop-color="#ffd76a"/><stop offset="1" stop-color="#6b3d00"/>
      </linearGradient>
      <pattern id="p-comb" width="28" height="50" patternUnits="userSpaceOnUse">
        <rect width="28" height="50" fill="#f6b40e"/>
        <path d="M14 33L0 25L0 8L14 0L28 8L28 25L14 33L14 50" fill="none" stroke="#7a4200" stroke-width="2"/>
      </pattern>
    </defs>
  </svg>

  <!-- ============ THE BEE ============ -->
  <div id="bee" aria-hidden="true">
    <div class="bee-layer bee-intro">
      <div class="bee-layer bee-bank">
        <div class="bee-layer bee-face">
          <div class="bee-layer bee-float">
            <svg viewBox="0 0 200 160">
              <defs>
                <radialGradient id="g-bee-body" cx="40%" cy="30%" r="75%">
                  <stop offset="0" stop-color="#ffe27a"/><stop offset=".55" stop-color="#f6b40e"/><stop offset="1" stop-color="#c46a00"/>
                </radialGradient>
                <radialGradient id="g-bee-head" cx="40%" cy="35%" r="70%">
                  <stop offset="0" stop-color="#3d2c12"/><stop offset="1" stop-color="#0d0904"/>
                </radialGradient>
                <linearGradient id="g-bee-wing" x1="0" y1="0" x2="0" y2="1">
                  <stop offset="0" stop-color="#fff" stop-opacity=".85"/><stop offset="1" stop-color="#d6ecff" stop-opacity=".25"/>
                </linearGradient>
                <clipPath id="clip-bee-body"><ellipse cx="96" cy="98" rx="54" ry="38"/></clipPath>
              </defs>

              <g id="wing-back">
                <path d="M104 64 C 110 24, 140 2, 158 16 C 172 30, 146 56, 104 64Z" fill="url(#g-bee-wing)" stroke="#fff" stroke-opacity=".55" stroke-width="1.5"/>
                <path d="M106 60 C 122 40, 138 26, 152 20" fill="none" stroke="#fff" stroke-opacity=".4"/>
              </g>
              <g stroke="#1a1207" stroke-width="4" stroke-linecap="round" fill="none">
                <path d="M76 130 q -4 10 -12 13"/><path d="M98 134 q -2 10 -8 15"/><path d="M120 130 q 2 10 -2 15"/>
              </g>
              <path d="M44 94 L 24 100 L 44 106 Z" fill="#1a1207"/>
              <ellipse cx="96" cy="98" rx="54" ry="38" fill="url(#g-bee-body)"/>
              <g clip-path="url(#clip-bee-body)" fill="#1a1207">
                <rect x="60" y="50" width="14" height="100" rx="6" transform="rotate(8 67 100)"/>
                <rect x="88" y="50" width="15" height="100" rx="6" transform="rotate(5 95 100)"/>
                <rect x="117" y="50" width="14" height="100" rx="6" transform="rotate(2 124 100)"/>
              </g>
              <ellipse cx="88" cy="78" rx="30" ry="9" fill="#fff" opacity=".28"/>
              <circle cx="150" cy="90" r="26" fill="url(#g-bee-head)"/>
              <circle cx="160" cy="84" r="8" fill="#fff"/>
              <circle cx="162.5" cy="84.5" r="4.5" fill="#0d0904"/>
              <circle cx="164.5" cy="81.5" r="1.6" fill="#fff"/>
              <circle cx="158" cy="101" r="4" fill="#ff8a1f" opacity=".6"/>
              <path d="M161 105 q 6 4 12 -1" stroke="#f6b40e" stroke-width="2.2" fill="none" stroke-linecap="round"/>
              <g id="antennae">
                <path d="M146 66 C 144 46, 150 34, 160 30" stroke="#1a1207" stroke-width="3.5" fill="none" stroke-linecap="round"/>
                <path d="M156 68 C 162 50, 174 42, 184 42" stroke="#1a1207" stroke-width="3.5" fill="none" stroke-linecap="round"/>
                <circle cx="160" cy="30" r="4.5" fill="#f6b40e"/><circle cx="184" cy="42" r="4.5" fill="#f6b40e"/>
              </g>
              <g id="wing-front">
                <path d="M96 64 C 70 20, 30 10, 22 34 C 16 54, 52 66, 96 64Z" fill="url(#g-bee-wing)" stroke="#fff" stroke-opacity=".7" stroke-width="1.5"/>
                <path d="M92 60 C 70 44, 46 34, 30 34" fill="none" stroke="#fff" stroke-opacity=".45"/>
              </g>
            </svg>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- ============ 01 · NAV ============ -->
  <header id="nav" class="fixed inset-x-0 top-0 z-50 border-b border-cream/10 bg-ink/60 backdrop-blur-xl">
    <nav class="mx-auto flex h-14 max-w-7xl items-center justify-between px-6">
      <a href="#hero" class="flex items-center gap-2 font-display text-xl font-semibold tracking-tight">
        <svg width="22" height="24" viewBox="0 0 22 24" aria-hidden="true"><path d="M11 1l9.5 5.5v11L11 23 1.5 17.5v-11z" fill="#f6b40e"/></svg>
        Hive
      </a>
      <ul class="hidden items-center gap-8 text-sm text-cream/70 md:flex">
        <li><a href="#statement" class="transition hover:text-cream">Story</a></li>
        <li><a href="#product" class="transition hover:text-cream">No.01</a></li>
        <li><a href="#gallery" class="transition hover:text-cream">Flavors</a></li>
        <li><a href="#process" class="transition hover:text-cream">Process</a></li>
        <li><a href="#reviews" class="transition hover:text-cream">Reviews</a></li>
      </ul>
      <a href="#cta" class="rounded-full bg-honey px-4 py-1.5 text-sm font-semibold text-ink transition hover:bg-amber">Pre-order</a>
    </nav>
    <div id="progress" class="h-[2px] bg-gradient-to-r from-honey to-amber" style="transform:scaleX(0)"></div>
  </header>

  <main>
    <!-- ============ 02 · HERO ============ -->
    <section id="hero" class="flex h-screen items-end overflow-hidden md:items-center"
      data-bee='[{"at":0,"x":0.74,"y":0.5,"s":1.35,"xm":0.66,"ym":0.24},{"at":1,"x":0.6,"y":0.2,"s":1,"xm":0.8,"ym":0.14}]'>
      <div class="honeycomb absolute inset-0"></div>
      <div class="hero-glow glow left-[55%] top-1/2 h-[90vmin] w-[90vmin] -translate-x-1/2 -translate-y-1/2"></div>
      <div class="hero-inner relative mx-auto w-full max-w-7xl px-6 pb-20 md:pb-0">
        <p class="hero-eyebrow mb-6 text-xs font-semibold uppercase tracking-[.3em] text-honey">Hive No.01 · Raw Wildflower Honey</p>
        <h1 class="font-display text-[clamp(3.2rem,10vw,9rem)] font-semibold leading-[.92] tracking-tight" aria-label="Pure gold. Made by bees.">
          <span class="line"><span class="split">Pure gold.</span></span>
          <span class="line"><span class="split italic text-honey">Made by bees.</span></span>
        </h1>
        <p class="hero-sub mt-8 max-w-md text-lg text-cream/70">Raw, cold-extracted, single-origin honey. Nothing added, nothing taken away. Just the summer, in a jar.</p>
        <div class="hero-cta mt-10 flex flex-wrap gap-4">
          <a href="#cta" class="rounded-full bg-honey px-7 py-3.5 font-semibold text-ink transition hover:bg-amber">Reserve a jar</a>
          <a href="#statement" class="rounded-full border border-cream/20 px-7 py-3.5 font-semibold transition hover:border-cream/50">Watch the story ↓</a>
        </div>
      </div>
      <div class="scroll-cue absolute bottom-8 left-1/2 hidden -translate-x-1/2 flex-col items-center gap-2 text-[11px] uppercase tracking-[.3em] text-cream/50 md:flex">
        Scroll
        <span class="flex h-9 w-5 justify-center rounded-full border border-cream/30 pt-1.5"><span class="cue-dot h-1.5 w-1.5 rounded-full bg-honey"></span></span>
      </div>
    </section>

    <!-- ============ 03 · STATEMENT (pinned) ============ -->
    <section id="statement" class="pin flex items-center justify-center px-6"
      data-bee='[{"at":0,"x":0.86,"y":0.2,"s":0.75},{"at":1,"x":0.14,"y":0.82,"s":0.75}]'>
      <div class="max-w-5xl text-center">
        <p id="statement-text" class="font-display text-[clamp(2rem,5.2vw,4.6rem)] font-medium leading-[1.12] tracking-tight">Every jar holds the work of <em class="italic text-honey">sixty thousand bees</em>, two million flowers, and one quiet promise: <em class="italic text-honey">nothing added, nothing taken away.</em></p>
        <p class="statement-meta mt-10 text-sm uppercase tracking-[.3em] text-cream/50">Harvested once a year · Never heated</p>
      </div>
    </section>

    <!-- ============ 04 · PRODUCT REVEAL (pinned) ============ -->
    <section id="product" class="pin"
      data-bee='[{"at":0,"x":0.82,"y":0.24,"s":0.85,"xm":0.85,"ym":0.18},{"at":0.45,"x":0.22,"y":0.42,"s":0.9,"xm":0.15},{"at":0.78,"el":"#jar-perch","oy":-34,"s":0.6},{"at":1,"el":"#jar-perch","oy":-34,"s":0.6}]'>
      <div class="product-copy absolute inset-x-0 top-[13vh] z-10 px-6 text-center">
        <p class="text-xs font-semibold uppercase tracking-[.3em] text-honey">Introducing</p>
        <h2 class="mt-3 font-display text-[clamp(2.6rem,7vw,6rem)] font-semibold leading-none tracking-tight">Hive <span class="italic text-honey">No.01</span></h2>
        <p class="mx-auto mt-4 max-w-md text-cream/60">Wildflower honey from a single valley, jarred within a day of the harvest.</p>
      </div>
      <div class="absolute inset-x-0 bottom-[5vh] flex justify-center">
        <div class="glow left-1/2 top-1/2 h-[min(80vw,640px)] w-[min(80vw,640px)] -translate-x-1/2 -translate-y-1/2"></div>
        <div id="jar-wrap" class="relative aspect-[3/4]" style="width:min(300px,58vw,40vh)">
          <div id="jar-perch" class="absolute left-1/2 top-[3%] h-px w-px"></div>
          <svg viewBox="0 0 240 320" class="h-full w-full" role="img" aria-label="A jar of Hive No.01 honey">
            <g id="jar-lid">
              <rect x="52" y="10" width="136" height="44" rx="10" fill="url(#g-lid)"/>
              <g stroke="#000" stroke-opacity=".22" stroke-width="2">
                <line x1="66" y1="16" x2="66" y2="48"/><line x1="80" y1="16" x2="80" y2="48"/><line x1="94" y1="16" x2="94" y2="48"/><line x1="108" y1="16" x2="108" y2="48"/><line x1="122" y1="16" x2="122" y2="48"/><line x1="136" y1="16" x2="136" y2="48"/><line x1="150" y1="16" x2="150" y2="48"/><line x1="164" y1="16" x2="164" y2="48"/><line x1="178" y1="16" x2="178" y2="48"/>
              </g>
            </g>
            <rect x="62" y="52" width="116" height="16" rx="4" fill="#2a1c08"/>
            <path d="M26 132 q 47 -14 94 0 t 94 0 v144 a30 30 0 0 1 -30 30 h-128 a30 30 0 0 1 -30 -30z" fill="url(#g-honey)"/>
            <path d="M48 70 h144 a28 28 0 0 1 28 28 v178 a34 34 0 0 1 -34 34 h-132 a34 34 0 0 1 -34 -34 v-178 a28 28 0 0 1 28 -28z" fill="url(#g-glass)" stroke="#fff3d6" stroke-opacity=".35" stroke-width="2"/>
            <rect x="62" y="172" width="116" height="84" rx="8" fill="#fff3d6"/>
            <text x="120" y="212" text-anchor="middle" font-family="Fraunces, serif" font-size="30" font-weight="700" fill="#0b0906">HIVE</text>
            <text x="120" y="236" text-anchor="middle" font-family="Inter, sans-serif" font-size="8.5" letter-spacing="1.2" fill="#7a4200">No.01 · WILDFLOWER</text>
            <rect x="34" y="92" width="8" height="186" rx="4" fill="#fff" opacity=".22"/>
          </svg>
          <div class="callout absolute right-[108%] top-[22%] hidden whitespace-nowrap rounded-full border border-cream/15 bg-ink/70 px-4 py-2 text-sm backdrop-blur md:block"><span class="mr-2 inline-block h-2 w-2 rounded-full bg-honey"></span>Raw, never heated</div>
          <div class="callout absolute left-[108%] top-[38%] hidden whitespace-nowrap rounded-full border border-cream/15 bg-ink/70 px-4 py-2 text-sm backdrop-blur md:block"><span class="mr-2 inline-block h-2 w-2 rounded-full bg-honey"></span>Cold-extracted at 22°C</div>
          <div class="callout absolute right-[108%] top-[62%] hidden whitespace-nowrap rounded-full border border-cream/15 bg-ink/70 px-4 py-2 text-sm backdrop-blur md:block"><span class="mr-2 inline-block h-2 w-2 rounded-full bg-honey"></span>Single-origin valley</div>
          <div class="callout absolute left-[108%] top-[78%] hidden whitespace-nowrap rounded-full border border-cream/15 bg-ink/70 px-4 py-2 text-sm backdrop-blur md:block"><span class="mr-2 inline-block h-2 w-2 rounded-full bg-honey"></span>Endlessly recyclable glass</div>
        </div>
      </div>
    </section>

    <!-- ============ 05 · FEATURES ============ -->
    <section id="features" class="px-6 py-32 md:py-44"
      data-bee='[{"at":0,"x":0.88,"y":0.18,"s":0.8},{"at":0.5,"x":0.5,"y":0.12,"s":0.7,"xm":0.85},{"at":1,"x":0.1,"y":0.85,"s":0.8}]'>
      <div class="mx-auto max-w-7xl">
        <p class="text-xs font-semibold uppercase tracking-[.3em] text-honey">Why it tastes different</p>
        <h2 class="mt-4 max-w-3xl font-display text-[clamp(2.2rem,5vw,4.2rem)] font-semibold leading-[1.05] tracking-tight">Three decisions we refuse to compromise on.</h2>
        <div class="mt-16 grid gap-6 md:grid-cols-3">
          <article class="feature-card rounded-3xl border border-cream/10 bg-ink-2 p-8">
            <svg class="h-10 w-10 text-honey" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" aria-hidden="true"><circle cx="12" cy="12" r="2.5"/><path d="M12 9.5C12 6 14 4 16 4s2 3-1 6M14.5 12c3.5 0 5.5 2 5.5 4s-3 2-6-1M12 14.5c0 3.5-2 5.5-4 5.5s-2-3 1-6M9.5 12C6 12 4 10 4 8s3-2 6 1"/></svg>
            <h3 class="mt-6 text-xl font-semibold">Raw &amp; unfiltered</h3>
            <p class="mt-3 text-cream/60">Pollen, enzymes and the faint perfume of the meadow stay in. Heat and fine filters stay out.</p>
          </article>
          <article class="feature-card rounded-3xl border border-cream/10 bg-ink-2 p-8">
            <svg class="h-10 w-10 text-honey" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" aria-hidden="true"><path d="M12 21s-7-6.2-7-11.5A7 7 0 0 1 19 9.5C19 14.8 12 21 12 21z"/><circle cx="12" cy="9.5" r="2.5"/></svg>
            <h3 class="mt-6 text-xl font-semibold">Single-origin</h3>
            <p class="mt-3 text-cream/60">Every jar traces back to one valley, one apiary and one harvest week. Scan the lid to see the exact field.</p>
          </article>
          <article class="feature-card rounded-3xl border border-cream/10 bg-ink-2 p-8">
            <svg class="h-10 w-10 text-honey" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.6" aria-hidden="true"><path d="M5 19c0-8 5-14 15-14 0 10-6 15-14 15"/><path d="M5 19c3-4 6-7 10-9"/></svg>
            <h3 class="mt-6 text-xl font-semibold">Hives first</h3>
            <p class="mt-3 text-cream/60">We only take the surplus. The colony always keeps enough honey to winter strong.</p>
          </article>
        </div>
      </div>
    </section>

    <!-- ============ 06 · HORIZONTAL GALLERY (pinned) ============ -->
    <section id="gallery" class="pin flex flex-col"
      data-bee='[{"at":0,"x":0.12,"y":0.84,"s":0.75},{"at":0.5,"x":0.5,"y":0.16,"s":0.7,"xm":0.85,"ym":0.12},{"at":1,"x":0.88,"y":0.84,"s":0.75}]'>
      <div class="px-[8vw] pt-24 md:pt-28">
        <p class="text-xs font-semibold uppercase tracking-[.3em] text-honey">The collection</p>
        <h2 class="mt-3 font-display text-[clamp(2rem,4.5vw,3.8rem)] font-semibold leading-none tracking-tight">Five flowers. Five golds.</h2>
      </div>
      <div class="flex flex-1 items-center">
        <div class="gallery-track">
          <article class="panel relative flex h-[56vh] w-[78vw] flex-col justify-between overflow-hidden rounded-[2rem] border border-cream/10 p-8 md:w-[40vw] md:p-12" style="--c:#f6b40e;background:linear-gradient(150deg,rgba(246,180,14,.28),#16110a 65%)">
            <span class="text-sm text-cream/60">01 — Wildflower</span>
            <svg class="drop absolute right-8 top-8 w-[28%]" viewBox="0 0 100 130" aria-hidden="true"><path d="M50 4C50 4 92 58 92 84a42 42 0 0 1-84 0C8 58 50 4 50 4Z" style="fill:var(--c)"/><ellipse cx="34" cy="80" rx="8" ry="16" fill="#fff" opacity=".3"/></svg>
            <div><h3 class="font-display text-4xl font-semibold md:text-6xl">Wildflower</h3><p class="mt-3 max-w-xs text-cream/60">Bright, floral, a little citrus. The everyday gold.</p></div>
          </article>
          <article class="panel relative flex h-[56vh] w-[78vw] flex-col justify-between overflow-hidden rounded-[2rem] border border-cream/10 p-8 md:w-[40vw] md:p-12" style="--c:#f7dc7c;background:linear-gradient(150deg,rgba(247,220,124,.24),#16110a 65%)">
            <span class="text-sm text-cream/60">02 — Acacia</span>
            <svg class="drop absolute right-8 top-8 w-[28%]" viewBox="0 0 100 130" aria-hidden="true"><path d="M50 4C50 4 92 58 92 84a42 42 0 0 1-84 0C8 58 50 4 50 4Z" style="fill:var(--c)"/><ellipse cx="34" cy="80" rx="8" ry="16" fill="#fff" opacity=".3"/></svg>
            <div><h3 class="font-display text-4xl font-semibold md:text-6xl">Acacia</h3><p class="mt-3 max-w-xs text-cream/60">Pale, clean and slow to crystallize. Vanilla on the finish.</p></div>
          </article>
          <article class="panel relative flex h-[56vh] w-[78vw] flex-col justify-between overflow-hidden rounded-[2rem] border border-cream/10 p-8 md:w-[40vw] md:p-12" style="--c:#b8650f;background:linear-gradient(150deg,rgba(184,101,15,.32),#16110a 65%)">
            <span class="text-sm text-cream/60">03 — Manuka</span>
            <svg class="drop absolute right-8 top-8 w-[28%]" viewBox="0 0 100 130" aria-hidden="true"><path d="M50 4C50 4 92 58 92 84a42 42 0 0 1-84 0C8 58 50 4 50 4Z" style="fill:var(--c)"/><ellipse cx="34" cy="80" rx="8" ry="16" fill="#fff" opacity=".3"/></svg>
            <div><h3 class="font-display text-4xl font-semibold md:text-6xl">Manuka</h3><p class="mt-3 max-w-xs text-cream/60">Dense, earthy, medicinal. A spoonful is a ritual.</p></div>
          </article>
          <article class="panel relative flex h-[56vh] w-[78vw] flex-col justify-between overflow-hidden rounded-[2rem] border border-cream/10 p-8 md:w-[40vw] md:p-12" style="--c:#c4aef0;background:linear-gradient(150deg,rgba(196,174,240,.22),#16110a 65%)">
            <span class="text-sm text-cream/60">04 — Lavender</span>
            <svg class="drop absolute right-8 top-8 w-[28%]" viewBox="0 0 100 130" aria-hidden="true"><path d="M50 4C50 4 92 58 92 84a42 42 0 0 1-84 0C8 58 50 4 50 4Z" style="fill:var(--c)"/><ellipse cx="34" cy="80" rx="8" ry="16" fill="#fff" opacity=".3"/></svg>
            <div><h3 class="font-display text-4xl font-semibold md:text-6xl">Lavender</h3><p class="mt-3 max-w-xs text-cream/60">Herbal and soft, from a single Provençal hillside.</p></div>
          </article>
          <article class="panel relative flex h-[56vh] w-[78vw] flex-col justify-between overflow-hidden rounded-[2rem] border border-cream/10 p-8 md:w-[40vw] md:p-12" style="--c:#6a3410;background:linear-gradient(150deg,rgba(140,70,20,.38),#16110a 65%)">
            <span class="text-sm text-cream/60">05 — Buckwheat</span>
            <svg class="drop absolute right-8 top-8 w-[28%]" viewBox="0 0 100 130" aria-hidden="true"><path d="M50 4C50 4 92 58 92 84a42 42 0 0 1-84 0C8 58 50 4 50 4Z" style="fill:var(--c)"/><ellipse cx="34" cy="80" rx="8" ry="16" fill="#fff" opacity=".3"/></svg>
            <div><h3 class="font-display text-4xl font-semibold md:text-6xl">Buckwheat</h3><p class="mt-3 max-w-xs text-cream/60">Dark as molasses. Malty, bold, unforgettable.</p></div>
          </article>
        </div>
      </div>
    </section>

    <!-- ============ 07 · STATS ============ -->
    <section id="stats" class="px-6 py-32 md:py-44"
      data-bee='[{"at":0,"x":0.88,"y":0.24,"s":0.8},{"at":0.5,"x":0.1,"y":0.5,"s":0.8},{"at":1,"x":0.85,"y":0.78,"s":0.8}]'>
      <div class="mx-auto max-w-7xl">
        <h2 class="max-w-3xl font-display text-[clamp(2.2rem,5vw,4.2rem)] font-semibold leading-[1.05] tracking-tight">Small jar. <span class="italic text-honey">Enormous effort.</span></h2>
        <div class="mt-16 grid grid-cols-2 gap-x-6 gap-y-14 md:grid-cols-4">
          <div class="stat"><p class="font-display text-[clamp(3rem,7vw,6rem)] font-semibold leading-none text-honey"><span class="count" data-to="60" data-suffix="k">60k</span></p><p class="mt-3 text-cream/60">bees in a single colony</p></div>
          <div class="stat"><p class="font-display text-[clamp(3rem,7vw,6rem)] font-semibold leading-none text-honey"><span class="count" data-to="2" data-suffix="M">2M</span></p><p class="mt-3 text-cream/60">flower visits per jar</p></div>
          <div class="stat"><p class="font-display text-[clamp(3rem,7vw,6rem)] font-semibold leading-none text-honey"><span class="count" data-to="0" data-suffix="">0</span></p><p class="mt-3 text-cream/60">additives, ever</p></div>
          <div class="stat"><p class="font-display text-[clamp(3rem,7vw,6rem)] font-semibold leading-none text-honey"><span class="count" data-to="100" data-suffix="%">100%</span></p><p class="mt-3 text-cream/60">traceable to the hive</p></div>
        </div>
      </div>
    </section>

    <!-- ============ 08 · ANATOMY / EXPLODED VIEW (pinned) ============ -->
    <section id="anatomy" class="pin"
      data-bee='[{"at":0,"x":0.82,"y":0.22,"s":0.8,"xm":0.82,"ym":0.16},{"at":1,"x":0.14,"y":0.72,"s":0.8,"xm":0.86,"ym":0.88}]'>
      <div class="anatomy-copy absolute inset-x-0 top-[12vh] z-10 mx-auto max-w-7xl px-6">
        <p class="text-xs font-semibold uppercase tracking-[.3em] text-honey">Anatomy of a jar</p>
        <h2 class="mt-3 max-w-xl font-display text-[clamp(2rem,4.5vw,3.8rem)] font-semibold leading-none tracking-tight">Taken apart. <span class="italic text-honey">Put together right.</span></h2>
      </div>
      <div class="anatomy-stage">
        <div class="layer" style="z-index:4">
          <svg viewBox="0 0 260 90" aria-hidden="true"><path d="M10 34v22a120 30 0 0 0 240 0V34" fill="#7a4800"/><ellipse cx="130" cy="34" rx="120" ry="30" fill="url(#g-lid)"/></svg>
          <span class="layer-label text-sm text-cream/80">Gold-leaf lid</span>
        </div>
        <div class="layer" style="z-index:3">
          <svg viewBox="0 0 260 90" aria-hidden="true"><path d="M10 34v14a120 30 0 0 0 240 0V34" fill="#a85e00"/><ellipse cx="130" cy="34" rx="120" ry="30" fill="url(#p-comb)"/></svg>
          <span class="layer-label text-sm text-cream/80">Comb cap</span>
        </div>
        <div class="layer" style="z-index:2">
          <svg viewBox="0 0 260 110" aria-hidden="true"><path d="M10 34v40a120 30 0 0 0 240 0V34" fill="#b85e00"/><ellipse cx="130" cy="34" rx="120" ry="30" fill="url(#g-honey)"/><ellipse cx="96" cy="28" rx="40" ry="8" fill="#fff" opacity=".25"/></svg>
          <span class="layer-label text-sm text-cream/80">Raw honey, 340 g</span>
        </div>
        <div class="layer" style="z-index:1">
          <svg viewBox="0 0 260 130" aria-hidden="true"><path d="M10 34v60a120 30 0 0 0 240 0V34" fill="#fff3d6" fill-opacity=".05" stroke="#fff3d6" stroke-opacity=".35" stroke-width="2"/><ellipse cx="130" cy="34" rx="120" ry="30" fill="none" stroke="#fff3d6" stroke-opacity=".45" stroke-width="2"/></svg>
          <span class="layer-label text-sm text-cream/80">Hand-blown glass</span>
        </div>
      </div>
    </section>

    <!-- ============ 09 · PROCESS ============ -->
    <section id="process" class="py-32 md:py-44"
      data-bee='[{"at":0,"el":"#process-line","y":0.5,"s":0.55},{"at":1,"el":"#process-line","y":0.5,"s":0.55}]'>
      <div class="mx-auto max-w-3xl px-6">
        <p class="text-xs font-semibold uppercase tracking-[.3em] text-honey">From flower to spoon</p>
        <h2 class="mt-4 font-display text-[clamp(2.2rem,5vw,4.2rem)] font-semibold leading-[1.05] tracking-tight">Four steps. No shortcuts.</h2>
        <div class="relative mt-20 pl-16 md:pl-24">
          <div id="process-line" class="absolute bottom-0 left-5 top-0 w-[2px] bg-cream/10 md:left-8">
            <div id="process-fill" class="absolute inset-0 origin-top bg-gradient-to-b from-honey to-amber"></div>
          </div>
          <div class="step relative pb-24"><span class="step-dot"></span><div class="step-body">
            <p class="text-sm text-honey">01</p><h3 class="mt-2 text-2xl font-semibold md:text-3xl">Forage</h3>
            <p class="mt-3 text-cream/60">Through late spring, the colony works a single valley of clover, thyme and wild rose.</p></div></div>
          <div class="step relative pb-24"><span class="step-dot"></span><div class="step-body">
            <p class="text-sm text-honey">02</p><h3 class="mt-2 text-2xl font-semibold md:text-3xl">Harvest</h3>
            <p class="mt-3 text-cream/60">Only fully capped frames are lifted, by hand, on one morning in July.</p></div></div>
          <div class="step relative pb-24"><span class="step-dot"></span><div class="step-body">
            <p class="text-sm text-honey">03</p><h3 class="mt-2 text-2xl font-semibold md:text-3xl">Cold-extract</h3>
            <p class="mt-3 text-cream/60">Spun at room temperature and strained once through cloth, never pasteurized.</p></div></div>
          <div class="step relative"><span class="step-dot"></span><div class="step-body">
            <p class="text-sm text-honey">04</p><h3 class="mt-2 text-2xl font-semibold md:text-3xl">Jar</h3>
            <p class="mt-3 text-cream/60">Poured, sealed and numbered within twenty-four hours. Then it comes to you.</p></div></div>
        </div>
      </div>
    </section>

    <!-- ============ 10 · REVIEWS ============ -->
    <section id="reviews" class="overflow-hidden px-6 py-32 md:py-44"
      data-bee='[{"at":0,"x":0.9,"y":0.2,"s":0.8},{"at":1,"x":0.1,"y":0.78,"s":0.8}]'>
      <div class="mx-auto max-w-7xl">
        <h2 class="max-w-3xl font-display text-[clamp(2.2rem,5vw,4.2rem)] font-semibold leading-[1.05] tracking-tight">People keep <span class="italic text-honey">licking the spoon.</span></h2>
        <div class="mt-16 grid gap-6 md:grid-cols-3">
          <div class="space-y-6" data-speed="0.6">
            <blockquote class="rounded-3xl border border-cream/10 bg-ink-2 p-8"><p class="text-lg">“It tastes like the field it came from. I didn't know honey could do that.”</p><footer class="mt-6 text-sm text-cream/50">Placeholder review · Lisbon</footer></blockquote>
            <blockquote class="rounded-3xl border border-cream/10 bg-ink-2 p-8"><p class="text-lg">“The jar alone is worth keeping. The honey didn't last a week.”</p><footer class="mt-6 text-sm text-cream/50">Placeholder review · Austin</footer></blockquote>
          </div>
          <div class="space-y-6 md:mt-24" data-speed="-0.4">
            <blockquote class="rounded-3xl border border-honey/30 bg-honey/10 p-8"><p class="font-display text-2xl italic">“Finally, a honey with a sense of place.”</p><footer class="mt-6 text-sm text-cream/50">Placeholder review · Kyoto</footer></blockquote>
            <blockquote class="rounded-3xl border border-cream/10 bg-ink-2 p-8"><p class="text-lg">“Scanned the lid, saw the actual hive. Unreasonably delightful.”</p><footer class="mt-6 text-sm text-cream/50">Placeholder review · Berlin</footer></blockquote>
          </div>
          <div class="space-y-6" data-speed="0.9">
            <blockquote class="rounded-3xl border border-cream/10 bg-ink-2 p-8"><p class="text-lg">“Floral, bright, and it crystallizes into something like butter.”</p><footer class="mt-6 text-sm text-cream/50">Placeholder review · Mexico City</footer></blockquote>
            <blockquote class="rounded-3xl border border-cream/10 bg-ink-2 p-8"><p class="text-lg">“Our tea ritual has a new main character.”</p><footer class="mt-6 text-sm text-cream/50">Placeholder review · London</footer></blockquote>
          </div>
        </div>
      </div>
    </section>

    <!-- ============ 11 · CTA (pinned) ============ -->
    <section id="cta" class="pin flex items-center justify-center px-6 text-center" style="background:#f6b40e;color:#0b0906"
      data-bee='[{"at":0,"x":0.84,"y":0.2,"s":0.9},{"at":0.7,"el":"#cta-btn","ax":1,"ay":0,"ox":-6,"oy":-22,"s":0.55},{"at":1,"el":"#cta-btn","ax":1,"ay":0,"ox":-6,"oy":-22,"s":0.55}]'>
      <div class="max-w-3xl">
        <p class="cta-eyebrow text-xs font-semibold uppercase tracking-[.3em] opacity-70">First harvest · Summer 2027</p>
        <h2 class="cta-title mt-5 font-display text-[clamp(2.6rem,7vw,6rem)] font-semibold leading-[.98] tracking-tight">Taste the year the bees had.</h2>
        <p class="cta-sub mx-auto mt-6 max-w-md text-lg opacity-70">Limited to 4,000 numbered jars. Reserve now, pay when it ships.</p>
        <button id="cta-btn" type="button" class="mt-10 inline-flex items-center gap-3 rounded-full bg-ink px-8 py-4 text-lg font-semibold text-cream transition hover:scale-[1.03]">Reserve a jar — $38 <span aria-hidden="true">→</span></button>
      </div>
    </section>
  </main>

  <!-- ============ 12 · FOOTER ============ -->
  <footer id="footer" class="border-t border-cream/10 px-6 py-16"
    data-bee='[{"at":1,"x":1.25,"y":0.1,"s":0.5}]'>
    <div class="mx-auto grid max-w-7xl gap-10 md:grid-cols-4">
      <div>
        <a href="#hero" class="flex items-center gap-2 font-display text-2xl font-semibold">
          <svg width="22" height="24" viewBox="0 0 22 24" aria-hidden="true"><path d="M11 1l9.5 5.5v11L11 23 1.5 17.5v-11z" fill="#f6b40e"/></svg>Hive
        </a>
        <p class="mt-4 max-w-xs text-sm text-cream/50">Raw honey from bees we know by name. Well, by hive number.</p>
      </div>
      <div><h4 class="text-sm font-semibold">Shop</h4><ul class="mt-4 space-y-2 text-sm text-cream/60"><li><a href="#product" class="hover:text-cream">No.01</a></li><li><a href="#gallery" class="hover:text-cream">Collection</a></li><li><a href="#cta" class="hover:text-cream">Pre-order</a></li></ul></div>
      <div><h4 class="text-sm font-semibold">Story</h4><ul class="mt-4 space-y-2 text-sm text-cream/60"><li><a href="#statement" class="hover:text-cream">Manifesto</a></li><li><a href="#process" class="hover:text-cream">Process</a></li><li><a href="#anatomy" class="hover:text-cream">The jar</a></li></ul></div>
      <div><h4 class="text-sm font-semibold">Stay in the loop</h4><p class="mt-4 text-sm text-cream/60">One email per harvest. That's it.</p></div>
    </div>
    <p class="mx-auto mt-14 max-w-7xl text-xs text-cream/40">© 2026 Hive — v1 functional prototype. Fictional brand, placeholder content.</p>
  </footer>

  <script>
    gsap.registerPlugin(ScrollTrigger, MotionPathPlugin);

    const $ = (s, r = document) => r.querySelector(s);
    const $$ = (s, r = document) => [...r.querySelectorAll(s)];

    /* ---------- Helpers ---------- */

    // Split text into word-wrapped character spans (hero headline)
    function splitChars(el) {
      const words = el.textContent.trim().split(/\s+/);
      el.textContent = '';
      el.setAttribute('aria-hidden', 'true');
      words.forEach((w, i) => {
        const ww = document.createElement('span');
        ww.className = 'word-wrap';
        [...w].forEach(c => {
          const s = document.createElement('span');
          s.className = 'char';
          s.textContent = c;
          ww.appendChild(s);
        });
        el.appendChild(ww);
        if (i < words.length - 1) el.appendChild(document.createTextNode(' '));
      });
    }

    // Split into word spans, keeping the classes of inline elements (statement)
    function splitWords(el) {
      const frag = document.createDocumentFragment();
      el.childNodes.forEach(n => {
        const cls = n.nodeType === 1 ? n.className : '';
        n.textContent.split(/(\s+)/).forEach(t => {
          if (!t) return;
          if (/^\s+$/.test(t)) return frag.appendChild(document.createTextNode(' '));
          const s = document.createElement('span');
          s.className = ('word ' + cls).trim();
          s.textContent = t;
          frag.appendChild(s);
        });
      });
      el.textContent = '';
      el.appendChild(frag);
    }

    // Layout offset of el inside root (ignores transforms, so it's the "resting" position)
    function offsetIn(el, root) {
      let x = 0, y = 0, n = el;
      while (n && n !== root) { x += n.offsetLeft; y += n.offsetTop; n = n.offsetParent; }
      return { left: x, top: y, width: el.offsetWidth, height: el.offsetHeight };
    }

    const outerOf = sec => sec.parentElement.classList.contains('pin-spacer') ? sec.parentElement : sec;

    /* ---------- Section scenes ---------- */

    function navScene() {
      const nav = $('#nav');
      gsap.fromTo('#progress', { scaleX: 0 }, { scaleX: 1, ease: 'none', scrollTrigger: { start: 0, end: 'max', scrub: .3 } });
      ScrollTrigger.create({
        start: 120, end: 'max',
        onUpdate: self => nav.classList.toggle('nav-hidden', self.direction === 1),
        onLeaveBack: () => nav.classList.remove('nav-hidden'),
      });
    }

    function heroScene() {
      gsap.timeline({ delay: .15 })
        .from('#hero .char', { yPercent: 110, rotation: 6, opacity: 0, duration: 1, ease: 'power4.out', stagger: .025 })
        .from('#hero .hero-eyebrow, #hero .hero-sub, #hero .hero-cta, #hero .scroll-cue', { y: 24, opacity: 0, duration: .8, stagger: .1, ease: 'power3.out' }, '-=.6');
      gsap.to('.cue-dot', { y: 14, duration: .8, repeat: -1, yoyo: true, ease: 'sine.inOut' });

      const st = { trigger: '#hero', start: 'top top', end: 'bottom top', scrub: true };
      gsap.to('#hero .hero-inner', { yPercent: -18, scale: .94, opacity: 0, ease: 'none', scrollTrigger: st });
      gsap.to('#hero .hero-glow', { scale: 1.6, opacity: .25, ease: 'none', scrollTrigger: { ...st } });
    }

    function statementScene() {
      gsap.timeline({ scrollTrigger: { trigger: '#statement', start: 'top top', end: '+=150%', pin: true, scrub: 1 } })
        .fromTo('#statement .word', { opacity: .12 }, { opacity: 1, stagger: .1, ease: 'none' })
        .fromTo('#statement .statement-meta', { opacity: 0, y: 20 }, { opacity: 1, y: 0, duration: .5 });
    }

    function productScene() {
      gsap.timeline({ scrollTrigger: { trigger: '#product', start: 'top top', end: '+=200%', pin: true, scrub: 1 } })
        .fromTo('#jar-wrap', { scale: .45, rotation: -10, y: 120, opacity: .2 }, { scale: 1, rotation: 0, y: 0, opacity: 1, duration: 1, ease: 'power2.out' }, 0)
        .fromTo('#product .glow', { scale: .2, opacity: 0 }, { scale: 1, opacity: 1, duration: 1 }, 0)
        .fromTo('#product .product-copy > *', { y: 40, opacity: 0 }, { y: 0, opacity: 1, stagger: .08, duration: .4 }, 0)
        .fromTo('#product .callout', { y: 20, opacity: 0 }, { y: 0, opacity: 1, stagger: .1, duration: .3 }, 1)
        .to({}, { duration: .3 });
    }

    function featuresScene() {
      gsap.fromTo('.feature-card', { y: 80, opacity: 0 }, {
        y: 0, opacity: 1, duration: 1, stagger: .15, ease: 'power3.out',
        scrollTrigger: { trigger: '#features .grid', start: 'top 80%', toggleActions: 'play none none reverse' },
      });
    }

    function galleryScene() {
      const track = $('.gallery-track');
      const dist = () => Math.max(0, track.scrollWidth - innerWidth);
      const tween = gsap.to(track, {
        x: () => -dist(), ease: 'none',
        scrollTrigger: { trigger: '#gallery', start: 'top top', end: () => '+=' + dist(), pin: true, scrub: 1, invalidateOnRefresh: true },
      });
      $$('#gallery .panel').forEach(p => {
        gsap.fromTo(p.querySelector('.drop'), { rotation: -25, scale: .7, y: 40 }, {
          rotation: 15, scale: 1.05, y: -30, ease: 'none',
          scrollTrigger: { trigger: p, containerAnimation: tween, start: 'left right', end: 'right left', scrub: true },
        });
      });
    }

    function statsScene() {
      gsap.fromTo('#stats .stat', { y: 50, opacity: 0 }, {
        y: 0, opacity: 1, duration: .9, stagger: .12, ease: 'power3.out',
        scrollTrigger: { trigger: '#stats .grid', start: 'top 80%' },
      });
      $$('#stats .count').forEach(el => {
        const o = { v: 0 }, to = +el.dataset.to, suf = el.dataset.suffix;
        el.textContent = '0' + suf;
        gsap.to(o, {
          v: to, duration: 2, ease: 'power2.out',
          scrollTrigger: { trigger: el, start: 'top 85%' },
          onUpdate: () => { el.textContent = Math.round(o.v) + suf; },
        });
      });
    }

    const layerGap = () => Math.min(130, innerHeight * .14);

    function anatomyScene() {
      gsap.timeline({ scrollTrigger: { trigger: '#anatomy', start: 'top top', end: '+=150%', pin: true, scrub: 1, invalidateOnRefresh: true } })
        .fromTo('#anatomy .anatomy-copy', { y: 40, opacity: 0 }, { y: 0, opacity: 1, duration: .3 }, 0)
        .fromTo('#anatomy .layer', { y: i => (i - 1.5) * 14 }, { y: i => (i - 1.5) * layerGap(), duration: 1, ease: 'power2.inOut' }, .1)
        .fromTo('#anatomy .layer-label', { x: -20, opacity: 0 }, { x: 0, opacity: 1, stagger: .08, duration: .4 }, .65)
        .to({}, { duration: .3 });
    }

    function processScene() {
      gsap.fromTo('#process-fill', { scaleY: 0 }, {
        scaleY: 1, ease: 'none',
        scrollTrigger: { trigger: '#process-line', start: 'top center', end: 'bottom center', scrub: true },
      });
      $$('#process .step').forEach(step => {
        ScrollTrigger.create({ trigger: step, start: 'top center', end: 'max', toggleClass: 'is-active' });
        gsap.fromTo(step.querySelector('.step-body'), { opacity: .25, x: 30 }, {
          opacity: 1, x: 0, ease: 'none',
          scrollTrigger: { trigger: step, start: 'top 75%', end: 'top 45%', scrub: true },
        });
      });
    }

    function reviewsScene() {
      $$('#reviews [data-speed]').forEach(col => {
        const s = +col.dataset.speed * 70;
        gsap.fromTo(col, { y: s }, { y: -s, ease: 'none', scrollTrigger: { trigger: '#reviews', start: 'top bottom', end: 'bottom top', scrub: true } });
      });
    }

    function ctaScene() {
      gsap.timeline({ scrollTrigger: { trigger: '#cta', start: 'top top', end: '+=120%', pin: true, scrub: 1 } })
        .fromTo('#cta', { backgroundColor: '#0b0906', color: '#fff3d6' }, { backgroundColor: '#f6b40e', color: '#0b0906', duration: 1, ease: 'none' }, 0)
        .fromTo('#cta .cta-title', { scale: .85, opacity: .4 }, { scale: 1, opacity: 1, duration: 1 }, 0)
        .fromTo('#cta-btn', { scale: .6, opacity: 0 }, { scale: 1, opacity: 1, duration: .4, ease: 'back.out(2)' }, .6)
        .to({}, { duration: .4 });
    }

    /* ---------- The bee ---------- */

    const dots = [];
    let dotIndex = 0;
    function buildTrailPool() {
      for (let i = 0; i < 18; i++) {
        const d = document.createElement('div');
        d.className = 'trail-dot';
        document.body.appendChild(d);
        dots.push(d);
      }
    }
    function puff(x, y) {
      const d = dots[dotIndex++ % dots.length];
      gsap.killTweensOf(d);
      gsap.fromTo(d, { x, y, xPercent: -50, yPercent: -50, opacity: .9, scale: 1 },
        { y: y + 18, opacity: 0, scale: .2, duration: .9, ease: 'power2.out' });
    }

    function beeScene() {
      const track = $('#bee'), intro = $('.bee-intro'), bank = $('.bee-bank'), face = $('.bee-face'), float = $('.bee-float');
      gsap.set(track, { xPercent: -50, yPercent: -50, autoAlpha: 1 });

      // Idle hover: three sine loops with unrelated periods feel organic
      gsap.to(float, { y: -16, duration: 1.5, ease: 'sine.inOut', yoyo: true, repeat: -1 });
      gsap.to(float, { x: 8, duration: 2.3, ease: 'sine.inOut', yoyo: true, repeat: -1 });
      gsap.to(float, { rotation: 4, duration: 1.9, ease: 'sine.inOut', yoyo: true, repeat: -1 });
      gsap.to('#antennae', { rotation: 7, svgOrigin: '150 68', duration: .9, ease: 'sine.inOut', yoyo: true, repeat: -1 });

      // Wing flap; timeScale is driven by scroll velocity
      const wings = gsap.timeline({ repeat: -1, yoyo: true })
        .to('#wing-front', { rotation: -32, scaleY: .6, svgOrigin: '98 66', duration: .055, ease: 'sine.inOut' }, 0)
        .to('#wing-back', { rotation: 30, scaleY: .6, svgOrigin: '104 66', duration: .055, ease: 'sine.inOut' }, 0);

      // Entrance
      gsap.from(intro, { x: -innerWidth * .7, y: innerHeight * .35, scale: .3, rotation: -25, duration: 2.4, ease: 'power3.out', delay: .2 });

      // Scroll path, rebuilt from data-bee waypoints on every refresh
      const state = { p: 0 };
      let beeTl = null;

      function buildBee() {
        if (beeTl) beeTl.kill();
        const vw = innerWidth, vh = innerHeight, mobile = vw < 768;
        const max = ScrollTrigger.maxScroll(window) || 1;
        const pts = [];

        $$('[data-bee]').forEach(sec => {
          const wrap = outerOf(sec), pinned = wrap !== sec;
          const top = wrap.getBoundingClientRect().top + scrollY;
          JSON.parse(sec.dataset.bee).forEach(w => {
            // Pinned: at 0..1 spans the pin. Otherwise: section top at viewport center -> bottom at center.
            const S = gsap.utils.clamp(0, max, pinned
              ? top + w.at * (wrap.offsetHeight - vh)
              : top - vh * .5 + w.at * sec.offsetHeight);
            let x = mobile && w.xm != null ? w.xm : w.x;
            let y = mobile && w.ym != null ? w.ym : w.y;
            x = x != null ? x * vw : null;
            y = y != null ? y * vh : null;
            if (w.el) {
              const o = offsetIn($(w.el, sec), sec);
              if (x == null) x = o.left + o.width * (w.ax ?? .5);
              if (y == null) y = (pinned ? 0 : top - S) + o.top + o.height * (w.ay ?? .5);
            }
            pts.push({ S, x: x + (w.ox || 0), y: y + (w.oy || 0), s: (w.s ?? 1) * (mobile ? .8 : 1) });
          });
        });
        pts.sort((a, b) => a.S - b.S);

        // A fresh paused timeline won't render at progress 0, so place the bee explicitly
        gsap.set(track, { x: pts[0].x, y: pts[0].y, scale: pts[0].s });
        beeTl = gsap.timeline({ paused: true });
        beeTl.set(track, { x: pts[0].x, y: pts[0].y, scale: pts[0].s }, 0);
        pts.forEach((a, i) => {
          const b = pts[i + 1];
          if (!b) return;
          const t = a.S / max, d = (b.S - a.S) / max;
          if (d <= .0001) return beeTl.set(track, { x: b.x, y: b.y, scale: b.s }, t);
          const dx = b.x - a.x, dy = b.y - a.y, dist = Math.hypot(dx, dy);
          if (dist < 4) return beeTl.to(track, { x: b.x, y: b.y, scale: b.s, duration: d, ease: 'none' }, t);
          // Swoop: bend each leg sideways, alternating sides
          const bend = Math.min(dist * .3, 180) * (i % 2 ? 1 : -1);
          const mid = { x: a.x + dx / 2 - dy / dist * bend, y: a.y + dy / 2 + dx / dist * bend };
          beeTl.to(track, {
            motionPath: { path: [{ x: a.x, y: a.y }, mid, { x: b.x, y: b.y }], curviness: 1.25, fromCurrent: false },
            scale: b.s, duration: d, ease: 'sine.inOut',
          }, t);
        });
        if (beeTl.duration() < 1) beeTl.set({}, {}, 1);
        beeTl.progress(state.p);
      }

      // Smoothed scroll progress + velocity-driven wing speed
      const master = ScrollTrigger.create({
        start: 0, end: 'max',
        onUpdate: self => {
          gsap.to(state, { p: self.progress, duration: .8, ease: 'power3.out', overwrite: true });
          const v = Math.abs(self.getVelocity());
          gsap.to(wings, { timeScale: 1 + Math.min(v / 600, 3), duration: .2, overwrite: true });
        },
      });
      const calm = () => gsap.to(wings, { timeScale: 1, duration: .8, overwrite: true });
      const onRefresh = () => { state.p = master.progress; buildBee(); };
      ScrollTrigger.addEventListener('scrollEnd', calm);
      ScrollTrigger.addEventListener('refresh', onRefresh);

      // Per-frame: apply path, face direction of travel, bank into turns, leave a trail
      const bankTo = gsap.quickTo(bank, 'rotation', { duration: .5, ease: 'power3.out' });
      let lastX = null, lastY = null, facing = 1, frame = 0;
      function render() {
        if (!beeTl) return;
        beeTl.progress(state.p);
        const x = gsap.getProperty(track, 'x'), y = gsap.getProperty(track, 'y'), s = gsap.getProperty(track, 'scale');
        if (lastX === null) { lastX = x; lastY = y; return; }
        const dx = x - lastX, dy = y - lastY;
        lastX = x; lastY = y;
        if (Math.abs(dx) > 1.2) {
          const f = dx > 0 ? 1 : -1;
          if (f !== facing) { facing = f; gsap.to(face, { scaleX: f, duration: .35, ease: 'power2.out' }); }
        }
        bankTo(gsap.utils.clamp(-30, 30, (dy * 1.2 + Math.abs(dx) * .3) * facing));
        if (Math.hypot(dx, dy) > 4 && ++frame % 2 === 0) {
          puff(x - facing * track.offsetWidth * s * .42, y + track.offsetHeight * s * .05);
        }
      }
      gsap.ticker.add(render);

      return () => {
        gsap.ticker.remove(render);
        ScrollTrigger.removeEventListener('scrollEnd', calm);
        ScrollTrigger.removeEventListener('refresh', onRefresh);
        if (beeTl) beeTl.kill();
      };
    }

    // Reduced motion: no scroll choreography, the bee rests in a corner
    function staticScene() {
      gsap.set('#bee', { xPercent: -50, yPercent: -50, x: innerWidth - 70, y: innerHeight - 60, scale: .5, autoAlpha: 1 });
      gsap.set('#anatomy .layer', { y: i => (i - 1.5) * layerGap() });
    }

    /* ---------- Nav links (pin-aware smooth scroll) ---------- */

    function initNavLinks() {
      $$('a[href^="#"]').forEach(a => a.addEventListener('click', e => {
        const target = $(a.getAttribute('href'));
        if (!target) return;
        e.preventDefault();
        const reduce = matchMedia('(prefers-reduced-motion: reduce)').matches;
        window.scrollTo({ top: outerOf(target).getBoundingClientRect().top + scrollY, behavior: reduce ? 'auto' : 'smooth' });
      }));
    }

    /* ---------- Boot ---------- */

    function init() {
      $$('#hero .split').forEach(splitChars);
      splitWords($('#statement-text'));
      buildTrailPool();

      gsap.matchMedia().add({
        motion: '(prefers-reduced-motion: no-preference)',
        reduce: '(prefers-reduced-motion: reduce)',
      }, ctx => {
        if (ctx.conditions.reduce) return staticScene();
        // Created in document order so pin spacing stacks correctly
        navScene();
        heroScene();
        statementScene();
        productScene();
        featuresScene();
        galleryScene();
        statsScene();
        anatomyScene();
        processScene();
        reviewsScene();
        ctaScene();
        return beeScene();
      });

      initNavLinks();
      ScrollTrigger.refresh();
      document.fonts?.ready.then(() => ScrollTrigger.refresh());
    }

    // Wait for Tailwind (runtime-compiled) and layout to settle before measuring
    window.addEventListener('load', () => requestAnimationFrame(() => requestAnimationFrame(init)));
  </script>
</body>
</html>
