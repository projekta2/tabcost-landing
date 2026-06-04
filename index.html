<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>TabCost Pro · Make your idle time visible</title>
  <meta name="description" content="Chrome extension that turns inactive tabs into a real economic metric based on your hourly rate. Free + Pro one-time $5.">
  <!-- Tabler Icons (for clean icons) -->
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@latest/dist/tabler-icons.min.css">
  <!-- Chart.js for 30-day history chart -->
  <script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.1/dist/chart.umd.min.js"></script>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #f8fafc;
      font-family: system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', sans-serif;
      color: #0f172a;
      line-height: 1.5;
      scroll-behavior: smooth;
    }

    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 24px;
    }

    /* Language switcher */
    .lang-bar {
      display: flex;
      justify-content: flex-end;
      gap: 12px;
      padding: 16px 0 8px;
      border-bottom: 1px solid #e2e8f0;
      margin-bottom: 32px;
    }
    .lang-btn {
      background: none;
      border: none;
      font-size: 14px;
      font-weight: 500;
      cursor: pointer;
      padding: 6px 12px;
      border-radius: 40px;
      transition: 0.2s;
      color: #475569;
    }
    .lang-btn.active {
      background: #f97316;
      color: white;
    }
    .lang-btn:hover:not(.active) {
      background: #e2e8f0;
    }

    /* Badges row */
    .badge-strip {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 12px;
      margin-bottom: 40px;
    }
    .badge-strip a {
      display: inline-block;
    }

    /* Hero */
    .hero {
      text-align: center;
      margin-bottom: 48px;
    }
    .hero h1 {
      font-size: 3rem;
      font-weight: 800;
      background: linear-gradient(135deg, #f97316, #ea580c);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      margin-bottom: 16px;
    }
    .hero p {
      font-size: 1.2rem;
      color: #334155;
      max-width: 720px;
      margin: 0 auto 24px;
    }
    .cta-buttons {
      display: flex;
      justify-content: center;
      gap: 16px;
      flex-wrap: wrap;
    }
    .btn {
      display: inline-block;
      padding: 12px 28px;
      border-radius: 40px;
      font-weight: 600;
      text-decoration: none;
      transition: 0.2s;
    }
    .btn-primary {
      background: #f97316;
      color: white;
      box-shadow: 0 4px 8px rgba(249,115,22,0.2);
    }
    .btn-primary:hover {
      background: #ea580c;
      transform: translateY(-2px);
    }
    .btn-outline {
      border: 1px solid #cbd5e1;
      color: #1e293b;
      background: white;
    }
    .btn-outline:hover {
      border-color: #f97316;
      color: #f97316;
    }

    /* Screenshot carousel (integrated from your file) */
    .carousel-section {
      background: #0b0f19;
      border-radius: 28px;
      padding: 24px 24px 32px;
      margin: 48px 0;
      box-shadow: 0 20px 35px -12px rgba(0,0,0,0.2);
    }
    .carousel-title {
      text-align: center;
      color: #e2e8f0;
      margin-bottom: 20px;
      font-size: 1.8rem;
      font-weight: 700;
    }
    .carousel-sub {
      text-align: center;
      color: #94a3b8;
      margin-bottom: 24px;
    }
    /* navigation */
    .nav-bar {
      display: flex;
      align-items: center;
      gap: 8px;
      padding: 12px 0 20px;
      flex-wrap: wrap;
      justify-content: center;
      border-bottom: 1px solid #1e293b;
      margin-bottom: 24px;
    }
    .nb {
      padding: 6px 16px;
      border-radius: 99px;
      border: 1px solid #334155;
      background: transparent;
      color: #cbd5e1;
      font-size: 12px;
      font-weight: 500;
      cursor: pointer;
      transition: all 0.2s;
    }
    .nb.active {
      background: #f97316;
      border-color: #f97316;
      color: white;
    }
    .nav-hint {
      font-size: 11px;
      color: #64748b;
      margin-left: auto;
    }
    .slide {
      width: 100%;
      border-radius: 20px;
      overflow: hidden;
      background: #0f172a;
      transition: 0.2s;
    }
    /* slide styles (from your HTML, slightly adapted) */
    .s1 { display: grid; grid-template-columns: 1fr 1fr; min-height: 400px; background: #0b0f19; }
    .s1-left { padding: 36px 28px; display: flex; flex-direction: column; justify-content: center; gap: 14px; }
    .s1-tag { font-size: 10px; color: #64748b; letter-spacing: 0.1em; text-transform: uppercase; font-weight: 700; }
    .s1-number { font-size: 62px; font-weight: 900; color: #f43f5e; line-height: 1; }
    .s1-sub { font-size: 19px; color: #f1f5f9; font-weight: 700; }
    .s1-desc { font-size: 12px; color: #94a3b8; line-height: 1.6; max-width: 270px; }
    .s1-badge { background: #1e293b; color: #38bdf8; font-size: 11px; font-weight: 700; padding: 6px 12px; border-radius: 8px; width: fit-content; }
    .s1-right { display: flex; align-items: center; justify-content: center; padding: 28px; background: #0f172a; }
    .pm { background: #0b0f19; border: 1px solid #1e293b; border-radius: 12px; padding: 14px; width: 210px; }
    .pm-hd { display: flex; justify-content: space-between; margin-bottom: 11px; }
    .pm-logo { font-weight: 800; font-size: 13px; color: #38bdf8; }
    .pm-pro { background: #f59e0b; color: #000; font-size: 9px; font-weight: 700; padding: 2px 7px; border-radius: 99px; }
    .pm-card { background: #0f172a; border: 1px solid #1e293b; border-radius: 10px; padding: 18px 10px; text-align: center; margin-bottom: 9px; }
    .pm-lbl { font-size: 8px; color: #64748b; text-transform: uppercase; }
    .pm-cost { font-size: 34px; font-weight: 900; color: #f43f5e; margin: 5px 0; }
    .pm-btn { width: 100%; background: #2563eb; color: white; border: none; padding: 8px; border-radius: 6px; font-size: 10px; font-weight: 700; margin-bottom: 5px; }
    .pm-btn2 { width: 100%; background: transparent; color: #475569; border: 1px solid #1e293b; padding: 6px; border-radius: 6px; font-size: 9px; }

    .s2 { padding: 28px; background: #0f172a; }
    .s-hook { font-size: 10px; color: #f43f5e; text-transform: uppercase; letter-spacing: 0.1em; margin-bottom: 6px; }
    .s-title { font-size: 20px; font-weight: 700; color: #f1f5f9; margin-bottom: 5px; }
    .s-sub { font-size: 12px; color: #475569; margin-bottom: 20px; }
    .at { width: 100%; border-collapse: collapse; }
    .at th { text-align: left; padding: 7px 10px; font-size: 9px; color: #334155; border-bottom: 1px solid #1e293b; }
    .at td { padding: 10px 10px; border-bottom: 1px solid #1e293b; font-size: 12px; color: #cbd5e1; }
    .at td:last-child { text-align: right; font-weight: 700; color: #f87171; }
    .dot { display: inline-block; width: 7px; height: 7px; border-radius: 50%; margin-right: 7px; }
    .dot-r { background: #f43f5e; } .dot-y { background: #f59e0b; } .dot-g { background: #475569; }
    .at-total { margin-top: 13px; display: flex; justify-content: space-between; background: #1e293b; padding: 11px 12px; border-radius: 8px; }
    .at-tl { font-size: 11px; color: #64748b; }

    .s3 { background: #0b0f19; padding: 28px; }
    .stats-row { display: grid; grid-template-columns: repeat(4,1fr); gap: 8px; margin-bottom: 20px; }
    .sc { background: #1e293b; border-radius: 8px; padding: 10px 12px; }
    .sc-lbl { font-size: 9px; color: #475569; }
    .sc-val { font-size: 20px; font-weight: 700; color: #f1f5f9; }
    .sc-val.r { color: #f87171; } .sc-val.g { color: #4ade80; }

    .s4 { display: grid; grid-template-columns: 1fr 1fr; min-height: 420px; }
    .s4l { background: #f8fafc; padding: 32px 28px; }
    .s4r { background: #0f172a; padding: 28px; }
    .pr-badge { background: #f59e0b; color: #000; font-size: 9px; font-weight: 700; padding: 2px 8px; border-radius: 4px; display: inline-block; margin-bottom: 12px; }
    .fi { display: flex; align-items: center; gap: 10px; margin-bottom: 12px; }
    .fi-ic { width: 26px; height: 26px; background: #eff6ff; border-radius: 6px; display: inline-flex; align-items: center; justify-content: center; color: #2563eb; }
    .ps-row { background: #1e293b; border-radius: 7px; padding: 8px 12px; display: flex; justify-content: space-between; margin-bottom: 6px; }

    .s5 { background: #f8fafc; padding: 32px 28px; text-align: center; }
    .plans { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; max-width: 600px; margin: 24px auto 0; }
    .pc { background: white; border-radius: 20px; padding: 20px; box-shadow: 0 4px 12px rgba(0,0,0,0.05); }
    .pc.featured { border: 2px solid #f97316; }
    .popular-tag { background: #fef3c7; color: #b45309; font-size: 10px; border-radius: 20px; padding: 2px 10px; display: inline-block; margin-bottom: 8px; }
    .pc-price { font-size: 28px; font-weight: 800; margin: 8px 0; }
    .pl { display: flex; align-items: center; gap: 8px; font-size: 13px; margin: 8px 0; }
    .ck { color: #10b981; font-weight: 700; }
    .cx { color: #cbd5e1; }
    .pc-cta { margin-top: 16px; width: 100%; padding: 10px; border-radius: 40px; font-weight: 700; border: none; cursor: pointer; }

    /* Guide Section */
    .guide-section {
      background: white;
      border-radius: 28px;
      padding: 32px;
      margin: 48px 0;
      box-shadow: 0 4px 20px rgba(0,0,0,0.05);
    }
    .guide-steps {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(240px,1fr));
      gap: 24px;
      margin: 32px 0;
    }
    .step-card {
      background: #f1f5f9;
      padding: 20px;
      border-radius: 20px;
    }
    .faq-q {
      font-weight: 700;
      margin-top: 20px;
    }
    .footer {
      text-align: center;
      padding: 40px 0 32px;
      border-top: 1px solid #e2e8f0;
      margin-top: 40px;
      color: #475569;
    }
    @media (max-width: 760px) {
      .s1, .s4 { grid-template-columns: 1fr; }
      .container { padding: 0 16px; }
      .hero h1 { font-size: 2.2rem; }
    }
  </style>
</head>
<body>

<div class="container">
  <!-- Language Switcher -->
  <div class="lang-bar">
    <button class="lang-btn active" data-lang="en">🇬🇧 English</button>
    <button class="lang-btn" data-lang="es">🇪🇸 Español</button>
  </div>

  <!-- Badge strip -->
  <div class="badge-strip">
    <a href="https://projekta2.github.io/tabcost-landing/"><img src="https://img.shields.io/badge/Landing%20Page-Live-brightgreen" alt="Live"></a>
    <a href="https://chrome.google.com/webstore/detail/tabcost-pro/oifegknejkfiibmfapdfcgemclgmmghm"><img src="https://img.shields.io/badge/Chrome%20Web%20Store-Install-blue" alt="Chrome Store"></a>
    <a href="https://github.com/projekta2/tabcost-pro-source"><img src="https://img.shields.io/badge/Source%20Code-GitHub-lightgrey" alt="Source"></a>
    <a href="https://github.com/projekta2/tabcost-privacy/blob/main/PRIVACY.md"><img src="https://img.shields.io/badge/Privacy%20Policy-6f42c1" alt="Privacy"></a>
    <a href="https://github.com/projekta2/tabcost-support/blob/main/SUPPORT.md"><img src="https://img.shields.io/badge/Support-28a745" alt="Support"></a>
    <a href="https://projekta2.gumroad.com/l/tabcost-pro"><img src="https://img.shields.io/badge/Buy%20License-ff90e8" alt="Buy"></a>
  </div>

  <!-- Hero -->
  <div class="hero">
    <h1 data-en="TabCost Pro" data-es="TabCost Pro">TabCost Pro</h1>
    <p data-en="Make your idle time visible — track the real cost of forgotten tabs based on your hourly rate." 
       data-es="Haz visible tu tiempo inactivo: el coste real de las pestañas olvidadas según tu tarifa por hora.">
       Make your idle time visible — track the real cost of forgotten tabs based on your hourly rate.
    </p>
    <div class="cta-buttons">
      <a href="https://chrome.google.com/webstore/detail/tabcost-pro/oifegknejkfiibmfapdfcgemclgmmghm" class="btn btn-primary" data-en="Install Free from Chrome Store" data-es="Instalar gratis desde Chrome Store">Install Free from Chrome Store</a>
      <a href="https://projekta2.gumroad.com/l/tabcost-pro" class="btn btn-outline" data-en="Upgrade to Pro ($5 one‑time)" data-es="Actualizar a Pro ($5 único pago)">Upgrade to Pro ($5 one‑time)</a>
    </div>
  </div>

  <!-- INTEGRATED SCREENSHOT CAROUSEL (from your HTML) -->
  <div class="carousel-section">
    <div class="carousel-title" data-en="See TabCost in action" data-es="TabCost en acción">See TabCost in action</div>
    <div class="carousel-sub" data-en="Real dashboard, real data" data-es="Panel real, datos reales">Real dashboard, real data</div>

    <div class="nav-bar">
      <button class="nb active" data-slide="1">1 · The hook</button>
      <button class="nb" data-slide="2">2 · Tab audit</button>
      <button class="nb" data-slide="3">3 · 30-day history</button>
      <button class="nb" data-slide="4">4 · Pro controls</button>
      <button class="nb" data-slide="5">5 · Free vs Pro</button>
      <span class="nav-hint">← navigate →</span>
    </div>

    <div id="carousel-container">
      <!-- Slide 1 -->
      <div class="slide s1" id="slide1">
        <div class="s1-left">
          <div class="s1-tag">Freelance UX consultant · $85/h · Tuesday</div>
          <div><div class="s1-number">$47.20</div><div class="s1-sub">lost to inactive<br>tabs today.</div></div>
          <div class="s1-desc">Your tabs don't sleep. Every minute a forgotten tab sits idle, it chips away at your hourly rate. TabCost makes the invisible cost visible.</div>
          <div class="s1-badge">TabCost · Free on Chrome Web Store</div>
        </div>
        <div class="s1-right">
          <div class="pm"><div class="pm-hd"><div class="pm-logo">TabCost</div><span class="pm-pro">PRO</span></div>
          <div class="pm-card"><div class="pm-lbl">Opportunity cost today</div><div class="pm-cost">$47.20</div><div class="pm-rate">Based on $85/h · 20% impact</div></div>
          <button class="pm-btn">Release focus & close inactive</button>
          <button class="pm-btn2">Advanced history & reports</button></div>
        </div>
      </div>
      <!-- Slide 2 -->
      <div class="slide s2" id="slide2" style="display:none">
        <div class="s-hook">Tab audit</div>
        <div class="s-title">See exactly what's costing you — tab by tab.</div>
        <div class="s-sub">7 inactive tabs · $85/h · Tuesday 14:32 · 5 min grace period</div>
        <table class="at"><thead><tr><th>Tab</th><th>Inactive time</th><th>Opportunity cost</th></tr></thead>
        <tbody>
          <tr><td><span class="dot dot-r"></span>Notion – Q3 Client Proposal</td><td>52 min</td><td>$12.35</td></tr>
          <tr><td><span class="dot dot-r"></span>Slack – #design-feedback</td><td>44 min</td><td>$10.47</td></tr>
          <tr><td><span class="dot dot-y"></span>Gmail – Inbox (7)</td><td>38 min</td><td>$9.03</td></tr>
          <tr><td><span class="dot dot-y"></span>YouTube – Figma Masterclass</td><td>29 min</td><td>$6.89</td></tr>
          <tr><td><span class="dot dot-g"></span>Linear – Sprint Backlog</td><td>21 min</td><td>$4.99</td></tr>
          <tr><td><span class="dot dot-g"></span>X / Twitter</td><td>15 min</td><td>$3.57</td></tr>
        </tbody></table>
        <div class="at-total"><span class="at-tl">Total opportunity cost today</span><span class="at-tv">$47.30</span></div>
      </div>
      <!-- Slide 3 with chart -->
      <div class="slide s3" id="slide3" style="display:none">
        <div class="s-hook">30-day history · Pro feature</div>
        <div class="s-title">Your productivity pattern, finally visible.</div>
        <div class="s-sub">May 2025 · Freelance UX consultant · $85/h</div>
        <div class="stats-row">
          <div class="sc"><div class="sc-lbl">Monthly total</div><div class="sc-val r">$847</div></div>
          <div class="sc"><div class="sc-lbl">Daily average</div><div class="sc-val">$42.30</div></div>
          <div class="sc"><div class="sc-lbl">Worst day</div><div class="sc-val r">$78.40</div></div>
          <div class="sc"><div class="sc-lbl">Best day</div><div class="sc-val g">$5.40</div></div>
        </div>
        <div style="height:200px; width:100%"><canvas id="histChart" style="height:100%; width:100%"></canvas></div>
      </div>
      <!-- Slide 4 -->
      <div class="slide s4" id="slide4" style="display:none">
        <div class="s4l"><div class="pr-badge">PRO</div><div class="s-title" style="color:#0f172a">Precision controls<br>for how you actually work.</div>
        <div class="s4-sub">Tune every parameter to your real rhythm.</div>
        <div class="fi"><div class="fi-ic"><i class="ti ti-clock"></i></div><div><strong>Grace period</strong><span> Tabs within 5 min ignored</span></div></div>
        <div class="fi"><div class="fi-ic"><i class="ti ti-x"></i></div><div><strong>Auto-close</strong><span> Idle tabs close after 30 min</span></div></div>
        <div class="fi"><div class="fi-ic"><i class="ti ti-eye-off"></i></div><div><strong>Ignored domains</strong><span> Spotify, Notion, YouTube</span></div></div>
        </div>
        <div class="s4r"><div style="font-size:10px;color:#334155">Pro settings</div>
        <div class="ps-row"><span>Grace minutes</span><span>5 min</span></div>
        <div class="ps-row"><span>Auto-close after</span><span>30 min</span></div>
        <div class="ps-row"><span>Ignored domains</span><span>spotify.com, notion.so</span></div>
        </div>
      </div>
      <!-- Slide 5 -->
      <div class="slide s5" id="slide5" style="display:none">
        <div class="s5h-t" style="font-size:24px; font-weight:700">Start free. Go Pro when you're ready.</div>
        <div class="s5h-s" style="margin-bottom:20px">One‑time payment · No subscription · Bilingual EN/ES</div>
        <div class="plans">
          <div class="pc"><div class="pc-name">Free</div><div class="pc-price">$0</div>
          <div class="pl"><span class="ck">✓</span> Daily cost tracking</div><div class="pl"><span class="ck">✓</span> Tab audit</div>
          <div class="pl"><span class="ck">✓</span> Close inactive tabs</div><div class="pl"><span class="cx">—</span> 365-day history</div>
          <button class="pc-cta cta-f" style="background:#f1f5f9">Install free</button></div>
          <div class="pc featured"><div class="popular-tag">Most popular</div><div class="pc-price">$5 <span>one time</span></div>
          <div class="pl"><span class="ck">✓</span> Everything in Free</div><div class="pl"><span class="ck">✓</span> 365-day history + CSV</div>
          <div class="pl"><span class="ck">✓</span> Auto-close + ignored domains</div><button class="pc-cta cta-p" style="background:#f97316;color:white">Activate Pro →</button></div>
        </div>
      </div>
    </div>
  </div>

  <!-- ACTIVATION GUIDE (from PDF) -->
  <div class="guide-section">
    <h2 data-en="📘 Activation Guide & License" data-es="📘 Guía de activación y licencia">📘 Activation Guide & License</h2>
    <p data-en="Keep this guide – your license key is unique and delivered in your Gumroad email." 
       data-es="Guarda esta guía – tu licencia es única y se entrega en tu correo de Gumroad.">
       Keep this guide – your license key is unique and delivered in your Gumroad email.
    </p>
    <div class="guide-steps">
      <div class="step-card"><strong>1️⃣ Install free extension</strong><br>Search "TabCost" on Chrome Web Store, add to Chrome.</div>
      <div class="step-card"><strong>2️⃣ Open popup</strong><br>Click the TabCost icon in toolbar.</div>
      <div class="step-card"><strong>3️⃣ Set hourly rate</strong><br>Enter your rate (e.g. $50/h).</div>
      <div class="step-card"><strong>4️⃣ Unlock Premium</strong><br>Click "Unlock Premium" in popup footer.</div>
      <div class="step-card"><strong>5️⃣ Paste license key</strong><br>Copy from Gumroad email exactly.</div>
      <div class="step-card"><strong>6️⃣ Enjoy Pro</strong><br>Badge turns PRO instantly.</div>
    </div>
    <div style="background:#f1f5f9; padding:16px; border-radius:20px; margin-top:20px">
      <p><strong>🔑 Your license key placeholder:</strong> <code>XXXX-XXXX-XXXX-XXXX</code> (check Gumroad receipt)</p>
      <p><strong>📌 What you unlocked:</strong> 365‑day history, auto‑close, CSV export, ignored domains, smart notifications, adjustable parameters.</p>
    </div>

    <h3 data-en="❓ Frequently asked questions" data-es="❓ Preguntas frecuentes">❓ Frequently asked questions</h3>
    <div class="faq-q">Q: Can I use the same key on multiple browsers?</div>
    <p data-en="Yes, on Chrome, Edge, Brave sharing same OS user account. One key = one user profile." 
       data-es="Sí, en Chrome, Edge, Brave con la misma cuenta de usuario. Una clave = un perfil.">
       Yes, on Chrome, Edge, Brave sharing same OS user account. One key = one user profile.
    </p>
    <div class="faq-q">Q: What if I change computers?</div>
    <p data-en="Contact hello@projekta2.com and we'll reset your license." data-es="Contacta a hello@projekta2.com y restableceremos tu licencia.">Contact hello@projekta2.com and we'll reset your license.</p>
    <div class="faq-q">Q: Is this a subscription?</div>
    <p data-en="No. One‑time payment, lifetime access, all future updates free." data-es="No. Pago único, acceso de por vida, actualizaciones gratis.">No. One‑time payment, lifetime access, all future updates free.</p>
    <div class="faq-q">Q: Where is my data stored?</div>
    <p data-en="Locally in your browser's storage. Only license verification contacts Gumroad servers." data-es="Localmente en tu navegador. Solo la verificación de licencia contacta servidores de Gumroad.">Locally in your browser's storage. Only license verification contacts Gumroad servers.</p>
  </div>

  <div class="footer">
    <p>© 2026 TabCost – Built by Alexandre Iglesias / Projekta2 · <a href="mailto:hello@projekta2.com">hello@projekta2.com</a></p>
    <p><a href="https://github.com/projekta2/tabcost-privacy/blob/main/PRIVACY.md">Privacy Policy</a> · <a href="https://github.com/projekta2/tabcost-support/blob/main/SUPPORT.md">Support</a></p>
  </div>
</div>

<script>
  // Carousel logic
  let currentSlide = 1;
  const slides = [1,2,3,4,5];
  function showSlide(n) {
    for(let i=1;i<=5;i++){
      const el = document.getElementById(`slide${i}`);
      if(el) el.style.display = i===n ? (i===1?'grid': (i===4?'grid':'block')) : 'none';
      const btn = document.querySelector(`.nb[data-slide="${i}"]`);
      if(btn) btn.classList.toggle('active', i===n);
    }
    currentSlide = n;
    if(n===3 && window.histChart) { setTimeout(() => { window.histChart.resize(); }, 50); }
  }
  document.querySelectorAll('.nb').forEach(btn => {
    btn.addEventListener('click', () => { const s = parseInt(btn.getAttribute('data-slide')); if(!isNaN(s)) showSlide(s); });
  });
  // Chart init for slide3
  const d30 = [38.4,47.2,52.1,44.8,31.2,8.4,5.2,55.6,71.2,78.4,61.8,49.2,12.1,6.8,42.3,38.9,45.2,41.7,35.4,11.2,9.4,28.4,22.1,31.5,19.8,24.6,7.2,5.4,18.9,14.2];
  const lbl30 = Array.from({length:30},(_,i)=>{const d=new Date(2025,4,1);d.setDate(i+1);return d.toLocaleDateString('en',{month:'short',day:'numeric'});});
  const clr = d30.map(v=>v>=60?'#f43f5e':v>=35?'#f97316':'#3b82f6');
  let histChart = null;
  window.addEventListener('load', () => {
    const ctx = document.getElementById('histChart')?.getContext('2d');
    if(ctx) {
      histChart = new Chart(ctx, {
        type:'bar', data:{labels:lbl30, datasets:[{data:d30, backgroundColor:clr, borderRadius:4}]},
        options:{ responsive:true, maintainAspectRatio:true, plugins:{legend:{display:false}, tooltip:{callbacks:{label:c=>' $'+c.parsed.y.toFixed(2)}}},
        scales:{x:{ticks:{color:'#475569', maxRotation:45, autoSkip:true}, grid:{display:false}}, y:{ticks:{color:'#475569', callback:v=>'$'+v}, grid:{color:'#1e293b'}}}
      });
    }
  });
  showSlide(1);

  // Bilingual switcher (EN/ES) for textual content
  const langBtns = document.querySelectorAll('.lang-btn');
  function setLanguage(lang) {
    document.querySelectorAll('[data-en][data-es]').forEach(el => {
      el.innerText = lang === 'en' ? el.getAttribute('data-en') : el.getAttribute('data-es');
    });
    document.querySelectorAll('.lang-btn').forEach(btn => btn.classList.remove('active'));
    document.querySelector(`.lang-btn[data-lang="${lang}"]`).classList.add('active');
  }
  langBtns.forEach(btn => {
    btn.addEventListener('click', () => { setLanguage(btn.getAttribute('data-lang')); });
  });
  setLanguage('en');
</script>

</body>
</html>
