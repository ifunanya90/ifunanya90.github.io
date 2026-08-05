<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ifunanya Ezulu — Revenue Operations & Customer Acquisition</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@400;500;600&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --ink: #12161D;
    --ink-soft: #1B212B;
    --paper: #F3F1EA;
    --paper-dim: #C9C6BC;
    --line: #2B3240;
    --amber: #E7A63C;
    --teal: #4E9490;
    --font-display: 'Space Grotesk', sans-serif;
    --font-body: 'Inter', sans-serif;
    --font-mono: 'IBM Plex Mono', monospace;
  }

  *{ margin:0; padding:0; box-sizing:border-box; }

  html{ scroll-behavior:smooth; }

  body{
    background:var(--ink);
    color:var(--paper);
    font-family:var(--font-body);
    line-height:1.6;
  }

  a{ color:inherit; }

  .wrap{
    max-width:1040px;
    margin:0 auto;
    padding:0 32px;
  }

  /* ---------- NAV ---------- */
  header{
    position:sticky; top:0; z-index:10;
    background:rgba(18,22,29,0.9);
    backdrop-filter:blur(8px);
    border-bottom:1px solid var(--line);
  }
  nav{
    display:flex; align-items:center; justify-content:space-between;
    padding:20px 0;
  }
  .logo{
    font-family:var(--font-mono);
    font-size:14px;
    letter-spacing:0.05em;
    color:var(--amber);
  }
  .nav-links{ display:flex; gap:28px; list-style:none; }
  .nav-links a{
    font-family:var(--font-mono);
    font-size:13px;
    text-decoration:none;
    color:var(--paper-dim);
    transition:color 0.2s;
  }
  .nav-links a:hover{ color:var(--amber); }

  /* ---------- HERO ---------- */
  .hero{
    padding:110px 0 90px;
    border-bottom:1px solid var(--line);
  }
  .eyebrow{
    font-family:var(--font-mono);
    font-size:13px;
    color:var(--teal);
    letter-spacing:0.08em;
    text-transform:uppercase;
    margin-bottom:24px;
    display:flex;
    align-items:center;
    gap:10px;
  }
  .eyebrow::before{
    content:'';
    width:8px; height:8px;
    background:var(--teal);
    border-radius:50%;
    display:inline-block;
  }
  h1{
    font-family:var(--font-display);
    font-weight:700;
    font-size:clamp(34px, 5vw, 56px);
    line-height:1.08;
    letter-spacing:-0.01em;
    max-width:820px;
    margin-bottom:26px;
  }
  h1 span{ color:var(--amber); }
  .hero-sub{
    font-size:18px;
    color:var(--paper-dim);
    max-width:560px;
    margin-bottom:44px;
  }
  .hero-actions{ display:flex; gap:16px; flex-wrap:wrap; }
  .btn{
    font-family:var(--font-mono);
    font-size:13px;
    padding:13px 22px;
    border-radius:2px;
    text-decoration:none;
    display:inline-block;
    transition:transform 0.15s, background 0.15s;
  }
  .btn-primary{ background:var(--amber); color:var(--ink); font-weight:500; }
  .btn-primary:hover{ transform:translateY(-2px); }
  .btn-ghost{ border:1px solid var(--line); color:var(--paper); }
  .btn-ghost:hover{ border-color:var(--amber); color:var(--amber); }

  /* ---------- PIPELINE (signature element) ---------- */
  .pipeline{
    margin-top:70px;
    display:flex;
    align-items:center;
    overflow-x:auto;
    padding-bottom:8px;
  }
  .node{
    flex:0 0 auto;
    display:flex;
    flex-direction:column;
    align-items:center;
    gap:10px;
    min-width:112px;
  }
  .node-dot{
    width:44px; height:44px;
    border:1px solid var(--line);
    background:var(--ink-soft);
    border-radius:50%;
    display:flex; align-items:center; justify-content:center;
    font-family:var(--font-mono);
    font-size:11px;
    color:var(--amber);
  }
  .node-label{
    font-family:var(--font-mono);
    font-size:11px;
    color:var(--paper-dim);
    text-align:center;
    letter-spacing:0.02em;
  }
  .node-connector{
    flex:1 1 auto;
    height:1px;
    min-width:24px;
    background:repeating-linear-gradient(90deg, var(--line) 0, var(--line) 4px, transparent 4px, transparent 9px);
  }

  /* ---------- SECTION SHARED ---------- */
  section{ padding:80px 0; border-bottom:1px solid var(--line); }
  .section-head{
    display:flex;
    align-items:baseline;
    justify-content:space-between;
    margin-bottom:48px;
    flex-wrap:wrap;
    gap:12px;
  }
  .section-tag{
    font-family:var(--font-mono);
    font-size:12px;
    color:var(--teal);
    letter-spacing:0.08em;
  }
  h2{
    font-family:var(--font-display);
    font-size:clamp(24px,3vw,32px);
    font-weight:600;
  }

  /* ---------- ABOUT ---------- */
  .about-grid{
    display:grid;
    grid-template-columns:1.1fr 0.9fr;
    gap:56px;
  }
  .about-grid p{ color:var(--paper-dim); margin-bottom:18px; }
  .about-grid p strong{ color:var(--paper); font-weight:500; }
  .fact-box{
    border:1px solid var(--line);
    background:var(--ink-soft);
    padding:26px;
  }
  .fact-box .fact{
    display:flex;
    justify-content:space-between;
    padding:12px 0;
    border-bottom:1px solid var(--line);
    font-size:14px;
  }
  .fact-box .fact:last-child{ border-bottom:none; }
  .fact-label{ color:var(--paper-dim); font-family:var(--font-mono); font-size:12px; }
  .fact-value{ text-align:right; }

  /* ---------- SERVICES ---------- */
  .services{
    display:grid;
    grid-template-columns:repeat(3, 1fr);
    gap:1px;
    background:var(--line);
    border:1px solid var(--line);
  }
  .service{
    background:var(--ink);
    padding:28px 24px;
  }
  .service-num{
    font-family:var(--font-mono);
    font-size:12px;
    color:var(--amber);
    margin-bottom:14px;
    display:block;
  }
  .service h3{
    font-family:var(--font-display);
    font-size:17px;
    font-weight:600;
    margin-bottom:10px;
  }
  .service p{ font-size:14px; color:var(--paper-dim); }

  /* ---------- PROJECTS ---------- */
  .project{
    border:1px solid var(--line);
    background:var(--ink-soft);
    margin-bottom:20px;
    padding:32px;
  }
  .project-top{
    display:flex;
    justify-content:space-between;
    align-items:flex-start;
    gap:20px;
    margin-bottom:18px;
    flex-wrap:wrap;
  }
  .project h3{
    font-family:var(--font-display);
    font-size:20px;
    font-weight:600;
    margin-bottom:6px;
  }
  .project-meta{
    font-family:var(--font-mono);
    font-size:11px;
    color:var(--teal);
    letter-spacing:0.04em;
  }
  .project-body{
    display:grid;
    grid-template-columns:repeat(3, 1fr);
    gap:24px;
    margin-top:20px;
  }
  .project-col span{
    display:block;
    font-family:var(--font-mono);
    font-size:11px;
    color:var(--paper-dim);
    text-transform:uppercase;
    letter-spacing:0.06em;
    margin-bottom:8px;
  }
  .project-col p{ font-size:14px; color:var(--paper); }
  .tags{ display:flex; flex-wrap:wrap; gap:8px; }
  .tag{
    font-family:var(--font-mono);
    font-size:11px;
    padding:4px 10px;
    border:1px solid var(--line);
    color:var(--paper-dim);
  }

  /* ---------- TOOLS ---------- */
  .tool-groups{ display:grid; grid-template-columns:repeat(3, 1fr); gap:32px; }
  .tool-group span{
    display:block;
    font-family:var(--font-mono);
    font-size:11px;
    color:var(--teal);
    text-transform:uppercase;
    letter-spacing:0.06em;
    margin-bottom:14px;
  }
  .tool-list{ display:flex; flex-wrap:wrap; gap:8px; }
  .tool-list .tag{ color:var(--paper); }

  /* ---------- CONTACT ---------- */
  .contact{ text-align:left; border-bottom:none; }
  .contact h2{ margin-bottom:16px; }
  .contact p{ color:var(--paper-dim); max-width:480px; margin-bottom:36px; }
  .contact-links{ display:flex; gap:16px; flex-wrap:wrap; }

  footer{
    padding:30px 0 50px;
    font-family:var(--font-mono);
    font-size:12px;
    color:var(--paper-dim);
    text-align:center;
  }

  @media (max-width:760px){
    .about-grid{ grid-template-columns:1fr; }
    .services{ grid-template-columns:1fr; }
    .project-body{ grid-template-columns:1fr; }
    .tool-groups{ grid-template-columns:1fr; }
    .nav-links{ display:none; }
  }
