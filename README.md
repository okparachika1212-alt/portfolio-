# portfolio-<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Chika Okpara — Social Media Strategist</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }

:root {
–cream: #F5F0E8;
–dark: #1A1410;
–gold: #C9A84C;
–terracotta: #C4623A;
–sage: #7A8C6E;
–light: #FAF8F4;
}

html { scroll-behavior: smooth; }

body {
font-family: ‘DM Sans’, sans-serif;
background: var(–cream);
color: var(–dark);
overflow-x: hidden;
}

/* NAV */
nav {
position: fixed;
top: 0; left: 0; right: 0;
z-index: 100;
padding: 20px 40px;
display: flex;
justify-content: space-between;
align-items: center;
background: rgba(245, 240, 232, 0.92);
backdrop-filter: blur(12px);
border-bottom: 1px solid rgba(201, 168, 76, 0.2);
}

.nav-logo {
font-family: ‘Playfair Display’, serif;
font-size: 1.3rem;
font-weight: 700;
color: var(–dark);
letter-spacing: -0.5px;
}

.nav-links {
display: flex;
gap: 32px;
list-style: none;
}

.nav-links a {
text-decoration: none;
color: var(–dark);
font-size: 0.85rem;
font-weight: 500;
letter-spacing: 0.5px;
text-transform: uppercase;
opacity: 0.7;
transition: opacity 0.2s;
}

.nav-links a:hover { opacity: 1; color: var(–terracotta); }

/* HERO */
.hero {
min-height: 100vh;
display: grid;
grid-template-columns: 1fr 1fr;
align-items: center;
padding: 120px 80px 80px;
gap: 60px;
position: relative;
overflow: hidden;
}

.hero::before {
content: ‘’;
position: absolute;
top: -100px; right: -100px;
width: 500px; height: 500px;
background: radial-gradient(circle, rgba(201,168,76,0.15) 0%, transparent 70%);
border-radius: 50%;
}

.hero::after {
content: ‘’;
position: absolute;
bottom: -50px; left: 20%;
width: 300px; height: 300px;
background: radial-gradient(circle, rgba(196,98,58,0.1) 0%, transparent 70%);
border-radius: 50%;
}

.hero-text { position: relative; z-index: 2; }

.hero-tag {
display: inline-block;
background: var(–gold);
color: var(–dark);
font-size: 0.7rem;
font-weight: 500;
letter-spacing: 2px;
text-transform: uppercase;
padding: 6px 14px;
border-radius: 2px;
margin-bottom: 28px;
animation: fadeUp 0.8s ease forwards;
}

.hero-name {
font-family: ‘Playfair Display’, serif;
font-size: clamp(3rem, 6vw, 5.5rem);
font-weight: 900;
line-height: 1.0;
letter-spacing: -2px;
margin-bottom: 20px;
animation: fadeUp 0.8s 0.1s ease both;
}

.hero-name em {
font-style: italic;
color: var(–terracotta);
}

.hero-sub {
font-size: 1.05rem;
font-weight: 300;
line-height: 1.7;
opacity: 0.75;
max-width: 440px;
margin-bottom: 40px;
animation: fadeUp 0.8s 0.2s ease both;
}

.hero-ctas {
display: flex;
gap: 16px;
flex-wrap: wrap;
animation: fadeUp 0.8s 0.3s ease both;
}

.btn-primary {
background: var(–dark);
color: var(–cream);
padding: 14px 32px;
border: none;
border-radius: 2px;
font-family: ‘DM Sans’, sans-serif;
font-size: 0.85rem;
font-weight: 500;
letter-spacing: 0.5px;
text-transform: uppercase;
cursor: pointer;
text-decoration: none;
display: inline-block;
transition: all 0.25s;
}

.btn-primary:hover {
background: var(–terracotta);
transform: translateY(-2px);
}

.btn-secondary {
background: transparent;
color: var(–dark);
padding: 14px 32px;
border: 1.5px solid var(–dark);
border-radius: 2px;
font-family: ‘DM Sans’, sans-serif;
font-size: 0.85rem;
font-weight: 500;
letter-spacing: 0.5px;
text-transform: uppercase;
cursor: pointer;
text-decoration: none;
display: inline-block;
transition: all 0.25s;
}

.btn-secondary:hover {
background: var(–dark);
color: var(–cream);
transform: translateY(-2px);
}

.hero-visual {
position: relative;
z-index: 2;
animation: fadeUp 0.8s 0.2s ease both;
}

.hero-card {
background: var(–dark);
color: var(–cream);
border-radius: 4px;
padding: 48px 40px;
position: relative;
overflow: hidden;
}

