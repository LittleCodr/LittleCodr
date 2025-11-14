<!-- ================== README: Lucifer / Devil Theme ================== -->
<div align="center" style="background:#000000;padding:32px;border-radius:16px;">

<!-- Custom SVG Banner: Name + Animated Devil Wings -->
<!-- SVG is self-contained; wings animate, banner uses black-gold gradient -->
<svg width="100%" height="220" viewBox="0 0 1200 220" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="Mayank Agrawal banner">
  <defs>
    <linearGradient id="bggrad" x1="0" x2="1">
      <stop offset="0%" stop-color="#040404"/>
      <stop offset="100%" stop-color="#0b0000"/>
    </linearGradient>

    <linearGradient id="gold" x1="0" x2="1">
      <stop offset="0%" stop-color="#b8860b"/>
      <stop offset="100%" stop-color="#ffd700"/>
    </linearGradient>

    <linearGradient id="redglow" x1="0" x2="1">
      <stop offset="0%" stop-color="#ff1a1a"/>
      <stop offset="100%" stop-color="#7a0000"/>
    </linearGradient>

    <!-- subtle noise/glitch filter -->
    <filter id="glitch">
      <feTurbulence type="fractalNoise" baseFrequency="0.9" numOctaves="2" stitchTiles="stitch" result="noise"/>
      <feDisplacementMap in="SourceGraphic" in2="noise" scale="6" xChannelSelector="R" yChannelSelector="G"/>
    </filter>

    <!-- wing path to reuse -->
    <path id="wingPath" d="M0 100 C40 20, 120 10, 200 80 C280 150, 360 160, 420 120 C480 80, 520 30, 580 20 L640 40 L560 120 C480 200, 300 210, 200 160 C100 110, 20 120, 0 100 Z"/>
  </defs>

  <!-- background -->
  <rect width="100%" height="100%" fill="url(#bggrad)"/>

  <!-- gradient border (animated stroke-dashoffset effect) -->
  <rect x="8" y="8" width="1184" height="204" rx="12" ry="12" fill="none" stroke="url(#redglow)" stroke-width="4"
        stroke-dasharray="12 8">
    <animate attributeName="stroke-dashoffset" from="0" to="60" dur="6s" repeatCount="indefinite" />
  </rect>

  <!-- left wing (mirrored) -->
  <g transform="translate(120,40) scale(0.9)" style="mix-blend-mode:screen;">
    <use xlink:href="#wingPath" fill="transparent" stroke="#2b0000" stroke-width="4" opacity="0.95">
      <animateTransform attributeName="transform" type="translate" dur="4s" values="0 0; -6 2; 0 0" repeatCount="indefinite"/>
    </use>
    <use xlink:href="#wingPath" fill="url(#redglow)" opacity="0.12">
      <animate attributeName="opacity" dur="3s" values="0.08;0.18;0.08" repeatCount="indefinite"/>
    </use>
  </g>

  <!-- right wing (mirrored) -->
  <g transform="translate(860,40) scale(-0.9,0.9)" style="mix-blend-mode:screen;">
    <use xlink:href="#wingPath" fill="transparent" stroke="#2b0000" stroke-width="4" opacity="0.95">
      <animateTransform attributeName="transform" type="translate" dur="4s" values="0 0; 6 2; 0 0" repeatCount="indefinite"/>
    </use>
    <use xlink:href="#wingPath" fill="url(#redglow)" opacity="0.12">
      <animate attributeName="opacity" dur="3s" values="0.08;0.18;0.08" repeatCount="indefinite"/>
    </use>
  </g>

  <!-- main name -->
  <g transform="translate(600,120)" text-anchor="middle" font-family="Cinzel, Georgia, serif">
    <!-- glitch clones -->
    <text x="0" y="4" font-size="46" font-weight="700" fill="#ffffff" opacity="0.06" style="filter:url(#glitch);">
      Mayank Agrawal
    </text>
    <text x="-4" y="0" font-size="52" font-weight="800" fill="#ff0000" opacity="0.18">
      Mayank Agrawal
      <animate attributeName="opacity" values="0.12;0.2;0.12" dur="2.5s" repeatCount="indefinite"/>
    </text>
    <text x="0" y="0" font-size="56" font-weight="900" fill="url(#gold)">
      Mayank Agrawal
    </text>

    <!-- neon underline (animated) -->
    <rect x="-220" y="18" width="440" height="6" rx="3" fill="none" stroke="#ff2b2b" stroke-width="3" opacity="0.9">
      <animate attributeName="x" dur="6s" values="-220; -110; -220" repeatCount="indefinite"/>
      <animate attributeName="stroke-opacity" dur="3s" values="0.6;1;0.6" repeatCount="indefinite"/>
    </rect>
  </g>
</svg>

<!-- Devil tagline -->
<p style="color:#ffaaaa;margin-top:12px;font-size:15px;">
  Save time. <strong style="color:#ff4d4d">Just open my portfolio.</strong>
</p>

