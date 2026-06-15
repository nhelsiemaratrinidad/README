# PORTFOLIO
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title> Nhelsiemar Trinidad — Virtual Assistant</title>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;1,300;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet" />

  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --cream:   #FAF8F5;
      --rose:    #E8C4B8;
      --rose-dk: #C9967E;
      --sage:    #B8C4B3;
      --charcoal:#2C2825;
      --mid:     #7A7270;
      --light:   #EDE9E4;
    }

    html { scroll-behavior: smooth; }

    body {
      background: var(--cream);
      color: var(--charcoal);
      font-family: 'DM Sans', sans-serif;
      font-weight: 300;
      line-height: 1.7;
      overflow-x: hidden;
    }

    /* ── NAV ── */
    nav {
      position: fixed;
      top: 0; left: 0; right: 0;
      z-index: 100;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1.4rem 5vw;
      background: rgba(250,248,245,0.85);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid var(--light);
    }

    .nav-logo {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.2rem;
      font-weight: 400;
      letter-spacing: 0.04em;
      color: var(--charcoal);
      text-decoration: none;
    }

    .nav-links {
      display: flex;
      gap: 2.2rem;
      list-style: none;
    }

    .nav-links a {
      font-size: 0.8rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      color: var(--mid);
      text-decoration: none;
      transition: color 0.2s;
    }

    .nav-links a:hover { color: var(--charcoal); }

    /* ── HERO ── */
    #hero {
      min-height: 100vh;
      display: grid;
      place-items: center;
      text-align: center;
      padding: 8rem 5vw 6rem;
    }

    .hero-eyebrow {
      font-size: 0.75rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--rose-dk);
      margin-bottom: 1.6rem;
      opacity: 0;
      animation: fadeUp 0.8s 0.2s forwards;
    }

    .hero-title {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(2.8rem, 7vw, 5.5rem);
      font-weight: 300;
      line-height: 1.12;
      letter-spacing: -0.01em;
      color: var(--charcoal);
      max-width: 820px;
      margin: 0 auto 1.8rem;
      opacity: 0;
      animation: fadeUp 0.9s 0.4s forwards;
    }

    .hero-title em {
      font-style: italic;
      color: var(--rose-dk);
    }

    .hero-sub {
      font-size: 1rem;
      color: var(--mid);
      max-width: 420px;
      margin: 0 auto 2.8rem;
      opacity: 0;
      animation: fadeUp 0.9s 0.6s forwards;
    }

    .btn {
      display: inline-block;
      padding: 0.85rem 2.2rem;
      border: 1px solid var(--charcoal);
      color: var(--charcoal);
      font-family: 'DM Sans', sans-serif;
      font-size: 0.78rem;
      font-weight: 400;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      text-decoration: none;
      transition: background 0.25s, color 0.25s;
      opacity: 0;
      animation: fadeUp 0.9s 0.8s forwards;
    }

    .btn:hover {
      background: var(--charcoal);
      color: var(--cream);
    }

    /* ── DIVIDER ── */
    .divider {
      display: flex;
      align-items: center;
      gap: 1.2rem;
      margin: 0 auto;
      max-width: 180px;
    }

    .divider-line {
      height: 1px;
      flex: 1;
      background: var(--rose);
      transform: scaleX(0);
      transform-origin: center;
      transition: transform 0.8s ease;
    }

    .divider-dot {
      width: 5px;
      height: 5px;
      border-radius: 50%;
      background: var(--rose);
      opacity: 0;
      transition: opacity 0.4s 0.4s;
    }

    .divider.visible .divider-line { transform: scaleX(1); }
    .divider.visible .divider-dot  { opacity: 1; }

    /* ── SECTIONS ── */
    section {
      padding: 6rem 5vw;
      max-width: 1100px;
      margin: 0 auto;
    }

    .section-label {
      font-size: 0.72rem;
      letter-spacing: 0.16em;
      text-transform: uppercase;
      color: var(--rose-dk);
      margin-bottom: 0.9rem;
    }

    .section-title {
      font-family: 'Cormorant Garamond', serif;
      font-size: clamp(2rem, 4vw, 3rem);
      font-weight: 300;
      line-height: 1.2;
      margin-bottom: 2.8rem;
    }

    /* ── ABOUT ── */
    #about .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 5rem;
      align-items: center;
    }

    .about-img-wrap {
      position: relative;
    }

    .about-img-placeholder {
      width: 100%;
      aspect-ratio: 3/4;
      background: var(--light);
      border-radius: 2px;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 0.7rem;
      color: var(--mid);
      font-size: 0.8rem;
      letter-spacing: 0.05em;
    }

    .about-img-placeholder svg {
      width: 36px;
      height: 36px;
      stroke: var(--rose-dk);
      fill: none;
      stroke-width: 1.2;
    }

    .about-accent {
      position: absolute;
      bottom: -14px;
      right: -14px;
      width: 60%;
      height: 60%;
      border: 1px solid var(--rose);
      z-index: -1;
    }

    .about-text p {
      color: var(--mid);
      margin-bottom: 1.2rem;
      font-size: 0.97rem;
    }

    .stats {
      display: flex;
      gap: 2.5rem;
      margin-top: 2.5rem;
      padding-top: 2rem;
      border-top: 1px solid var(--light);
    }

    .stat-num {
      font-family: 'Cormorant Garamond', serif;
      font-size: 2.2rem;
      font-weight: 300;
      color: var(--charcoal);
      line-height: 1;
    }

    .stat-label {
      font-size: 0.72rem;
      letter-spacing: 0.08em;
      color: var(--mid);
      margin-top: 0.3rem;
    }

    /* ── SERVICES ── */
    #services { background: transparent; }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1.5rem;
      margin-top: 0.5rem;
    }

    .service-card {
      background: #fff;
      border: 1px solid var(--light);
      padding: 2.2rem 2rem;
      border-radius: 2px;
      transition: box-shadow 0.25s, transform 0.25s;
      opacity: 0;
      transform: translateY(18px);
    }

    .service-card.visible {
      opacity: 1;
      transform: translateY(0);
      transition: opacity 0.6s ease, transform 0.6s ease, box-shadow 0.25s, border-color 0.25s;
    }

    .service-card:hover {
      box-shadow: 0 8px 32px rgba(44,40,37,0.07);
      border-color: var(--rose);
    }

    .service-icon {
      width: 40px;
      height: 40px;
      margin-bottom: 1.4rem;
      stroke: var(--rose-dk);
      fill: none;
      stroke-width: 1.3;
    }

    .service-name {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.35rem;
      font-weight: 400;
      margin-bottom: 0.7rem;
    }

    .service-desc {
      font-size: 0.87rem;
      color: var(--mid);
      line-height: 1.75;
    }

    .service-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
      margin-top: 1.3rem;
    }

    .tag {
      font-size: 0.68rem;
      letter-spacing: 0.07em;
      padding: 0.28rem 0.75rem;
      border: 1px solid var(--light);
      color: var(--mid);
      border-radius: 20px;
    }

    /* ── PROCESS ── */
    #process .process-steps {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 2rem;
      margin-top: 1rem;
    }

    .process-step {
      padding-top: 1.2rem;
      border-top: 2px solid var(--rose);
    }

    .step-num {
      font-family: 'Cormorant Garamond', serif;
      font-size: 0.95rem;
      color: var(--rose-dk);
      margin-bottom: 0.7rem;
    }

    .step-title {
      font-size: 0.95rem;
      font-weight: 500;
      margin-bottom: 0.5rem;
    }

    .step-desc {
      font-size: 0.84rem;
      color: var(--mid);
    }

    /* ── TESTIMONIALS ── */
    #testimonials {
      background: var(--charcoal);
      color: var(--cream);
      max-width: 100%;
      padding: 6rem 5vw;
    }

    #testimonials .inner {
      max-width: 1100px;
      margin: 0 auto;
    }

    #testimonials .section-label { color: var(--rose); }

    #testimonials .section-title { color: var(--cream); }

    .testimonial-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
    }

    .testimonial-card {
      background: rgba(255,255,255,0.05);
      border: 1px solid rgba(255,255,255,0.1);
      padding: 2rem;
      border-radius: 2px;
    }

    .testimonial-quote {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.15rem;
      font-weight: 300;
      font-style: italic;
      line-height: 1.65;
      color: #EDE9E4;
      margin-bottom: 1.5rem;
    }

    .testimonial-author {
      font-size: 0.78rem;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      color: var(--rose);
    }

    /* ── CONTACT ── */
    #contact {
      max-width: 680px;
      margin: 0 auto;
      padding: 6rem 5vw;
      text-align: center;
    }

    #contact .section-title { margin-bottom: 0.8rem; }

    .contact-intro {
      font-size: 0.95rem;
      color: var(--mid);
      margin-bottom: 3rem;
    }

    .contact-form {
      text-align: left;
    }

    .form-row {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 1rem;
    }

    .form-group {
      display: flex;
      flex-direction: column;
      gap: 0.45rem;
      margin-bottom: 1.2rem;
    }

    .form-group label {
      font-size: 0.72rem;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--mid);
    }

    .form-group input,
    .form-group select,
    .form-group textarea {
      background: #fff;
      border: 1px solid var(--light);
      padding: 0.8rem 1rem;
      font-family: 'DM Sans', sans-serif;
      font-size: 0.9rem;
      color: var(--charcoal);
      border-radius: 2px;
      outline: none;
      transition: border-color 0.2s;
      width: 100%;
    }

    .form-group input:focus,
    .form-group select:focus,
    .form-group textarea:focus {
      border-color: var(--rose-dk);
    }

    .form-group textarea {
      resize: vertical;
      min-height: 130px;
    }

    .form-submit {
      width: 100%;
      padding: 1rem;
      background: var(--charcoal);
      color: var(--cream);
      border: none;
      font-family: 'DM Sans', sans-serif;
      font-size: 0.78rem;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      cursor: pointer;
      transition: background 0.2s;
      margin-top: 0.5rem;
    }

    .form-submit:hover { background: #1a1614; }

    .form-note {
      text-align: center;
      font-size: 0.78rem;
      color: var(--mid);
      margin-top: 1.2rem;
    }

    /* ── FOOTER ── */
    footer {
      border-top: 1px solid var(--light);
      padding: 2.5rem 5vw;
      display: flex;
      justify-content: space-between;
      align-items: center;
      flex-wrap: wrap;
      gap: 1rem;
    }

    .footer-name {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1rem;
      color: var(--mid);
    }

    .footer-links {
      display: flex;
      gap: 1.5rem;
      list-style: none;
    }

    .footer-links a {
      font-size: 0.75rem;
      letter-spacing: 0.08em;
      color: var(--mid);
      text-decoration: none;
      text-transform: uppercase;
      transition: color 0.2s;
    }

    .footer-links a:hover { color: var(--charcoal); }

    /* ── ANIMATIONS ── */
    @keyframes fadeUp {
      from { opacity: 0; transform: translateY(20px); }
      to   { opacity: 1; transform: translateY(0); }
    }

    .reveal {
      opacity: 0;
      transform: translateY(20px);
      transition: opacity 0.7s ease, transform 0.7s ease;
    }

    .reveal.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* ── RESPONSIVE ── */
    @media (max-width: 700px) {
      .nav-links { display: none; }
      #about .about-grid { grid-template-columns: 1fr; gap: 3rem; }
      .form-row { grid-template-columns: 1fr; }
      footer { flex-direction: column; text-align: center; }
    }

    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after { animation-duration: 0.01ms !important; transition-duration: 0.01ms !important; }
    }
  </style>