.hero-card::before {
content: ‘’;
position: absolute;
top: 0; right: 0;
width: 150px; height: 150px;
background: var(–gold);
opacity: 0.15;
border-radius: 50%;
transform: translate(50px, -50px);
}

.stat-grid {
display: grid;
grid-template-columns: 1fr 1fr;
gap: 32px;
margin-bottom: 32px;
}

.stat-item { }

.stat-num {
font-family: ‘Playfair Display’, serif;
font-size: 2.8rem;
font-weight: 700;
color: var(–gold);
line-height: 1;
margin-bottom: 6px;
}

.stat-label {
font-size: 0.78rem;
opacity: 0.6;
letter-spacing: 0.5px;
text-transform: uppercase;
font-weight: 400;
}

.award-badge {
background: rgba(201, 168, 76, 0.15);
border: 1px solid rgba(201, 168, 76, 0.3);
border-radius: 3px;
padding: 14px 18px;
display: flex;
align-items: center;
gap: 12px;
}

.award-icon { font-size: 1.5rem; }

.award-text { font-size: 0.82rem; opacity: 0.85; line-height: 1.4; }

/* ABOUT */
#about {
padding: 100px 80px;
background: var(–light);
}

.section-label {
font-size: 0.7rem;
letter-spacing: 3px;
text-transform: uppercase;
color: var(–terracotta);
font-weight: 500;
margin-bottom: 16px;
}

.section-title {
font-family: ‘Playfair Display’, serif;
font-size: clamp(2rem, 4vw, 3.2rem);
font-weight: 700;
line-height: 1.15;
letter-spacing: -1px;
margin-bottom: 24px;
max-width: 600px;
}

.about-grid {
display: grid;
grid-template-columns: 1.2fr 1fr;
gap: 80px;
align-items: start;
margin-top: 60px;
}

.about-text p {
font-size: 1rem;
line-height: 1.8;
opacity: 0.75;
margin-bottom: 20px;
font-weight: 300;
}

.skills-list {
display: flex;
flex-direction: column;
gap: 12px;
}

.skill-item {
display: flex;
align-items: center;
gap: 12px;
padding: 14px 20px;
background: var(–cream);
border-radius: 3px;
border-left: 3px solid var(–gold);
font-size: 0.88rem;
font-weight: 400;
transition: transform 0.2s;
}

.skill-item:hover { transform: translateX(4px); }

.skill-dot {
width: 6px; height: 6px;
background: var(–terracotta);
border-radius: 50%;
flex-shrink: 0;
}

/* WORK */
#work {
padding: 100px 80px;
background: var(–cream);
}

.work-header {
display: flex;
justify-content: space-between;
align-items: flex-end;
margin-bottom: 60px;
}

.work-grid {
display: grid;
grid-template-columns: repeat(3, 1fr);
gap: 24px;
margin-bottom: 40px;
}

.work-card {
background: var(–dark);
border-radius: 4px;
overflow: hidden;
transition: transform 0.3s;
cursor: pointer;
}

.work-card:hover { transform: translateY(-8px); }

.work-img {
width: 100%;
aspect-ratio: 4/3;
display: flex;
align-items: center;
justify-content: center;
font-size: 3rem;
position: relative;
overflow: hidden;
}