</style>
</head>
<body>

<header>
  <div class="wrap">
    <nav>
      <div class="logo">IFUNANYA_EZULU.OPS</div>
      <ul class="nav-links">
        <li><a href="#about">About</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#tools">Tools</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </div>
</header>

<section class="hero">
  <div class="wrap">
    <div class="eyebrow">Available for freelance engagements</div>
    <h1>I build the systems that turn a founder's <span>growing pipeline</span> into something they can actually run.</h1>
    <p class="hero-sub">Revenue Operations and Customer Acquisition specialist. I set up your CRM, automate the busywork, and get outbound outreach actually landing meetings, so you can spend your time closing instead of managing spreadsheets.</p>
    <div class="hero-actions">
      <a href="#projects" class="btn btn-primary">See the work</a>
      <a href="#contact" class="btn btn-ghost">Get in touch</a>
    </div>

    <div class="pipeline">
      <div class="node"><div class="node-dot">IN</div><div class="node-label">Lead comes in</div></div>
      <div class="node-connector"></div>
      <div class="node"><div class="node-dot">QA</div><div class="node-label">Qualify & score</div></div>
      <div class="node-connector"></div>
      <div class="node"><div class="node-dot">CRM</div><div class="node-label">Route in HubSpot</div></div>
      <div class="node-connector"></div>
      <div class="node"><div class="node-dot">OUT</div><div class="node-label">Outreach sequence</div></div>
      <div class="node-connector"></div>
      <div class="node"><div class="node-dot">RPT</div><div class="node-label">Report to team</div></div>
    </div>
  </div>