</head>
<body>

  <!-- NAV -->
  <nav>
    <a href="#hero" class="nav-logo">Nhelsiemar Trinidad</a>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#process">Process</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <!-- HERO -->
  <section id="hero">
    <div>
      <p class="hero-eyebrow">Virtual Assistant — Philippines</p>
      <h1 class="hero-title">Behind every busy person<br>is a <em>detail-oriented</em> partner</h1>
      <p class="hero-sub">I handle the tasks that eat your time — so you can focus on the work only you can do.</p>
      <a href="#contact" class="btn">Work Smarter and Not Harder! Let's Work Together!</a>
    </div>
  </section>

  <!-- ABOUT -->
  <section id="about">
    <div class="about-grid">
      <div class="about-img-wrap reveal">
        <div class="about-img-placeholder">
          <svg viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
            <circle cx="12" cy="8" r="4"/>
            <path d="M4 20c0-4 3.6-7 8-7s8 3 8 7"/>
          </svg>
          <span>Add your photo here</span>
        </div>
        <div class="about-accent"></div>
      </div>
      <div class="about-text reveal">
        <p class="section-label">About Me</p>
        <h2 class="section-title">Organized, creative,<br>and genuinely reliable</h2>
        <p>Hi! I'm <strong>[Nhelsiemar Trinidad]</strong>, a virtual assistant based in the Philippines with a passion for helping entrepreneurs, small business owners, and creatives reclaim their time.</p>
        <p>I specialize in creative & design support, social media management, and general administrative tasks — bringing a thoughtful, aesthetic eye to everything I touch.</p>
        <p>Whether you need someone to manage your inbox, refresh your visuals, or keep your social presence consistent and on-brand, I've got you covered.</p>

      </div>
    </div>
  </section>

  <div class="divider" style="padding: 0 5vw;">
    <div class="divider-line"></div>
    <div class="divider-dot"></div>
    <div class="divider-line"></div>
  </div>

  <!-- SERVICES -->
  <section id="services">
    <p class="section-label reveal">What I Offer</p>
    <h2 class="section-title reveal">Services designed to<br>lighten your load</h2>

    <!-- SERVICE 1: Creative & Design -->
    <div class="service-block reveal">
      <div class="service-block-header">
        <svg class="service-icon" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
          <rect x="3" y="3" width="18" height="18" rx="2"/>
          <path d="M3 9h18M9 21V9"/>
        </svg>
        <div>
          <div class="service-name">Creative & Design Support</div>
          <p class="service-desc">Visual assets that look polished and on-brand — from Canva graphics to presentations and simple layout work.</p>
          <div class="service-tags">
            <span class="tag">Canva</span>
            <span class="tag">Presentations</span>
            <span class="tag">Brand Assets</span>
            <span class="tag">Infographics</span>
          </div>
        </div>
      </div>
      <div class="samples-label">Work Samples</div>
      <div class="samples-grid">
        <div class="sample-slot">
          <div class="sample-img-placeholder">
            <svg viewBox="0 0 24 24" fill="none" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round">
              <rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/>
            </svg>
            <span>Brand Kit / Logo Design</span>
          </div>
        </div>
        <div class="sample-slot">
          <div class="sample-img-placeholder">
            <svg viewBox="0 0 24 24" fill="none" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round">
              <rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/>
            </svg>
            <span>Canva Graphic / Poster</span>
          </div>
        </div>
        <div class="sample-slot">
          <div class="sample-img-placeholder">
            <svg viewBox="0 0 24 24" fill="none" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round">
              <rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/>
            </svg>
            <span>Presentation Slide Deck</span>
          </div>
        </div>
        <div class="sample-slot">
          <div class="sample-img-placeholder">
            <svg viewBox="0 0 24 24" fill="none" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round">
              <rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/>
            </svg>
            <span>Infographic / Data Visual</span>
          </div>
        </div>
      </div>
      <p class="samples-hint">💡 Replace placeholders with your actual work — see instructions below.</p>
    </div>

    <!-- SERVICE 2: Social Media -->
    <div class="service-block reveal">
      <div class="service-block-header">
        <svg class="service-icon" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
          <path d="M22 2L11 13"/>
          <path d="M22 2L15 22 11 13 2 9l20-7z"/>
        </svg>
        <div>
          <div class="service-name">Social Media & Content</div>
          <p class="service-desc">Consistent, engaging social presence managed for you — from scheduling and captions to light copywriting and community replies.</p>
          <div class="service-tags">
            <span class="tag">Instagram</span>
            <span class="tag">Facebook</span>
            <span class="tag">Copywriting</span>
            <span class="tag">Scheduling</span>
          </div>
        </div>
      </div>
      <div class="samples-label">Work Samples</div>
      <div class="samples-grid">
        <div class="sample-slot">
          <div class="sample-img-placeholder">
            <svg viewBox="0 0 24 24" fill="none" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round">
              <rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/>
            </svg>
            <span>Instagram Feed Post</span>
          </div>
        </div>
        <div class="sample-slot">
          <div class="sample-img-placeholder">
            <svg viewBox="0 0 24 24" fill="none" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round">
              <rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/>
            </svg>
            <span>Story / Reel Cover</span>
          </div>
        </div>
        <div class="sample-slot">
          <div class="sample-img-placeholder">
            <svg viewBox="0 0 24 24" fill="none" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round">
              <rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/>
            </svg>
            <span>Content Calendar</span>
          </div>
        </div>
        <div class="sample-slot">
          <div class="sample-img-placeholder">
            <svg viewBox="0 0 24 24" fill="none" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round">
              <rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/>
            </svg>
            <span>Caption / Copy Sample</span>
          </div>
        </div>
      </div>
      <p class="samples-hint">💡 Replace placeholders with your actual work — see instructions below.</p>
    </div>

    <!-- SERVICE 3: General Admin -->
    <div class="service-block reveal">
      <div class="service-block-header">
        <svg class="service-icon" viewBox="0 0 24 24" stroke-linecap="round" stroke-linejoin="round">
          <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/>
          <polyline points="14 2 14 8 20 8"/>
          <line x1="16" y1="13" x2="8" y2="13"/>
          <line x1="16" y1="17" x2="8" y2="17"/>
          <line x1="10" y1="9" x2="8" y2="9"/>
        </svg>
        <div>
          <div class="service-name">General Admin Support</div>
          <p class="service-desc">Email management, calendar coordination, data entry, research, and all the behind-the-scenes tasks that keep things running smoothly.</p>
          <div class="service-tags">
            <span class="tag">Email Management</span>
            <span class="tag">Scheduling</span>
            <span class="tag">Research</span>
            <span class="tag">Data Entry</span>
          </div>
        </div>
      </div>
      <div class="samples-label">Work Samples</div>
      <div class="samples-grid">
        <div class="sample-slot">
          <div class="sample-img-placeholder">
            <svg viewBox="0 0 24 24" fill="none" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round">
              <rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/>
            </svg>
            <span>Spreadsheet / Tracker</span>
          </div>
        </div>
        <div class="sample-slot">
          <div class="sample-img-placeholder">
            <svg viewBox="0 0 24 24" fill="none" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round">
              <rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/>
            </svg>
            <span>Research Report</span>
          </div>
        </div>
        <div class="sample-slot">
          <div class="sample-img-placeholder">
            <svg viewBox="0 0 24 24" fill="none" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round">
              <rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/>
            </svg>
            <span>Calendar / SOPs</span>
          </div>
        </div>
        <div class="sample-slot">
          <div class="sample-img-placeholder">
            <svg viewBox="0 0 24 24" fill="none" stroke-width="1.2" stroke-linecap="round" stroke-linejoin="round">
              <rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/>
            </svg>
            <span>Email Draft / Template</span>
          </div>
        </div>
      </div>
      <p class="samples-hint">💡 Replace placeholders with your actual work — see instructions below.</p>
    </div>

  </section>

  <!-- PROCESS -->
  <section id="process">
    <p class="section-label reveal">How It Works</p>
    <h2 class="section-title reveal">Simple to start,<br>smooth to work with</h2>
    <div class="process-steps">
      <div class="reveal">
        <div class="process-step">
          <div class="step-num">Step 01</div>
          <div class="step-title">Discovery Call</div>
          <p class="step-desc">We chat about your needs, pain points, and goals — no pressure, just a conversation.</p>
        </div>
      </div>
      <div class="reveal">
        <div class="process-step">
          <div class="step-num">Step 02</div>
          <div class="step-title">Proposal & Scope</div>
          <p class="step-desc">I put together a clear proposal with services, timelines, and pricing — no surprises.</p>
        </div>
      </div>
      <div class="reveal">
        <div class="process-step">
          <div class="step-num">Step 03</div>
          <div class="step-title">Onboarding</div>
          <p class="step-desc">We set up tools, workflows, and communication channels so we're fully in sync from day one.</p>
        </div>
      </div>
      <div class="reveal">
        <div class="process-step">
          <div class="step-num">Step 04</div>
          <div class="step-title">We Get to Work</div>
          <p class="step-desc">I handle your tasks with regular check-ins and transparent updates. You focus on what matters most.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- CONTACT -->
  <section id="contact">
    <p class="section-label reveal">Get in Touch</p>
    <h2 class="section-title reveal">Ready to get some<br>time back?</h2>
    <p class="contact-intro reveal">Fill out the form below and I'll get back to you within 24 hours.</p>
    <form class="contact-form reveal" name="contact" netlify onsubmit="handleSubmit(event)">
      <div class="form-row">
        <div class="form-group">
          <label for="name">Your Name</label>
          <input type="text" id="name" name="name" placeholder="Jane Smith" required />
        </div>
        <div class="form-group">
          <label for="email">Email Address</label>
          <input type="email" id="email" name="email" placeholder="jane@example.com" required />
        </div>
      </div>
      <div class="form-group">
        <label for="service">Service Interested In</label>
        <select id="service" name="service">
          <option value="">Select a service…</option>
          <option>Creative & Design Support</option>
          <option>Social Media & Content</option>
          <option>General Admin Support</option>
          <option>Multiple / Not sure yet</option>
        </select>
      </div>
      <div class="form-group">
        <label for="message">Tell me about your needs</label>
        <textarea id="message" name="message" placeholder="What tasks are taking up most of your time right now?" required></textarea>
      </div>
      <button type="submit" class="form-submit">Send Message</button>
      <p class="form-note" id="form-status"></p>
    </form>
  </section>

  <!-- FOOTER -->
  <footer>
    <span class="footer-name">Nhelsiemar Trinidad — Virtual Assistant</span>
    <ul class="footer-links">
      <li><a href="mailto:youremail@example.com">Email</a></li>
      <li><a href="https://linkedin.com/in/yourprofile" target="_blank" rel="noopener">LinkedIn</a></li>
      <li><a href="https://instagram.com/yourhandle" target="_blank" rel="noopener">Instagram</a></li>
    </ul>
  </footer>

  <script>
    // Intersection Observer for reveal animations
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(el => {
        if (el.isIntersecting) {
          el.target.classList.add('visible');
          observer.unobserve(el.target);
        }
      });
    }, { threshold: 0.15 });

    document.querySelectorAll('.reveal, .service-card').forEach(el => observer.observe(el));

    // Divider animation
    const dividerObs = new IntersectionObserver((entries) => {
      entries.forEach(el => {
        if (el.isIntersecting) el.target.classList.add('visible');
      });
    }, { threshold: 0.5 });

    document.querySelectorAll('.divider').forEach(el => dividerObs.observe(el));

    // Stagger service cards
    document.querySelectorAll('.service-card').forEach((card, i) => {
      card.style.transitionDelay = `${i * 0.12}s`;
    });

    // Form handler (works without a backend; swap in your preferred form service)
    function handleSubmit(e) {
      e.preventDefault();
      const status = document.getElementById('form-status');
      status.textContent = 'Thank you! I\'ll be in touch within 24 hours.';
      status.style.color = '#C9967E';
      e.target.reset();
    }
  </script>

</body>
</html>