<!-- Floating SVG flames (decorative, small) -->
<div style="margin-top:10px;">
  <!-- flame cluster: multiple tiny animated SVGs -->
  <svg width="300" height="80" viewBox="0 0 300 80" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
    <defs>
      <linearGradient id="flameGrad" x1="0" x2="1">
        <stop offset="0%" stop-color="#ff9a00"/>
        <stop offset="60%" stop-color="#ff1a1a"/>
        <stop offset="100%" stop-color="#7a0000"/>
      </linearGradient>
    </defs>

    <!-- flame 1 -->
    <g transform="translate(30,50)">
      <path d="M0 0 C8 -18, 18 -28, 28 -20 C38 -12, 44 -30, 28 -40 C12 -50, -10 -40, 0 0 Z" fill="url(#flameGrad)" opacity="0.95">
        <animateTransform attributeName="transform" type="translate" dur="3.2s" values="0 0; 0 -6; 0 0" repeatCount="indefinite"/>
        <animate attributeName="opacity" dur="2.6s" values="0.85;1;0.85" repeatCount="indefinite"/>
      </path>
    </g>

    <!-- flame 2 -->
    <g transform="translate(90,56)">
      <path d="M0 0 C8 -22, 18 -34, 28 -18 C38 -2, 44 -28, 28 -38 C12 -48, -6 -34, 0 0 Z" fill="url(#flameGrad)" opacity="0.88">
        <animateTransform attributeName="transform" type="translate" dur="3.6s" values="0 0; 0 -8; 0 0" repeatCount="indefinite"/>
        <animate attributeName="opacity" dur="3.0s" values="0.7;0.98;0.7" repeatCount="indefinite"/>
      </path>
    </g>

    <!-- flame 3 -->
    <g transform="translate(200,54)">
      <path d="M0 0 C10 -20, 24 -36, 30 -22 C36 -8, 46 -34, 30 -44 C14 -54, -4 -30, 0 0 Z" fill="url(#flameGrad)" opacity="0.9">
        <animateTransform attributeName="transform" type="translate" dur="4.2s" values="0 0; 0 -10; 0 0" repeatCount="indefinite"/>
        <animate attributeName="opacity" dur="3.4s" values="0.75;1;0.75" repeatCount="indefinite"/>
      </path>
    </g>

    <!-- subtle drifting -->
    <animateTransform attributeName="transform" type="translate" dur="8s" values="0 0; 6 0; 0 0" repeatCount="indefinite"/>
  </svg>
</div>

<!-- short description -->
<p style="color:#caa7a7;max-width:780px;margin:12px auto 22px;font-size:14.5px;">
  iOS & Android engineer • Full-stack craftsman • Microsoft Learn Ambassador  
  <span style="display:block;color:#ff8b8b;margin-top:8px;">I build fast, scalable systems and don't apologize for clean design.</span>
</p>

<!-- buttons / badges -->
<div style="display:flex;gap:10px;justify-content:center;flex-wrap:wrap;margin-bottom:16px;">
  <a href="https://mayank1406.pro" style="text-decoration:none;">
    <img src="https://img.shields.io/badge/PORTFOLIO-%20mayank1406.pro-8B0000?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Portfolio" />
  </a>
  <a href="https://github.com/LittleCodr" style="text-decoration:none;">
    <img src="https://img.shields.io/badge/GitHub-LittleCodr-300000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
  </a>
  <a href="mailto:littlecodr@gmail.com" style="text-decoration:none;">
    <img src="https://img.shields.io/badge/Email-Hit%20Me-5c0000?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
  </a>
</div>

<!-- animated border container for "Arsenal" -->
<div style="padding:18px;border-radius:12px;background:linear-gradient(180deg,#050505, #080303);max-width:900px;margin:8px auto 28px;border:1px solid rgba(255,0,0,0.05);box-shadow:0 8px 40px rgba(0,0,0,0.7);">
  <div style="display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap;">
    <div style="display:flex;align-items:center;gap:14px;">
      <!-- small flame icon (svg) -->
      <svg width="44" height="44" viewBox="0 0 44 44" xmlns="http://www.w3.org/2000/svg" aria-hidden="true">
        <circle cx="22" cy="22" r="20" fill="#060606" stroke="#2b0000" stroke-width="2"/>
        <path d="M22 34 C26 28, 30 22, 24 16 C20 14, 18 18, 22 12 C20 18, 12 18, 16 26 C18 30, 22 34, 22 34 Z"
              fill="url(#flameGrad)" transform="translate(0,0)"/>
      </svg>

      <div style="text-align:left;">
        <div style="font-weight:700;color:#ffd16a;font-size:15px;">🩸 Infernal Arsenal</div>
        <div style="color:#c9a3a3;font-size:13px;">iOS, Android, React, Node, AWS, Docker, Clean Architecture</div>
      </div>
    </div>

    <div style="text-align:right;">
      <div style="font-weight:700;color:#ff6b6b;">Current Focus</div>
      <div style="color:#c9a3a3;font-size:13px;">Startup product, scaling infra, mobile-first design</div>
    </div>
  </div>
</div>

<!-- final footer -->
<p style="color:#8e8e8e;font-size:13px;margin-bottom:6px;">Profile views <img src="https://komarev.com/ghpvc/?username=LittleCodr&style=flat-square" alt="views" style="vertical-align:middle;margin-left:6px;"/></p>
<p style="color:#bdbdbd;font-size:13px;">Portfolio: <a href="https://mayank1406.pro" style="color:#ff4d4d;">mayank1406.pro</a></p>

</div>
<!-- ================== END README ================== -->