</section>

<section id="about">
  <div class="wrap">
    <div class="section-head">
      <div>
        <div class="section-tag">01 / ABOUT</div>
        <h2>Two years in, still allergic to messy pipelines</h2>
      </div>
    </div>
    <div class="about-grid">
      <div>
        <p>I'm a freelance Revenue Operations and Customer Acquisition specialist based in Nigeria, working with startups and midsized businesses to bring structure to how they find, track, and close customers.</p>
        <p>Most of the founders I work with aren't short on leads. They're short on a system that catches those leads consistently. <strong>That's the gap I fill</strong>: CRM setup, outreach that doesn't feel like spam, and automation that quietly does the reporting no one has time for.</p>
        <p>Before this, I worked as an educator. It shows up in how I work now: I don't just build a system and walk away, I document it clearly enough that your team can run it without me.</p>
      </div>
      <div class="fact-box">
        <div class="fact"><span class="fact-label">EXPERIENCE</span><span class="fact-value">~3 years B2B</span></div>
        <div class="fact"><span class="fact-label">BASED IN</span><span class="fact-value">Nigeria</span></div>
        <div class="fact"><span class="fact-label">CRM</span><span class="fact-value">HubSpot & others</span></div>
        <div class="fact"><span class="fact-label">AUTOMATION</span><span class="fact-value">n8n, Make.com</span></div>
        <div class="fact"><span class="fact-label">BACKGROUND</span><span class="fact-value">Educator</span></div>
        <div class="fact"><span class="fact-label">FIND ME ON</span><span class="fact-value">Upwork, LinkedIn</span></div>
      </div>
    </div>
  </div>
</section>

<section id="services">
  <div class="wrap">
    <div class="section-head">
      <div>
        <div class="section-tag">02 / SERVICES</div>
        <h2>Where I plug into your pipeline</h2>
      </div>
    </div>
    <div class="services">
      <div class="service">
        <span class="service-num">01</span>
        <h3>CRM setup & management</h3>
        <p>Getting your CRM actually set up the way your sales process works, not the other way around.</p>
      </div>
      <div class="service">
        <span class="service-num">02</span>
        <h3>Outbound outreach & lead gen</h3>
        <p>Finding the right people and reaching them with messages that get replies, not silence.</p>
      </div>
      <div class="service">
        <span class="service-num">03</span>
        <h3>Sales automation</h3>
        <p>Workflows in n8n and Make.com that handle the repetitive steps between a lead and a booked call.</p>
      </div>
      <div class="service">
        <span class="service-num">04</span>
        <h3>Pipeline management</h3>
        <p>Keeping deals moving and visible, so nothing quietly stalls in a stage no one is watching.</p>
      </div>
      <div class="service">
        <span class="service-num">05</span>
        <h3>Process documentation</h3>
        <p>Clear, written systems your team can follow, built from years of explaining things for a living.</p>
      </div>
      <div class="service">
        <span class="service-num">06</span>
        <h3>Email & growth marketing</h3>
        <p>Campaigns and sequences built around what actually moves someone from interested to signed.</p>
      </div>
    </div>
  </div>
