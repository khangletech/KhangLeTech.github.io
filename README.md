<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <meta name="description" content="Portfolio page" />
  <title>Khang Le | Portfolio</title>

  <style>
    :root{
      --bg: #0b0f17;
      --panel: rgba(255,255,255,.06);
      --panel2: rgba(255,255,255,.09);
      --text: rgba(255,255,255,.92);
      --muted: rgba(255,255,255,.68);
      --border: rgba(255,255,255,.12);
      --shadow: 0 20px 60px rgba(0,0,0,.35);
      --accent: #6ee7ff;
      --accent2:#a78bfa;
      --chip: rgba(110,231,255,.12);
      --focus: 0 0 0 4px rgba(110,231,255,.18);
      --radius: 18px;
      --max: 1050px;
    }

    /* Light mode tokens (toggled by JS) */
    [data-theme="light"]{
      --bg: #f7f7fb;
      --panel: rgba(0,0,0,.04);
      --panel2: rgba(0,0,0,.06);
      --text: rgba(0,0,0,.86);
      --muted: rgba(0,0,0,.58);
      --border: rgba(0,0,0,.10);
      --shadow: 0 20px 60px rgba(0,0,0,.10);
      --chip: rgba(10,88,202,.10);
    }

    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji";
      background: radial-gradient(1200px 700px at 20% 10%, rgba(110,231,255,.18), transparent 55%),
                  radial-gradient(900px 600px at 90% 15%, rgba(167,139,250,.20), transparent 60%),
                  radial-gradient(900px 600px at 55% 95%, rgba(110,231,255,.10), transparent 55%),
                  var(--bg);
      color: var(--text);
      overflow-x:hidden;
    }

    a{color:inherit; text-decoration:none}
    a:hover{opacity:.92}
    .wrap{max-width: var(--max); margin:0 auto; padding: 24px}

    /* Top nav */
    .nav{
      position: sticky; top:0; z-index: 50;
      backdrop-filter: blur(12px);
      background: linear-gradient(to bottom, rgba(0,0,0,.22), transparent);
      border-bottom: 1px solid rgba(255,255,255,.06);
    }
    [data-theme="light"] .nav{
      background: linear-gradient(to bottom, rgba(255,255,255,.65), transparent);
      border-bottom: 1px solid rgba(0,0,0,.06);
    }
    .nav-inner{
      display:flex; align-items:center; justify-content:space-between;
      gap:14px;
      max-width: var(--max);
      margin:0 auto;
      padding: 14px 24px;
    }
    .brand{
      display:flex; align-items:center; gap:10px;
      font-weight: 700;
      letter-spacing: .2px;
    }
    .dot{
      width:11px; height:11px; border-radius:999px;
      background: linear-gradient(135deg, var(--accent), var(--accent2));
      box-shadow: 0 0 0 4px rgba(110,231,255,.12);
    }
    .nav-links{
      display:flex; align-items:center; gap: 14px;
      font-size: 14px;
      color: var(--muted);
    }
    .nav-links a{padding:8px 10px; border-radius: 999px}
    .nav-links a:hover{background: var(--panel)}
    .nav-actions{display:flex; gap:10px; align-items:center}

    .btn{
      display:inline-flex; align-items:center; justify-content:center;
      gap:10px;
      padding: 10px 12px;
      border-radius: 999px;
      border: 1px solid var(--border);
      background: var(--panel);
      color: var(--text);
      box-shadow: none;
      cursor:pointer;
      font-weight: 600;
      font-size: 14px;
    }
    .btn:hover{background: var(--panel2)}
    .btn:focus{outline:none; box-shadow: var(--focus)}
    .btn.primary{
      border: 1px solid rgba(110,231,255,.35);
      background: linear-gradient(135deg, rgba(110,231,255,.14), rgba(167,139,250,.14));
    }

    /* Hero */
    .hero{padding: 38px 0 8px}
    .hero-grid{
      display:grid;
      grid-template-columns: 1.3fr .7fr;
      gap: 18px;
      align-items: stretch;
    }
    @media (max-width: 900px){
      .hero-grid{grid-template-columns: 1fr}
      .nav-links{display:none}
    }

    .card{
      border: 1px solid var(--border);
      background: linear-gradient(180deg, rgba(255,255,255,.06), rgba(255,255,255,.03));
      border-radius: var(--radius);
      box-shadow: var(--shadow);
    }
    [data-theme="light"] .card{
      background: linear-gradient(180deg, rgba(255,255,255,.9), rgba(255,255,255,.8));
    }

    .hero-main{padding: 22px 22px 18px}
    .eyebrow{
      display:inline-flex; align-items:center; gap:10px;
      font-size: 13px; color: var(--muted);
      padding: 8px 12px;
      border: 1px solid var(--border);
      border-radius: 999px;
      background: var(--panel);
      width: fit-content;
    }
    .h1{
      margin: 14px 0 8px;
      font-size: clamp(32px, 4vw, 48px);
      line-height: 1.05;
      letter-spacing: -0.7px;
    }
    .lead{
      margin: 0 0 16px;
      color: var(--muted);
      max-width: 62ch;
      font-size: 16px;
      line-height: 1.6;
    }
    .hero-cta{display:flex; gap:10px; flex-wrap: wrap}

    /* Side panel */
    .hero-side{padding: 18px}
    .stat{
      padding: 14px;
      border-radius: 14px;
      border: 1px solid var(--border);
      background: var(--panel);
      margin-bottom: 12px;
    }
    .stat h3{margin:0 0 6px; font-size: 14px}
    .stat p{margin:0; color: var(--muted); font-size: 14px; line-height:1.5}

    .chips{display:flex; flex-wrap:wrap; gap:8px; margin-top: 10px}
    .chip{
      padding: 7px 10px;
      border-radius: 999px;
      border: 1px solid var(--border);
      background: var(--chip);
      font-size: 12.5px;
      color: var(--text);
    }

    /* Sections */
    section{padding: 22px 0}
    .section-title{
      display:flex; align-items:end; justify-content:space-between;
      gap: 14px;
      margin-bottom: 12px;
    }
    .section-title h2{
      margin:0;
      font-size: 18px;
      letter-spacing: -.2px;
    }
    .section-title p{
      margin:0;
      color: var(--muted);
      font-size: 14px;
    }

    .grid{
      display:grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 14px;
    }
    @media (max-width: 980px){ .grid{grid-template-columns: repeat(2, 1fr);} }
    @media (max-width: 620px){ .grid{grid-template-columns: 1fr;} }

    .project{
      padding: 16px;
      border-radius: var(--radius);
      border: 1px solid var(--border);
      background: var(--panel);
      transition: transform .15s ease, background .15s ease;
      display:flex; flex-direction:column; gap: 10px;
      min-height: 170px;
    }
    .project:hover{transform: translateY(-2px); background: var(--panel2)}
    .project h3{margin:0; font-size: 15px}
    .project p{margin:0; color: var(--muted); font-size: 14px; line-height:1.55}
    .project .meta{display:flex; flex-wrap:wrap; gap:8px; margin-top:auto}
    .tag{
      font-size: 12px;
      padding: 6px 10px;
      border: 1px solid var(--border);
      border-radius: 999px;
      color: var(--muted);
      background: rgba(255,255,255,.03);
    }
    [data-theme="light"] .tag{background: rgba(0,0,0,.03);}

    /* Footer */
    footer{
      padding: 26px 0 34px;
      color: var(--muted);
      font-size: 13px;
      text-align:center;
    }

    /* Smooth anchor offset for sticky nav */
    [id]{scroll-margin-top: 90px;}

    /* Small helper */
    .muted{color: var(--muted)}
  </style>
