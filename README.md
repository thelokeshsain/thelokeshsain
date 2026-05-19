<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width,initial-scale=1"/>
<title>Lokesh Sain — Software Engineer</title>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link href="https://fonts.googleapis.com/css2?family=Archivo:ital,wght@0,400;0,500;0,600;0,700;0,800;0,900;1,400&family=DM+Mono:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
/* ─── RESET & BASE ─────────────────────────────────────────── */
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --y:#ffde2d;
  --y-dim:#e8c900;
  --ink:#080808;
  --paper:#f7f5ef;
  --surface:#eeebe2;
  --line:rgba(8,8,8,.12);
  --muted:#666;
  --font-head:'Archivo',sans-serif;
  --font-mono:'DM Mono',monospace;
  --max:1200px;
  --r:3px;
}
html{scroll-behavior:smooth;font-size:16px}
body{
  background:var(--paper);
  color:var(--ink);
  font-family:var(--font-head);
  line-height:1.5;
  overflow-x:hidden;
  -webkit-font-smoothing:antialiased;
}
a{color:inherit;text-decoration:none}
img{display:block;max-width:100%}

/* ─── UTILITY ──────────────────────────────────────────────── */
.wrap{max-width:var(--max);margin:0 auto;padding:0 2.5rem}
.tag{
  display:inline-block;font-family:var(--font-mono);
  font-size:.65rem;letter-spacing:.12em;text-transform:uppercase;
  border:1px solid var(--ink);padding:.25rem .7rem;
  border-radius:100px;
}
.tag-filled{background:var(--y);border-color:var(--y);font-weight:500}
.label{
  font-family:var(--font-mono);font-size:.68rem;
  letter-spacing:.14em;text-transform:uppercase;color:var(--muted);
}
.reveal{opacity:0;transform:translateY(28px);transition:opacity .55s cubic-bezier(.22,1,.36,1),transform .55s cubic-bezier(.22,1,.36,1)}
.reveal.in{opacity:1;transform:none}
.reveal-d1{transition-delay:.08s}
.reveal-d2{transition-delay:.16s}
.reveal-d3{transition-delay:.24s}
.divider{height:1px;background:var(--ink);opacity:.12}

/* ─── CURSOR BLINK ─────────────────────────────────────────── */
.blink{animation:blink .9s step-end infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:0}}