</section>

<section id="projects">
  <div class="wrap">
    <div class="section-head">
      <div>
        <div class="section-tag">03 / PROJECTS</div>
        <h2>Systems I've built</h2>
      </div>
    </div>

    <div class="project">
      <div class="project-top">
        <div>
          <h3>24-company cold outreach campaign</h3>
          <div class="project-meta">RESEARCH + OUTBOUND · SELF-INITIATED</div>
        </div>
      </div>
      <div class="project-body">
        <div class="project-col">
          <span>Problem</span>
          <p>Needed a repeatable way to reach founders and CEOs directly, instead of relying on job boards alone.</p>
        </div>
        <div class="project-col">
          <span>Approach</span>
          <p>Researched 24 target companies and built a full research and outreach workbook, then ran a targeted cold email campaign to founders and CEOs.</p>
        </div>
        <div class="project-col">
          <span>Result</span>
          <p>A reusable outreach system and research process now used for ongoing client prospecting.</p>
        </div>
      </div>
      <div class="tags" style="margin-top:18px;">
        <span class="tag">Cold Email</span>
        <span class="tag">Research</span>
        <span class="tag">Lemlist</span>
      </div>
    </div>

    <div class="project">
      <div class="project-top">
        <div>
          <h3>End to end pipeline ownership system</h3>
          <div class="project-meta">AUTOMATION · N8N / SLACK</div>
        </div>
      </div>
      <div class="project-body">
        <div class="project-col">
          <span>Problem</span>
          <p>Leads were coming in but nothing owned them end to end, so good leads sat untouched between search and follow up.</p>
        </div>
        <div class="project-col">
          <span>Approach</span>
          <p>Built a system that owns the whole pipeline from the ground up: lead search and qualification, lead validation, lead routing, and a Slack notification the moment a qualified lead lands.</p>
        </div>
        <div class="project-col">
          <span>Result</span>
          <p>Qualified leads get found, validated, and routed automatically, with the team notified in Slack instead of checking a dashboard.</p>
        </div>
      </div>
      <div class="tags" style="margin-top:18px;">
        <span class="tag">Lead Qualification</span>
        <span class="tag">Lead Routing</span>
        <span class="tag">Slack</span>
      </div>
    </div>

    <div class="project">
      <div class="project-top">
        <div>
          <h3>Sentiment-based customer response routing</h3>
          <div class="project-meta">AUTOMATION · CUSTOMER RESPONSE</div>
        </div>
      </div>
      <div class="project-body">
        <div class="project-col">
          <span>Problem</span>
          <p>Customer responses were going into one pile, so upset customers waited the same amount of time as happy ones.</p>
        </div>
        <div class="project-col">
          <span>Approach</span>
          <p>Built a system that captures customer sentiment from responses, routes each one accordingly, and flags negative sentiment for immediate follow up.</p>
        </div>
        <div class="project-col">
          <span>Result</span>
          <p>Negative responses get caught and followed up on fast, instead of sitting in a general inbox.</p>
        </div>
      </div>
      <div class="tags" style="margin-top:18px;">
        <span class="tag">Sentiment Analysis</span>
        <span class="tag">Response Routing</span>
        <span class="tag">Automation</span>
      </div>
    </div>

    <div class="project">
      <div class="project-top">
        <div>
          <h3>Automated manager reporting workflow</h3>
          <div class="project-meta">AUTOMATION · N8N</div>
        </div>
      </div>
      <div class="project-body">
        <div class="project-col">
          <span>Problem</span>
          <p>Manual reporting from Google Sheets to managers was slow and easy to forget.</p>
        </div>
        <div class="project-col">
          <span>Approach</span>
          <p>Built a workflow in n8n that pulls from Google Sheets and routes formatted reports straight to managers, including setting up and troubleshooting Google OAuth credentials.</p>
        </div>
        <div class="project-col">
          <span>Result</span>
          <p>Reporting now runs on its own, no manual pulling or formatting required.</p>
        </div>
      </div>
      <div class="tags" style="margin-top:18px;">
        <span class="tag">n8n</span>
        <span class="tag">Google Sheets</span>
        <span class="tag">Google OAuth</span>
      </div>
    </div>

    <div class="project">
      <div class="project-top">
        <div>
          <h3>Student performance tracking system</h3>
          <div class="project-meta">AUTOMATION · AIRTABLE + HUBSPOT</div>
        </div>
      </div>
      <div class="project-body">
        <div class="project-col">
          <span>Problem</span>
          <p>Student performance data needed to be tracked and made visible without manual entry across tools.</p>
        </div>
        <div class="project-col">
          <span>Approach</span>
          <p>Built a system that routes performance data into Airtable and HubSpot, keeping both in sync automatically.</p>
        </div>
        <div class="project-col">
          <span>Result</span>
          <p>A single automated pipeline replacing manual tracking across two separate tools.</p>
        </div>
      </div>
      <div class="tags" style="margin-top:18px;">
        <span class="tag">Airtable</span>
        <span class="tag">HubSpot</span>
        <span class="tag">Automation</span>
      </div>
    </div>

    <div class="project">
      <div class="project-top">
        <div>
          <h3>CRM cleanup & prospecting, Flowmingo AI</h3>
          <div class="project-meta">SALES ADMINISTRATOR · CLIENT WORK</div>
        </div>
      </div>
      <div class="project-body">
        <div class="project-col">
          <span>Problem</span>
          <p>CRM data was messy and outreach sequencing wasn't consistent, making prospecting inefficient.</p>
        </div>
        <div class="project-col">
          <span>Approach</span>
          <p>Handled LinkedIn prospecting, cleaned up CRM data, and built out consistent outreach sequencing.</p>
        </div>
        <div class="project-col">
          <span>Result</span>
          <p>A cleaner CRM and a repeatable outreach process for the sales team to build on.</p>
        </div>
      </div>
      <div class="tags" style="margin-top:18px;">
        <span class="tag">LinkedIn</span>
        <span class="tag">CRM Cleanup</span>
        <span class="tag">Outreach Sequencing</span>
      </div>
    </div>

  </div>