</head>

<body>
  <div class="nav">
    <div class="nav-inner">
      <div class="brand">
        <div class="dot" aria-hidden="true"></div>
        <span>Khang Le</span>
      </div>

      <div class="nav-links" role="navigation" aria-label="Primary">
        <a href="#projects">Projects</a>
        <a href="#skills">Skills</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
      </div>

      <div class="nav-actions">
        <button class="btn" id="themeBtn" type="button" aria-label="Toggle theme">🌙 Theme</button>
        <a class="btn primary" href="#contact">Get in touch</a>
      </div>
    </div>
  </div>

  <main class="wrap">
    <!-- HERO -->
    <div class="hero">
      <div class="hero-grid">
        <div class="card hero-main">
          <div class="eyebrow">IT Support • Networking • Troubleshooting</div>
          <h1 class="h1">Portfolio & Projects</h1>
          <p class="lead">
            Hi — I’m <strong>Khang Le</strong>. I build practical IT + networking projects and document them clearly.
            Below are highlights from school and hands-on work.
          </p>

          <div class="hero-cta">
            <a class="btn primary" href="#projects">View Projects</a>
            <a class="btn" href="https://github.com/" target="_blank" rel="noreferrer">GitHub</a>
            <a class="btn" href="#" title="Upload your resume PDF and link it here">Resume (PDF)</a>
          </div>
        </div>

        <div class="card hero-side">
          <div class="stat">
            <h3>Quick info</h3>
            <p><strong>Location:</strong> Toronto, Canada</p>
            <p><strong>Focus:</strong> Help Desk • Networking • Customer support</p>
          </div>

          <div class="stat">
            <h3>Certifications</h3>
            <p>CompTIA A+</p>
            <p>CompTIA Network+</p>
          </div>

          <div class="stat">
            <h3>Tech I use</h3>
            <div class="chips">
              <span class="chip">Windows</span>
              <span class="chip">Linux</span>
              <span class="chip">TCP/IP</span>
              <span class="chip">DNS/DHCP</span>
              <span class="chip">Wireshark</span>
              <span class="chip">PowerShell</span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- PROJECTS -->
    <section id="projects">
      <div class="section-title">
        <div>
          <h2>Featured Projects</h2>
          <p>Replace these with your real school projects + repo links.</p>
        </div>
        <p class="muted">Tip: keep each description 1–2 lines</p>
      </div>

      <div class="grid">
        <a class="project" href="#" target="_blank" rel="noreferrer">
          <h3>Active Directory Lab (School)</h3>
          <p>Built a small Windows Server domain, created users/groups, and applied GPOs for policy enforcement.</p>
          <div class="meta">
            <span class="tag">Windows Server</span>
            <span class="tag">AD DS</span>
            <span class="tag">GPO</span>
          </div>
        </a>

        <a class="project" href="#" target="_blank" rel="noreferrer">
          <h3>Network Troubleshooting Pack</h3>
          <p>Packet captures + notes diagnosing DNS issues, latency, and connectivity using repeatable steps.</p>
          <div class="meta">
            <span class="tag">Wireshark</span>
            <span class="tag">DNS</span>
            <span class="tag">TCP/IP</span>
          </div>
        </a>

        <a class="project" href="#" target="_blank" rel="noreferrer">
          <h3>Automation Script</h3>
          <p>PowerShell script to collect system info, export logs, and generate a support-friendly report.</p>
          <div class="meta">
            <span class="tag">PowerShell</span>
            <span class="tag">Windows</span>
            <span class="tag">Automation</span>
          </div>
        </a>

        <a class="project" href="#" target="_blank" rel="noreferrer">
          <h3>Ticketing Workflow Notes</h3>
          <p>Documented triage steps and resolution templates to improve consistency and reduce repeat issues.</p>
          <div class="meta">
            <span class="tag">Help Desk</span>
            <span class="tag">Documentation</span>
          </div>
        </a>

        <a class="project" href="#" target="_blank" rel="noreferrer">
          <h3>Linux Services Mini-Lab</h3>
          <p>Configured users, permissions, SSH hardening, and basic monitoring with clear setup instructions.</p>
          <div class="meta">
            <span class="tag">Linux</span>
            <span class="tag">SSH</span>
            <span class="tag">Security</span>
          </div>
        </a>

        <a class="project" href="#" target="_blank" rel="noreferrer">
          <h3>Home Network Upgrade</h3>
          <p>Designed a simple network layout and tuned Wi-Fi for stability; documented before/after results.</p>
          <div class="meta">
            <span class="tag">Networking</span>
            <span class="tag">Wi-Fi</span>
          </div>
        </a>
      </div>
    </section>

    <!-- SKILLS -->
    <section id="skills">
      <div class="section-title">
        <div>
          <h2>Skills</h2>
          <p>Keep this aligned with the jobs you’re applying for.</p>
        </div>
      </div>

      <div class="grid">
        <div class="project" role="article">
          <h3>IT Support</h3>
          <p>Hardware/software troubleshooting, escalation, documentation, customer communication.</p>
          <div class="meta">
            <span class="tag">Ticketing</span>
            <span class="tag">User Support</span>
            <span class="tag">SLA mindset</span>
          </div>
        </div>

        <div class="project" role="article">
          <h3>Networking</h3>
          <p>TCP/IP fundamentals, subnetting basics, DNS/DHCP, Wi-Fi troubleshooting, packet analysis.</p>
          <div class="meta">
            <span class="tag">TCP/IP</span>
            <span class="tag">DNS</span>
            <span class="tag">Wireshark</span>
          </div>
        </div>

        <div class="project" role="article">
          <h3>Systems</h3>
          <p>Windows & Linux basics, permissions, scripting/automation for repeatable support tasks.</p>
          <div class="meta">
            <span class="tag">Windows</span>
            <span class="tag">Linux</span>
            <span class="tag">PowerShell</span>
          </div>
        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about">
      <div class="section-title">
        <div>
          <h2>About</h2>
          <p>Short and practical beats long and vague.</p>
        </div>
      </div>

      <div class="card" style="padding:18px">
        <p style="margin:0; color:var(--muted); line-height:1.7">
          I’m an IT support / help desk focused professional with CompTIA A+ and Network+.
          I like building labs, documenting steps clearly, and solving real user problems.
          <br><br>
          <span class="muted">Replace this paragraph with 3–5 sentences from your resume (education + experience + what you want next).</span>
        </p>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact">
      <div class="section-title">
        <div>
          <h2>Contact</h2>
          <p>Add your real links here.</p>
        </div>
      </div>

      <div class="grid">
        <a class="project" href="mailto:you@example.com">
          <h3>Email</h3>
          <p>you@example.com</p>
          <div class="meta"><span class="tag">mailto</span></div>
        </a>
        <a class="project" href="#" target="_blank" rel="noreferrer">
          <h3>LinkedIn</h3>
          <p>linkedin.com/in/your-handle</p>
          <div class="meta"><span class="tag">profile</span></div>
        </a>
        <a class="project" href="https://github.com/" target="_blank" rel="noreferrer">
          <h3>GitHub</h3>
          <p>github.com/your-username</p>
          <div class="meta"><span class="tag">repos</span></div>
        </a>
      </div>
    </section>

    <footer>
      <div>© <span id="year"></span> Khang Le • Built with plain HTML/CSS • Hosted on GitHub Pages</div>
    </footer>
  </main>

  <script>
    // Theme toggle with localStorage
    const root = document.documentElement;
    const btn = document.getElementById("themeBtn");

    const saved = localStorage.getItem("theme");
    if (saved) root.setAttribute("data-theme", saved);

    function label(){
      const t = root.getAttribute("data-theme") || "dark";
      btn.textContent = (t === "light") ? "☀️ Theme" : "🌙 Theme";
    }
    label();

    btn.addEventListener("click", () => {
      const t = root.getAttribute("data-theme") || "dark";
      const next = (t === "light") ? "dark" : "light";
      root.setAttribute("data-theme", next);
      localStorage.setItem("theme", next);
      label();
    });

    // Footer year
    document.getElementById("year").textContent = new Date().getFullYear();
  </script>
</body>
</html>