.work-img-1 { background: linear-gradient(135deg, #C4623A 0%, #8B3A1F 100%); }
.work-img-2 { background: linear-gradient(135deg, #C9A84C 0%, #8B6914 100%); }
.work-img-3 { background: linear-gradient(135deg, #7A8C6E 0%, #3D4A34 100%); }

.work-img-overlay {
position: absolute;
inset: 0;
background: rgba(0,0,0,0.3);
display: flex;
align-items: center;
justify-content: center;
opacity: 0;
transition: opacity 0.3s;
font-size: 0.8rem;
color: white;
letter-spacing: 1px;
text-transform: uppercase;
font-weight: 500;
}

.work-card:hover .work-img-overlay { opacity: 1; }

.work-info {
padding: 20px;
color: var(–cream);
}

.work-type {
font-size: 0.68rem;
letter-spacing: 2px;
text-transform: uppercase;
opacity: 0.5;
margin-bottom: 6px;
}

.work-title {
font-family: ‘Playfair Display’, serif;
font-size: 1.1rem;
font-weight: 600;
margin-bottom: 4px;
}

.work-desc {
font-size: 0.78rem;
opacity: 0.55;
line-height: 1.5;
}

.drive-cta {
background: var(–dark);
border-radius: 4px;
padding: 32px 40px;
display: flex;
justify-content: space-between;
align-items: center;
gap: 24px;
}

.drive-text h3 {
font-family: ‘Playfair Display’, serif;
font-size: 1.4rem;
color: var(–cream);
margin-bottom: 6px;
}

.drive-text p {
font-size: 0.85rem;
color: rgba(245,240,232,0.5);
}

/* VIDEO */
#videos {
padding: 100px 80px;
background: var(–dark);
color: var(–cream);
}

#videos .section-label { color: var(–gold); }

.video-grid {
display: grid;
grid-template-columns: 1fr 1fr;
gap: 24px;
margin-top: 50px;
margin-bottom: 40px;
}

.video-card {
border-radius: 4px;
overflow: hidden;
background: rgba(255,255,255,0.05);
transition: transform 0.3s;
}

.video-card:hover { transform: translateY(-6px); }

.video-thumb {
width: 100%;
aspect-ratio: 16/9;
display: flex;
align-items: center;
justify-content: center;
font-size: 3rem;
position: relative;
}

.video-thumb-1 { background: linear-gradient(135deg, #2D1B69 0%, #11998e 100%); }
.video-thumb-2 { background: linear-gradient(135deg, #C4623A 0%, #1A1410 100%); }

.play-btn {
position: absolute;
width: 56px; height: 56px;
background: rgba(255,255,255,0.9);
border-radius: 50%;
display: flex;
align-items: center;
justify-content: center;
font-size: 1.2rem;
transition: transform 0.2s;
}

.video-card:hover .play-btn { transform: scale(1.1); }

.video-info {
padding: 20px;
}

.video-title {
font-family: ‘Playfair Display’, serif;
font-size: 1.05rem;
margin-bottom: 6px;
}

.video-desc {
font-size: 0.78rem;
opacity: 0.5;
}

.video-cta {
background: rgba(201,168,76,0.1);
border: 1px solid rgba(201,168,76,0.25);
border-radius: 4px;
padding: 28px 36px;
display: flex;
justify-content: space-between;
align-items: center;
}

.video-cta p { font-size: 0.9rem; opacity: 0.7; }

/* AWARD */
#award {
padding: 100px 80px;
background: var(–light);
}

.award-section {
display: grid;
grid-template-columns: 1fr 1fr;
gap: 80px;
align-items: center;
margin-top: 60px;
}

.award-visual {
background: var(–dark);
border-radius: 4px;
padding: 60px 40px;
text-align: center;
position: relative;
overflow: hidden;
}

.award-visual::before {
content: ‘’;
position: absolute;
top: -60px; left: -60px;
width: 200px; height: 200px;
background: var(–gold);
opacity: 0.08;
border-radius: 50%;
}

.award-trophy { font-size: 5rem; margin-bottom: 20px; display: block; }

.award-visual h3 {
font-family: ‘Playfair Display’, serif;
color: var(–gold);
font-size: 1.8rem;
margin-bottom: 8px;
}

.award-visual p {
color: rgba(245,240,232,0.6);
font-size: 0.88rem;
line-height: 1.6;
}

.award-tag {
display: inline-block;
background: var(–gold);
color: var(–dark);
font-size: 0.68rem;
font-weight: 600;
letter-spacing: 2px;
text-transform: uppercase;
padding: 5px 12px;
border-radius: 2px;
margin-top: 16px;
}

.award-content h3 {
font-family: ‘Playfair Display’, serif;
font-size: 2rem;
line-height: 1.3;
margin-bottom: 20px;
letter-spacing: -0.5px;
}

.award-content p {
font-size: 0.95rem;
line-height: 1.8;
opacity: 0.7;
font-weight: 300;
margin-bottom: 16px;
}

/* CONTACT */
#contact {
padding: 100px 80px;
background: var(–dark);
color: var(–cream);
text-align: center;
}

#contact .section-label { color: var(–gold); }

#contact .section-title {
color: var(–cream);
margin: 0 auto 16px;
text-align: center;
}

#contact .sub {
font-size: 1rem;
opacity: 0.55;
margin-bottom: 48px;
font-weight: 300;
}

.contact-links {
display: flex;
justify-content: center;
gap: 16px;
flex-wrap: wrap;
margin-bottom: 60px;
}

.contact-chip {
display: flex;
align-items: center;
gap: 8px;
background: rgba(255,255,255,0.06);
border: 1px solid rgba(255,255,255,0.1);
border-radius: 100px;
padding: 10px 20px;
font-size: 0.85rem;
color: var(–cream);
text-decoration: none;
transition: all 0.2s;
}

.contact-chip:hover {
background: var(–gold);
color: var(–dark);
border-color: var(–gold);
}

.footer-line {
border-top: 1px solid rgba(255,255,255,0.08);
padding-top: 40px;
font-size: 0.78rem;
opacity: 0.35;
letter-spacing: 0.5px;
}

/* ANIMATIONS */
@keyframes fadeUp {
from { opacity: 0; transform: translateY(24px); }
to { opacity: 1; transform: translateY(0); }
}

/* MOBILE */
@media (max-width: 768px) {
nav { padding: 16px 20px; }
.nav-links { display: none; }
.hero { grid-template-columns: 1fr; padding: 100px 24px 60px; gap: 40px; }
#about, #work, #videos, #award, #contact { padding: 70px 24px; }
.about-grid, .award-section { grid-template-columns: 1fr; gap: 40px; }
.work-grid { grid-template-columns: 1fr; }
.video-grid { grid-template-columns: 1fr; }
.work-header { flex-direction: column; align-items: flex-start; gap: 20px; }
.drive-cta { flex-direction: column; align-items: flex-start; }
.video-cta { flex-direction: column; align-items: flex-start; gap: 16px; }
.stat-grid { grid-template-columns: 1fr 1fr; }
}
</style>

</head>
<body>

<nav>
  <div class="nav-logo">Chika Okpara</div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#work">Work</a></li>
    <li><a href="#videos">Videos</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->

<section class="hero">
  <div class="hero-text">
    <span class="hero-tag">Available for New Roles</span>
    <h1 class="hero-name">Chika<br><em>Okpara.</em></h1>
    <p class="hero-sub">Social Media Strategist & Digital Marketing Specialist who turns brand visibility into real, measurable revenue. 4+ years building brands that actually convert.</p>
    <div class="hero-ctas">
      <a href="#work" class="btn-primary">View My Work</a>
      <a href="#contact" class="btn-secondary">Let's Talk</a>
    </div>
  </div>
  <div class="hero-visual">
    <div class="hero-card">
      <div class="stat-grid">
        <div class="stat-item">
          <div class="stat-num">4+</div>
          <div class="stat-label">Years Experience</div>
        </div>
        <div class="stat-item">
          <div class="stat-num">10+</div>
          <div class="stat-label">Brands Managed</div>
        </div>
        <div class="stat-item">
          <div class="stat-num">3</div>
          <div class="stat-label">Platforms Mastered</div>
        </div>
        <div class="stat-item">
          <div class="stat-num">↑</div>
          <div class="stat-label">Sales Conversions</div>
        </div>
      </div>
      <div class="award-badge">
        <span class="award-icon">🏆</span>
        <span class="award-text">Q1 Hardworking Staff Award — Ajex Princeps Global, 2026</span>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->

<section id="about">
  <div class="section-label">Who I Am</div>
  <h2 class="section-title">Strategy first. Content second. Results always.</h2>
  <div class="about-grid">
    <div class="about-text">
      <p>I'm Chika — a Social Media Strategist and Digital Marketing Specialist based in Lagos, Nigeria. I don't just post content. I build systems that turn attention into action, and action into revenue.</p>
      <p>Over the past 4+ years I've managed social media for multiple consumer lifestyle brands simultaneously — running paid campaigns, creating content that converts, building communities and executing brand activation strategies across Instagram, TikTok, Facebook and LinkedIn.</p>
      <p>Through CtokSocials Agency, I've also worked with founders and business owners who needed more than just a content creator — they needed someone who could think strategically and execute with precision.</p>
    </div>
    <div class="skills-list">
      <div class="skill-item"><span class="skill-dot"></span>Social Media Strategy & Management</div>
      <div class="skill-item"><span class="skill-dot"></span>Paid Ad Campaigns (Meta, TikTok)</div>
      <div class="skill-item"><span class="skill-dot"></span>Organic Sales Conversion</div>
      <div class="skill-item"><span class="skill-dot"></span>Multi-Brand Content Management</div>
      <div class="skill-item"><span class="skill-dot"></span>Short-Form Video & Reels</div>
      <div class="skill-item"><span class="skill-dot"></span>Brand Activation & Market Launch</div>
      <div class="skill-item"><span class="skill-dot"></span>Community Engagement</div>
      <div class="skill-item"><span class="skill-dot"></span>Analytics & Performance Reporting</div>
    </div>
  </div>
</section>

<!-- WORK -->

<section id="work">
  <div class="work-header">
    <div>
      <div class="section-label">Selected Work</div>
      <h2 class="section-title">Graphics & Design Work</h2>
    </div>
  </div>

  <div class="work-grid">
    <div class="work-card">
      <div class="work-img work-img-1">
        <div class="work-img-overlay">View Project</div>
        <span>🎨</span>
      </div>
      <div class="work-info">
        <div class="work-type">Brand Graphics</div>
        <div class="work-title">Replace with your graphic 1</div>
        <div class="work-desc">Add your description here</div>
      </div>
    </div>
    <div class="work-card">
      <div class="work-img work-img-2">
        <div class="work-img-overlay">View Project</div>
        <span>📱</span>
      </div>
      <div class="work-info">
        <div class="work-type">Social Media</div>
        <div class="work-title">Replace with your graphic 2</div>
        <div class="work-desc">Add your description here</div>
      </div>
    </div>
    <div class="work-card">
      <div class="work-img work-img-3">
        <div class="work-img-overlay">View Project</div>
        <span>✨</span>
      </div>
      <div class="work-info">
        <div class="work-type">Content Strategy</div>
        <div class="work-title">Replace with your graphic 3</div>
        <div class="work-desc">Add your description here</div>
      </div>
    </div>
  </div>

  <div class="drive-cta">
    <div class="drive-text">
      <h3>See More Design Work</h3>
      <p>Full portfolio of graphics, campaigns and brand work available on Google Drive</p>
    </div>
    <a href="YOUR_GOOGLE_DRIVE_LINK_HERE" target="_blank" class="btn-primary" style="background:var(--gold);color:var(--dark);white-space:nowrap;">View Full Portfolio →</a>
  </div>
</section>

<!-- VIDEOS -->

<section id="videos">
  <div class="section-label">Content Work</div>
  <h2 class="section-title" style="color:var(--cream);">Video & Reels</h2>

  <div class="video-grid">
    <div class="video-card">
      <div class="video-thumb video-thumb-1">
        <div class="play-btn">▶</div>
      </div>
      <div class="video-info">
        <div class="video-title">Replace with your video 1</div>
        <div class="video-desc">Add your description here</div>
      </div>
    </div>
    <div class="video-card">
      <div class="video-thumb video-thumb-2">
        <div class="play-btn">▶</div>
      </div>
      <div class="video-info">
        <div class="video-title">Replace with your video 2</div>
        <div class="video-desc">Add your description here</div>
      </div>
    </div>
  </div>

  <div class="video-cta">
    <p>More video content and campaign work available on Google Drive</p>
    <a href="YOUR_GOOGLE_DRIVE_VIDEO_LINK_HERE" target="_blank" class="btn-primary" style="white-space:nowrap;">View All Videos →</a>
  </div>
</section>

<!-- AWARD -->

<section id="award">
  <div class="section-label">Recognition</div>
  <h2 class="section-title">Acknowledged for Excellence</h2>
  <div class="award-section">
    <div class="award-visual">
      <span class="award-trophy">🏆</span>
      <h3>Q1 Hardworking Staff Award</h3>
      <p>Recognised for outstanding dedication, consistency and contribution to brand growth across multiple verticals.</p>
      <span class="award-tag">Ajex Princeps Global · 2026</span>
    </div>
    <div class="award-content">
      <h3>Results speak louder than titles.</h3>
      <p>In my first full quarter at Ajex Princeps Global I was recognised as the Q1 Hardworking Staff — an acknowledgment of the work I put into managing multiple brand strategies, executing campaigns and driving real growth across the company's digital presence.</p>
      <p>This recognition reflects not just effort but impact — the kind of work that moves numbers, builds communities and positions brands for long-term visibility.</p>
      <a href="#contact" class="btn-primary" style="margin-top:8px;">Work With Me</a>
    </div>
  </div>
</section>

<!-- CONTACT -->

<section id="contact">
  <div class="section-label">Get In Touch</div>
  <h2 class="section-title">Let's build something great together.</h2>
  <p class="sub">Open to remote roles, freelance projects and brand collaborations.</p>
  <div class="contact-links">
    <a href="mailto:Okparachika1212@gmail.com" class="contact-chip">📧 Okparachika1212@gmail.com</a>
    <a href="tel:+2348130977830" class="contact-chip">📞 +2348130977830</a>
    <a href="https://www.linkedin.com/in/okpara-chika" target="_blank" class="contact-chip">💼 LinkedIn</a>
    <a href="https://chika-okpara.my.canva.site" target="_blank" class="contact-chip">🌐 Canva Portfolio</a>
  </div>
  <div class="footer-line">
    © 2026 Chika Okpara · Social Media Strategist · Lagos, Nigeria
  </div>
</section>

</body>
</html>