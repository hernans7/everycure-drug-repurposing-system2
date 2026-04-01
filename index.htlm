<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DrugMatch — EveryCure-Style Repurposing System</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Mono:wght@400;500&family=Outfit:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --cream: #f5f0e8;
    --ink: #1a1a14;
    --ink-soft: #4a4a3a;
    --teal: #0e7c6b;
    --teal-light: #d4ede8;
    --teal-mid: #1a9f8a;
    --amber: #c97a1a;
    --amber-light: #faebd4;
    --coral: #c94a2a;
    --coral-light: #fae0d8;
    --rule: #d4cfc2;
    --card-bg: #fffdf8;
    --mono: 'DM Mono', monospace;
    --serif: 'DM Serif Display', serif;
    --sans: 'Outfit', sans-serif;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    font-family: var(--sans);
    background-color: var(--cream);
    color: var(--ink);
    font-size: 16px;
    line-height: 1.7;
    overflow-x: hidden;
  }

  /* ── HEADER ── */
  header {
    border-bottom: 1.5px solid var(--rule);
    padding: 0 48px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 64px;
    background: var(--cream);
    position: sticky;
    top: 0;
    z-index: 100;
  }

  .logo {
    font-family: var(--mono);
    font-size: 14px;
    font-weight: 500;
    letter-spacing: 0.08em;
    color: var(--teal);
    text-transform: uppercase;
  }

  nav { display: flex; gap: 32px; }
  nav a {
    font-size: 13px;
    font-weight: 400;
    color: var(--ink-soft);
    text-decoration: none;
    letter-spacing: 0.03em;
    transition: color 0.2s;
  }
  nav a:hover { color: var(--teal); }

  /* ── HERO ── */
  .hero {
    padding: 96px 48px 80px;
    max-width: 1100px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 64px;
    align-items: center;
    animation: fadeUp 0.7s ease both;
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  .hero-label {
    font-family: var(--mono);
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.15em;
    color: var(--teal);
    text-transform: uppercase;
    margin-bottom: 20px;
  }

  h1 {
    font-family: var(--serif);
    font-size: clamp(38px, 5vw, 58px);
    line-height: 1.08;
    color: var(--ink);
    margin-bottom: 24px;
  }

  h1 em {
    font-style: italic;
    color: var(--teal);
  }

  .hero-desc {
    font-size: 17px;
    font-weight: 300;
    color: var(--ink-soft);
    line-height: 1.75;
    max-width: 440px;
  }

  .hero-cta {
    margin-top: 36px;
    display: flex;
    gap: 16px;
    align-items: center;
  }

  .btn-primary {
    background: var(--teal);
    color: #fff;
    padding: 12px 28px;
    border-radius: 4px;
    font-family: var(--sans);
    font-size: 14px;
    font-weight: 500;
    text-decoration: none;
    letter-spacing: 0.02em;
    transition: background 0.2s, transform 0.15s;
    display: inline-block;
  }
  .btn-primary:hover { background: var(--teal-mid); transform: translateY(-1px); }

  .btn-ghost {
    font-size: 14px;
    font-weight: 400;
    color: var(--ink-soft);
    text-decoration: none;
    letter-spacing: 0.02em;
    border-bottom: 1px solid var(--rule);
    padding-bottom: 2px;
    transition: color 0.2s, border-color 0.2s;
  }
  .btn-ghost:hover { color: var(--teal); border-color: var(--teal); }

  /* Hero graphic: mini network */
  .hero-graphic {
    display: flex;
    align-items: center;
    justify-content: center;
    animation: fadeUp 0.7s 0.15s ease both;
  }

  .network-svg { width: 100%; max-width: 420px; }

  /* ── SECTION WRAPPER ── */
  .section {
    max-width: 1100px;
    margin: 0 auto;
    padding: 80px 48px;
    animation: fadeUp 0.6s ease both;
  }

  .section-label {
    font-family: var(--mono);
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.15em;
    color: var(--amber);
    text-transform: uppercase;
    margin-bottom: 14px;
  }

  h2 {
    font-family: var(--serif);
    font-size: clamp(28px, 3.5vw, 40px);
    line-height: 1.12;
    color: var(--ink);
    margin-bottom: 20px;
  }

  .section-intro {
    font-size: 16px;
    font-weight: 300;
    color: var(--ink-soft);
    max-width: 600px;
    margin-bottom: 48px;
    line-height: 1.8;
  }

  hr.section-rule {
    border: none;
    border-top: 1.5px solid var(--rule);
    margin: 0 48px;
  }

  /* ── HOW IT WORKS ── */
  .steps {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 32px;
  }

  .step-card {
    background: var(--card-bg);
    border: 1.5px solid var(--rule);
    border-radius: 8px;
    padding: 32px 28px;
    position: relative;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .step-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 32px rgba(0,0,0,0.07);
  }

  .step-num {
    font-family: var(--mono);
    font-size: 11px;
    font-weight: 500;
    letter-spacing: 0.12em;
    color: var(--teal);
    margin-bottom: 16px;
    text-transform: uppercase;
  }

  .step-title {
    font-family: var(--serif);
    font-size: 20px;
    margin-bottom: 12px;
    color: var(--ink);
  }

  .step-body {
    font-size: 14px;
    font-weight: 300;
    color: var(--ink-soft);
    line-height: 1.75;
  }

  .step-tag {
    display: inline-block;
    margin-top: 16px;
    font-family: var(--mono);
    font-size: 11px;
    padding: 4px 10px;
    border-radius: 3px;
    background: var(--teal-light);
    color: var(--teal);
    font-weight: 500;
  }

  /* ── EXAMPLE OUTPUT ── */
  .output-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 24px;
  }

  .match-card {
    background: var(--card-bg);
    border: 1.5px solid var(--rule);
    border-radius: 8px;
    overflow: hidden;
    transition: transform 0.2s, box-shadow 0.2s;
  }
  .match-card:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 32px rgba(0,0,0,0.07);
  }

  .match-header {
    padding: 16px 24px;
    border-bottom: 1.5px solid var(--rule);
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .match-drug {
    font-family: var(--serif);
    font-size: 20px;
    color: var(--ink);
  }

  .score-badge {
    font-family: var(--mono);
    font-size: 11px;
    font-weight: 500;
    padding: 5px 12px;
    border-radius: 3px;
    letter-spacing: 0.08em;
  }
  .score-high   { background: var(--teal-light);  color: var(--teal); }
  .score-medium { background: var(--amber-light); color: var(--amber); }
  .score-low    { background: var(--coral-light);  color: var(--coral); }

  .match-body { padding: 20px 24px; }

  .match-row {
    display: flex;
    gap: 12px;
    align-items: baseline;
    margin-bottom: 10px;
    font-size: 14px;
  }

  .match-row-label {
    font-family: var(--mono);
    font-size: 11px;
    font-weight: 500;
    color: var(--ink-soft);
    min-width: 120px;
    text-transform: uppercase;
    letter-spacing: 0.06em;
    padding-top: 2px;
  }

  .match-row-value {
    font-weight: 400;
    color: var(--ink);
    line-height: 1.5;
  }

  .target-pill {
    display: inline-block;
    background: var(--teal-light);
    color: var(--teal);
    font-family: var(--mono);
    font-size: 11px;
    font-weight: 500;
    padding: 3px 9px;
    border-radius: 3px;
    margin-right: 4px;
    margin-bottom: 4px;
  }

  .match-explanation {
    margin-top: 14px;
    padding: 14px 16px;
    background: #f0f7f5;
    border-left: 3px solid var(--teal);
    border-radius: 0 4px 4px 0;
    font-size: 13px;
    font-weight: 300;
    color: var(--ink-soft);
    font-style: italic;
    line-height: 1.65;
  }

  /* ── DATA SECTION ── */
  .data-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 24px;
  }

  .data-card {
    background: var(--card-bg);
    border: 1.5px solid var(--rule);
    border-radius: 8px;
    padding: 28px;
  }

  .data-card-header {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 20px;
  }

  .data-icon {
    width: 32px;
    height: 32px;
    border-radius: 4px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: var(--mono);
    font-size: 13px;
    font-weight: 500;
  }
  .icon-drug    { background: var(--teal-light);  color: var(--teal); }
  .icon-target  { background: var(--amber-light); color: var(--amber); }
  .icon-disease { background: var(--coral-light);  color: var(--coral); }

  .data-card-title {
    font-family: var(--mono);
    font-size: 12px;
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    color: var(--ink-soft);
  }

  .data-list { list-style: none; }
  .data-list li {
    font-size: 13px;
    font-weight: 400;
    color: var(--ink);
    padding: 7px 0;
    border-bottom: 1px solid var(--rule);
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .data-list li:last-child { border-bottom: none; }
  .data-list li::before {
    content: '';
    display: inline-block;
    width: 5px;
    height: 5px;
    border-radius: 50%;
    flex-shrink: 0;
  }
  .drug-dot::before    { background: var(--teal); }
  .target-dot::before  { background: var(--amber); }
  .disease-dot::before { background: var(--coral); }

  /* ── FOOTER ── */
  footer {
    border-top: 1.5px solid var(--rule);
    padding: 40px 48px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .footer-note {
    font-size: 13px;
    font-weight: 300;
    color: var(--ink-soft);
    max-width: 520px;
    line-height: 1.6;
  }

  .footer-logo {
    font-family: var(--mono);
    font-size: 12px;
    font-weight: 500;
    color: var(--teal);
    letter-spacing: 0.1em;
    text-transform: uppercase;
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 860px) {
    header { padding: 0 24px; }
    nav { gap: 20px; }
    .hero { grid-template-columns: 1fr; padding: 64px 24px 48px; gap: 40px; }
    .hero-graphic { display: none; }
    .section { padding: 60px 24px; }
    hr.section-rule { margin: 0 24px; }
    .steps { grid-template-columns: 1fr; }
    .output-grid { grid-template-columns: 1fr; }
    .data-grid { grid-template-columns: 1fr; }
    footer { flex-direction: column; gap: 16px; padding: 32px 24px; }
  }
</style>
</head>
<body>

<!-- ── HEADER ── -->
<header>
  <span class="logo">DrugMatch</span>
  <nav>
    <a href="#how">How it works</a>
    <a href="#output">Example output</a>
    <a href="#data">The data</a>
  </nav>
</header>

<!-- ── HERO ── -->
<div class="hero">
  <div class="hero-text">
    <p class="hero-label">EveryCure-style system</p>
    <h1>Finding new uses for <em>existing</em> drugs</h1>
    <p class="hero-desc">
      DrugMatch is a beginner-friendly model of how drug repurposing works.
      It scans approved drugs for hidden biological connections to diseases
      they were never designed to treat — and ranks the best matches automatically.
    </p>
    <div class="hero-cta">
      <a href="#output" class="btn-primary">See example results</a>
      <a href="#how" class="btn-ghost">How it works</a>
    </div>
  </div>
  <div class="hero-graphic">
    <!-- Mini network diagram SVG -->
    <svg class="network-svg" viewBox="0 0 420 340" fill="none" xmlns="http://www.w3.org/2000/svg">
      <!-- Connection lines -->
      <line x1="100" y1="80"  x2="210" y2="130" stroke="#0e7c6b" stroke-width="1.5" stroke-dasharray="5 4" opacity="0.5"/>
      <line x1="100" y1="170" x2="210" y2="130" stroke="#0e7c6b" stroke-width="1.5" stroke-dasharray="5 4" opacity="0.5"/>
      <line x1="100" y1="170" x2="210" y2="210" stroke="#0e7c6b" stroke-width="1.5" stroke-dasharray="5 4" opacity="0.5"/>
      <line x1="100" y1="260" x2="210" y2="210" stroke="#0e7c6b" stroke-width="1.5" stroke-dasharray="5 4" opacity="0.5"/>
      <line x1="210" y1="130" x2="330" y2="80"  stroke="#c94a2a" stroke-width="1.5" stroke-dasharray="5 4" opacity="0.5"/>
      <line x1="210" y1="130" x2="330" y2="170" stroke="#c94a2a" stroke-width="1.5" stroke-dasharray="5 4" opacity="0.5"/>
      <line x1="210" y1="210" x2="330" y2="170" stroke="#c94a2a" stroke-width="1.5" stroke-dasharray="5 4" opacity="0.5"/>
      <line x1="210" y1="210" x2="330" y2="260" stroke="#c94a2a" stroke-width="1.5" stroke-dasharray="5 4" opacity="0.5"/>
      <!-- Highlight path: Metformin → mTOR → Alzheimer's -->
      <line x1="100" y1="80"  x2="210" y2="130" stroke="#0e7c6b" stroke-width="2.5" opacity="0.9"/>
      <line x1="210" y1="130" x2="330" y2="80"  stroke="#c94a2a" stroke-width="2.5" opacity="0.9"/>
      <!-- Drug nodes (teal) -->
      <rect x="28" y="58"  width="144" height="44" rx="6" fill="#d4ede8" stroke="#0e7c6b" stroke-width="1.5"/>
      <rect x="28" y="148" width="144" height="44" rx="6" fill="#d4ede8" stroke="#0e7c6b" stroke-width="1.5"/>
      <rect x="28" y="238" width="144" height="44" rx="6" fill="#d4ede8" stroke="#0e7c6b" stroke-width="1.5"/>
      <text x="100" y="85"  text-anchor="middle" font-family="'DM Mono',monospace" font-size="13" fill="#0e7c6b" font-weight="500">Metformin</text>
      <text x="100" y="175" text-anchor="middle" font-family="'DM Mono',monospace" font-size="13" fill="#0e7c6b" font-weight="500">Rapamycin</text>
      <text x="100" y="265" text-anchor="middle" font-family="'DM Mono',monospace" font-size="13" fill="#0e7c6b" font-weight="500">Simvastatin</text>
      <!-- Target nodes (amber) -->
      <rect x="152" y="108" width="116" height="44" rx="6" fill="#faebd4" stroke="#c97a1a" stroke-width="2"/>
      <rect x="152" y="188" width="116" height="44" rx="6" fill="#faebd4" stroke="#c97a1a" stroke-width="1.5"/>
      <text x="210" y="135" text-anchor="middle" font-family="'DM Mono',monospace" font-size="13" fill="#c97a1a" font-weight="500">mTOR</text>
      <text x="210" y="215" text-anchor="middle" font-family="'DM Mono',monospace" font-size="13" fill="#c97a1a" font-weight="500">NF-kB</text>
      <!-- Disease nodes (coral) -->
      <rect x="278" y="58"  width="134" height="44" rx="6" fill="#fae0d8" stroke="#c94a2a" stroke-width="1.5"/>
      <rect x="278" y="148" width="134" height="44" rx="6" fill="#fae0d8" stroke="#c94a2a" stroke-width="1.5"/>
      <rect x="278" y="238" width="134" height="44" rx="6" fill="#fae0d8" stroke="#c94a2a" stroke-width="1.5"/>
      <text x="345" y="83"  text-anchor="middle" font-family="'DM Mono',monospace" font-size="11" fill="#c94a2a" font-weight="500">Alzheimer's</text>
      <text x="345" y="170" text-anchor="middle" font-family="'DM Mono',monospace" font-size="11" fill="#c94a2a" font-weight="500">Pancreatic</text>
      <text x="345" y="184" text-anchor="middle" font-family="'DM Mono',monospace" font-size="11" fill="#c94a2a" font-weight="500">Cancer</text>
      <text x="345" y="261" text-anchor="middle" font-family="'DM Mono',monospace" font-size="11" fill="#c94a2a" font-weight="500">Lung Cancer</text>
      <!-- Column labels -->
      <text x="100" y="312" text-anchor="middle" font-family="'Outfit',sans-serif" font-size="11" fill="#4a4a3a" font-weight="300">Drugs</text>
      <text x="210" y="312" text-anchor="middle" font-family="'Outfit',sans-serif" font-size="11" fill="#4a4a3a" font-weight="300">Targets</text>
      <text x="345" y="312" text-anchor="middle" font-family="'Outfit',sans-serif" font-size="11" fill="#4a4a3a" font-weight="300">Diseases</text>
      <!-- Glowing highlight dot on mTOR node -->
      <circle cx="210" cy="130" r="5" fill="#c97a1a" opacity="0.85"/>
    </svg>
  </div>
</div>

<hr class="section-rule">

<!-- ── HOW IT WORKS ── -->
<section class="section" id="how">
  <p class="section-label">The method</p>
  <h2>How DrugMatch finds connections</h2>
  <p class="section-intro">
    Inside your body, diseases and drugs both interact with tiny biological switches called
    <strong>targets</strong> — proteins and enzymes that control what cells do.
    DrugMatch looks for drugs and diseases that share the same targets.
    A shared target is a potential shortcut to a new treatment.
  </p>

  <div class="steps">
    <div class="step-card">
      <p class="step-num">Step 01</p>
      <p class="step-title">Map every drug to its targets</p>
      <p class="step-body">
        Each approved drug affects one or more biological targets — proteins or enzymes
        inside the body. We store these connections in a Python dictionary.
        Metformin, for example, hits AMPK and mTOR.
      </p>
      <span class="step-tag">drug_targets dict</span>
    </div>

    <div class="step-card">
      <p class="step-num">Step 02</p>
      <p class="step-title">Map every disease to its targets</p>
      <p class="step-body">
        Scientists know which biological targets drive each disease.
        Alzheimer's disease, for example, is linked to mTOR and NF-kB.
        We store these connections in a second dictionary.
      </p>
      <span class="step-tag">disease_targets dict</span>
    </div>

    <div class="step-card">
      <p class="step-num">Step 03</p>
      <p class="step-title">Find the overlap — and score it</p>
      <p class="step-body">
        The matching engine compares every drug against every disease.
        When they share at least one target, that pair becomes a candidate.
        The score equals the number of shared targets — more overlap means
        a stronger biological case for repurposing.
      </p>
      <span class="step-tag">score = len(shared)</span>
    </div>
  </div>
</section>

<hr class="section-rule">

<!-- ── EXAMPLE OUTPUT ── -->
<section class="section" id="output">
  <p class="section-label">Example results</p>
  <h2>Top repurposing candidates</h2>
  <p class="section-intro">
    Below are real output cards generated by the DrugMatch Python system,
    ranked highest score first. Each card shows the drug, the disease it
    may help treat, which biological targets they share, and why.
  </p>

  <div class="output-grid">

    <!-- Match 1: Imatinib — Gastrointestinal Tumor (score 2) -->
    <div class="match-card">
      <div class="match-header">
        <span class="match-drug">Imatinib</span>
        <span class="score-badge score-medium">Score 2 &middot; Medium</span>
      </div>
      <div class="match-body">
        <div class="match-row">
          <span class="match-row-label">Currently for</span>
          <span class="match-row-value">Chronic Myeloid Leukemia</span>
        </div>
        <div class="match-row">
          <span class="match-row-label">May also treat</span>
          <span class="match-row-value">Gastrointestinal Tumor</span>
        </div>
        <div class="match-row">
          <span class="match-row-label">Shared targets</span>
          <span class="match-row-value">
            <span class="target-pill">PDGFR</span>
            <span class="target-pill">KIT</span>
          </span>
        </div>
        <div class="match-explanation">
          Imatinib may help treat Gastrointestinal Tumor because both are connected to PDGFR and KIT.
        </div>
      </div>
    </div>

    <!-- Match 2: Simvastatin — Alzheimer's (score 2) -->
    <div class="match-card">
      <div class="match-header">
        <span class="match-drug">Simvastatin</span>
        <span class="score-badge score-medium">Score 2 &middot; Medium</span>
      </div>
      <div class="match-body">
        <div class="match-row">
          <span class="match-row-label">Currently for</span>
          <span class="match-row-value">High Cholesterol</span>
        </div>
        <div class="match-row">
          <span class="match-row-label">May also treat</span>
          <span class="match-row-value">Alzheimer's Disease</span>
        </div>
        <div class="match-row">
          <span class="match-row-label">Shared targets</span>
          <span class="match-row-value">
            <span class="target-pill">NF-kB</span>
            <span class="target-pill">VEGF</span>
          </span>
        </div>
        <div class="match-explanation">
          Simvastatin may help treat Alzheimer's Disease because both are connected to NF-kB and VEGF.
        </div>
      </div>
    </div>

    <!-- Match 3: Dexamethasone — Multiple Sclerosis (score 2) -->
    <div class="match-card">
      <div class="match-header">
        <span class="match-drug">Dexamethasone</span>
        <span class="score-badge score-medium">Score 2 &middot; Medium</span>
      </div>
      <div class="match-body">
        <div class="match-row">
          <span class="match-row-label">Currently for</span>
          <span class="match-row-value">Inflammation / Certain Cancers</span>
        </div>
        <div class="match-row">
          <span class="match-row-label">May also treat</span>
          <span class="match-row-value">Multiple Sclerosis</span>
        </div>
        <div class="match-row">
          <span class="match-row-label">Shared targets</span>
          <span class="match-row-value">
            <span class="target-pill">NF-kB</span>
            <span class="target-pill">IL-6</span>
          </span>
        </div>
        <div class="match-explanation">
          Dexamethasone may help treat Multiple Sclerosis because both are connected to NF-kB and IL-6.
        </div>
      </div>
    </div>

    <!-- Match 4: Metformin — Alzheimer's (score 1) -->
    <div class="match-card">
      <div class="match-header">
        <span class="match-drug">Metformin</span>
        <span class="score-badge score-low">Score 1 &middot; Low</span>
      </div>
      <div class="match-body">
        <div class="match-row">
          <span class="match-row-label">Currently for</span>
          <span class="match-row-value">Type 2 Diabetes</span>
        </div>
        <div class="match-row">
          <span class="match-row-label">May also treat</span>
          <span class="match-row-value">Alzheimer's Disease</span>
        </div>
        <div class="match-row">
          <span class="match-row-label">Shared targets</span>
          <span class="match-row-value">
            <span class="target-pill">mTOR</span>
          </span>
        </div>
        <div class="match-explanation">
          Metformin may help treat Alzheimer's Disease because both are connected to mTOR.
        </div>
      </div>
    </div>

  </div>
</section>

<hr class="section-rule">

<!-- ── THE DATA ── -->
<section class="section" id="data">
  <p class="section-label">What's inside</p>
  <h2>The three data dictionaries</h2>
  <p class="section-intro">
    The entire system runs on three simple Python dictionaries.
    Add a new row to any dictionary and the matching engine
    automatically discovers new connections — no other code changes needed.
  </p>

  <div class="data-grid">

    <div class="data-card">
      <div class="data-card-header">
        <div class="data-icon icon-drug">Rx</div>
        <span class="data-card-title">Drugs in the system</span>
      </div>
      <ul class="data-list">
        <li class="drug-dot">Metformin</li>
        <li class="drug-dot">Aspirin</li>
        <li class="drug-dot">Imatinib</li>
        <li class="drug-dot">Rapamycin</li>
        <li class="drug-dot">Simvastatin</li>
        <li class="drug-dot">Dexamethasone</li>
      </ul>
    </div>

    <div class="data-card">
      <div class="data-card-header">
        <div class="data-icon icon-target">Tg</div>
        <span class="data-card-title">Biological targets</span>
      </div>
      <ul class="data-list">
        <li class="target-dot">mTOR</li>
        <li class="target-dot">AMPK</li>
        <li class="target-dot">NF-kB</li>
        <li class="target-dot">COX-1 / COX-2</li>
        <li class="target-dot">PDGFR / KIT</li>
        <li class="target-dot">VEGF / IL-6</li>
      </ul>
    </div>

    <div class="data-card">
      <div class="data-card-header">
        <div class="data-icon icon-disease">Dx</div>
        <span class="data-card-title">Diseases covered</span>
      </div>
      <ul class="data-list">
        <li class="disease-dot">Pancreatic Cancer</li>
        <li class="disease-dot">Alzheimer's Disease</li>
        <li class="disease-dot">Rheumatoid Arthritis</li>
        <li class="disease-dot">Lung Cancer</li>
        <li class="disease-dot">Gastrointestinal Tumor</li>
        <li class="disease-dot">Multiple Sclerosis</li>
      </ul>
    </div>

  </div>
</section>

<hr class="section-rule">

<!-- ── FOOTER ── -->
<footer>
  <p class="footer-note">
    DrugMatch is a beginner-friendly educational model inspired by EveryCure.
    All matches shown are computational hypotheses only — not medical advice.
    Every candidate would require laboratory testing and clinical trials before use.
  </p>
  <span class="footer-logo">DrugMatch</span>
</footer>

</body>
</html>