/* ════════════════════════════════════════════════════════════ */
/*  NAV                                                         */
/* ════════════════════════════════════════════════════════════ */
nav{
  position:fixed;top:0;left:0;right:0;z-index:200;
  background:rgba(247,245,239,.9);
  backdrop-filter:blur(20px);-webkit-backdrop-filter:blur(20px);
  border-bottom:1px solid var(--line);
}
.nav-inner{
  max-width:var(--max);margin:0 auto;padding:0 2.5rem;
  height:60px;display:flex;align-items:center;justify-content:space-between;
}
.nav-logo{
  font-size:1rem;font-weight:900;letter-spacing:-.02em;
  display:flex;align-items:center;gap:8px;
}
.nav-logo-dot{
  width:8px;height:8px;border-radius:50%;
  background:var(--y);border:1.5px solid var(--ink);
  animation:pulse 2.5s ease-in-out infinite;
}
@keyframes pulse{0%,100%{box-shadow:0 0 0 0 rgba(255,222,45,.6)}60%{box-shadow:0 0 0 7px rgba(255,222,45,0)}}
.nav-links{display:flex;gap:2rem;list-style:none}
.nav-links a{
  font-size:.8rem;font-weight:600;letter-spacing:.04em;
  opacity:.5;transition:opacity .2s;
}
.nav-links a:hover{opacity:1}
.nav-cta{
  background:var(--ink);color:var(--y);
  font-size:.75rem;font-weight:700;letter-spacing:.06em;text-transform:uppercase;
  padding:.45rem 1.1rem;border-radius:var(--r);
  transition:background .2s,transform .15s;
}
.nav-cta:hover{background:#222;transform:translateY(-1px)}

/* ════════════════════════════════════════════════════════════ */
/*  HERO                                                        */
/* ════════════════════════════════════════════════════════════ */
.hero{
  min-height:100svh;
  padding:calc(60px + 6rem) 2.5rem 5rem;
  max-width:var(--max);margin:0 auto;
  display:grid;grid-template-columns:1fr 400px;
  align-items:center;gap:4rem;
}
.hero-eyebrow{
  display:flex;align-items:center;gap:.6rem;
  margin-bottom:2rem;
}
.hero-eyebrow-line{width:32px;height:2px;background:var(--y);flex-shrink:0}
.hero-name{
  font-size:clamp(4.5rem,9vw,8.5rem);
  font-weight:900;line-height:.9;letter-spacing:-.04em;
  margin-bottom:1.5rem;
}
.hero-name .line2{
  -webkit-text-stroke:2px var(--ink);
  color:transparent;
}
.hero-name .highlight{
  position:relative;display:inline-block;
}
.hero-name .highlight::after{
  content:'';position:absolute;
  left:0;bottom:6px;right:0;height:.18em;
  background:var(--y);z-index:-1;
}
.hero-typed{
  font-family:var(--font-mono);font-size:1rem;
  color:var(--muted);margin-bottom:3rem;min-height:1.5em;
}
.hero-typed-cursor{
  display:inline-block;width:1.5px;height:.9em;
  background:var(--ink);vertical-align:middle;margin-left:1px;
}
.hero-actions{display:flex;gap:12px;flex-wrap:wrap}
.btn{
  display:inline-flex;align-items:center;gap:6px;
  font-family:var(--font-head);font-weight:700;
  font-size:.8rem;letter-spacing:.05em;text-transform:uppercase;
  padding:.7rem 1.6rem;border-radius:var(--r);
  border:1.5px solid transparent;cursor:pointer;
  transition:transform .15s,box-shadow .15s,background .15s;
}
.btn:hover{transform:translateY(-2px)}
.btn-dark{background:var(--ink);color:var(--y);border-color:var(--ink)}
.btn-dark:hover{box-shadow:0 6px 20px rgba(8,8,8,.25)}
.btn-outline{background:transparent;color:var(--ink);border-color:var(--ink)}
.btn-outline:hover{background:var(--ink);color:var(--y)}
.btn-arrow{font-size:1rem;transition:transform .15s}
.btn:hover .btn-arrow{transform:translateX(3px)}

/* Hero right panel */
.hero-panel{
  background:var(--ink);border-radius:12px;
  padding:2.5rem;display:flex;flex-direction:column;gap:2rem;
}
.hero-panel-label{color:rgba(255,255,255,.3);font-family:var(--font-mono);font-size:.62rem;letter-spacing:.14em;text-transform:uppercase;margin-bottom:.5rem}
.hero-status{
  display:flex;align-items:center;gap:.6rem;
  color:#fff;font-size:.85rem;font-weight:600;
}
.status-dot{width:7px;height:7px;border-radius:50%;background:#4ade80;flex-shrink:0;animation:pulse2 2s infinite}
@keyframes pulse2{0%,100%{opacity:1}50%{opacity:.4}}
.hero-stats-grid{display:grid;grid-template-columns:1fr 1fr;gap:1px;background:#222}
.hero-stat{background:var(--ink);padding:1.25rem}
.hero-stat-n{font-size:2.2rem;font-weight:900;color:var(--y);line-height:1}
.hero-stat-l{font-family:var(--font-mono);font-size:.6rem;color:rgba(255,255,255,.35);letter-spacing:.1em;text-transform:uppercase;margin-top:.25rem}
.hero-chips{display:flex;flex-wrap:wrap;gap:6px}
.hero-chip{
  font-family:var(--font-mono);font-size:.68rem;
  padding:.3rem .7rem;border-radius:100px;
  border:1px solid #333;color:rgba(255,255,255,.5);
  transition:border-color .2s,color .2s;
}
.hero-chip:hover{border-color:var(--y);color:var(--y)}
.hero-loc{display:flex;align-items:center;gap:.5rem;color:rgba(255,255,255,.3);font-family:var(--font-mono);font-size:.7rem}
.hero-loc-pin{color:var(--y)}

/* ════════════════════════════════════════════════════════════ */
/*  MARQUEE                                                     */
/* ════════════════════════════════════════════════════════════ */
.marquee-wrap{
  background:var(--y);
  border-top:1.5px solid var(--ink);border-bottom:1.5px solid var(--ink);
  overflow:hidden;padding:.6rem 0;
}
.marquee-track{
  display:flex;width:max-content;
  animation:marquee 22s linear infinite;
}
@keyframes marquee{from{transform:translateX(0)}to{transform:translateX(-50%)}}
.marquee-item{
  white-space:nowrap;
  font-size:.72rem;font-weight:800;letter-spacing:.12em;text-transform:uppercase;
  padding:0 2rem;display:flex;align-items:center;gap:1rem;
}
.marquee-sep{width:4px;height:4px;border-radius:50%;background:var(--ink);opacity:.3}

/* ════════════════════════════════════════════════════════════ */
/*  ABOUT                                                       */
/* ════════════════════════════════════════════════════════════ */
.section{padding:7rem 0}
.section-header{
  display:flex;align-items:flex-start;justify-content:space-between;
  gap:2rem;margin-bottom:5rem;
}
.section-title{
  font-size:clamp(2.8rem,5vw,4.5rem);
  font-weight:900;line-height:.95;letter-spacing:-.04em;
}
.section-title em{font-style:normal;color:var(--y);-webkit-text-stroke:1px var(--ink)}
.section-num{
  font-family:var(--font-mono);font-size:.7rem;color:var(--muted);
  letter-spacing:.12em;text-transform:uppercase;padding-top:.5rem;white-space:nowrap;
}
.about-grid{display:grid;grid-template-columns:1.1fr .9fr;gap:5rem;align-items:start}
.about-bio p{font-size:1.1rem;line-height:1.85;color:#333;margin-bottom:1.25rem}
.about-bio p strong{color:var(--ink);font-weight:700}
.about-bio p:last-child{margin:0}
.skills-wrap{display:flex;flex-direction:column;gap:2.5rem}
.skill-group-title{font-size:.65rem;font-weight:700;letter-spacing:.14em;text-transform:uppercase;color:var(--muted);font-family:var(--font-mono);margin-bottom:.75rem}
.skill-tags{display:flex;flex-wrap:wrap;gap:6px}
.skill-tag{
  font-size:.75rem;font-weight:600;
  padding:.35rem .85rem;border-radius:100px;
  border:1.5px solid var(--ink);
  transition:background .15s,color .15s,border-color .15s;cursor:default;
}
.skill-tag:hover{background:var(--y);border-color:var(--y)}

/* ════════════════════════════════════════════════════════════ */
/*  EXPERIENCE                                                  */
/* ════════════════════════════════════════════════════════════ */
.exp-section{background:var(--ink);padding:7rem 0}
.exp-section .section-title{color:#fff}
.exp-section .section-title em{-webkit-text-stroke:1px var(--y)}
.exp-section .section-num{color:rgba(255,255,255,.25)}
.exp-section .label{color:rgba(255,255,255,.3)}
.timeline{display:flex;flex-direction:column;gap:0}
.exp-card{
  display:grid;grid-template-columns:260px 1fr;
  border-top:1px solid rgba(255,255,255,.08);
  padding:3rem 0;gap:4rem;
  transition:background .2s;
}
.exp-card:last-child{border-bottom:1px solid rgba(255,255,255,.08)}
.exp-left{}
.exp-period{
  font-family:var(--font-mono);font-size:.72rem;
  color:rgba(255,255,255,.3);letter-spacing:.06em;margin-bottom:.75rem;
}
.exp-company{font-size:1rem;font-weight:800;color:#fff;margin-bottom:.4rem}
.exp-type{
  display:inline-block;font-family:var(--font-mono);font-size:.62rem;
  font-weight:500;letter-spacing:.1em;text-transform:uppercase;
  padding:.25rem .7rem;border-radius:100px;
  background:var(--y);color:var(--ink);
}
.exp-right{}
.exp-role{font-size:1.6rem;font-weight:900;color:#fff;letter-spacing:-.03em;margin-bottom:1.5rem;line-height:1.1}
.exp-list{list-style:none;display:flex;flex-direction:column;gap:.75rem;margin-bottom:1.5rem}
.exp-list li{
  font-size:.92rem;line-height:1.7;
  color:rgba(255,255,255,.55);
  padding-left:1.2rem;position:relative;
}
.exp-list li::before{
  content:'';position:absolute;left:0;top:.65em;
  width:5px;height:5px;border-radius:50%;
  background:var(--y);
}
.exp-tags{display:flex;flex-wrap:wrap;gap:6px}
.exp-tag{
  font-family:var(--font-mono);font-size:.65rem;letter-spacing:.06em;
  padding:.2rem .65rem;border-radius:100px;
  border:1px solid rgba(255,255,255,.12);color:rgba(255,255,255,.35);
}

/* ════════════════════════════════════════════════════════════ */
/*  PROJECTS                                                    */
/* ════════════════════════════════════════════════════════════ */
.projects-grid{
  display:grid;grid-template-columns:1fr 1fr 1fr;
  gap:1.5rem;
}
.proj-card{
  background:#fff;border:1.5px solid var(--ink);
  border-radius:10px;padding:2rem;
  display:flex;flex-direction:column;gap:1rem;
  position:relative;overflow:hidden;
  transition:transform .2s,box-shadow .2s;
}
.proj-card::before{
  content:'';position:absolute;inset:0;
  background:var(--y);transform:translateY(100%);
  transition:transform .35s cubic-bezier(.22,1,.36,1);
  z-index:0;
}
.proj-card:hover{transform:translateY(-4px);box-shadow:0 16px 40px rgba(8,8,8,.12)}
.proj-card:hover::before{transform:translateY(0)}
.proj-card:hover .proj-num,
.proj-card:hover .proj-name,
.proj-card:hover .proj-desc,
.proj-card:hover .proj-tag{color:var(--ink)!important;border-color:rgba(8,8,8,.3)!important}
.proj-card > *{position:relative;z-index:1}
.proj-num{font-family:var(--font-mono);font-size:.65rem;color:var(--muted);letter-spacing:.1em;transition:color .3s}
.proj-name{font-size:1.3rem;font-weight:900;letter-spacing:-.03em;transition:color .3s}
.proj-desc{font-size:.85rem;line-height:1.75;color:#555;flex:1;transition:color .3s}
.proj-footer{display:flex;flex-wrap:wrap;gap:6px;margin-top:auto}
.proj-tag{
  font-family:var(--font-mono);font-size:.63rem;letter-spacing:.06em;
  padding:.2rem .6rem;border-radius:100px;
  border:1px solid rgba(8,8,8,.15);color:var(--muted);
  transition:color .3s,border-color .3s;
}
.proj-arrow{
  position:absolute;top:1.5rem;right:1.5rem;
  width:32px;height:32px;border-radius:50%;
  border:1.5px solid var(--ink);
  display:flex;align-items:center;justify-content:center;
  font-size:.9rem;z-index:1;transition:background .2s,color .2s;
}
.proj-card:hover .proj-arrow{background:var(--ink);color:var(--y)}

/* ════════════════════════════════════════════════════════════ */
/*  EDUCATION                                                   */
/* ════════════════════════════════════════════════════════════ */
.edu-section{background:var(--surface);padding:7rem 0}
.edu-grid{display:grid;grid-template-columns:1fr 1fr;gap:1.5rem;margin-bottom:1.5rem}
.edu-card{
  background:var(--paper);border:1.5px solid var(--ink);
  border-radius:10px;padding:2.5rem;
}
.edu-year{font-family:var(--font-mono);font-size:.68rem;color:var(--muted);letter-spacing:.1em;margin-bottom:1.25rem}
.edu-degree{font-size:1.25rem;font-weight:900;letter-spacing:-.03em;line-height:1.2;margin-bottom:.4rem}
.edu-school{font-size:.88rem;color:#555;margin-bottom:.3rem}
.edu-location{font-family:var(--font-mono);font-size:.7rem;color:var(--muted);margin-bottom:1.25rem}
.edu-score{
  display:inline-flex;align-items:center;gap:.4rem;
  background:var(--y);border:1.5px solid var(--ink);
  font-family:var(--font-mono);font-size:.75rem;font-weight:600;
  padding:.3rem .85rem;border-radius:100px;
}
.certs-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem}
.cert-card{
  background:var(--paper);border:1.5px solid var(--ink);
  border-radius:10px;padding:1.75rem;
  transition:background .2s,transform .2s;
}
.cert-card:hover{background:var(--y);transform:translateY(-2px)}
.cert-by{font-family:var(--font-mono);font-size:.62rem;color:var(--muted);letter-spacing:.1em;margin-bottom:.5rem}
.cert-name{font-size:.95rem;font-weight:800;letter-spacing:-.01em}

/* ════════════════════════════════════════════════════════════ */
/*  CONTACT                                                     */
/* ════════════════════════════════════════════════════════════ */
.contact-section{background:var(--ink);padding:8rem 0}
.contact-inner{
  display:grid;grid-template-columns:1fr .9fr;
  gap:6rem;align-items:center;
}
.contact-title{
  font-size:clamp(3rem,6vw,5.5rem);
  font-weight:900;color:#fff;letter-spacing:-.04em;line-height:.95;
  margin-bottom:1.5rem;
}
.contact-title span{color:var(--y)}
.contact-sub{font-size:1rem;color:rgba(255,255,255,.35);line-height:1.75;max-width:380px}
.contact-links{display:flex;flex-direction:column;gap:1px;border:1px solid rgba(255,255,255,.08);border-radius:10px;overflow:hidden}
.contact-link{
  display:flex;align-items:center;justify-content:space-between;
  padding:1.4rem 1.75rem;
  border-bottom:1px solid rgba(255,255,255,.06);
  background:rgba(255,255,255,.02);
  transition:background .2s;cursor:pointer;
}
.contact-link:last-child{border-bottom:none}
.contact-link:hover{background:rgba(255,222,45,.07)}
.contact-link-left{display:flex;flex-direction:column;gap:.2rem}
.contact-link-platform{font-family:var(--font-mono);font-size:.6rem;color:rgba(255,255,255,.25);letter-spacing:.12em;text-transform:uppercase}
.contact-link-value{font-size:.9rem;font-weight:600;color:#fff}
.contact-link-arrow{color:var(--y);font-size:1.1rem;transition:transform .2s}
.contact-link:hover .contact-link-arrow{transform:translate(3px,-3px)}

/* ════════════════════════════════════════════════════════════ */
/*  FOOTER                                                      */
/* ════════════════════════════════════════════════════════════ */
footer{
  background:var(--ink);
  border-top:1px solid rgba(255,255,255,.06);
  padding:1.75rem 2.5rem;
  display:flex;align-items:center;justify-content:space-between;
}
.footer-logo{font-weight:900;font-size:.9rem;color:var(--y);letter-spacing:-.01em}
.footer-copy{font-family:var(--font-mono);font-size:.65rem;color:rgba(255,255,255,.2);letter-spacing:.06em}
.footer-back{
  font-family:var(--font-mono);font-size:.65rem;letter-spacing:.1em;text-transform:uppercase;
  color:rgba(255,255,255,.25);cursor:pointer;transition:color .2s;border:none;background:none;
}
.footer-back:hover{color:var(--y)}

/* ─── RESPONSIVE ───────────────────────────────────────────── */
@media(max-width:960px){
  .hero{grid-template-columns:1fr;padding-top:calc(60px + 4rem)}
  .hero-panel{display:none}
  .about-grid,.contact-inner{grid-template-columns:1fr;gap:3rem}
  .projects-grid{grid-template-columns:1fr 1fr}
  .exp-card{grid-template-columns:1fr;gap:1rem}
  .certs-grid{grid-template-columns:1fr 1fr}
}
@media(max-width:640px){
  .wrap{padding:0 1.25rem}
  .section{padding:5rem 0}
  .projects-grid,.edu-grid,.certs-grid{grid-template-columns:1fr}
  .hero-name{font-size:4rem}
  .section-title{font-size:2.8rem}
  .nav-links{display:none}
  footer{flex-direction:column;gap:.75rem;text-align:center}
}
</style>
</head>
<body>

<!-- ─── NAV ─────────────────────────────────────────────────── -->
<nav>
  <div class="nav-inner">
    <div class="nav-logo">
      <div class="nav-logo-dot"></div>
      Lokesh Sain
    </div>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#education">Education</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
    <a href="mailto:iamlokeshsain@gmail.com" class="nav-cta">Hire me</a>
  </div>
</nav>

<!-- ─── HERO ─────────────────────────────────────────────────── -->
<div style="max-width:var(--max);margin:0 auto">
  <div class="hero">
    <div>
      <div class="hero-eyebrow reveal">
        <div class="hero-eyebrow-line"></div>
        <span class="label">Based in Jaipur, Rajasthan</span>
      </div>
      <h1 class="hero-name reveal reveal-d1">
        <div>Lokesh</div>
        <div class="line2"><span class="highlight">Sain</span></div>
      </h1>
      <p class="hero-typed reveal reveal-d2">
        <span id="typed"></span><span class="hero-typed-cursor blink"></span>
      </p>
      <div class="hero-actions reveal reveal-d3">
        <a href="#projects" class="btn btn-dark">View Projects <span class="btn-arrow">→</span></a>
        <a href="#contact" class="btn btn-outline">Get in touch</a>
      </div>
    </div>
    <!-- Panel -->
    <div class="hero-panel reveal reveal-d2">
      <div>
        <div class="hero-panel-label">Current Status</div>
        <div class="hero-status"><span class="status-dot"></span>Open to opportunities</div>
      </div>
      <div>
        <div class="hero-panel-label" style="margin-bottom:.75rem">By the numbers</div>
        <div class="hero-stats-grid">
          <div class="hero-stat"><div class="hero-stat-n">1+</div><div class="hero-stat-l">Yrs. experience</div></div>
          <div class="hero-stat"><div class="hero-stat-n">3+</div><div class="hero-stat-l">Live projects</div></div>
          <div class="hero-stat"><div class="hero-stat-n">8.29</div><div class="hero-stat-l">MCA CGPA</div></div>
          <div class="hero-stat"><div class="hero-stat-n">2+</div><div class="hero-stat-l">Certifications</div></div>
        </div>
      </div>
      <div>
        <div class="hero-panel-label" style="margin-bottom:.75rem">Tech I love</div>
        <div class="hero-chips">
          <span class="hero-chip">React.js</span>
          <span class="hero-chip">JavaScript</span>
          <span class="hero-chip">Node.js</span>
          <span class="hero-chip">REST APIs</span>
          <span class="hero-chip">MySQL</span>
          <span class="hero-chip">MongoDB</span>
          <span class="hero-chip">Git</span>
        </div>
      </div>
      <div class="hero-loc">
        <span class="hero-loc-pin">◉</span>
        Jaipur, Rajasthan, India
      </div>
    </div>
  </div>
</div>

<!-- ─── MARQUEE ───────────────────────────────────────────────── -->
<div class="marquee-wrap">
  <div class="marquee-track" id="marquee"></div>
</div>

<!-- ─── ABOUT ────────────────────────────────────────────────── -->
<section class="section" id="about">
  <div class="wrap">
    <div class="section-header">
      <h2 class="section-title reveal">About <em>Me</em></h2>
      <span class="section-num reveal">01 / 04</span>
    </div>
    <div class="about-grid">
      <div class="about-bio reveal">
        <p>I'm a <strong>Software Engineer at 3Handshake Techsoft</strong>, where I architect scalable React.js applications that perform beautifully under real-world conditions. Promoted from intern to full-time in under 6 months.</p>
        <p>My focus is on the intersection of strong <strong>frontend engineering</strong> and thoughtful UX — building component systems, optimizing Core Web Vitals, and integrating REST APIs with clean, maintainable patterns.</p>
        <p>Currently finishing my <strong>MCA (CGPA: 8.29)</strong> at DY Patil Institute, Pune. I care deeply about code quality, design precision, and shipping things that actually work.</p>
      </div>
      <div class="skills-wrap reveal reveal-d1">
        <div>
          <div class="skill-group-title">Frontend</div>
          <div class="skill-tags">
            <span class="skill-tag">React.js</span>
            <span class="skill-tag">HTML5</span>
            <span class="skill-tag">CSS3</span>
            <span class="skill-tag">React Hooks</span>
            <span class="skill-tag">Context API</span>
          </div>
        </div>
        <div>
          <div class="skill-group-title">Languages</div>
          <div class="skill-tags">
            <span class="skill-tag">JavaScript</span>
            <span class="skill-tag">Python</span>
            <span class="skill-tag">PHP</span>
            <span class="skill-tag">SQL</span>
          </div>
        </div>
        <div>
          <div class="skill-group-title">Backend & Data</div>
          <div class="skill-tags">
            <span class="skill-tag">Node.js</span>
            <span class="skill-tag">REST APIs</span>
            <span class="skill-tag">MySQL</span>
            <span class="skill-tag">MongoDB</span>
          </div>
        </div>
        <div>
          <div class="skill-group-title">Tools</div>
          <div class="skill-tags">
            <span class="skill-tag">Git</span>
            <span class="skill-tag">GitHub</span>
            <span class="skill-tag">VS Code</span>
            <span class="skill-tag">Chrome DevTools</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ─── EXPERIENCE ───────────────────────────────────────────── -->
<section class="exp-section" id="experience">
  <div class="wrap">
    <div class="section-header">
      <h2 class="section-title reveal">Work <em>Experience</em></h2>
      <span class="section-num reveal">02 / 04</span>
    </div>
    <div class="timeline">

      <div class="exp-card reveal">
        <div class="exp-left">
          <div class="exp-period">Jul 2025 — Present</div>
          <div class="exp-company">3Handshake Techsoft</div>
          <br/>
          <span class="exp-type">Full-time</span>
        </div>
        <div class="exp-right">
          <div class="exp-role">Software Engineer</div>
          <ul class="exp-list">
            <li>Promoted from intern after demonstrating exceptional ownership of critical product features</li>
            <li>Architected scalable web apps in React.js using component-driven design for long-term maintainability</li>
            <li>Improved Core Web Vitals — code splitting, lazy loading, and optimized state management</li>
            <li>Collaborated cross-functionally with backend engineers and UI/UX designers in Agile/Scrum</li>
          </ul>
          <div class="exp-tags">
            <span class="exp-tag">React.js</span>
            <span class="exp-tag">JavaScript</span>
            <span class="exp-tag">REST APIs</span>
            <span class="exp-tag">Agile/Scrum</span>
            <span class="exp-tag">Core Web Vitals</span>
          </div>
        </div>
      </div>

      <div class="exp-card reveal reveal-d1">
        <div class="exp-left">
          <div class="exp-period">Jan 2025 — Jul 2025</div>
          <div class="exp-company">3Handshake Techsoft</div>
          <br/>
          <span class="exp-type">Internship</span>
        </div>
        <div class="exp-right">
          <div class="exp-role">Web Developer Intern</div>
          <ul class="exp-list">
            <li>Built responsive, accessible UIs with React.js, HTML5, CSS3 — mobile-first across all browsers</li>
            <li>Integrated RESTful APIs with efficient data-fetching and robust error-handling patterns</li>
            <li>Developed reusable component library using atomic design principles, cutting dev time significantly</li>
            <li>Resolved critical production bugs, directly improving stability and user retention metrics</li>
          </ul>
          <div class="exp-tags">
            <span class="exp-tag">React.js</span>
            <span class="exp-tag">Context API</span>
            <span class="exp-tag">CSS3</span>
            <span class="exp-tag">Atomic Design</span>
            <span class="exp-tag">API Integration</span>
          </div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- ─── PROJECTS ─────────────────────────────────────────────── -->
<section class="section" id="projects">
  <div class="wrap">
    <div class="section-header">
      <h2 class="section-title reveal">Selected <em>Work</em></h2>
      <span class="section-num reveal">03 / 04</span>
    </div>
    <div class="projects-grid">

      <div class="proj-card reveal">
        <div class="proj-arrow">↗</div>
        <div class="proj-num">Project 01</div>
        <div class="proj-name">Apna Backup</div>
        <div class="proj-desc">Full-stack web app for secure online backup solutions — intuitive UI, seamless navigation, and real-time data synchronization through RESTful API integration.</div>
        <div class="proj-footer">
          <span class="proj-tag">React.js</span>
          <span class="proj-tag">REST APIs</span>
          <span class="proj-tag">Responsive Design</span>
        </div>
      </div>

      <div class="proj-card reveal reveal-d1">
        <div class="proj-arrow">↗</div>
        <div class="proj-num">Project 02</div>
        <div class="proj-name">FoodCourt App</div>
        <div class="proj-desc">Android application to streamline cafeteria ordering — live order tracking, real-time database, secure authentication, and Material Design UI to boost engagement.</div>
        <div class="proj-footer">
          <span class="proj-tag">Android</span>
          <span class="proj-tag">Java</span>
          <span class="proj-tag">XML</span>
          <span class="proj-tag">Real-time DB</span>
        </div>
      </div>

      <div class="proj-card reveal reveal-d2">
        <div class="proj-arrow">↗</div>
        <div class="proj-num">Project 03</div>
        <div class="proj-name">Sizzling Salon</div>
        <div class="proj-desc">Full-stack salon management platform — appointment booking, service dashboard, secure PHP session auth, and normalized MySQL schema for efficient data retrieval.</div>
        <div class="proj-footer">
          <span class="proj-tag">PHP</span>
          <span class="proj-tag">MySQL</span>
          <span class="proj-tag">HTML5</span>
          <span class="proj-tag">CSS3</span>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- ─── EDUCATION ────────────────────────────────────────────── -->
<section class="edu-section" id="education">
  <div class="wrap">
    <div class="section-header">
      <h2 class="section-title reveal">Education &amp; <em>Certs</em></h2>
      <span class="section-num reveal">04 / 04</span>
    </div>
    <div class="edu-grid">
      <div class="edu-card reveal">
        <div class="edu-year">Aug 2023 — Jun 2025</div>
        <div class="edu-degree">Master of Computer Applications</div>
        <div class="edu-school">DY Patil Institute of MCA and Management</div>
        <div class="edu-location">Pune, Maharashtra</div>
        <span class="edu-score">⭑ CGPA 8.29 / 10</span>
      </div>
      <div class="edu-card reveal reveal-d1">
        <div class="edu-year">Aug 2020 — Jul 2023</div>
        <div class="edu-degree">Bachelor of Computer Applications</div>
        <div class="edu-school">S.S. Jain Subodh PG College</div>
        <div class="edu-location">Jaipur, Rajasthan</div>
        <span class="edu-score">⭑ 81.64%</span>
      </div>
    </div>
    <div class="certs-grid">
      <div class="cert-card reveal">
        <div class="cert-by">IIT Bombay Spoken Tutorial</div>
        <div class="cert-name">Python Programming</div>
      </div>
      <div class="cert-card reveal reveal-d1">
        <div class="cert-by">IIT Bombay Spoken Tutorial</div>
        <div class="cert-name">HTML Web Development</div>
      </div>
      <div class="cert-card reveal reveal-d2">
        <div class="cert-by">MIT-WPU School of Business · Apr 2024</div>
        <div class="cert-name">Codeathon Hackathon</div>
      </div>
    </div>
  </div>
</section>

<!-- ─── CONTACT ──────────────────────────────────────────────── -->
<section class="contact-section" id="contact">
  <div class="wrap">
    <div class="contact-inner">
      <div class="reveal">
        <h2 class="contact-title">Let's build<br/><span>something</span><br/>great.</h2>
        <p class="contact-sub">Open to full-time roles, freelance projects, and interesting collaborations. Always happy to chat.</p>
      </div>
      <div class="contact-links reveal reveal-d1">
        <a href="mailto:iamlokeshsain@gmail.com" class="contact-link">
          <div class="contact-link-left">
            <span class="contact-link-platform">Email</span>
            <span class="contact-link-value">iamlokeshsain@gmail.com</span>
          </div>
          <span class="contact-link-arrow">↗</span>
        </a>
        <a href="https://linkedin.com/in/thelokeshsain" target="_blank" class="contact-link">
          <div class="contact-link-left">
            <span class="contact-link-platform">LinkedIn</span>
            <span class="contact-link-value">thelokeshsain</span>
          </div>
          <span class="contact-link-arrow">↗</span>
        </a>
        <a href="https://github.com/thelokeshsain" target="_blank" class="contact-link">
          <div class="contact-link-left">
            <span class="contact-link-platform">GitHub</span>
            <span class="contact-link-value">thelokeshsain</span>
          </div>
          <span class="contact-link-arrow">↗</span>
        </a>
      </div>
    </div>
  </div>
</section>

<!-- ─── FOOTER ───────────────────────────────────────────────── -->
<footer>
  <div class="footer-logo">Lokesh Sain</div>
  <div class="footer-copy">© 2025 · All rights reserved</div>
  <button class="footer-back" onclick="window.scrollTo({top:0,behavior:'smooth'})">↑ Back to top</button>
</footer>

<!-- ─── JS ──────────────────────────────────────────────────── -->
<script>
/* Typing effect */
const roles=['Software Engineer','React.js Developer','Frontend Engineer','Full Stack Developer'];
let ri=0,ci=0,del=false,el=document.getElementById('typed');
function tick(){
  const w=roles[ri];
  el.textContent=del?w.slice(0,ci--):w.slice(0,ci++);
  if(!del&&ci>w.length){setTimeout(()=>{del=true;tick()},1600);return}
  if(del&&ci<0){del=false;ri=(ri+1)%roles.length;ci=0}
  setTimeout(tick,del?38:78);
}
tick();

/* Marquee */
const items=['React.js','Frontend Engineering','Component Architecture','REST API Integration','Performance Optimization','Responsive Design','JavaScript','Node.js','MongoDB','MySQL','UI Development','Agile & Scrum'];
const m=document.getElementById('marquee');
const str=items.map(t=>`<span class="marquee-item">${t}<span class="marquee-sep"></span></span>`).join('');
m.innerHTML=str+str;

/* Scroll reveal */
const obs=new IntersectionObserver(es=>{es.forEach(e=>{if(e.isIntersecting)e.target.classList.add('in')})},{threshold:.12});
document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));

/* Nav active state */
window.addEventListener('scroll',()=>{
  const n=document.querySelector('nav');
  n.style.borderBottomColor=scrollY>10?'rgba(8,8,8,.12)':'transparent';
});
</script>
</body>
</html>
