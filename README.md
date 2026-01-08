<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Khang Le | Cybersecurity • Networking • IT Technician</title>
  <meta name="description" content="Cybersecurity student portfolio: SOC/Blue Team, Networking, IT Technician. Projects in AD attack simulation, AWS IoT monitoring, penetration testing, and secure network design." />

  <style>
    :root{
      --bg:#0b1020;
      --panel:#0f1733;
      --panel2:#0c132b;
      --text:#e7ecff;
      --muted:#b9c2e6;
      --line:rgba(231,236,255,.12);
      --accent:#7aa2ff;
      --accent2:#7df0d6;
      --shadow: 0 10px 30px rgba(0,0,0,.35);
      --radius:18px;
      --max:1080px;
      --mono: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
      --sans: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji","Segoe UI Emoji";
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:var(--sans);
      color:var(--text);
      background:
        radial-gradient(900px 600px at 10% -10%, rgba(122,162,255,.25), transparent 60%),
        radial-gradient(700px 500px at 90% 0%, rgba(125,240,214,.18), transparent 55%),
        radial-gradient(900px 700px at 50% 120%, rgba(122,162,255,.12), transparent 60%),
        var(--bg);
      line-height:1.55;
    }
    a{color:inherit}
    .wrap{max-width:var(--max); margin:0 auto; padding:26px 18px 60px}
    .nav{
      position:sticky; top:0; z-index:10;
      backdrop-filter: blur(10px);
      background: linear-gradient(to bottom, rgba(11,16,32,.85), rgba(11,16,32,.45));
      border-bottom:1px solid var(--line);
    }
    .nav .inner{max-width:var(--max); margin:0 auto; display:flex; gap:14px; align-items:center; justify-content:space-between; padding:14px 18px}
    .brand{display:flex; gap:10px; align-items:center; text-decoration:none}
    .dot{
      width:12px; height:12px; border-radius:50%;
      background: linear-gradient(135deg, var(--accent), var(--accent2));
      box-shadow:0 0 0 6px rgba(122,162,255,.12);
    }
    .brand b{letter-spacing:.2px}
    .links{display:flex; gap:10px; flex-wrap:wrap; justify-content:flex-end}
    .pill{
      text-decoration:none;
      font-size:14px;
      padding:8px 12px;
      border:1px solid var(--line);
      border-radius:999px;
      background: rgba(15,23,51,.35);
      transition: transform .15s ease, border-color .15s ease, background .15s ease;
    }
    .pill:hover{transform: translateY(-1px); border-color: rgba(122,162,255,.45); background: rgba(15,23,51,.55)}
    .hero{
      margin-top:22px;
      border:1px solid var(--line);
      background: linear-gradient(180deg, rgba(15,23,51,.72), rgba(12,19,43,.52));
      border-radius:var(--radius);
      padding:26px;
      box-shadow: var(--shadow);
      overflow:hidden;
      position:relative;
    }
    .hero:before{
      content:"";
      position:absolute; inset:-2px;
      background: radial-gradient(400px 200px at 10% 20%, rgba(122,162,255,.22), transparent 55%),
                  radial-gradient(420px 220px at 85% 25%, rgba(125,240,214,.14), transparent 60%);
      pointer-events:none;
    }
    .hero .grid{display:grid; grid-template-columns: 1.35fr .65fr; gap:18px; position:relative}

    /* === PHOTO AREA (Put your image at /assets/profile.jpg) === */
    .profile{
      display:flex;
      align-items:center;
      gap:18px;
      margin-bottom: 10px;
    }
    .avatar{
      width:120px;
      height:120px;
      border-radius:50%;
      object-fit:cover;
      border: 2px solid rgba(122,162,255,.5);
      box-shadow: 0 0 0 6px rgba(122,162,255,.15);
      background: rgba(15,23,51,.5);
    }

    h1{margin:0 0 6px; font-size:34px; letter-spacing:.2px}
    .sub{margin:0; color:var(--muted)}
    .badges{display:flex; gap:8px; flex-wrap:wrap; margin-top:14px}
    .badge{
      font-family:var(--mono);
      font-size:12px;
      padding:7px 10px;
      border-radius:999px;
      border:1px solid var(--line);
      background: rgba(12,19,43,.35);
      color: var(--muted);
    }
    .cta{display:flex; gap:10px; flex-wrap:wrap; margin-top:16px}
    .btn{
      text-decoration:none;
      display:inline-flex; align-items:center; gap:8px;
      padding:10px 12px;
      border-radius:12px;
      border:1px solid var(--line);
      background: rgba(15,23,51,.45);
      transition: transform .15s ease, border-color .15s ease;
      font-weight:600;
    }
    .btn:hover{transform: translateY(-1px); border-color: rgba(125,240,214,.5)}
    .btn.primary{
      background: linear-gradient(135deg, rgba(122,162,255,.22), rgba(125,240,214,.14));
      border-color: rgba(122,162,255,.45);
    }
    .card{
      border:1px solid var(--line);
      background: rgba(15,23,51,.35);
      border-radius:var(--radius);
      padding:16px;
      box-shadow: 0 8px 22px rgba(0,0,0,.22);
      position:relative;
    }
    .stat{display:grid; gap:8px}
    .stat .k{font-size:12px; color:var(--muted); font-family:var(--mono)}
    .stat .v{font-size:16px; font-weight:700}
    .section{margin-top:22px}
    .section h2{margin:0 0 10px; font-size:18px; letter-spacing:.2px}
    .grid2{display:grid; grid-template-columns: 1fr 1fr; gap:14px}
    .grid3{display:grid; grid-template-columns: repeat(3, 1fr); gap:14px}
    .muted{color:var(--muted)}
    ul{margin:10px 0 0; padding-left:18px}
    li{margin:6px 0}
    .tags{display:flex; gap:8px; flex-wrap:wrap; margin-top:10px}
    .tag{
      font-size:12px;
      padding:6px 9px;
      border-radius:999px;
      border:1px solid var(--line);
      color: var(--muted);
      background: rgba(12,19,43,.25);
      font-family:var(--mono);
    }
    .proj{
      display:grid; gap:10px;
      border:1px solid var(--line);
      border-radius:var(--radius);
      padding:16px;
      background: linear-gradient(180deg, rgba(15,23,51,.45), rgba(12,19,43,.25));
    }
    .proj h3{margin:0; font-size:16px}
    .proj p{margin:0; color:var(--muted)}
    .proj .meta{display:flex; gap:10px; flex-wrap:wrap; color:var(--muted); font-family:var(--mono); font-size:12px}
    .proj .actions{display:flex; gap:10px; flex-wrap:wrap; margin-top:4px}
    .proj .actions a{font-size:13px}
    .split{display:grid; grid-template-columns: 1fr 1fr; gap:14px}
    .foot{
      margin-top:26px;
      padding-top:18px;
      border-top:1px solid var(--line);
      color:var(--muted);
      display:flex;
      justify-content:space-between;
      gap:12px;
      flex-wrap:wrap;
      font-size:14px;
    }
    .kbd{
      font-family:var(--mono);
      padding:2px 8px;
      border:1px solid var(--line);
      border-radius:999px;
      background: rgba(15,23,51,.25);
      color:var(--muted);
      font-size:12px;
    }

    @media (max-width: 900px){
      .hero .grid{grid-template-columns: 1fr}
      .grid3{grid-template-columns: 1fr}
      .grid2, .split{grid-template-columns: 1fr}

      /* Photo stacks nicely on mobile */
      .profile{flex-direction:column; text-align:center}
    }
  </style>
