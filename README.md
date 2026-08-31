<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Canada Economic Dashboard 2025</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=Inconsolata:wght@400;500;600&family=Lora:ital,wght@0,400;0,600;1,400&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #000000;
  --surface: #0d0d0d;
  --surface2: #111111;
  --border: #2a2a2a;
  --text: #f0f0f0;
  --muted: #c8c8c8;
  --subtle: #909090;
  --red: #ff4d4d;
  --red-soft: #1a0a0a;
  --green: #2ecc7a;
  --green-soft: #071a0f;
  --amber: #f0b429;
  --amber-soft: #1a1200;
  --blue: #4da6ff;
  --blue-soft: #070f1a;
  --maple: #ff4d4d;
  --gold: #f0b429;
}

* { margin: 0; padding: 0; box-sizing: border-box; }

body {
  background: var(--bg);
  color: var(--text);
  font-family: 'Lora', serif;
  font-size: 14px;
  line-height: 1.6;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-rendering: optimizeLegibility;
}

/* ── HEADER ── */
.header {
  background: #050505;
  color: white;
  padding: 32px 40px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 16px;
  position: relative;
  overflow: hidden;
}
.header::before {
  content: '🍁';
  position: absolute;
  right: 40px;
  top: 50%;
  transform: translateY(-50%);
  font-size: 120px;
  opacity: 0.06;
  pointer-events: none;
}
.header-left h1 {
  font-family: 'Syne', sans-serif;
  font-weight: 800;
  font-size: 28px;
  letter-spacing: -0.5px;
  color: white;
}
.header-left p {
  font-family: 'Inconsolata', monospace;
  font-size: 12px;
  color: rgba(255,255,255,0.65);
  letter-spacing: 2px;
  margin-top: 4px;
  text-transform: uppercase;
}
.header-right {
  display: flex;
  gap: 32px;
  flex-wrap: wrap;
}
.header-stat { text-align: right; }
.header-stat .val {
  font-family: 'Syne', sans-serif;
  font-weight: 800;
  font-size: 26px;
  color: white;
  line-height: 1;
}
.header-stat .lbl {
  font-family: 'Inconsolata', monospace;
  font-size: 10px;
  color: rgba(255,255,255,0.45);
  text-transform: uppercase;
  letter-spacing: 1.5px;
  margin-top: 3px;
}
.badge-pos { color: #4ec994; }
.badge-neg { color: #e07070; }
.badge-neu { color: #f0c060; }

/* ── NAV TABS ── */
.nav {
  background: var(--surface);
  border-bottom: 1px solid var(--border);
  padding: 0 40px;
  display: flex;
  gap: 0;
  overflow-x: auto;
}
.nav-tab {
  font-family: 'Inconsolata', monospace;
  font-size: 11px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  padding: 14px 20px;
  cursor: pointer;
  border-bottom: 2px solid transparent;
  color: var(--subtle);
  white-space: nowrap;
  transition: all 0.2s;
}
.nav-tab:hover { color: var(--text); }
.nav-tab.active {
  color: var(--maple);
  border-bottom-color: var(--maple);
  font-weight: 600;
}

/* ── CONTENT ── */
.content { padding: 32px 40px; max-width: 1400px; }
.section { display: none; }
.section.active { display: block; }

/* ── GRID LAYOUTS ── */
.grid-4 { display: grid; grid-template-columns: repeat(4, 1fr); gap: 16px; margin-bottom: 24px; }
.grid-3 { display: grid; grid-template-columns: repeat(3, 1fr); gap: 16px; margin-bottom: 24px; }
.grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 24px; }
.grid-2-1 { display: grid; grid-template-columns: 2fr 1fr; gap: 16px; margin-bottom: 24px; }
.grid-1-2 { display: grid; grid-template-columns: 1fr 2fr; gap: 16px; margin-bottom: 24px; }

/* ── CARD ── */
.card {
  background: var(--surface);
  border: 1px solid var(--border);
  padding: 22px;
  position: relative;
}
.card-sm { padding: 16px; }
.card-title {
  font-family: 'Inconsolata', monospace;
  font-size: 10px;
  letter-spacing: 2px;
  text-transform: uppercase;
  color: var(--subtle);
  margin-bottom: 12px;
}
.card-value {
  font-family: 'Syne', sans-serif;
  font-weight: 800;
  font-size: 36px;
  line-height: 1;
  color: var(--text);
}
.card-value.green { color: var(--green); }
.card-value.red { color: var(--red); }
.card-value.amber { color: var(--amber); }
.card-value.blue { color: var(--blue); }
.card-sub {
  font-size: 12px;
  color: var(--muted);
  margin-top: 6px;
  font-family: 'Inconsolata', monospace;
}
.trend-up { color: var(--green); }
.trend-down { color: var(--red); }
.trend-flat { color: var(--amber); }
.card-note {
  font-size: 12px;
  color: var(--muted);
  margin-top: 10px;
  font-style: italic;
  line-height: 1.5;
  border-top: 1px solid var(--border);
  padding-top: 10px;
}

/* ── SECTION HEADER ── */
.sec-head {
  display: flex;
  align-items: baseline;
  gap: 12px;
  margin-bottom: 20px;
}
.sec-head h2 {
  font-family: 'Syne', sans-serif;
  font-weight: 800;
  font-size: 22px;
  letter-spacing: -0.3px;
}
.sec-head span {
  font-family: 'Inconsolata', monospace;
  font-size: 11px;
  color: var(--subtle);
  letter-spacing: 1.5px;
  text-transform: uppercase;
}

/* ── BAR CHART ── */
.bar-chart { padding: 4px 0; }
.bar-row { display: flex; align-items: center; gap: 10px; margin-bottom: 10px; }
.bar-label { font-family: 'Inconsolata', monospace; font-size: 11px; color: var(--muted); width: 120px; flex-shrink: 0; }
.bar-track { flex: 1; background: var(--bg); height: 20px; position: relative; border: 1px solid var(--border); }
.bar-fill { height: 100%; position: relative; transition: width 1s ease; display: flex; align-items: center; justify-content: flex-end; padding-right: 6px; }
.bar-fill span { font-family: 'Inconsolata', monospace; font-size: 10px; font-weight: 600; color: white; }
.bar-maple { background: var(--maple); }
.bar-blue  { background: var(--blue); }
.bar-green { background: var(--green); }
.bar-amber { background: var(--amber); }
.bar-muted { background: var(--subtle); }

/* ── LINE CHART ── */
.chart-wrap { position: relative; height: 180px; width: 100%; }
svg.linechart { width: 100%; height: 100%; overflow: visible; }

/* ── TIMELINE ── */
.timeline { position: relative; padding-left: 20px; }
.timeline::before { content: ''; position: absolute; left: 0; top: 0; bottom: 0; width: 2px; background: var(--border); }
.tl-item { position: relative; margin-bottom: 20px; padding-left: 20px; }
.tl-item::before { content: ''; position: absolute; left: -5px; top: 5px; width: 8px; height: 8px; border-radius: 50%; background: var(--maple); border: 2px solid var(--surface); }
.tl-year { font-family: 'Inconsolata', monospace; font-size: 11px; color: var(--maple); font-weight: 600; letter-spacing: 1px; }
.tl-text { font-size: 13px; color: var(--muted); line-height: 1.5; margin-top: 2px; }

/* ── SECTOR TABLE ── */
.sector-table { width: 100%; border-collapse: collapse; }
.sector-table th {
  font-family: 'Inconsolata', monospace;
  font-size: 10px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  color: var(--subtle);
  text-align: left;
  padding: 10px 12px;
  border-bottom: 1px solid var(--border);
  background: var(--surface2);
}
.sector-table td {
  padding: 11px 12px;
  border-bottom: 1px solid var(--border);
  font-size: 13px;
  color: var(--text);
}
.sector-table tr:last-child td { border-bottom: none; }
.sector-table tr:hover td { background: #181818; }
.pill {
  display: inline-block;
  padding: 2px 8px;
  font-family: 'Inconsolata', monospace;
  font-size: 10px;
  font-weight: 600;
  letter-spacing: 1px;
  border-radius: 2px;
}
.pill-up { background: var(--green-soft); color: var(--green); }
.pill-down { background: var(--red-soft); color: var(--red); }
.pill-watch { background: var(--amber-soft); color: var(--amber); }

/* ── RISK METER ── */
.risk-bar { display: flex; height: 14px; border-radius: 2px; overflow: hidden; margin: 8px 0; }
.risk-low  { background: var(--green); }
.risk-mid  { background: var(--amber); }
.risk-high { background: var(--red); }
.risk-labels { display: flex; justify-content: space-between; font-family: 'Inconsolata', monospace; font-size: 10px; color: var(--subtle); }

/* ── PROVINCE MAP LEGEND ── */
.province-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 8px; }
.prov-card {
  background: var(--surface2);
  border: 1px solid var(--border);
  padding: 12px;
}
.prov-name { font-family: 'Syne', sans-serif; font-weight: 700; font-size: 13px; }
.prov-gdp { font-family: 'Inconsolata', monospace; font-size: 11px; color: var(--muted); margin-top: 2px; }
.prov-tag { margin-top: 6px; }

/* ── DONUT-STYLE ── */
.donut-row { display: flex; align-items: center; gap: 12px; margin-bottom: 8px; }
.donut-color { width: 12px; height: 12px; flex-shrink: 0; border-radius: 2px; }
.donut-name { font-size: 13px; flex: 1; }
.donut-val { font-family: 'Inconsolata', monospace; font-size: 12px; font-weight: 600; color: var(--muted); }
.donut-bar { width: 100%; height: 6px; background: var(--bg); margin-top: 4px; border-radius: 1px; }
.donut-bar-fill { height: 100%; border-radius: 1px; }

/* ── FORECAST TABLE ── */
.forecast-grid { display: grid; grid-template-columns: repeat(5, 1fr); gap: 2px; }
.fc-cell {
  background: var(--surface);
  border: 1px solid var(--border);
  padding: 14px 10px;
  text-align: center;
}
.fc-year { font-family: 'Inconsolata', monospace; font-size: 11px; color: var(--subtle); letter-spacing: 1px; }
.fc-val { font-family: 'Syne', sans-serif; font-weight: 700; font-size: 22px; margin: 4px 0; }
.fc-label { font-size: 11px; color: var(--muted); font-style: italic; }
.fc-positive { color: var(--green); }
.fc-negative { color: var(--red); }
.fc-neutral { color: var(--amber); }

/* ── INNOVATION CARD ── */
.innov-card {
  background: var(--surface);
  border: 1px solid var(--border);
  padding: 20px;
  display: flex;
  gap: 16px;
  transition: border-color 0.2s;
}
.innov-card:hover { border-color: var(--maple); }
.innov-icon { font-size: 28px; line-height: 1; flex-shrink: 0; }
.innov-card h4 { font-family: 'Syne', sans-serif; font-weight: 700; font-size: 14px; margin-bottom: 6px; }
.innov-card p { font-size: 12px; color: var(--muted); line-height: 1.5; }
.innov-card .tag {
  display: inline-block;
  margin-top: 8px;
  font-family: 'Inconsolata', monospace;
  font-size: 10px;
  letter-spacing: 1px;
  padding: 2px 8px;
  background: #1a0a0a;
  color: var(--maple);
  border: 1px solid rgba(192,57,43,0.15);
}

/* ── ALERT BOX ── */
.alert { padding: 14px 16px; border-left: 3px solid; margin-bottom: 12px; font-size: 13px; line-height: 1.5; }
.alert-warn { border-color: var(--amber); background: var(--amber-soft); color: #f0b429; }
.alert-good { border-color: var(--green); background: var(--green-soft); color: #2ecc7a; }
.alert-info { border-color: var(--blue); background: var(--blue-soft); color: #4da6ff; }
.alert strong { font-family: 'Inconsolata', monospace; font-size: 11px; letter-spacing: 1px; text-transform: uppercase; display: block; margin-bottom: 4px; }

/* ── SOURCE NOTE ── */
.source { font-family: 'Inconsolata', monospace; font-size: 10px; color: var(--subtle); letter-spacing: 0.5px; margin-top: 6px; }

/* ── ANIMATIONS ── */
@keyframes fadeIn { from { opacity: 0; transform: translateY(10px); } to { opacity: 1; transform: translateY(0); } }
.section.active > * { animation: fadeIn 0.4s ease both; }

/* ── RESPONSIVE ── */
@media (max-width: 900px) {
  .grid-4, .grid-3 { grid-template-columns: 1fr 1fr; }
  .grid-2-1, .grid-1-2, .grid-2 { grid-template-columns: 1fr; }
  .content { padding: 20px 16px; }
  .header { padding: 20px 16px; }
  .forecast-grid { grid-template-columns: repeat(3, 1fr); }
  .province-grid { grid-template-columns: 1fr 1fr; }
}
</style>
</head>
<body>

<!-- ── HEADER ── -->
<div class="header">
  <div class="header-left">
    <h1>🍁 Canada Economic Dashboard</h1>
    <p>State of the Economy — Updated March 2026 · Sources: StatCan, BoC, RBC, TD, IMF</p>
  </div>
  <div class="header-right">
    <div class="header-stat">
      <div class="val">$2.39T</div>
      <div class="lbl">Nominal GDP (USD)</div>
    </div>
    <div class="header-stat">
      <div class="val badge-neu">1.7%</div>
      <div class="lbl">2025 GDP Growth</div>
    </div>
    <div class="header-stat">
      <div class="val badge-pos">2.3%</div>
      <div class="lbl">CPI Inflation</div>
    </div>
    <div class="header-stat">
      <div class="val badge-neu">6.5%</div>
      <div class="lbl">Unemployment</div>
    </div>
    <div class="header-stat">
      <div class="val badge-pos">2.25%</div>
      <div class="lbl">BoC Policy Rate</div>
    </div>
  </div>
</div>

<!-- ── NAV ── -->
<div class="nav">
  <div class="nav-tab active" onclick="showTab('overview')">Overview</div>
  <div class="nav-tab" onclick="showTab('financial')">Financial</div>
  <div class="nav-tab" onclick="showTab('jobs')">Jobs & Labour</div>
  <div class="nav-tab" onclick="showTab('sectors')">Growth Sectors</div>
  <div class="nav-tab" onclick="showTab('innovation')">Innovation</div>
  <div class="nav-tab" onclick="showTab('resources')">Resources & Assets</div>
  <div class="nav-tab" onclick="showTab('population')">Population</div>
  <div class="nav-tab" onclick="showTab('forecast')">10-Year Outlook</div>
</div>

<!-- ── CONTENT ── -->
<div class="content">

<!-- ════════════════════════ OVERVIEW ════════════════════════ -->
<div class="section active" id="overview">
  <div class="sec-head"><h2>Economic Overview</h2><span>Canada 2025 Snapshot</span></div>

  <div class="grid-4">
    <div class="card">
      <div class="card-title">GDP Annual Growth</div>
      <div class="card-value amber">1.7%</div>
      <div class="card-sub trend-down">▼ Slowest since 2020 (excl. pandemic)</div>
      <div class="card-note">Full-year 2025 growth. Q4 contracted -0.6% annualized on inventory drawdown. Lower U.S. exports were the main drag.</div>
    </div>
    <div class="card">
      <div class="card-title">GDP Per Capita (USD)</div>
      <div class="card-value blue">$58,400</div>
      <div class="card-sub trend-up">▲ First per-capita rise in 3 years</div>
      <div class="card-note">Per-capita GDP rose in 2025 for the first time since 2022 — a meaningful milestone as population growth slowed.</div>
    </div>
    <div class="card">
      <div class="card-title">Nominal GDP (USD)</div>
      <div class="card-value">$2.39T</div>
      <div class="card-sub">9th largest economy globally</div>
      <div class="card-note">Canada ranks 9th by nominal GDP. 56 companies in the Forbes Global 2000. TSX is 10th-largest exchange by market cap.</div>
    </div>
    <div class="card">
      <div class="card-title">Household Consumption</div>
      <div class="card-value green">58%</div>
      <div class="card-sub">of GDP composition</div>
      <div class="card-note">Consumer spending was a bright spot in 2025 — a resilient anchor despite trade uncertainty and rising unemployment.</div>
    </div>
  </div>

  <div class="grid-2-1">
    <div class="card">
      <div class="card-title">GDP Quarterly Growth — 2025</div>
      <div class="chart-wrap">
        <svg class="linechart" viewBox="0 0 500 160">
          <defs>
            <linearGradient id="fillGrad" x1="0" y1="0" x2="0" y2="1">
              <stop offset="0%" stop-color="#ff4d4d" stop-opacity="0.2"/>
              <stop offset="100%" stop-color="#ff4d4d" stop-opacity="0"/>
            </linearGradient>
          </defs>
          <!-- grid lines -->
          <line x1="0" y1="40" x2="500" y2="40" stroke="#2a2a2a" stroke-width="1"/>
          <line x1="0" y1="80" x2="500" y2="80" stroke="#2a2a2a" stroke-width="1"/>
          <line x1="0" y1="120" x2="500" y2="120" stroke="#2a2a2a" stroke-width="1"/>
          <!-- zero line -->
          <line x1="0" y1="80" x2="500" y2="80" stroke="#606060" stroke-width="1.5" stroke-dasharray="4,3"/>
          <!-- labels -->
          <text x="60" y="155" font-family="Inconsolata" font-size="11" fill="#888888">Q1 +0.5%</text>
          <text x="183" y="155" font-family="Inconsolata" font-size="11" fill="#888888">Q2 -1.6%</text>
          <text x="303" y="155" font-family="Inconsolata" font-size="11" fill="#888888">Q3 +2.6%</text>
          <text x="413" y="155" font-family="Inconsolata" font-size="11" fill="#888888">Q4 -0.6%</text>
          <!-- area fill -->
          <path d="M 80 72 L 210 102 L 330 46 L 450 86 L 450 80 L 330 80 L 210 80 L 80 80 Z" fill="url(#fillGrad)"/>
          <!-- line -->
          <polyline points="80,72 210,102 330,46 450,86" fill="none" stroke="#ff4d4d" stroke-width="2.5" stroke-linejoin="round"/>
          <!-- dots -->
          <circle cx="80" cy="72" r="5" fill="#ff4d4d"/>
          <circle cx="210" cy="102" r="5" fill="#ff4d4d"/>
          <circle cx="330" cy="46" r="5" fill="#2ecc7a"/>
          <circle cx="450" cy="86" r="5" fill="#ff4d4d"/>
          <!-- y-axis labels -->
          <text x="2" y="44" font-family="Inconsolata" font-size="10" fill="#888888">+2.5%</text>
          <text x="2" y="84" font-family="Inconsolata" font-size="10" fill="#888888">0%</text>
          <text x="2" y="124" font-family="Inconsolata" font-size="10" fill="#888888">-2.5%</text>
        </svg>
      </div>
      <div class="source">SOURCE: STATISTICS CANADA · ANNUALIZED QUARTERLY RATES · 2025</div>
    </div>

    <div class="card">
      <div class="card-title">GDP Composition (Expenditure)</div>
      <div style="margin-top:8px">
        <div class="donut-row"><div class="donut-color" style="background:#c0392b"></div><div class="donut-name">Household Consumption</div><div class="donut-val">58%</div></div>
        <div class="donut-bar"><div class="donut-bar-fill" style="width:58%;background:#ff4d4d"></div></div>
        <div class="donut-row" style="margin-top:8px"><div class="donut-color" style="background:#1a4a7a"></div><div class="donut-name">Gross Fixed Capital</div><div class="donut-val">22%</div></div>
        <div class="donut-bar"><div class="donut-bar-fill" style="width:22%;background:#4da6ff"></div></div>
        <div class="donut-row" style="margin-top:8px"><div class="donut-color" style="background:#1a7a4a"></div><div class="donut-name">Gov't Expenditure</div><div class="donut-val">19%</div></div>
        <div class="donut-bar"><div class="donut-bar-fill" style="width:19%;background:#2ecc7a"></div></div>
        <div class="donut-row" style="margin-top:8px"><div class="donut-color" style="background:#b8860b"></div><div class="donut-name">Net Exports (Goods/Svcs)</div><div class="donut-val">-1%</div></div>
        <div class="donut-bar"><div class="donut-bar-fill" style="width:1%;background:#f0b429"></div></div>
      </div>
      <div class="source" style="margin-top:10px">SOURCE: STATISTICS CANADA · 2025</div>
    </div>
  </div>

  <div class="grid-3">
    <div class="alert alert-warn">
      <strong>⚠ Trade Headwind</strong>
      U.S. tariff uncertainty suppressed business investment and exports throughout 2025. Lower exports to the U.S. were cited by StatCan as the main contributor to Canada's slowest annual growth since 2020.
    </div>
    <div class="alert alert-good">
      <strong>✓ Consumer Resilience</strong>
      Despite headwinds, household spending remained positive — supported by BoC rate cuts (cumulative 225 bps), improving household balance sheets, and real wage growth of 3.8% YoY.
    </div>
    <div class="alert alert-info">
      <strong>ℹ CUSMA Shield</strong>
      The average effective U.S. tariff on Canadian imports remained the lowest of any major U.S. trade partner — a critical structural advantage protecting ~85% of oil & gas exports and key manufactured goods.
    </div>
  </div>
</div>

<!-- ════════════════════════ FINANCIAL ════════════════════════ -->
<div class="section" id="financial">
  <div class="sec-head"><h2>Financial Conditions</h2><span>Monetary · Fiscal · Markets</span></div>

  <div class="grid-4">
    <div class="card">
      <div class="card-title">BoC Policy Rate</div>
      <div class="card-value blue">2.25%</div>
      <div class="card-sub trend-down">▼ Cut 225 bps since June 2024</div>
      <div class="card-note">Rate held at 2.25% as of Dec 2025. BoC signaling cautious, data-dependent approach in 2026 as inflation nears target.</div>
    </div>
    <div class="card">
      <div class="card-title">CPI Inflation</div>
      <div class="card-value green">2.3%</div>
      <div class="card-sub trend-down">▼ Jan 2026 reading; near 2% target</div>
      <div class="card-note">Core inflation still running ~2.5–3%. BoC expects ongoing slack to offset tariff-related cost pressures, keeping CPI near 2%.</div>
    </div>
    <div class="card">
      <div class="card-title">Federal Debt-to-GDP</div>
      <div class="card-value amber">~42%</div>
      <div class="card-sub">Fiscal pressure rising</div>
      <div class="card-note">Defence spending hit NATO's 2% of GDP target in FY2025-26 — a significant fiscal commitment with questions around deployment and budget impact.</div>
    </div>
    <div class="card">
      <div class="card-title">CAD / USD Exchange</div>
      <div class="card-value red">~0.70</div>
      <div class="card-sub trend-down">▼ Weak dollar weighing on imports</div>
      <div class="card-note">The weak Canadian dollar raises import costs but provides a competitive edge for exporters. Persistent uncertainty tied to CUSMA renegotiation.</div>
    </div>
  </div>

  <div class="grid-2">
    <div class="card">
      <div class="card-title">Interest Rate History — BoC Overnight Rate</div>
      <div class="chart-wrap">
        <svg class="linechart" viewBox="0 0 500 160">
          <line x1="0" y1="40" x2="500" y2="40" stroke="#2a2a2a" stroke-width="1"/>
          <line x1="0" y1="80" x2="500" y2="80" stroke="#2a2a2a" stroke-width="1"/>
          <line x1="0" y1="120" x2="500" y2="120" stroke="#2a2a2a" stroke-width="1"/>
          <text x="2" y="16" font-family="Inconsolata" font-size="10" fill="#888888">5.5%</text>
          <text x="2" y="56" font-family="Inconsolata" font-size="10" fill="#888888">4.0%</text>
          <text x="2" y="96" font-family="Inconsolata" font-size="10" fill="#888888">2.5%</text>
          <text x="2" y="136" font-family="Inconsolata" font-size="10" fill="#888888">1.0%</text>
          <!-- flat near zero 2020 -->
          <text x="10" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2020</text>
          <text x="155" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2022</text>
          <text x="300" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2024</text>
          <text x="440" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2026</text>
          <!-- path: 2020 near 0 → 2022 raises → peak 5.0 mid-2023 → cuts to 2.25 -->
          <path d="M 30 128 L 100 128 L 165 108 L 230 30 L 280 26 L 340 80 L 430 95 L 470 98" fill="none" stroke="#4da6ff" stroke-width="2.5" stroke-linejoin="round"/>
          <circle cx="30" cy="128" r="4" fill="#4da6ff"/>
          <circle cx="280" cy="26" r="5" fill="#ff4d4d"/>
          <circle cx="470" cy="98" r="5" fill="#2ecc7a"/>
          <text x="250" y="22" font-family="Inconsolata" font-size="10" fill="#ff4d4d">Peak 5.0%</text>
          <text x="438" y="92" font-family="Inconsolata" font-size="10" fill="#2ecc7a">2.25%</text>
        </svg>
      </div>
      <div class="source">BANK OF CANADA · 2020–2026</div>
    </div>

    <div class="card">
      <div class="card-title">Inflation Trajectory (CPI YoY)</div>
      <div class="chart-wrap">
        <svg class="linechart" viewBox="0 0 500 160">
          <line x1="0" y1="40" x2="500" y2="40" stroke="#2a2a2a" stroke-width="1"/>
          <line x1="0" y1="80" x2="500" y2="80" stroke="#2a2a2a" stroke-width="1"/>
          <line x1="0" y1="120" x2="500" y2="120" stroke="#2a2a2a" stroke-width="1"/>
          <!-- 2% target line -->
          <line x1="0" y1="100" x2="500" y2="100" stroke="#2ecc7a" stroke-width="1.5" stroke-dasharray="5,4"/>
          <text x="410" y="96" font-family="Inconsolata" font-size="10" fill="#2ecc7a">2% target</text>
          <text x="2" y="16" font-family="Inconsolata" font-size="10" fill="#888888">8%</text>
          <text x="2" y="56" font-family="Inconsolata" font-size="10" fill="#888888">6%</text>
          <text x="2" y="96" font-family="Inconsolata" font-size="10" fill="#888888">3%</text>
          <text x="2" y="136" font-family="Inconsolata" font-size="10" fill="#888888">0%</text>
          <text x="10" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2020</text>
          <text x="155" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2022</text>
          <text x="300" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2024</text>
          <text x="440" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2026</text>
          <path d="M 30 108 L 100 110 L 165 105 L 220 20 L 265 25 L 320 80 L 390 98 L 440 104 L 470 102" fill="none" stroke="#f0b429" stroke-width="2.5" stroke-linejoin="round"/>
          <circle cx="220" cy="20" r="5" fill="#ff4d4d"/>
          <text x="190" y="16" font-family="Inconsolata" font-size="10" fill="#ff4d4d">7.9% Jun 2022</text>
        </svg>
      </div>
      <div class="source">STATISTICS CANADA · CPI YoY % CHANGE · 2020–2026</div>
    </div>
  </div>

  <div class="grid-3">
    <div class="card">
      <div class="card-title">Housing Market</div>
      <div class="card-value amber">+1.4%</div>
      <div class="card-sub">2025 national avg. home price change</div>
      <div class="card-note">Pre-construction condo sales in GTA down ~90% vs. 9-year average. Starts expected to fall 10%+ in 2026 and 2027 as population growth stalls.</div>
    </div>
    <div class="card">
      <div class="card-title">Household Debt-to-Income</div>
      <div class="card-value red">~180%</div>
      <div class="card-sub">Among highest in G7</div>
      <div class="card-note">High household leverage remains a structural vulnerability. Rate cuts are easing debt servicing costs but the underlying stock of debt remains elevated.</div>
    </div>
    <div class="card">
      <div class="card-title">TSX (Toronto Stock Exchange)</div>
      <div class="card-value blue">10th</div>
      <div class="card-sub">Largest exchange by market cap globally</div>
      <div class="card-note">Over 1,500 listed companies. Dominated by financials, energy, and materials. Equity valuations have been a positive wealth effect supporting consumer spending.</div>
    </div>
  </div>
</div>

<!-- ════════════════════════ JOBS & LABOUR ════════════════════════ -->
<div class="section" id="jobs">
  <div class="sec-head"><h2>Jobs & Labour Market</h2><span>Employment · Wages · Sectors</span></div>

  <div class="grid-4">
    <div class="card">
      <div class="card-title">Unemployment Rate</div>
      <div class="card-value amber">6.5%</div>
      <div class="card-sub">Jan 2026 · down from 6.8% in Dec</div>
      <div class="card-note">Still elevated — roughly 1 point above year-ago levels and near decade-highs outside COVID. Tariff pressure hit trade-sensitive sectors hardest.</div>
    </div>
    <div class="card">
      <div class="card-title">Total Employed</div>
      <div class="card-value green">21.1M</div>
      <div class="card-sub">Net positions as of Jan 2026</div>
      <div class="card-note">~181,000 new jobs added Sept–Nov 2025 after near-zero gains in H1. Jan 2026 lost 25k net positions, but full-time work rose 45k.</div>
    </div>
    <div class="card">
      <div class="card-title">Average Hourly Wage</div>
      <div class="card-value">$36.14</div>
      <div class="card-sub trend-up">▲ +3.8% YoY</div>
      <div class="card-note">Wage growth above inflation but cooling from 2023 highs. No longer a significant contributor to inflationary pressure — conditions reflect an employer's market.</div>
    </div>
    <div class="card">
      <div class="card-title">Participation Rate</div>
      <div class="card-value blue">65.0%</div>
      <div class="card-sub">Lowest since May 2021</div>
      <div class="card-note">Drop partly explained by more youth attending school. Demographic slowdown expected to reduce labour force growth through 2028.</div>
    </div>
  </div>

  <div class="grid-2">
    <div class="card">
      <div class="card-title">Employment by Sector (Est. Share of 21.1M Jobs)</div>
      <div class="bar-chart" style="margin-top:8px">
        <div class="bar-row"><div class="bar-label">Services (Total)</div><div class="bar-track"><div class="bar-fill bar-maple" style="width:77%"><span>77%</span></div></div></div>
        <div class="bar-row"><div class="bar-label">Healthcare & Social</div><div class="bar-track"><div class="bar-fill bar-blue" style="width:14%"><span>14%</span></div></div></div>
        <div class="bar-row"><div class="bar-label">Trade (Retail/Wholesale)</div><div class="bar-track"><div class="bar-fill bar-blue" style="width:15%"><span>15%</span></div></div></div>
        <div class="bar-row"><div class="bar-label">Construction</div><div class="bar-track"><div class="bar-fill bar-amber" style="width:8%"><span>8%</span></div></div></div>
        <div class="bar-row"><div class="bar-label">Manufacturing</div><div class="bar-track"><div class="bar-fill bar-amber" style="width:9%"><span>9%</span></div></div></div>
        <div class="bar-row"><div class="bar-label">Finance & Insurance</div><div class="bar-track"><div class="bar-fill bar-green" style="width:7%"><span>7%</span></div></div></div>
        <div class="bar-row"><div class="bar-label">Prof., Sci. & Tech.</div><div class="bar-track"><div class="bar-fill bar-green" style="width:8%"><span>8%</span></div></div></div>
        <div class="bar-row"><div class="bar-label">Natural Resources</div><div class="bar-track"><div class="bar-fill bar-muted" style="width:4%"><span>4%</span></div></div></div>
        <div class="bar-row"><div class="bar-label">Tech (Ontario alone)</div><div class="bar-track"><div class="bar-fill" style="width:8%;background:#a07aff"><span>8%</span></div></div></div>
      </div>
      <div class="source">STATISTICS CANADA · LABOUR FORCE SURVEY · 2025</div>
    </div>

    <div class="card">
      <div class="card-title">Unemployment Rate — Historical Trend</div>
      <div class="chart-wrap">
        <svg class="linechart" viewBox="0 0 500 160">
          <line x1="0" y1="40" x2="500" y2="40" stroke="#2a2a2a" stroke-width="1"/>
          <line x1="0" y1="80" x2="500" y2="80" stroke="#2a2a2a" stroke-width="1"/>
          <line x1="0" y1="120" x2="500" y2="120" stroke="#2a2a2a" stroke-width="1"/>
          <text x="2" y="16" font-family="Inconsolata" font-size="10" fill="#888888">12%</text>
          <text x="2" y="56" font-family="Inconsolata" font-size="10" fill="#888888">8%</text>
          <text x="2" y="96" font-family="Inconsolata" font-size="10" fill="#888888">5%</text>
          <text x="2" y="136" font-family="Inconsolata" font-size="10" fill="#888888">2%</text>
          <text x="10" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2019</text>
          <text x="120" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2020</text>
          <text x="230" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2022</text>
          <text x="350" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2024</text>
          <text x="450" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2026</text>
          <!-- spike during COVID then recovery then slight rise -->
          <path d="M 30 96 L 100 96 L 120 24 L 160 55 L 210 82 L 260 88 L 310 88 L 350 84 L 390 100 L 430 104 L 470 104" fill="none" stroke="#f0b429" stroke-width="2.5" stroke-linejoin="round"/>
          <circle cx="120" cy="24" r="5" fill="#ff4d4d"/>
          <text x="85" y="20" font-family="Inconsolata" font-size="10" fill="#ff4d4d">13.7% COVID peak</text>
          <!-- low point -->
          <circle cx="310" cy="88" r="4" fill="#2ecc7a"/>
          <text x="275" y="83" font-family="Inconsolata" font-size="10" fill="#2ecc7a">5.2% low</text>
          <circle cx="470" cy="104" r="4" fill="#f0b429"/>
        </svg>
      </div>
      <div class="source">STATISTICS CANADA · LFS · 2019–2026</div>
    </div>
  </div>

  <div class="card" style="margin-bottom:24px">
    <div class="card-title">Top Growing Job Categories (2025–2026)</div>
    <table class="sector-table">
      <thead><tr><th>Sector</th><th>Key Roles</th><th>YoY Change</th><th>Wage Premium</th><th>Outlook</th></tr></thead>
      <tbody>
        <tr><td><strong>Technology & AI</strong></td><td>AI Engineers, Cloud Architects, DevSecOps</td><td><span class="pill pill-up">▲ +2.3%</span></td><td>+22–40% vs. avg</td><td>Strong — Toronto, Montreal, Vancouver hubs</td></tr>
        <tr><td><strong>Healthcare</strong></td><td>Nurses, PSWs, Diagnostics, Biotech</td><td><span class="pill pill-up">▲ +3.2%</span></td><td>Stable, union-backed</td><td>Aging population drives structural demand</td></tr>
        <tr><td><strong>Construction</strong></td><td>Trades, Project Mgmt, Infrastructure</td><td><span class="pill pill-up">▲ +2.3%</span></td><td>+15–25% vs. avg</td><td>Infrastructure & defence spending surge</td></tr>
        <tr><td><strong>Finance & Insurance</strong></td><td>Analysts, Compliance, Fintech</td><td><span class="pill pill-watch">→ Flat</span></td><td>High</td><td>Stable but under fintech disruption pressure</td></tr>
        <tr><td><strong>Manufacturing</strong></td><td>Advanced Mfg, EV supply chain</td><td><span class="pill pill-down">▼ -0.8%</span></td><td>Avg</td><td>Tariff headwinds; EV pivot a medium-term opportunity</td></tr>
        <tr><td><strong>Natural Resources</strong></td><td>Mining, Oil & Gas, Forestry</td><td><span class="pill pill-watch">→ Stable</span></td><td>High in AB/SK</td><td>Critical minerals growth; oil production stable</td></tr>
      </tbody>
    </table>
  </div>
</div>

<!-- ════════════════════════ SECTORS ════════════════════════ -->
<div class="section" id="sectors">
  <div class="sec-head"><h2>Growth Sectors</h2><span>Leading Industries & Regional Divergence</span></div>

  <div class="grid-3">
    <div class="card">
      <div class="card-title">🤖 Artificial Intelligence</div>
      <div class="card-value green">$2B+</div>
      <div class="card-sub">Federal AI compute investment (Budget 2025)</div>
      <div class="card-note">Canada is a global AI leader anchored in Toronto, Montreal, and Vancouver. Budget 2025 committed $925.6M for sovereign AI compute capacity. Cohere (Toronto) finalized federal backing. AI employment in tech-adjacent roles +2.3% YoY.</div>
    </div>
    <div class="card">
      <div class="card-title">⚡ Clean Technology</div>
      <div class="card-value green">82%</div>
      <div class="card-sub">Canada's electricity grid is clean energy</div>
      <div class="card-note">Canada's clean grid is a global competitive advantage. Government targets carbon capture, critical minerals, EV tech, and sustainable manufacturing. The Strategic Innovation Fund explicitly prioritizes cleantech as a pillar sector.</div>
    </div>
    <div class="card">
      <div class="card-title">⛏️ Critical Minerals</div>
      <div class="card-value blue">$383B</div>
      <div class="card-sub">Natural resource exports (2024)</div>
      <div class="card-note">53% of all Canadian merchandise exports. Cobalt, lithium, nickel, uranium, and rare earths are strategic priorities for global EV and defence supply chains. U.S. defence grant awarded for cobalt refinery in Ontario.</div>
    </div>
    <div class="card">
      <div class="card-title">🧬 Life Sciences & Biotech</div>
      <div class="card-value">Growing</div>
      <div class="card-sub">Recession-resilient sector</div>
      <div class="card-note">Aging population + demand for personalized medicine driving structural growth. Government-backed biomanufacturing investments through Strategic Innovation Fund. AI-driven drug discovery (ProteinQure, etc.) gaining traction.</div>
    </div>
    <div class="card">
      <div class="card-title">🏗️ Infrastructure & Defence</div>
      <div class="card-value amber">2.0%</div>
      <div class="card-sub">of GDP NATO commitment (FY2025-26)</div>
      <div class="card-note">Defence spending was the largest single item in the federal budget — a 45.9% annual rise in weapons expenditure. Investors are increasingly looking to defence and construction stocks as Canada fast-tracks "nation-building" projects.</div>
    </div>
    <div class="card">
      <div class="card-title">🔬 Quantum Computing</div>
      <div class="card-value blue">$334M</div>
      <div class="card-sub">5-year Defence Industrial Strategy allocation</div>
      <div class="card-note">Canada launched its National Quantum Strategy with $360M. Projected global quantum sector value: US$139B. Applications in cybersecurity, finance, drug discovery, and logistics align with Canada's strengths.</div>
    </div>
  </div>

  <div class="card" style="margin-bottom:24px">
    <div class="card-title">Provincial GDP Growth Leaders 2025–2026</div>
    <div class="province-grid">
      <div class="prov-card">
        <div class="prov-name">🛢️ Alberta</div>
        <div class="prov-gdp">GDP Growth: ~2.0% (2026F)</div>
        <div class="prov-tag"><span class="pill pill-up">STRONG</span></div>
        <div style="font-size:12px;color:var(--muted);margin-top:6px">Trans Mountain pipeline, oil & gas CUSMA protection, population inflows</div>
      </div>
      <div class="prov-card">
        <div class="prov-name">⚗️ Saskatchewan</div>
        <div class="prov-gdp">GDP Growth: ~2.0% (2026F)</div>
        <div class="prov-tag"><span class="pill pill-up">STRONG</span></div>
        <div style="font-size:12px;color:var(--muted);margin-top:6px">Potash, uranium investment. Near all-time high resale market.</div>
      </div>
      <div class="prov-card">
        <div class="prov-name">🌊 Newfoundland & Labrador</div>
        <div class="prov-gdp">GDP Growth: ~1.8% (2026F)</div>
        <div class="prov-tag"><span class="pill pill-up">LEADING</span></div>
        <div style="font-size:12px;color:var(--muted);margin-top:6px">Oil production resumption at White Rose; Vale Voisey Bay nickel expansion</div>
      </div>
      <div class="prov-card">
        <div class="prov-name">🌲 British Columbia</div>
        <div class="prov-gdp">GDP Growth: ~1.7% (2026F)</div>
        <div class="prov-tag"><span class="pill pill-up">POSITIVE</span></div>
        <div style="font-size:12px;color:var(--muted);margin-top:6px">LNG exports, tech hub (Vancouver AI), Asian trade diversification</div>
      </div>
      <div class="prov-card">
        <div class="prov-name">🏙️ Ontario</div>
        <div class="prov-gdp">GDP Growth: ~0.8% (2026F)</div>
        <div class="prov-tag"><span class="pill pill-watch">MODERATE</span></div>
        <div style="font-size:12px;color:var(--muted);margin-top:6px">Tariff headwinds on manufacturing; 48% of Canada's tech workforce</div>
      </div>
      <div class="prov-card">
        <div class="prov-name">🥐 Quebec</div>
        <div class="prov-gdp">GDP Growth: ~0.7% (2026F)</div>
        <div class="prov-tag"><span class="pill pill-watch">MODERATE</span></div>
        <div style="font-size:12px;color:var(--muted);margin-top:6px">AI hub in Montreal; manufacturing exposure to tariffs a headwind</div>
      </div>
    </div>
    <div class="source" style="margin-top:12px">SOURCE: SIGNAL49 RESEARCH (FMR. CONFERENCE BOARD OF CANADA) · RBC ECONOMICS · 2025</div>
  </div>
</div>

<!-- ════════════════════════ INNOVATION ════════════════════════ -->
<div class="section" id="innovation">
  <div class="sec-head"><h2>Innovation Economy</h2><span>R&D · Startups · IP · Tech Hubs</span></div>

  <div class="grid-4">
    <div class="card">
      <div class="card-title">SR&ED R&D Tax Support</div>
      <div class="card-value blue">$4.2B</div>
      <div class="card-sub">Annual business R&D incentives</div>
      <div class="card-note">Budget 2025 expanded SR&ED — raised enhanced credit limit to $4.5M, extended 35% tax credit to public corps, restored capital expenditure eligibility.</div>
    </div>
    <div class="card">
      <div class="card-title">Tech Jobs (Ontario)</div>
      <div class="card-value green">690K+</div>
      <div class="card-sub">~8% of Ontario employment</div>
      <div class="card-note">Toronto alone projected to have 414,000+ tech jobs in 2025. Toronto ranks top 5 North American cities for AI competitiveness (CBRE, 2024).</div>
    </div>
    <div class="card">
      <div class="card-title">Sovereign AI Compute</div>
      <div class="card-value amber">$925M</div>
      <div class="card-sub">5-year Budget 2025 commitment</div>
      <div class="card-note">Canada's Sovereign AI Compute Strategy ensures domestic AI infrastructure independence. AI Compute Access Fund now active for startups and researchers.</div>
    </div>
    <div class="card">
      <div class="card-title">Industrial Automation CAGR</div>
      <div class="card-value red">56%</div>
      <div class="card-sub">2024–2030 projected growth rate</div>
      <div class="card-note">Canada's process automation market valued at $1.21B in 2023, forecast to reach $1.88B by 2030. AI-powered RPA, analytics, and IoT driving the shift.</div>
    </div>
  </div>

  <div class="grid-3" style="margin-bottom:24px">
    <div class="innov-card">
      <div class="innov-icon">🧠</div>
      <div>
        <h4>AI Leadership</h4>
        <p>Canada is among the top global AI nations with world-class research in Toronto (Vector Institute), Montreal (Mila), and Edmonton (Alberta Machine Intelligence). Pan-Canadian AI Strategy now in Phase 2 commercialization focus.</p>
        <span class="tag">GLOBAL LEADER</span>
      </div>
    </div>
    <div class="innov-card">
      <div class="innov-icon">🌱</div>
      <div>
        <h4>Cleantech & Net Zero</h4>
        <p>82% clean electricity grid is a global competitive edge. Key areas: carbon capture, critical minerals, EV batteries, sustainable manufacturing. New "Made-in-Canada" sustainable investment guidelines in development.</p>
        <span class="tag">STRATEGIC PRIORITY</span>
      </div>
    </div>
    <div class="innov-card">
      <div class="innov-icon">⚛️</div>
      <div>
        <h4>Quantum Computing</h4>
        <p>National Quantum Strategy (NQS) launched with $360M. Three missions: global quantum leadership, secure quantum communications, and quantum sensing for industry. Projected to become a $139B sector globally.</p>
        <span class="tag">EMERGING</span>
      </div>
    </div>
    <div class="innov-card">
      <div class="innov-icon">🏦</div>
      <div>
        <h4>Fintech & Blockchain</h4>
        <p>Blockchain in Canada projected to reach $40B (2025). Toronto and Vancouver are leading fintech hubs. AI-driven financial modelling, credit scoring, and embedded finance are top growth areas in 2025.</p>
        <span class="tag">HIGH GROWTH</span>
      </div>
    </div>
    <div class="innov-card">
      <div class="innov-icon">🧬</div>
      <div>
        <h4>Life Sciences & AI Drug Discovery</h4>
        <p>Government-backed biomanufacturing through the Strategic Innovation Fund. Companies like ProteinQure (AI-designed peptide cancer drugs) entering clinical trials. Genomics and cell/gene therapy emerging.</p>
        <span class="tag">LONG-TERM GROWTH</span>
      </div>
    </div>
    <div class="innov-card">
      <div class="innov-icon">🛡️</div>
      <div>
        <h4>Cybersecurity & Defence Tech</h4>
        <p>$334.3M over 5 years for the quantum ecosystem under Defence Industrial Strategy. Growing demand for DevSecOps, cloud security, and infrastructure protection as Canada scales defence spending to 2%+ of GDP.</p>
        <span class="tag">SCALING FAST</span>
      </div>
    </div>
  </div>
</div>

<!-- ════════════════════════ RESOURCES & ASSETS ════════════════════════ -->
<div class="section" id="resources">
  <div class="sec-head"><h2>Resources & National Assets</h2><span>Energy · Minerals · Agriculture · Infrastructure</span></div>

  <div class="grid-4">
    <div class="card">
      <div class="card-title">Natural Resource Exports</div>
      <div class="card-value green">$383B</div>
      <div class="card-sub">53% of all merchandise exports (2024)</div>
      <div class="card-note">Rose from $370B in 2023. Top partners: USA 75%, China 6%, UK 4%, Japan 2%, South Korea 1%.</div>
    </div>
    <div class="card">
      <div class="card-title">Oil Reserves</div>
      <div class="card-value blue">3rd</div>
      <div class="card-sub">Largest proven oil reserves globally</div>
      <div class="card-note">~170B barrels in oil sands (Alberta). Trans Mountain Pipeline Expansion (TMX) operational — opens Pacific access. ~85% of oil & gas exports remain tariff-free to U.S.</div>
    </div>
    <div class="card">
      <div class="card-title">Clean Electricity Grid</div>
      <div class="card-value green">82%</div>
      <div class="card-sub">Clean energy (hydro, nuclear, wind, solar)</div>
      <div class="card-note">Hydro dominates (60%+). Canada's clean grid is a key competitive advantage for attracting AI data centres, EV manufacturing, and clean hydrogen production.</div>
    </div>
    <div class="card">
      <div class="card-title">Freshwater Reserves</div>
      <div class="card-value blue">20%</div>
      <div class="card-sub">Of the world's surface freshwater</div>
      <div class="card-note">Canada holds approximately 20% of global surface fresh water and 7% of renewable fresh water — an increasingly strategic asset in a warming world.</div>
    </div>
  </div>

  <div class="grid-2">
    <div class="card">
      <div class="card-title">Key Resource Sectors by Export Value</div>
      <div class="bar-chart" style="margin-top:8px">
        <div class="bar-row"><div class="bar-label">Oil & Gas Energy</div><div class="bar-track"><div class="bar-fill bar-maple" style="width:70%"><span>~$270B</span></div></div></div>
        <div class="bar-row"><div class="bar-label">Minerals & Metals</div><div class="bar-track"><div class="bar-fill bar-blue" style="width:30%"><span>~$80B</span></div></div></div>
        <div class="bar-row"><div class="bar-label">Forestry & Wood</div><div class="bar-track"><div class="bar-fill bar-green" style="width:18%"><span>~$50B</span></div></div></div>
        <div class="bar-row"><div class="bar-label">Agriculture & Food</div><div class="bar-track"><div class="bar-fill bar-amber" style="width:16%"><span>~$45B</span></div></div></div>
        <div class="bar-row"><div class="bar-label">Seafood & Marine</div><div class="bar-track"><div class="bar-fill bar-muted" style="width:6%"><span>~$8B</span></div></div></div>
      </div>
      <div class="source">NATURAL RESOURCES CANADA · 2024 ESTIMATES</div>
    </div>

    <div class="card">
      <div class="card-title">Critical Minerals — Strategic Priority Map</div>
      <table class="sector-table">
        <thead><tr><th>Mineral</th><th>Use</th><th>Status</th></tr></thead>
        <tbody>
          <tr><td>🔋 Lithium</td><td>EV Batteries</td><td><span class="pill pill-up">HIGH DEMAND</span></td></tr>
          <tr><td>⚙️ Cobalt</td><td>Batteries, Defence</td><td><span class="pill pill-up">U.S. Strategic</span></td></tr>
          <tr><td>🪨 Nickel</td><td>Steel, EV Batteries</td><td><span class="pill pill-up">Voisey Bay ↑</span></td></tr>
          <tr><td>☢️ Uranium</td><td>Nuclear Energy</td><td><span class="pill pill-up">Surging Demand</span></td></tr>
          <tr><td>🌱 Potash</td><td>Fertilizer</td><td><span class="pill pill-up">SK Leading</span></td></tr>
          <tr><td>✨ Rare Earths</td><td>Defence, Electronics</td><td><span class="pill pill-watch">Developing</span></td></tr>
        </tbody>
      </table>
    </div>
  </div>

  <div class="grid-3">
    <div class="card">
      <div class="card-title">Agriculture</div>
      <div class="card-value green">Top 5</div>
      <div class="card-sub">Global agricultural exporter</div>
      <div class="card-note">Major exporter of wheat, canola, pulses, and pork. Chinese tariffs on Canadian agriculture (~25%) are a headwind — seafood to China dropped 34% YTD, though Europe is absorbing some demand.</div>
    </div>
    <div class="card">
      <div class="card-title">Forestry</div>
      <div class="card-value amber">Challenged</div>
      <div class="card-sub">Lumber under pressure</div>
      <div class="card-note">U.S. softwood lumber duties continue to squeeze margins. Housing slowdown at home and in the U.S. reduces demand. Saw industry adaptation and diversification are in progress.</div>
    </div>
    <div class="card">
      <div class="card-title">Foreign Direct Investment</div>
      <div class="card-value blue">$331B</div>
      <div class="card-sub">CDIA in natural resources (2024)</div>
      <div class="card-note">Canadian direct investment abroad in natural resources grew 56.1% over the past decade to $331B. FDI inbound to Canada's resource sector declined 4.9% over the same period.</div>
    </div>
  </div>
</div>

<!-- ════════════════════════ POPULATION ════════════════════════ -->
<div class="section" id="population">
  <div class="sec-head"><h2>Population & Demographics</h2><span>Growth · Immigration · Age Structure</span></div>

  <div class="grid-4">
    <div class="card">
      <div class="card-title">Total Population</div>
      <div class="card-value">~41M</div>
      <div class="card-sub">2025 estimate</div>
      <div class="card-note">Crossed 40M in 2023 — a historic milestone. Growth now sharply decelerating as federal immigration targets are revised downward.</div>
    </div>
    <div class="card">
      <div class="card-title">Pop. Growth Rate (Q3 2025)</div>
      <div class="card-value red">0.3%</div>
      <div class="card-sub">Annualized · Slowest outside pandemic</div>
      <div class="card-note">Decline in temporary resident arrivals + uptick in outflows. Parliamentary Budget Officer projects zero or even negative population growth in 2026 — first time since Confederation.</div>
    </div>
    <div class="card">
      <div class="card-title">Immigration Targets (2025)</div>
      <div class="card-value amber">~395K</div>
      <div class="card-sub">Permanent residents (down from 500K)</div>
      <div class="card-note">Government significantly cut immigration targets after years of 750K+ annual arrivals. Policy now focused on reducing non-permanent residents — international students and TFWs.</div>
    </div>
    <div class="card">
      <div class="card-title">Aging Population</div>
      <div class="card-value blue">18%</div>
      <div class="card-sub">Aged 65+ (growing rapidly)</div>
      <div class="card-note">By 2030, nearly 1 in 4 Canadians will be 65+. This is the key long-term structural driver for healthcare, seniors housing, and pension system pressure.</div>
    </div>
  </div>

  <div class="grid-2">
    <div class="card">
      <div class="card-title">Population Growth History & Outlook</div>
      <div class="chart-wrap">
        <svg class="linechart" viewBox="0 0 500 160">
          <line x1="0" y1="40" x2="500" y2="40" stroke="#2a2a2a" stroke-width="1"/>
          <line x1="0" y1="80" x2="500" y2="80" stroke="#2a2a2a" stroke-width="1"/>
          <line x1="0" y1="120" x2="500" y2="120" stroke="#2a2a2a" stroke-width="1"/>
          <text x="2" y="16" font-family="Inconsolata" font-size="10" fill="#888888">1.0M/yr</text>
          <text x="2" y="56" font-family="Inconsolata" font-size="10" fill="#888888">600K/yr</text>
          <text x="2" y="96" font-family="Inconsolata" font-size="10" fill="#888888">200K/yr</text>
          <text x="2" y="136" font-family="Inconsolata" font-size="10" fill="#888888">~0</text>
          <text x="10" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2019</text>
          <text x="120" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2021</text>
          <text x="240" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2023</text>
          <text x="370" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2025</text>
          <text x="440" y="155" font-family="Inconsolata" font-size="10" fill="#888888">2026F</text>
          <!-- pop growth: pre-pandemic steady, COVID dip, massive surge post-pandemic, now dropping -->
          <path d="M 30 90 L 80 88 L 120 118 L 170 82 L 230 42 L 290 30 L 340 42 L 400 100 L 450 132 L 480 138" fill="none" stroke="#ff4d4d" stroke-width="2.5" stroke-linejoin="round"/>
          <circle cx="290" cy="30" r="5" fill="#ff4d4d"/>
          <text x="255" y="26" font-family="Inconsolata" font-size="10" fill="#ff4d4d">Record ~1M (2023)</text>
          <circle cx="480" cy="138" r="5" fill="#f0b429"/>
          <text x="390" y="135" font-family="Inconsolata" font-size="10" fill="#f0b429">Near zero (2026F)</text>
        </svg>
      </div>
      <div class="source">STATISTICS CANADA · PARLIAMENTARY BUDGET OFFICE · 2019–2026</div>
    </div>

    <div class="card">
      <div class="card-title">Demographic Age Distribution (Est. 2025)</div>
      <div class="bar-chart" style="margin-top:8px">
        <div class="bar-row"><div class="bar-label">0–14 (Youth)</div><div class="bar-track"><div class="bar-fill bar-blue" style="width:16%"><span>16%</span></div></div></div>
        <div class="bar-row"><div class="bar-label">15–24 (Young Adult)</div><div class="bar-track"><div class="bar-fill bar-blue" style="width:12%"><span>12%</span></div></div></div>
        <div class="bar-row"><div class="bar-label">25–44 (Prime Working)</div><div class="bar-track"><div class="bar-fill bar-maple" style="width:28%"><span>28%</span></div></div></div>
        <div class="bar-row"><div class="bar-label">45–64 (Late Working)</div><div class="bar-track"><div class="bar-fill bar-amber" style="width:26%"><span>26%</span></div></div></div>
        <div class="bar-row"><div class="bar-label">65+ (Senior)</div><div class="bar-track"><div class="bar-fill bar-muted" style="width:18%"><span>18%</span></div></div></div>
      </div>
      <div style="margin-top:12px">
        <div class="alert alert-warn" style="margin-bottom:0">
          <strong>⚠ Demographic Pressure</strong>
          The 65+ cohort is growing fastest, driving healthcare demand, pension costs, and eventual labour shortages. The 20–35 age group — key renters and entry-level buyers — is set to shrink over the next decade.
        </div>
      </div>
    </div>
  </div>
</div>

<!-- ════════════════════════ 10-YEAR OUTLOOK ════════════════════════ -->
<div class="section" id="forecast">
  <div class="sec-head"><h2>10-Year Economic Outlook</h2><span>2025–2035 Projections & Scenarios</span></div>

  <div class="forecast-grid" style="margin-bottom:24px">
    <div class="fc-cell">
      <div class="fc-year">2025</div>
      <div class="fc-val fc-neutral">1.7%</div>
      <div class="fc-label">GDP (Actual)</div>
    </div>
    <div class="fc-cell">
      <div class="fc-year">2026</div>
      <div class="fc-val fc-neutral">~1.4%</div>
      <div class="fc-label">GDP (BoC Forecast)</div>
    </div>
    <div class="fc-cell">
      <div class="fc-year">2027</div>
      <div class="fc-val fc-positive">~1.8%</div>
      <div class="fc-label">GDP (Vanguard Est.)</div>
    </div>
    <div class="fc-cell">
      <div class="fc-year">2030</div>
      <div class="fc-val fc-positive">~2.2%</div>
      <div class="fc-label">GDP (IMF Projection)</div>
    </div>
    <div class="fc-cell">
      <div class="fc-year">2035</div>
      <div class="fc-val fc-positive">~2.5%</div>
      <div class="fc-label">GDP (Trend Estimate)</div>
    </div>
  </div>

  <div class="grid-2" style="margin-bottom:24px">
    <div class="card">
      <div class="card-title">10-Year Timeline: Key Inflection Points</div>
      <div class="timeline" style="margin-top:8px">
        <div class="tl-item">
          <div class="tl-year">2025–2026</div>
          <div class="tl-text">Structural adjustment to U.S. trade policy. Population growth near zero. Per-capita GDP recovery begins. AI and defence investment surge. CUSMA renegotiation critical.</div>
        </div>
        <div class="tl-item">
          <div class="tl-year">2026–2027</div>
          <div class="tl-text">Labour market stabilization. Business investment expected to rebound as trade uncertainty clears. Housing starts near cycle bottom. Critical minerals ramp-up accelerates.</div>
        </div>
        <div class="tl-item">
          <div class="tl-year">2027–2028</div>
          <div class="tl-text">Productivity improvements from AI adoption begin contributing to GDP. Energy sector revenues strengthen with TMX, White Rose, and Bay du Nord. Unemployment declines toward 6.5%.</div>
        </div>
        <div class="tl-item">
          <div class="tl-year">2028–2030</div>
          <div class="tl-text">Clean technology export revenues build. Quantum computing and AI-adjacent sectors mature. 65+ population crosses 21% — healthcare and senior housing become dominant demand drivers.</div>
        </div>
        <div class="tl-item">
          <div class="tl-year">2030–2035</div>
          <div class="tl-text">Canada potentially a net exporter of clean electricity and hydrogen. Critical minerals strategic importance reaches peak. Demographic labour shortage may require renewed calibrated immigration.</div>
        </div>
      </div>
    </div>

    <div class="card">
      <div class="card-title">Risk & Opportunity Matrix</div>
      <table class="sector-table">
        <thead><tr><th>Factor</th><th>Direction</th><th>Magnitude</th></tr></thead>
        <tbody>
          <tr><td><strong>U.S. Trade Relations / CUSMA</strong></td><td><span class="pill pill-down">Risk</span></td><td>Very High</td></tr>
          <tr><td><strong>Critical Minerals Demand</strong></td><td><span class="pill pill-up">Opportunity</span></td><td>Very High</td></tr>
          <tr><td><strong>AI Leadership & Compute</strong></td><td><span class="pill pill-up">Opportunity</span></td><td>High</td></tr>
          <tr><td><strong>Population Aging / Labour</strong></td><td><span class="pill pill-down">Risk</span></td><td>High (Structural)</td></tr>
          <tr><td><strong>Clean Energy Advantage</strong></td><td><span class="pill pill-up">Opportunity</span></td><td>High (Long-term)</td></tr>
          <tr><td><strong>Household Debt Levels</strong></td><td><span class="pill pill-down">Risk</span></td><td>Medium</td></tr>
          <tr><td><strong>Housing Construction Decline</strong></td><td><span class="pill pill-down">Risk</span></td><td>Medium</td></tr>
          <tr><td><strong>Productivity Growth Gap</strong></td><td><span class="pill pill-watch">Watch</span></td><td>High (Structural)</td></tr>
          <tr><td><strong>Defence Spending Surge</strong></td><td><span class="pill pill-up">Opportunity</span></td><td>Medium</td></tr>
          <tr><td><strong>China Trade Diversification</strong></td><td><span class="pill pill-watch">Watch</span></td><td>Medium</td></tr>
        </tbody>
      </table>
    </div>
  </div>

  <div class="grid-3">
    <div class="alert alert-warn">
      <strong>⚠ Structural Challenge: Productivity</strong>
      Canada's long-running business underinvestment has created a productivity gap vs. the U.S. and other G7 peers. GDP per hour worked has lagged for over a decade — AI adoption is the most cited potential remedy, but execution remains uncertain.
    </div>
    <div class="alert alert-good">
      <strong>✓ Long-Term Advantage: Resources</strong>
      Canada's combination of oil sands, freshwater, critical minerals, clean electricity, and agricultural land positions it uniquely for a world transitioning to electrification, decarbonization, and resource security. These are durable multi-decade strengths.
    </div>
    <div class="alert alert-info">
      <strong>ℹ Wildcard: CUSMA Renegotiation</strong>
      The renegotiation of the Canada-United States-Mexico Agreement is the single greatest binary risk to Canada's 10-year trajectory. A favourable outcome stabilizes the outlook; failure would represent the largest economic shock since the 2008 financial crisis.
    </div>
  </div>
</div>

</div><!-- end .content -->

<script>
  function showTab(id) {
    document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
    document.querySelectorAll('.nav-tab').forEach(t => t.classList.remove('active'));
    document.getElementById(id).classList.add('active');
    event.target.classList.add('active');
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }
</script>
</body>
</html>