</section>

<section id="tools">
  <div class="wrap">
    <div class="section-head">
      <div>
        <div class="section-tag">04 / TOOLS</div>
        <h2>What I work in</h2>
      </div>
    </div>
    <div class="tool-groups">
      <div class="tool-group">
        <span>CRM & Outreach</span>
        <div class="tool-list">
          <span class="tag">HubSpot</span>
          <span class="tag">Apollo.io</span>
          <span class="tag">Hunter.io</span>
          <span class="tag">Lemlist</span>
          <span class="tag">Instantly</span>
          <span class="tag">Mailchimp</span>
          <span class="tag">Sales Navigator</span>
        </div>
      </div>
      <div class="tool-group">
        <span>Automation</span>
        <div class="tool-list">
          <span class="tag">n8n</span>
          <span class="tag">Make.com</span>
          <span class="tag">Zapier</span>
        </div>
      </div>
      <div class="tool-group">
        <span>Project Management</span>
        <div class="tool-list">
          <span class="tag">ClickUp</span>
          <span class="tag">Notion</span>
          <span class="tag">Asana</span>
          <span class="tag">Monday.com</span>
          <span class="tag">Airtable</span>
          <span class="tag">Trello</span>
        </div>
      </div>
    </div>
  </div>
</section>

<section id="contact" class="contact">
  <div class="wrap">
    <div class="section-tag">05 / CONTACT</div>
    <h2>Have a pipeline that needs sorting out?</h2>
    <p>I'm currently taking on new projects/tasks. If you need a CRM set up right, outreach that gets replies, or a workflow built so your team stops doing it by hand, let's talk.</p>
    <div class="contact-links">
      <a href="#" class="btn btn-primary"> →</a>https://www.upwork.com/freelancers/~019888d8d087a6aa30?mp_source=share
      <a href="#" class="btn btn-ghost">https://www.linkedin.com/in/ifunanya-ezulu90/ →</a>
      <a href="mailto:ifunanyaezulu90@gmail.com" class="btn btn-ghost">Email me →</a>
    </div>
  </div>
</section>

<footer>
</footer>

</body>
</html>
