<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>RajeevGandhi-EXE | GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Syne:wght@400;700;800;900&family=JetBrains+Mono:wght@300;400;700&display=swap" rel="stylesheet"/>
<style>
  :root {
    --blue: #0057FF;
    --cyan: #00F0FF;
    --green: #00FF88;
    --dark: #050810;
    --card: #0a0f1e;
    --border: rgba(0,87,255,0.25);
    --text: #c8d8ff;
    --dim: #4a5a80;
  }

  * { margin:0; padding:0; box-sizing:border-box; }

  body {
    background: var(--dark);
    color: var(--text);
    font-family: 'JetBrains Mono', monospace;
    overflow-x: hidden;
    cursor: none;
  }

  /* Custom cursor */
  .cursor {
    width: 12px; height: 12px;
    background: var(--cyan);
    border-radius: 50%;
    position: fixed;
    pointer-events: none;
    z-index: 9999;
    transition: transform 0.1s;
    mix-blend-mode: screen;
  }
  .cursor-ring {
    width: 36px; height: 36px;
    border: 1px solid rgba(0,240,255,0.4);
    border-radius: 50%;
    position: fixed;
    pointer-events: none;
    z-index: 9998;
    transition: all 0.15s ease;
    mix-blend-mode: screen;
  }

  /* Grid background */
  body::before {
    content: '';
    position: fixed; inset: 0;
    background-image:
      linear-gradient(rgba(0,87,255,0.05) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,87,255,0.05) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  /* Glow orbs */
  .orb {
    position: fixed;
    border-radius: 50%;
    filter: blur(100px);
    pointer-events: none;
    z-index: 0;
    opacity: 0.15;
    animation: drift 20s ease-in-out infinite alternate;
  }
  .orb1 { width:500px; height:500px; background:var(--blue); top:-100px; left:-100px; }
  .orb2 { width:400px; height:400px; background:var(--cyan); bottom:-100px; right:-100px; animation-delay:-10s; }
  .orb3 { width:300px; height:300px; background:var(--green); top:40%; left:40%; animation-delay:-5s; opacity:0.08; }

  @keyframes drift {
    from { transform: translate(0,0) scale(1); }
    to { transform: translate(60px, 40px) scale(1.1); }
  }

  /* Scanline */
  body::after {
    content:'';
    position:fixed; inset:0;
    background: repeating-linear-gradient(0deg, transparent, transparent 2px, rgba(0,0,0,0.03) 2px, rgba(0,0,0,0.03) 4px);
    pointer-events:none;
    z-index:1;
  }

  .wrapper { position:relative; z-index:2; max-width:900px; margin:0 auto; padding:40px 24px 80px; }

  /* ── HERO ── */
  .hero { text-align:center; padding:60px 0 40px; }

  .status-pill {
    display:inline-flex; align-items:center; gap:8px;
    border:1px solid rgba(0,255,136,0.3);
    background: rgba(0,255,136,0.05);
    padding:6px 16px; border-radius:999px;
    font-size:11px; letter-spacing:2px; text-transform:uppercase;
    color: var(--green);
    margin-bottom:32px;
    animation: pulse-border 2s ease-in-out infinite;
  }
  .status-dot { width:7px; height:7px; border-radius:50%; background:var(--green); animation: blink 1.2s ease-in-out infinite; }
  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0.2} }
  @keyframes pulse-border { 0%,100%{box-shadow:0 0 0 0 rgba(0,255,136,0.2)} 50%{box-shadow:0 0 0 8px rgba(0,255,136,0)} }

  .name-block { margin-bottom:16px; }
  .name-first {
    display:block;
    font-family:'Syne', sans-serif;
    font-weight:900;
    font-size:clamp(56px,10vw,110px);
    line-height:0.9;
    color:#fff;
    letter-spacing:-3px;
    animation: fadeUp 0.8s ease both;
  }
  .name-last {
    display:block;
    font-family:'Syne', sans-serif;
    font-weight:900;
    font-size:clamp(56px,10vw,110px);
    line-height:0.9;
    color:var(--blue);
    letter-spacing:-3px;
    animation: fadeUp 0.8s 0.15s ease both;
  }
  .name-k {
    color: var(--cyan);
  }
  @keyframes fadeUp { from{opacity:0;transform:translateY(30px)} to{opacity:1;transform:translateY(0)} }

  .tagline {
    font-family:'Share Tech Mono', monospace;
    font-size:13px;
    color: var(--dim);
    letter-spacing:3px;
    margin:16px 0 28px;
    animation: fadeUp 0.8s 0.3s ease both;
  }
  .tagline span { color:var(--blue); }

  .terminal-bio {
    display:inline-block;
    text-align:left;
    background: rgba(0,87,255,0.04);
    border:1px solid var(--border);
    border-radius:8px;
    padding:20px 28px;
    font-size:12px;
    line-height:2;
    max-width:560px;
    animation: fadeUp 0.8s 0.45s ease both;
  }
  .terminal-bio .prompt { color:var(--blue); }
  .terminal-bio .cmd { color:var(--cyan); }
  .terminal-bio .out { color:var(--text); }
  .cursor-blink { display:inline-block; width:8px; height:14px; background:var(--cyan); animation:blink 1s infinite; vertical-align:middle; }

  /* badges */
  .badges {
    display:flex; flex-wrap:wrap; justify-content:center; gap:10px;
    margin:28px 0 0;
    animation: fadeUp 0.8s 0.6s ease both;
  }
  .badge {
    display:flex; align-items:center; gap:7px;
    padding:8px 16px; border-radius:6px;
    font-size:11px; letter-spacing:1px; text-transform:uppercase;
    border:1px solid;
    transition: all 0.25s ease;
    text-decoration:none;
    font-family:'Share Tech Mono',monospace;
  }
  .badge:hover { transform:translateY(-3px); }
  .badge-blue  { border-color:var(--blue);  color:var(--blue);  background:rgba(0,87,255,0.08); }
  .badge-blue:hover  { background:rgba(0,87,255,0.18); box-shadow:0 8px 24px rgba(0,87,255,0.3); }
  .badge-cyan  { border-color:var(--cyan);  color:var(--cyan);  background:rgba(0,240,255,0.05); }
  .badge-cyan:hover  { background:rgba(0,240,255,0.12); box-shadow:0 8px 24px rgba(0,240,255,0.2); }
  .badge-green { border-color:var(--green); color:var(--green); background:rgba(0,255,136,0.05); }
  .badge-green:hover { background:rgba(0,255,136,0.12); box-shadow:0 8px 24px rgba(0,255,136,0.2); }
  .badge-red   { border-color:#ff4444; color:#ff4444; background:rgba(255,68,68,0.05); }
  .badge-red:hover   { background:rgba(255,68,68,0.12); box-shadow:0 8px 24px rgba(255,68,68,0.2); }

  /* ── SECTIONS ── */
  .section { margin-top:64px; animation: fadeUp 0.8s ease both; }
  .section-header {
    display:flex; align-items:center; gap:12px;
    margin-bottom:28px;
  }
  .section-label {
    font-family:'Share Tech Mono', monospace;
    font-size:11px; letter-spacing:3px; text-transform:uppercase;
    color:var(--blue);
  }
  .section-line { flex:1; height:1px; background:linear-gradient(90deg,var(--border),transparent); }
  .section-num { font-size:10px; color:var(--dim); font-family:'Share Tech Mono',monospace; }

  /* ── STATS ROW ── */
  .stats-row {
    display:grid; grid-template-columns:repeat(3,1fr); gap:16px;
    margin-bottom:40px;
  }
  .stat-card {
    border:1px solid var(--border);
    border-radius:8px;
    padding:20px 16px;
    text-align:center;
    background: rgba(0,87,255,0.03);
    transition: all 0.3s ease;
    position:relative; overflow:hidden;
  }
  .stat-card::before {
    content:'';
    position:absolute; inset:0;
    background: linear-gradient(135deg, rgba(0,87,255,0.08), transparent);
    opacity:0;
    transition:opacity 0.3s;
  }
  .stat-card:hover { transform:translateY(-4px); border-color:var(--blue); box-shadow:0 12px 32px rgba(0,87,255,0.15); }
  .stat-card:hover::before { opacity:1; }
  .stat-num { font-family:'Syne',sans-serif; font-weight:900; font-size:48px; color:var(--blue); line-height:1; }
  .stat-num span { color:var(--cyan); }
  .stat-label { font-size:10px; letter-spacing:2px; text-transform:uppercase; color:var(--dim); margin-top:6px; }

  /* ── STACK ── */
  .stack-grid { display:grid; grid-template-columns:repeat(auto-fill,minmax(260px,1fr)); gap:16px; }
  .stack-card {
    border:1px solid var(--border);
    border-radius:8px;
    padding:20px;
    background: var(--card);
    transition: all 0.3s ease;
    position:relative; overflow:hidden;
  }
  .stack-card::after {
    content:'';
    position:absolute; top:0; left:0; right:0; height:2px;
    background: linear-gradient(90deg, var(--blue), var(--cyan));
    transform: scaleX(0);
    transform-origin: left;
    transition: transform 0.3s ease;
  }
  .stack-card:hover { transform:translateY(-4px); border-color:rgba(0,87,255,0.5); box-shadow:0 16px 40px rgba(0,87,255,0.12); }
  .stack-card:hover::after { transform:scaleX(1); }
  .stack-icon { font-size:22px; margin-bottom:10px; }
  .stack-title { font-size:10px; letter-spacing:2px; text-transform:uppercase; color:var(--blue); margin-bottom:12px; font-family:'Share Tech Mono',monospace; }
  .stack-tags { display:flex; flex-wrap:wrap; gap:6px; }
  .tag {
    font-size:10px; padding:3px 9px; border-radius:4px;
    border:1px solid rgba(0,87,255,0.2);
    color:var(--text);
    background: rgba(0,87,255,0.06);
    transition: all 0.2s;
  }
  .tag:hover { border-color:var(--cyan); color:var(--cyan); background:rgba(0,240,255,0.08); }

  /* ── PROJECTS ── */
  .projects-grid { display:grid; gap:20px; }
  .project-card {
    border:1px solid var(--border);
    border-radius:12px;
    padding:28px;
    background: var(--card);
    transition: all 0.35s ease;
    position:relative; overflow:hidden;
    display:grid; grid-template-columns:1fr auto;
    gap:16px;
  }
  .project-card::before {
    content:'';
    position:absolute; inset:0;
    background: linear-gradient(135deg, rgba(0,87,255,0.05) 0%, transparent 60%);
    opacity:0; transition:opacity 0.35s;
  }
  .project-card:hover { transform:translateY(-6px); border-color:rgba(0,87,255,0.6); box-shadow:0 24px 60px rgba(0,87,255,0.15); }
  .project-card:hover::before { opacity:1; }
  .project-accent {
    position:absolute; top:0; left:0; bottom:0; width:3px;
    background: linear-gradient(180deg, var(--blue), var(--cyan));
    border-radius:12px 0 0 12px;
    transform: scaleY(0); transform-origin:top;
    transition:transform 0.35s ease;
  }
  .project-card:hover .project-accent { transform:scaleY(1); }
  .project-number { font-family:'Share Tech Mono',monospace; font-size:10px; color:var(--dim); margin-bottom:8px; letter-spacing:2px; }
  .project-title { font-family:'Syne',sans-serif; font-weight:800; font-size:22px; color:#fff; margin-bottom:8px; }
  .project-desc { font-size:12px; color:var(--dim); line-height:1.8; margin-bottom:16px; }
  .project-metrics { display:flex; gap:20px; margin-bottom:16px; }
  .metric { display:flex; align-items:center; gap:6px; font-size:11px; }
  .metric-val { font-family:'Syne',sans-serif; font-weight:800; font-size:20px; color:var(--cyan); }
  .metric-label { color:var(--dim); font-size:10px; }
  .project-stack { display:flex; flex-wrap:wrap; gap:6px; }
  .project-link {
    align-self:start;
    width:36px; height:36px;
    border:1px solid var(--border);
    border-radius:8px;
    display:flex; align-items:center; justify-content:center;
    font-size:16px;
    transition:all 0.2s;
    text-decoration:none;
    flex-shrink:0;
  }
  .project-link:hover { border-color:var(--cyan); background:rgba(0,240,255,0.08); transform:scale(1.1); }

  /* ── EXPERIENCE ── */
  .exp-list { display:grid; gap:14px; }
  .exp-card {
    border:1px solid var(--border);
    border-radius:8px;
    padding:20px 24px;
    background:var(--card);
    display:grid; grid-template-columns:auto 1fr auto;
    align-items:center; gap:20px;
    transition:all 0.3s ease;
  }
  .exp-card:hover { border-color:rgba(0,87,255,0.5); transform:translateX(6px); box-shadow:0 8px 32px rgba(0,87,255,0.1); }
  .exp-icon { font-size:22px; width:44px; height:44px; border:1px solid var(--border); border-radius:8px; display:flex; align-items:center; justify-content:center; }
  .exp-role { font-family:'Syne',sans-serif; font-weight:700; font-size:14px; color:#fff; }
  .exp-company { font-size:11px; color:var(--blue); margin-top:3px; letter-spacing:1px; }
  .exp-year { font-family:'Share Tech Mono',monospace; font-size:11px; color:var(--dim); }

  /* ── CONNECT ── */
  .connect-grid { display:grid; grid-template-columns:repeat(auto-fill,minmax(200px,1fr)); gap:14px; }
  .connect-card {
    border:1px solid var(--border);
    border-radius:8px;
    padding:20px;
    text-align:center;
    text-decoration:none;
    background:var(--card);
    transition:all 0.3s ease;
    display:block;
  }
  .connect-card:hover { transform:translateY(-6px); }
  .connect-card.blue:hover  { border-color:var(--blue);  box-shadow:0 16px 40px rgba(0,87,255,0.2); }
  .connect-card.cyan:hover  { border-color:var(--cyan);  box-shadow:0 16px 40px rgba(0,240,255,0.15); }
  .connect-card.green:hover { border-color:var(--green); box-shadow:0 16px 40px rgba(0,255,136,0.15); }
  .connect-icon { font-size:28px; margin-bottom:10px; display:block; }
  .connect-label { font-size:10px; letter-spacing:2px; text-transform:uppercase; color:var(--dim); margin-bottom:4px; font-family:'Share Tech Mono',monospace; }
  .connect-val { font-size:12px; color:var(--text); }

  /* ── FOOTER ── */
  .footer {
    text-align:center; margin-top:80px; padding-top:40px;
    border-top:1px solid var(--border);
  }
  .footer-quote {
    font-family:'Syne',sans-serif;
    font-weight:700;
    font-size:clamp(16px,3vw,24px);
    color:#fff;
    line-height:1.5;
    margin-bottom:20px;
  }
  .footer-quote em { font-style:normal; color:var(--blue); }
  .footer-sub { font-size:11px; color:var(--dim); letter-spacing:2px; }

  /* Divider */
  .divider { height:1px; background:linear-gradient(90deg,transparent,var(--border),transparent); margin:60px 0 0; }

  /* Animations on scroll */
  .reveal { opacity:0; transform:translateY(24px); transition:all 0.7s ease; }
  .reveal.visible { opacity:1; transform:translateY(0); }

  @media(max-width:600px) {
    .stats-row { grid-template-columns:1fr 1fr; }
    .project-card { grid-template-columns:1fr; }
    .exp-card { grid-template-columns:auto 1fr; }
    .exp-year { grid-column:2; }
  }
</style>
</head>
<body>

<div class="cursor" id="cur"></div>
<div class="cursor-ring" id="ring"></div>

<div class="orb orb1"></div>
<div class="orb orb2"></div>
<div class="orb orb3"></div>

<div class="wrapper">

  <!-- HERO -->
  <div class="hero">
    <div class="status-pill"><span class="status-dot"></span> &gt; AVAILABLE FOR OPPORTUNITIES</div>

    <div class="name-block">
      <span class="name-first">Rajeev</span>
      <span class="name-last">Gandhi <span class="name-k">K</span></span>
    </div>

    <p class="tagline">~/developer $ <span>Cloud</span> • <span>AI</span> • <span>Full-Stack</span></p>

    <div class="terminal-bio">
      <div><span class="prompt">~/portfolio $</span> <span class="cmd">whoami</span></div>
      <div class="out">Rajeev Gandhi K — CS Undergrad | Chennai, India</div>
      <br/>
      <div><span class="prompt">~/portfolio $</span> <span class="cmd">cat about.txt</span></div>
      <div class="out">Specializing in Java, Python &amp; SQL.</div>
      <div class="out">Cloud + AI + Full-Stack Systems builder.</div>
      <div class="out">3 internships · 6+ projects · 8+ tech skills.</div>
      <br/>
      <div><span class="prompt">~/portfolio $</span> <span class="cursor-blink"></span></div>
    </div>

    <div class="badges">
      <a class="badge badge-blue" href="https://rajeevgandhi-portfolio.vercel.app/" target="_blank">⚡ Portfolio</a>
      <a class="badge badge-cyan" href="https://linkedin.com/in/rajeev-gandhi-9bb516351" target="_blank">🔗 LinkedIn</a>
      <a class="badge badge-red" href="mailto:rajeevgandhi.exe@gmail.com">📧 Hire Me</a>
      <a class="badge badge-green" href="#">✅ Open to Work</a>
    </div>
  </div>

  <!-- STATS -->
  <div class="section reveal">
    <div class="stats-row">
      <div class="stat-card">
        <div class="stat-num">6<span>+</span></div>
        <div class="stat-label">Projects Shipped</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">3</div>
        <div class="stat-label">Internships</div>
      </div>
      <div class="stat-card">
        <div class="stat-num">8<span>+</span></div>
        <div class="stat-label">Tech Skills</div>
      </div>
    </div>
  </div>

  <!-- STACK -->
  <div class="section reveal">
    <div class="section-header">
      <span class="section-label">~/stack</span>
      <div class="section-line"></div>
      <span class="section-num">02</span>
    </div>
    <div class="stack-grid">
      <div class="stack-card">
        <div class="stack-icon">👨‍💻</div>
        <div class="stack-title">Languages</div>
        <div class="stack-tags">
          <span class="tag">Java</span><span class="tag">Python</span><span class="tag">SQL</span><span class="tag">JavaScript</span><span class="tag">C++</span>
        </div>
      </div>
      <div class="stack-card">
        <div class="stack-icon">🌐</div>
        <div class="stack-title">Frontend</div>
        <div class="stack-tags">
          <span class="tag">React.js</span><span class="tag">HTML5</span><span class="tag">CSS3</span>
        </div>
      </div>
      <div class="stack-card">
        <div class="stack-icon">🔙</div>
        <div class="stack-title">Backend & APIs</div>
        <div class="stack-tags">
          <span class="tag">Node.js</span><span class="tag">REST APIs</span><span class="tag">JDBC</span>
        </div>
      </div>
      <div class="stack-card">
        <div class="stack-icon">☁️</div>
        <div class="stack-title">Cloud & DevOps</div>
        <div class="stack-tags">
          <span class="tag">AWS EC2</span><span class="tag">AWS S3</span><span class="tag">Lambda</span><span class="tag">IAM</span><span class="tag">Docker</span><span class="tag">Git</span>
        </div>
      </div>
      <div class="stack-card">
        <div class="stack-icon">🤖</div>
        <div class="stack-title">AI / ML</div>
        <div class="stack-tags">
          <span class="tag">YOLO</span><span class="tag">OpenCV</span><span class="tag">BERT</span><span class="tag">NLP</span><span class="tag">TensorFlow</span><span class="tag">Streamlit</span>
        </div>
      </div>
      <div class="stack-card">
        <div class="stack-icon">🗄️</div>
        <div class="stack-title">Databases</div>
        <div class="stack-tags">
          <span class="tag">MySQL</span><span class="tag">JDBC</span>
        </div>
      </div>
    </div>
  </div>

  <!-- PROJECTS -->
  <div class="section reveal">
    <div class="section-header">
      <span class="section-label">~/featured-projects</span>
      <div class="section-line"></div>
      <span class="section-num">03</span>
    </div>
    <div class="projects-grid">

      <div class="project-card">
        <div class="project-accent"></div>
        <div>
          <div class="project-number">PROJECT_01 / JOB-BRIDGE-ML</div>
          <div class="project-title">JobBridge — Skill Gap Analyzer</div>
          <div class="project-desc">NLP-powered platform that semantically matches resumes to job descriptions using BERT transformers. Identifies missing skills, suggests learning paths, and provides match scores in real-time.</div>
          <div class="project-metrics">
            <div class="metric"><div class="metric-val">96%</div><div class="metric-label">Accuracy</div></div>
            <div class="metric"><div class="metric-val">BERT</div><div class="metric-label">Model</div></div>
          </div>
          <div class="project-stack">
            <span class="tag">Python</span><span class="tag">Streamlit</span><span class="tag">NLP</span><span class="tag">BERT</span><span class="tag">ML</span>
          </div>
        </div>
        <a class="project-link" href="https://github.com/rajeev-exe/Job-Bridge-ML" target="_blank">↗</a>
      </div>

      <div class="project-card">
        <div class="project-accent"></div>
        <div>
          <div class="project-number">PROJECT_02 / CLOUD-SECURITY-PLATFORM</div>
          <div class="project-title">Cloud Security Platform</div>
          <div class="project-desc">Cloud infrastructure vulnerability analysis and monitoring platform. Automated security checks, IAM policy auditing, and real-time threat detection across AWS services.</div>
          <div class="project-metrics">
            <div class="metric"><div class="metric-val">AWS</div><div class="metric-label">Cloud</div></div>
            <div class="metric"><div class="metric-val">IAM</div><div class="metric-label">Security</div></div>
          </div>
          <div class="project-stack">
            <span class="tag">AWS</span><span class="tag">Docker</span><span class="tag">Node.js</span><span class="tag">JavaScript</span>
          </div>
        </div>
        <a class="project-link" href="https://github.com/rajeev-exe/Cloud-Security-Platform" target="_blank">↗</a>
      </div>

      <div class="project-card">
        <div class="project-accent"></div>
        <div>
          <div class="project-number">PROJECT_03 / EYE-GESTURE-ARM</div>
          <div class="project-title">Eye-Gesture Robotic Arm</div>
          <div class="project-desc">Real-time eye gaze tracking system that translates eye movements into robotic arm commands. Enables hands-free hardware control using computer vision — designed for accessibility applications.</div>
          <div class="project-metrics">
            <div class="metric"><div class="metric-val">95%</div><div class="metric-label">Gaze Accuracy</div></div>
            <div class="metric"><div class="metric-val">RPi</div><div class="metric-label">Hardware</div></div>
          </div>
          <div class="project-stack">
            <span class="tag">Python</span><span class="tag">OpenCV</span><span class="tag">Raspberry Pi</span><span class="tag">ESP32-CAM</span>
          </div>
        </div>
        <div class="project-link">🔒</div>
      </div>

      <div class="project-card">
        <div class="project-accent"></div>
        <div>
          <div class="project-number">PROJECT_04 / DEFECT-FORGE</div>
          <div class="project-title">Defect Forge — Engine QC System</div>
          <div class="project-desc">YOLO-based manufacturing defect detection system for engine components. Real-time visual inspection pipeline with a Tkinter GUI, reducing manual QC time significantly in industrial settings.</div>
          <div class="project-metrics">
            <div class="metric"><div class="metric-val">92%</div><div class="metric-label">Precision</div></div>
            <div class="metric"><div class="metric-val">YOLO</div><div class="metric-label">Model</div></div>
          </div>
          <div class="project-stack">
            <span class="tag">Python</span><span class="tag">YOLO</span><span class="tag">OpenCV</span><span class="tag">Tkinter</span>
          </div>
        </div>
        <div class="project-link">🔒</div>
      </div>

    </div>
  </div>

  <!-- EXPERIENCE -->
  <div class="section reveal">
    <div class="section-header">
      <span class="section-label">~/experience</span>
      <div class="section-line"></div>
      <span class="section-num">04</span>
    </div>
    <div class="exp-list">
      <div class="exp-card">
        <div class="exp-icon">🔐</div>
        <div>
          <div class="exp-role">Cyber Security Intern</div>
          <div class="exp-company">NSIC — GOVERNMENT OF INDIA</div>
        </div>
        <div class="exp-year">2024</div>
      </div>
      <div class="exp-card">
        <div class="exp-icon">☁️</div>
        <div>
          <div class="exp-role">Cloud Computing Intern</div>
          <div class="exp-company">DLK TECHNOLOGIES</div>
        </div>
        <div class="exp-year">2024</div>
      </div>
      <div class="exp-card">
        <div class="exp-icon">🌐</div>
        <div>
          <div class="exp-role">Web App Development Intern</div>
          <div class="exp-company">ROBOWAVES</div>
        </div>
        <div class="exp-year">2024</div>
      </div>
    </div>
  </div>

  <!-- CONNECT -->
  <div class="section reveal">
    <div class="section-header">
      <span class="section-label">~/connect</span>
      <div class="section-line"></div>
      <span class="section-num">05</span>
    </div>
    <div class="connect-grid">
      <a class="connect-card blue" href="https://rajeevgandhi-portfolio.vercel.app/" target="_blank">
        <span class="connect-icon">⚡</span>
        <div class="connect-label">Portfolio</div>
        <div class="connect-val">rajeevgandhi-portfolio.vercel.app</div>
      </a>
      <a class="connect-card cyan" href="https://linkedin.com/in/rajeev-gandhi-9bb516351" target="_blank">
        <span class="connect-icon">🔗</span>
        <div class="connect-label">LinkedIn</div>
        <div class="connect-val">rajeev-gandhi-9bb516351</div>
      </a>
      <a class="connect-card green" href="mailto:rajeevgandhi.exe@gmail.com">
        <span class="connect-icon">📧</span>
        <div class="connect-label">Email</div>
        <div class="connect-val">rajeevgandhi.exe@gmail.com</div>
      </a>
    </div>
  </div>

  <div class="divider"></div>

  <!-- FOOTER -->
  <div class="footer reveal">
    <div class="footer-quote">
      "Building <em>scalable systems.</em><br/>
      Solving <em>real-world problems.</em><br/>
      Shipping <em>impact.</em>"
    </div>
    <div class="footer-sub">RAJEEV GANDHI K · CHENNAI, INDIA · 2025</div>
  </div>

</div>

<script>
  // Custom cursor
  const cur = document.getElementById('cur');
  const ring = document.getElementById('ring');
  let mx=0,my=0,rx=0,ry=0;
  document.addEventListener('mousemove', e => { mx=e.clientX; my=e.clientY; cur.style.left=mx-6+'px'; cur.style.top=my-6+'px'; });
  function animRing(){ rx+=(mx-rx)*0.12; ry+=(my-ry)*0.12; ring.style.left=rx-18+'px'; ring.style.top=ry-18+'px'; requestAnimationFrame(animRing); }
  animRing();
  document.querySelectorAll('a,.stat-card,.stack-card,.project-card,.exp-card,.connect-card,.badge').forEach(el=>{
    el.addEventListener('mouseenter',()=>{ cur.style.transform='scale(2)'; ring.style.transform='scale(1.5)'; });
    el.addEventListener('mouseleave',()=>{ cur.style.transform='scale(1)'; ring.style.transform='scale(1)'; });
  });

  // Scroll reveal
  const obs = new IntersectionObserver(entries=>{
    entries.forEach(e=>{ if(e.isIntersecting) e.target.classList.add('visible'); });
  },{threshold:0.1});
  document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));

  // Typing effect
  const phrases = ['Cloud Engineer','AI Developer','Full-Stack Dev','CS Undergrad'];
  let pi=0, ci=0, del=false;
  const typed = document.querySelector('.cmd');
  if(typed) {
    function type(){
      const phrase = 'cat about.txt';
      typed.textContent = phrase;
    }
    type();
  }
</script>
</body>
</html>