</head>

<body>
  <div class="nav">
    <div class="inner">
      <a class="brand" href="#top">
        <span class="dot" aria-hidden="true"></span>
        <b>Khang Le</b>
      </a>
      <div class="links">
        <a class="pill" href="#about">About</a>
        <a class="pill" href="#skills">Skills</a>
        <a class="pill" href="#projects">Projects</a>
        <a class="pill" href="#experience">Experience</a>
        <a class="pill" href="#contact">Contact</a>
      </div>
    </div>
  </div>

  <main class="wrap" id="top">
    <!-- HERO -->
    <section class="hero">
      <div class="grid">
        <div>
          <!-- PHOTO AREA: Put your image at assets/profile.jpg -->
          <div class="profile">
            <img class="avatar" src="./assets/photo.jpg" alt="Khang Le profile photo" />
            <div>
              <h1>Cybersecurity • Networking • IT Technician</h1>
              <p class="sub">
                Seneca Cybersecurity student (GPA 3.9). Targeting SOC/Blue Team, NOC/Network Tech, and IT Technician roles.
                Building skills in cloud security, pentesting labs, and infrastructure.
              </p>

              <div class="badges">
                <span class="badge">Seneca CYT (Sep 2025 → Apr 2026)</span>
                <span class="badge">GPA 3.9</span>
                <span class="badge">CompTIA A+</span>
                <span class="badge">CompTIA Network+</span>
                <span class="badge">Security+ (In Progress)</span>
                <span class="badge">Toronto, ON</span>
              </div>

              <div class="cta">
                <!-- Replace these links -->
                <a class="btn primary" href="https://github.com/YOUR_GITHUB" target="_blank" rel="noreferrer">GitHub ↗</a>
                <a class="btn" href="https://www.linkedin.com/in/YOUR_LINKEDIN" target="_blank" rel="noreferrer">LinkedIn ↗</a>
                <a class="btn" href="mailto:khangle.tech@gmail.com">Email</a>
                <!-- Optional: add resume.pdf to repo root -->
                <a class="btn" href="./resume.pdf">Resume (PDF)</a>
              </div>
            </div>
          </div>

          <div class="section">
            <h2>Target Roles</h2>
            <div class="tags">
              <span class="tag">SOC / Blue Team</span>
              <span class="tag">NOC / Network Tech</span>
              <span class="tag">IT Technician</span>
              <span class="tag">Cloud Security</span>
              <span class="tag">Pentesting</span>
              <span class="tag">Infrastructure / Servers</span>
            </div>
          </div>
        </div>

        <div class="card">
          <div class="stat">
            <div class="k">Program</div>
            <div class="v">Cybersecurity (CYT), Seneca Polytechnic</div>
            <div class="k">Dates</div>
            <div class="v">Sep 2025 → Apr 2026</div>
            <div class="k">GPA</div>
            <div class="v">3.9</div>
            <div class="k">Strengths</div>
            <div class="v">Networking + monitoring + documentation</div>
          </div>
        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section class="section" id="about">
      <h2>About</h2>
      <div class="split">
        <div class="card">
          <p class="muted" style="margin:0">
            I’m a cybersecurity student with hands-on labs in Active Directory security, vulnerability assessment,
            penetration testing, and cloud/IoT monitoring. I’m aiming for co-op roles where I can apply strong troubleshooting
            skills and keep learning security operations.
          </p>
          <ul class="muted">
            <li>Strong documentation and reporting (findings, impact, remediations).</li>
            <li>Comfortable working across Windows/macOS environments.</li>
            <li>Focused on practical security + networking fundamentals.</li>
          </ul>
        </div>

        <div class="card">
          <h3 style="margin:0 0 8px; font-size:15px">Highlights</h3>
          <ul class="muted">
            <li>AD attack simulation (recon → exploit → lateral movement) + remediations</li>
            <li>AWS IoT monitoring stack with Suricata + ELK + VPC Flow Logs</li>
            <li>Pen testing report with risk rating + mitigation steps</li>
            <li>Secure network design using ACLs, port security, DNS, HTTPS, SSH</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- SKILLS -->
    <section class="section" id="skills">
      <h2>Skills</h2>
      <div class="grid3">
        <div class="card">
          <h3 style="margin:0 0 6px; font-size:15px">Cybersecurity</h3>
          <ul class="muted">
            <li>Recon & enumeration (Nmap, web enumeration)</li>
            <li>Vulnerability assessment (OpenVAS/Greenbone)</li>
            <li>AD lab concepts: lateral movement, credential risks, hardening</li>
            <li>Monitoring/detection: Suricata alerts, dashboards (ELK/Kibana)</li>
            <li>Reporting: severity, likelihood, remediation recommendations</li>
          </ul>
        </div>

        <div class="card">
          <h3 style="margin:0 0 6px; font-size:15px">Networking</h3>
          <ul class="muted">
            <li>TCP/IP, DNS, DHCP fundamentals</li>
            <li>Network design in Packet Tracer</li>
            <li>ACLs, port security, SSH remote management</li>
            <li>Troubleshooting routers/extenders and connectivity issues</li>
          </ul>
        </div>

        <div class="card">
          <h3 style="margin:0 0 6px; font-size:15px">Systems / IT</h3>
          <ul class="muted">
            <li>Windows 10/11, macOS, iOS/Android</li>
            <li>Microsoft 365, Teams/Zoom support</li>
            <li>Active Directory exposure (accounts, troubleshooting)</li>
            <li>Ticketing/workflows: Jira, Remedy</li>
          </ul>
        </div>
      </div>
    </section>

    <!-- PROJECTS -->
    <section class="section" id="projects">
      <h2>Projects</h2>

      <div class="grid2">
        <article class="proj">
          <h3>Active Directory Attack Simulation + Remediation Plan</h3>
          <div class="meta">
            <span>AD Lab</span><span>•</span><span>Kali + Windows Server</span><span>•</span><span>Recon → Lateral Movement</span>
          </div>
          <p>
            Simulated a full attack lifecycle in an isolated domain environment and documented remediation recommendations
            (patching, segmentation, credential hygiene, access restrictions).
          </p>
          <div class="tags">
            <span class="tag">Nmap</span><span class="tag">OpenVAS</span><span class="tag">Metasploit</span><span class="tag">Impacket</span><span class="tag">AD</span>
          </div>
          <div class="actions">
            <a class="pill" href="https://github.com/YOUR_GITHUB/ad-attack-lab" target="_blank" rel="noreferrer">Repo ↗</a>
            <a class="pill" href="#" title="Optional: link to sanitized PDF in repo">Report (PDF)</a>
          </div>
        </article>

        <article class="proj">
          <h3>AWS IoT Temperature Monitoring + Security Detection</h3>
          <div class="meta">
            <span>Cloud/IoT</span><span>•</span><span>Raspberry Pi</span><span>•</span><span>Suricata + ELK</span>
          </div>
          <p>
            Built an IoT pipeline sending data to AWS IoT Core over TLS, mirrored MQTT to EC2, detected simulated attacks
            using Suricata rules + Kibana dashboards, and validated activity via VPC Flow Logs stored in S3.
          </p>
          <div class="tags">
            <span class="tag">AWS IoT</span><span class="tag">EC2</span><span class="tag">S3</span><span class="tag">Suricata</span><span class="tag">Kibana</span><span class="tag">VPC Logs</span>
          </div>
          <div class="actions">
            <a class="pill" href="https://github.com/YOUR_GITHUB/aws-iot-security-monitoring" target="_blank" rel="noreferrer">Repo ↗</a>
            <a class="pill" href="#" title="Optional: link to sanitized PDF in repo">Report (PDF)</a>
          </div>
        </article>

        <article class="proj">
          <h3>Penetration Testing Report (Metasploitable2)</h3>
          <div class="meta">
            <span>Pen Testing</span><span>•</span><span>Web + Network</span><span>•</span><span>Risk Rating + Mitigation</span>
          </div>
          <p>
            Conducted scanning, validated vulnerabilities, and produced a professional report with impact, likelihood,
            severity, and recommendations.
          </p>
          <div class="tags">
            <span class="tag">Nmap</span><span class="tag">Metasploit</span><span class="tag">Web Vulns</span><span class="tag">Reporting</span>
          </div>
          <div class="actions">
            <a class="pill" href="https://github.com/YOUR_GITHUB/pentest-reports" target="_blank" rel="noreferrer">Repo ↗</a>
            <a class="pill" href="#" title="Optional: link to sanitized PDF in repo">Report (PDF)</a>
          </div>
        </article>

        <article class="proj">
          <h3>Secure Dual-LAN Network Design (Packet Tracer)</h3>
          <div class="meta">
            <span>Networking</span><span>•</span><span>ACLs + Port Security</span><span>•</span><span>DNS + HTTPS + SSH</span>
          </div>
          <p>
            Designed a dual-LAN topology with router + switches, configured static IPs, DNS + web services, enforced port security,
            and implemented ACL rules to restrict access and secure remote management.
          </p>
          <div class="tags">
            <span class="tag">Cisco</span><span class="tag">ACL</span><span class="tag">Port Security</span><span class="tag">DNS</span><span class="tag">SSH</span>
          </div>
          <div class="actions">
            <a class="pill" href="https://github.com/YOUR_GITHUB/network-design-labs" target="_blank" rel="noreferrer">Repo ↗</a>
            <a class="pill" href="#" title="Optional: add diagram/screenshots in repo">Diagram</a>
          </div>
        </article>
      </div>

      <p class="muted" style="margin-top:12px">
        Note: Keep public repos sanitized (no credentials, no active payloads). We can publish safe “case studies” + diagrams.
      </p>
    </section>

    <!-- EXPERIENCE -->
    <section class="section" id="experience">
      <h2>Experience</h2>
      <div class="grid2">
        <div class="card">
          <h3 style="margin:0 0 6px; font-size:15px">IT Client Services Technician — George Brown College</h3>
          <p class="muted" style="margin:0">
            Support across Windows/macOS/mobile, device deployment, ticket workflows, and classroom/lab AV troubleshooting.
          </p>
          <div class="tags">
            <span class="tag">Windows/macOS</span><span class="tag">M365</span><span class="tag">AD</span><span class="tag">Jira</span><span class="tag">Remedy</span>
          </div>
        </div>

        <div class="card">
          <h3 style="margin:0 0 6px; font-size:15px">Technology Consultant — Best Buy Canada</h3>
          <p class="muted" style="margin:0">
            Home networking setup and troubleshooting (routers, extenders, smart devices) plus hardware/software support.
          </p>
          <div class="tags">
            <span class="tag">Networking</span><span class="tag">Troubleshooting</span><span class="tag">Customer-facing</span>
          </div>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section class="section" id="contact">
      <h2>Contact</h2>
      <div class="card">
        <p class="muted" style="margin:0 0 10px">
          Open to co-op roles in SOC/Blue Team, NOC/Network Tech, and IT Technician positions.
        </p>
        <div class="cta">
          <a class="btn primary" href="mailto:khangle.tech@gmail.com">khangle.tech@gmail.com</a>
          <a class="btn" href="https://github.com/YOUR_GITHUB" target="_blank" rel="noreferrer">GitHub ↗</a>
          <a class="btn" href="https://www.linkedin.com/in/YOUR_LINKEDIN" target="_blank" rel="noreferrer">LinkedIn ↗</a>
        </div>
        <p class="muted" style="margin:12px 0 0">
          <span class="kbd">Last updated</span> <span id="lastUpdated"></span>
        </p>
      </div>
    </section>

    <footer class="foot">
      <span>© <span id="year"></span> Khang Le</span>
      <span class="muted">Single-file HTML portfolio • Hosted on GitHub Pages</span>
    </footer>
  </main>

  <script>
    document.getElementById("year").textContent = new Date().getFullYear();
    const d = new Date();
    document.getElementById("lastUpdated").textContent =
      d.toLocaleDateString(undefined, { year:"numeric", month:"short", day:"2-digit" });
  </script>
</body>
</html>
