CANADA OUTLOOK
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Canada Economic Dashboard — August 2026</title>
<style>
  :root{
    --paper:#F4F6F8;
    --surface:#FFFFFF;
    --surface-2:#F7F9FA;
    --ink:#1B242C;
    --ink-2:#5B6872;
    --ink-3:#8B97A1;
    --rule:#DCE2E7;
    --rule-soft:#EAEEF1;
    --spruce:#15704E;
    --spruce-soft:#E8F2EE;
    --rust:#B03A2E;
    --rust-soft:#FAEBE9;
    --amber:#8F6D1C;
    --amber-soft:#F8F0DE;
    --slate:#215C8F;
    --slate-soft:#E9F0F6;
    --sans: ui-sans-serif,-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue","Inter",Arial,sans-serif;
  }
  *{box-sizing:border-box}
  html{scroll-behavior:smooth}
  @media (prefers-reduced-motion: reduce){html{scroll-behavior:auto} *{transition:none!important;animation:none!important}}
  body{
    margin:0; background:var(--paper); color:var(--ink);
    font-family:var(--sans); font-size:16px; line-height:1.62;
    -webkit-font-smoothing:antialiased; -moz-osx-font-smoothing:grayscale;
  }
  .num,.ui{font-variant-numeric:tabular-nums; font-feature-settings:"tnum" 1}

  /* ---------- shell ---------- */
  .shell{display:flex; align-items:flex-start; max-width:1400px; margin:0 auto}
  nav.rail{
    position:sticky; top:0; flex:0 0 236px; height:100vh; overflow-y:auto;
    padding:34px 20px 40px 28px; border-right:1px solid var(--rule);
    background:var(--paper);
  }
  .rail .mark{font-family:var(--sans); font-weight:700; font-size:14px; letter-spacing:-.01em; line-height:1.35; margin-bottom:4px}
  .rail .mark span{display:block; font-weight:450; color:var(--ink-2); font-size:12.5px}
  .rail ol{list-style:none; margin:26px 0 0; padding:0; font-family:var(--sans); font-size:13.5px}
  .rail li{margin:0}
  .rail a{
    display:block; padding:6px 10px 6px 12px; color:var(--ink-2); text-decoration:none;
    border-left:2px solid transparent; transition:color .12s, border-color .12s;
  }
  .rail a:hover{color:var(--ink)}
  .rail a.on{color:var(--ink); border-left-color:var(--rust); font-weight:600}
  .rail a:focus-visible,button:focus-visible,select:focus-visible,summary:focus-visible{outline:2px solid var(--slate); outline-offset:2px}
  main{flex:1 1 auto; min-width:0; padding:0 clamp(20px,4vw,64px) 120px}

  /* ---------- hero ---------- */
  header.hero{padding:52px 0 30px; border-bottom:1px solid var(--rule)}
  h1{font-size:clamp(31px,4.1vw,45px); line-height:1.1; margin:0 0 16px; font-weight:650; letter-spacing:-.028em; max-width:17ch}
  .standfirst{font-size:18px; line-height:1.55; color:var(--ink-2); max-width:64ch; margin:0 0 26px; font-weight:400}
  .asof{font-family:var(--sans); font-size:12.5px; color:var(--ink-3); display:flex; flex-wrap:wrap; gap:18px; margin-bottom:30px}
  .asof b{color:var(--ink-2); font-weight:600}

  /* exposure band — the signature element */
  .band{background:var(--surface); border:1px solid var(--rule); border-radius:3px; padding:22px 24px 20px}
  .band h2{font-family:var(--sans); font-size:14px; margin:0 0 4px; font-weight:650}
  .band p.sub{font-family:var(--sans); font-size:13px; color:var(--ink-2); margin:0 0 18px; max-width:70ch}
  .expbar{display:flex; height:46px; width:100%; border-radius:2px; overflow:hidden; border:1px solid var(--rule)}
  .expbar div{position:relative; display:flex; align-items:center; justify-content:center;
    font-family:var(--sans); font-size:12px; font-weight:600; color:#fff; overflow:hidden}
  .seg-us{background:var(--slate)}
  .seg-tar{background:repeating-linear-gradient(45deg,var(--rust),var(--rust) 5px,#93301F 5px,#93301F 10px)}
  .seg-uk{background:#5E82A3}
  .seg-cn{background:#8FA4B7}
  .seg-eu{background:#B6C4D0; color:var(--ink)}
  .seg-ot{background:#D8DFE5; color:var(--ink)}
  .explegend{display:flex; flex-wrap:wrap; gap:6px 22px; margin-top:14px; font-family:var(--sans); font-size:12.5px; color:var(--ink-2)}
  .explegend i{display:inline-block; width:10px; height:10px; margin-right:7px; vertical-align:baseline; border-radius:1px}
  .expnote{margin-top:16px; padding-top:14px; border-top:1px solid var(--rule-soft); font-family:var(--sans); font-size:13px; color:var(--ink-2); max-width:78ch}

  /* ---------- sections ---------- */
  section{padding:56px 0 8px; border-bottom:1px solid var(--rule)}
  section:last-of-type{border-bottom:none}
  h2.sec{font-size:clamp(22px,2.4vw,28px); font-weight:650; letter-spacing:-.022em; margin:0 0 8px; line-height:1.2}
  .deck{color:var(--ink-2); max-width:68ch; margin:0 0 30px; font-size:16.5px; line-height:1.6}
  h3{font-size:15px; font-weight:650; margin:34px 0 12px; letter-spacing:-.008em}
  h4{font-size:13.5px; font-weight:650; margin:0 0 6px; letter-spacing:-.005em}
  p{max-width:68ch}
  .src{font-size:12px; color:var(--ink-3); margin-top:14px; max-width:80ch; line-height:1.55}
  a{color:var(--slate)}

  /* vitals grid */
  .vitals{display:grid; grid-template-columns:repeat(auto-fit,minmax(188px,1fr)); gap:1px; background:var(--rule); border:1px solid var(--rule); border-radius:3px; overflow:hidden}
  .vital{background:var(--surface); padding:16px 17px 15px}
  .vital .lab{font-family:var(--sans); font-size:12px; color:var(--ink-2); margin-bottom:9px; line-height:1.3}
  .vital .val{font-family:var(--sans); font-variant-numeric:tabular-nums; font-size:29px; font-weight:600; letter-spacing:-.025em; line-height:1}
  .vital .met{font-family:var(--sans); font-size:11.5px; margin-top:8px; line-height:1.4; color:var(--ink-3)}
  .up{color:var(--spruce)} .down{color:var(--rust)} .watch{color:var(--amber)} .neu{color:var(--slate)}
  .vital.hot{box-shadow:inset 3px 0 0 var(--rust)}
  .vital.good{box-shadow:inset 3px 0 0 var(--spruce)}
  .vital.mid{box-shadow:inset 3px 0 0 var(--amber)}

  /* generic panel */
  .panel{background:var(--surface); border:1px solid var(--rule); border-radius:3px; padding:20px 22px; margin:18px 0}
  .panel.spine-r{box-shadow:inset 4px 0 0 var(--rust)}
  .panel.spine-g{box-shadow:inset 4px 0 0 var(--spruce)}
  .panel.spine-a{box-shadow:inset 4px 0 0 var(--amber)}
  .panel.spine-s{box-shadow:inset 4px 0 0 var(--slate)}

  /* tables */
  table{width:100%; border-collapse:collapse; font-family:var(--sans); font-size:13.5px; background:var(--surface)}
  .tablewrap{border:1px solid var(--rule); border-radius:3px; overflow-x:auto; margin:16px 0}
  th{text-align:left; font-weight:650; font-size:12px; color:var(--ink-2); padding:11px 14px; border-bottom:1px solid var(--rule); background:var(--surface-2); white-space:nowrap}
  td{padding:12px 14px; border-bottom:1px solid var(--rule-soft); vertical-align:top; line-height:1.48}
  tr:last-child td{border-bottom:none}
  td.n{font-variant-numeric:tabular-nums; white-space:nowrap}
  .tag{display:inline-block; font-size:11px; font-weight:650; padding:2.5px 8px; border-radius:2px; white-space:nowrap}
  .t-exp{background:var(--spruce-soft); color:var(--spruce)}
  .t-mix{background:var(--amber-soft); color:var(--amber)}
  .t-con{background:var(--rust-soft); color:var(--rust)}
  .t-neu{background:var(--slate-soft); color:var(--slate)}

  /* filter + control buttons */
  .controls{display:flex; flex-wrap:wrap; gap:8px; margin:20px 0 4px; font-family:var(--sans)}
  button.pill{
    font-family:var(--sans); font-size:13px; font-weight:550; padding:7px 15px; cursor:pointer;
    background:var(--surface); color:var(--ink-2); border:1px solid var(--rule); border-radius:2px;
    transition:background .12s,color .12s,border-color .12s;
  }
  button.pill:hover{border-color:var(--ink-3); color:var(--ink)}
  button.pill[aria-pressed="true"]{background:var(--ink); color:#fff; border-color:var(--ink)}

  /* scenario */
  .scen-grid{display:grid; grid-template-columns:repeat(auto-fit,minmax(150px,1fr)); gap:1px; background:var(--rule); border:1px solid var(--rule); border-radius:3px; margin-top:18px; overflow:hidden}
  .scen-cell{background:var(--surface); padding:15px 16px}
  .scen-cell .lab{font-family:var(--sans); font-size:11.5px; color:var(--ink-2); margin-bottom:8px}
  .scen-cell .val{font-family:var(--sans); font-size:23px; font-weight:600; letter-spacing:-.02em; font-variant-numeric:tabular-nums}
  #scenNarr{margin-top:18px}

  /* charts */
  figure{margin:20px 0; background:var(--surface); border:1px solid var(--rule); border-radius:3px; padding:20px 22px 16px}
  figcaption{font-family:var(--sans); font-size:12.5px; color:var(--ink-2); margin-top:12px; line-height:1.5}
  svg{display:block; width:100%; height:auto; overflow:visible}
  svg text{font-family:var(--sans); font-variant-numeric:tabular-nums}

  /* calendar */
  .cal{display:grid; gap:1px; background:var(--rule); border:1px solid var(--rule); border-radius:3px; overflow:hidden}
  .cal .row{display:grid; grid-template-columns:110px 1fr 116px; gap:0; background:var(--surface); align-items:baseline; padding:13px 16px; font-family:var(--sans); font-size:13.5px}
  .cal .row .d{font-variant-numeric:tabular-nums; color:var(--ink-2); font-size:12.5px}
  .cal .row .c{text-align:right; font-size:12px; font-weight:650}
  .cal .row.past{background:var(--surface-2); color:var(--ink-3)}
  .cal .row.past .c{color:var(--ink-3); font-weight:500}

  /* exposure checker */
  .tool{background:var(--surface); border:1px solid var(--rule); border-radius:3px; padding:22px}
  .tool .fields{display:flex; flex-wrap:wrap; gap:14px; margin-bottom:6px}
  label.f{font-family:var(--sans); font-size:12.5px; color:var(--ink-2); display:flex; flex-direction:column; gap:6px}
  select{font-family:var(--sans); font-size:14px; padding:8px 10px; border:1px solid var(--rule); border-radius:2px; background:var(--surface-2); color:var(--ink); min-width:220px}
  #toolOut{margin-top:20px; padding-top:18px; border-top:1px solid var(--rule-soft); font-family:var(--sans); font-size:14px; line-height:1.6}
  #toolOut .score{font-size:15px; font-weight:650; margin-bottom:8px}

  details{background:var(--surface); border:1px solid var(--rule); border-radius:3px; margin:10px 0; padding:0}
  summary{cursor:pointer; padding:13px 18px; font-family:var(--sans); font-size:14px; font-weight:600; list-style:none}
  summary::-webkit-details-marker{display:none}
  summary::before{content:"+"; display:inline-block; width:16px; color:var(--ink-3); font-weight:400}
  details[open] summary::before{content:"–"}
  details .body{padding:0 18px 18px 34px; font-size:15.5px}
  details .body p{margin:0 0 10px}

  ul.clean{padding-left:20px; max-width:70ch}
  ul.clean li{margin-bottom:8px}

  footer{padding:48px 0 0; font-family:var(--sans); font-size:12.5px; color:var(--ink-3); max-width:80ch}

  @media (max-width:900px){
    body{font-size:16px}
    .shell{display:block}
    nav.rail{position:sticky; top:0; z-index:20; height:auto; width:100%; flex:none;
      padding:10px 14px; border-right:none; border-bottom:1px solid var(--rule); background:rgba(231,235,238,.96); backdrop-filter:blur(6px)}
    .rail .mark{display:none}
    .rail ol{display:flex; margin:0; gap:2px; overflow-x:auto; -webkit-overflow-scrolling:touch; scrollbar-width:none}
    .rail ol::-webkit-scrollbar{display:none}
    .rail a{white-space:nowrap; border-left:none; border-bottom:2px solid transparent; padding:6px 10px}
    .rail a.on{border-left:none; border-bottom-color:var(--rust)}
    main{padding:0 16px 80px}
    header.hero{padding:30px 0 24px}
    .cal .row{grid-template-columns:1fr; gap:3px}
    .cal .row .c{text-align:left}
    .expbar{height:38px}
    .expbar div{font-size:10px}
  }
  /* --- polish pass --- */
  .vital .val{font-weight:650; letter-spacing:-.032em; font-size:28px}
  .vital .lab{font-weight:500}
  tbody tr{transition:background .1s}
  tbody tr:hover{background:var(--surface-2)}
  td{line-height:1.55}
  .tag{letter-spacing:-.005em}
  .deck strong,p strong,li strong{font-weight:650; color:var(--ink)}
  details .body{font-size:15px; line-height:1.62; color:var(--ink-2)}
  details .body strong,details .body em{color:var(--ink)}
  .scen-cell .val{font-weight:650; letter-spacing:-.028em}
  .band h2{letter-spacing:-.01em}
  ul.clean li{line-height:1.58}
  figcaption{max-width:78ch}
  .cal .row strong{font-weight:650}
  ::selection{background:var(--slate-soft)}
</style>
</head>
<body>
<div class="shell">

<nav class="rail" aria-label="Sections">
  <div class="mark">Canada Economic Dashboard<span>Structural read to 2035</span></div>
  <ol>
    <li><a href="#vitals">Vital signs</a></li>
    <li><a href="#trade">Trade war status</a></li>
    <li><a href="#partners">Trading partners</a></li>
    <li><a href="#sectors">Sector map</a></li>
    <li><a href="#labour">Labour market</a></li>
    <li><a href="#people">People and housing</a></li>
    <li><a href="#capital">Where capital is going</a></li>
    <li><a href="#productivity">The productivity problem</a></li>
    <li><a href="#provinces">Provincial split</a></li>
    <li><a href="#outlook">Ten-year outlook</a></li>
    <li><a href="#exposure">Your exposure</a></li>
    <li><a href="#calendar">What's next</a></li>
  </ol>
</nav>

<main>

<header class="hero">
  <h1>Canada's economy, read from the outside in</h1>
  <p class="standfirst">The domestic numbers look better than they have in two years. The external ones look worse than they have in decades. Almost everything about the next ten years turns on which of those two facts dominates.</p>
  <div class="asof">
    <span><b>Data as of</b> 31 August 2026</span>
    <span><b>Latest GDP</b> Q2 2026, released 28 Aug</span>
    <span><b>Latest jobs</b> July 2026, released 7 Aug</span>
    <span><b>Latest CPI</b> July 2026, released 17 Aug</span>
  </div>

  <div class="band">
    <h2>The single most important chart in the Canadian economy</h2>
    <p class="sub">Where Canada's merchandise exports went in the first half of 2026, and how much of it is now under a 50% US tariff. Every other structural question sits downstream of this bar.</p>
    <div class="expbar" role="img" aria-label="Export destination shares: United States 68 percent, of which about 5 percent is tariffed at 50 percent; United Kingdom 9.2 percent; China 5 percent; European Union about 5 percent; rest of world about 12.8 percent.">
      <div class="seg-us" style="width:64.6%">United States 63%</div>
      <div class="seg-tar" style="width:3.4%" title="Under 50% US tariff since 22 Aug 2026">3.4%</div>
      <div class="seg-uk" style="width:9.2%">UK 9.2%</div>
      <div class="seg-cn" style="width:5%">China 5%</div>
      <div class="seg-eu" style="width:5%">EU 5%</div>
      <div class="seg-ot" style="width:12.8%">Rest 12.8%</div>
    </div>
    <div class="explegend">
      <span><i style="background:var(--slate)"></i>US, tariff-free or CUSMA-compliant</span>
      <span><i class="seg-tar" style="background:var(--rust)"></i>US, hit by the 22 Aug 50% tariffs (~C$28bn)</span>
      <span><i style="background:#5E82A3"></i>United Kingdom — mostly gold, not a real market</span>
      <span><i style="background:#8FA4B7"></i>China</span>
      <span><i style="background:#B6C4D0"></i>European Union</span>
    </div>
    <div class="expnote">
      Read it carefully. The UK's 9.2% is largely unwrought gold moving to London vaults for foreign investors, not British demand for Canadian goods. Strip that out and the honest picture is: roughly two-thirds United States, about 5% China, about 5% the EU, and a long tail. The EU and China together absorb about a tenth of what the US does, which is why "diversify away from America" is a decade-long project rather than a plan for this year.
    </div>
  </div>
</header>

<!-- ============ VITALS ============ -->
<section id="vitals">
  <h2 class="sec">Vital signs</h2>
  <p class="deck">The paradox of late 2026: the strongest quarter of growth since early 2023, the lowest unemployment in two years, and an inflation rate above target — all recorded in the weeks before the trade relationship broke.</p>

  <div class="vitals">
    <div class="vital good">
      <div class="lab">Real GDP, Q2 2026</div>
      <div class="val up">+3.3%</div>
      <div class="met">Annualized. Fastest since Q1 2023. Q1 revised up to +0.3%, so no technical recession. June monthly +0.3%; July flash estimate flat.</div>
    </div>
    <div class="vital good">
      <div class="lab">Unemployment rate, July</div>
      <div class="val up">6.4%</div>
      <div class="met">Third straight monthly fall, down 0.5pt since April. Lowest since July 2024. +75,000 jobs in the month against a 15,000 consensus.</div>
    </div>
    <div class="vital mid">
      <div class="lab">CPI inflation, July</div>
      <div class="val watch">3.0%</div>
      <div class="met">Up from 2.8%. Gasoline +25.7% on the Middle East oil shock. Core is calm: CPI-trim 1.9%, CPI-median 2.0%.</div>
    </div>
    <div class="vital">
      <div class="lab">Bank of Canada policy rate</div>
      <div class="val neu">2.25%</div>
      <div class="met">Held six consecutive meetings. Next decision 2 September. Markets price no change; some swap pricing leans to a hike by January.</div>
    </div>
    <div class="vital hot">
      <div class="lab">US tariff on targeted goods</div>
      <div class="val down">50%</div>
      <div class="met">In force since 22 August on roughly C$28bn of exports. Canadian counter-tariffs of 15–50% begin 8 September.</div>
    </div>
    <div class="vital">
      <div class="lab">Canadian dollar</div>
      <div class="val neu">72.2¢</div>
      <div class="met">About C$1.386 per USD on 28 August. Soft, but supported by high oil and a wide terms-of-trade gain.</div>
    </div>
    <div class="vital good">
      <div class="lab">Merchandise trade balance, June</div>
      <div class="val up">+$3.9B</div>
      <div class="met">Fourth consecutive surplus. Goods exports at a record $77.5bn. Surplus with the US $10.0bn; deficit with everyone else $6.1bn.</div>
    </div>
    <div class="vital mid">
      <div class="lab">Federal deficit, 2026–27</div>
      <div class="val watch">$65.3B</div>
      <div class="met">After $66.9bn in 2025–26 (2.1% of GDP). Debt-to-GDP projected at 41.5% and broadly flat to 2030–31.</div>
    </div>
    <div class="vital mid">
      <div class="lab">Population, Q1 2026</div>
      <div class="val watch">41.47M</div>
      <div class="met">Fell by 55,025 in the quarter — a third consecutive quarterly decline. This is deliberate policy, and it changes everything downstream.</div>
    </div>
    <div class="vital">
      <div class="lab">Job vacancy rate, Q1 2026</div>
      <div class="val neu">2.8%</div>
      <div class="met">Against a long-run norm nearer 3.5%. Employers are not scrambling. Roughly 490,500 open positions.</div>
    </div>
    <div class="vital hot">
      <div class="lab">Business productivity, Q1 2026</div>
      <div class="val down">−0.5%</div>
      <div class="met">Second straight quarterly fall. Unit labour costs +1.4%. The single most important number on this page for 2035.</div>
    </div>
    <div class="vital good">
      <div class="lab">Real GDP per capita, Q2</div>
      <div class="val up">+3.8%</div>
      <div class="met">Annualized, fastest since late 2021. But note the mechanism: output rose while the denominator shrank.</div>
    </div>
  </div>
  <div class="panel spine-a">
    <h4>Three cautions about the numbers above</h4>
    <p style="margin:0 0 10px"><strong>Population figures are preliminary.</strong> Statistics Canada has flagged that the Q1 decline could be revised smaller, larger, or into growth when September data lands. Everything per-capita inherits that uncertainty.</p>
    <p style="margin:0 0 10px"><strong>Forecasts disagree meaningfully.</strong> The Bank of Canada projected 0.7% growth for 2026 in July; Finance Canada used 1.1%; Q2 came in at 3.3% annualized. That is not one of them being wrong — it is genuine uncertainty about a small open economy in a tariff war, and any dashboard showing a single confident number is hiding it from you.</p>
    <p style="margin:0"><strong>Gold distorts the trade data.</strong> Large unwrought gold movements to London inflate both total exports and the UK's apparent share. Always check whether a strong export month reflects industrial demand or vault logistics.</p>
  </div>
  <p class="src">Sources: Statistics Canada (GDP Q2 2026, Labour Force Survey July 2026, CPI July 2026, merchandise trade June 2026, quarterly population estimates, productivity Q1 2026); Bank of Canada July 2026 rate decision; Finance Canada Spring Economic Update, April 2026.</p>
</section>

<!-- ============ TRADE ============ -->
<section id="trade">
  <h2 class="sec">Trade war status board</h2>
  <p class="deck">Two things happened this summer that will shape the next decade more than any budget: the US declined to renew CUSMA, and talks collapsed into a 50% tariff. Neither is a temporary shock. Both convert trade policy from a background condition into an annual recurring risk.</p>

  <div class="panel spine-r">
    <h4>Live position</h4>
    <p style="margin:0 0 10px">Since <strong>22 August 2026</strong>, the United States has applied 50% tariffs under Section 338 of the Tariff Act of 1930 to roughly C$28 billion of Canadian goods — hockey sticks, building materials, liquor, some clothing categories among them. That is about 5% of what Canada ships south. BMO estimates the measures could subtract around half a percentage point from GDP growth.</p>
    <p style="margin:0 0 10px">Canada's response takes effect <strong>8 September 2026</strong>: matching tariffs of 15%, 25% and 50% on roughly $20 billion of annual US imports, concentrated in steel, dairy, appliances, agricultural equipment, pulp and paper, and electronics. Ottawa has paired it with $7.5 billion in support for affected workers and businesses.</p>
    <p style="margin:0">Sitting underneath all of this: the pre-existing 50% sectoral tariffs on steel and aluminum, and the auto and parts measures. Those have been grinding away since 2025 and account for most of the damage done so far.</p>
  </div>

  <h3>What actually changed on 1 July</h3>
  <p>The CUSMA joint review was not an expiry date and the agreement did not lapse. Canada and Mexico both confirmed they wanted the 16-year extension. The United States declined to renew in its current form, which triggers Article 34.7.4: an annual joint review, every year, until either the parties agree to extend or the agreement reaches its built-in expiry on <strong>1 July 2036</strong>. Preferential tariffs, rules of origin, investment protections and dispute settlement all continue to operate in the meantime.</p>
  <p>The practical consequence is subtle and worse than it sounds. A clean renewal would have given ten years of planning certainty. An outright collapse would at least have been a decision. What Canada got instead is a treaty whose survival is re-litigated every twelve months against whatever US trade politics look like that year. That is the hardest environment to make a twenty-year capital commitment in, and capital commitment is precisely what Canada needs most.</p>

  <div class="tablewrap">
    <table>
      <thead><tr><th>Measure</th><th>Rate</th><th>Coverage</th><th>Status</th></tr></thead>
      <tbody>
        <tr><td>US Section 338 tariffs</td><td class="n">50%</td><td>~C$28bn of exports (~5% of US-bound)</td><td><span class="tag t-con">In force 22 Aug 2026</span></td></tr>
        <tr><td>Canadian counter-tariffs</td><td class="n">15 / 25 / 50%</td><td>~$20bn of US imports</td><td><span class="tag t-con">Effective 8 Sep 2026</span></td></tr>
        <tr><td>US steel and aluminum tariffs</td><td class="n">50%</td><td>Sectoral, all origins</td><td><span class="tag t-con">In force since 2025</span></td></tr>
        <tr><td>US autos and parts tariffs</td><td class="n">Sectoral</td><td>Assembly and components</td><td><span class="tag t-con">In force</span></td></tr>
        <tr><td>US 10% global baseline tariff</td><td class="n">10%</td><td>Largely exempts CUSMA-compliant goods</td><td><span class="tag t-mix">Replaced struck-down IEEPA tariffs</span></td></tr>
        <tr><td>CUSMA / T-MEC</td><td class="n">—</td><td>Roughly two-thirds of Canadian exports</td><td><span class="tag t-mix">In force, annual review to 2036</span></td></tr>
        <tr><td>China–Canada tariff settlement</td><td class="n">6.1% / ~15%</td><td>49,000 Chinese EVs in; canola relief out</td><td><span class="tag t-exp">Agreed Jan 2026</span></td></tr>
      </tbody>
    </table>
  </div>
  <p class="src">Sources: USTR statement on the USMCA joint review, 1 July 2026; White &amp; Case and McMillan LLP analyses of Article 34.7; Department of Finance Canada countermeasures announcement, 25 August 2026; BMO Economics.</p>
</section>

<!-- ============ PARTNERS ============ -->
<section id="partners">
  <h2 class="sec">Trading partners, honestly assessed</h2>
  <p class="deck">Ottawa's stated goal is to double exports to non-US markets by 2035. It is the right objective and the arithmetic is brutal.</p>

  <figure>
    <svg viewBox="0 0 720 260" role="img" aria-label="Bar chart of Canada's merchandise export destinations, first half of 2026. United States 68 percent, United Kingdom 9.2 percent, China 5 percent, European Union about 5 percent, all others about 12.8 percent.">
      <g id="partnerBars"></g>
    </svg>
    <figcaption>Share of Canadian merchandise exports by destination, first half of 2026, balance-of-payments basis. Even doubling both the EU and China shares would replace under a fifth of the US market. Diversification is real and worth doing; it is not a substitute.</figcaption>
  </figure>

  <h3>Where the openings actually are</h3>
  <div class="tablewrap">
    <table>
      <thead><tr><th>Partner</th><th>Current state</th><th>Ten-year read</th></tr></thead>
      <tbody>
        <tr>
          <td><strong>United States</strong><br><span style="color:var(--ink-3)">~68% of exports</span></td>
          <td>Trade surplus of $10.0bn in June, five straight months of rising exports, and a 50% tariff on a slice of it. Deep integration in autos, energy and machinery.</td>
          <td><span class="tag t-mix">Structurally unavoidable</span> Share drifts down slowly, to maybe 60–63% by 2035 in the base case. Anyone forecasting a rapid decoupling is describing a recession, not a strategy.</td>
        </tr>
        <tr>
          <td><strong>China</strong><br><span style="color:var(--ink-3)">~5%, second-largest</span></td>
          <td>January 2026 deal cut Chinese canola seed duties toward 15% from 84–100%, lifted duties on canola meal, lobster, crab and peas, and opened visa-free travel. In exchange Canada admits 49,000 Chinese EVs at 6.1%, rising toward 70,000 over five years.</td>
          <td><span class="tag t-exp">Fastest available upside</span> Agriculture, energy, forestry, seafood and potash all have real Chinese demand. The cost is domestic: Ontario and the auto sector called the EV concession lopsided, and they have a point.</td>
        </tr>
        <tr>
          <td><strong>European Union</strong><br><span style="color:var(--ink-3)">~5%</span></td>
          <td>CETA is in place. Canada joined the EU's SAFE defence-procurement initiative in February 2026, which is the most concrete new channel.</td>
          <td><span class="tag t-mix">Strategic, slow</span> Defence, LNG, critical minerals and aluminum are the credible lanes. Critics argue Ottawa has over-invested diplomatic capital here relative to Asia; the counter-argument is that the EU is the only partner that shares Canada's regulatory instincts.</td>
        </tr>
        <tr>
          <td><strong>United Kingdom</strong><br><span style="color:var(--ink-3)">~9.2% on paper</span></td>
          <td>Dominated by unwrought gold flows to London, up 27.9% in June. This is investor positioning, not industrial demand.</td>
          <td><span class="tag t-neu">Treat as a statistical artefact</span> Do not build a strategy on this number.</td>
        </tr>
        <tr>
          <td><strong>Indo-Pacific ex-China</strong><br><span style="color:var(--ink-3)">Japan, Korea, India, ASEAN</span></td>
          <td>TMX has been shipping Alberta crude to Asian buyers since 2024. Metal ore exports to Japan, Korea and Finland rose in June. CPTPP membership already in hand.</td>
          <td><span class="tag t-exp">Most underused</span> The binding constraints are port capacity, rail, and permitting — not market access. Fix the corridor and the demand is there.</td>
        </tr>
        <tr>
          <td><strong>Interprovincial</strong><br><span style="color:var(--ink-3)">Canada to Canada</span></td>
          <td>The One Canadian Economy Act and mutual-recognition agreements are chipping at internal barriers that have cost the economy for decades.</td>
          <td><span class="tag t-exp">Cheapest win available</span> No foreign negotiation required, no tariff risk, and estimates of the gain run into the tens of billions. Watch whether provinces actually implement rather than announce.</td>
        </tr>
      </tbody>
    </table>
  </div>
  <p class="src">Sources: Statistics Canada merchandise trade data, H1 2026, via Visual Capitalist; Global Affairs Canada monthly trade report, June 2026; CBC and Reuters coverage of the January 2026 Canada–China agreement; Asia Pacific Foundation of Canada on TMX export flows.</p>
</section>

<!-- ============ SECTORS ============ -->
<section id="sectors">
  <h2 class="sec">Sector map: what's growing, what's dying</h2>
  <p class="deck">The clean split isn't old economy versus new. It's tradeable-into-the-US versus everything else. Sectors that ship to America across an integrated border are being restructured. Sectors selling energy, minerals, compute, defence or care are expanding.</p>

  <div class="controls" role="group" aria-label="Filter sectors">
    <button class="pill" data-filter="all" aria-pressed="true">All sectors</button>
    <button class="pill" data-filter="exp" aria-pressed="false">Expanding</button>
    <button class="pill" data-filter="mix" aria-pressed="false">Mixed</button>
    <button class="pill" data-filter="con" aria-pressed="false">Contracting</button>
  </div>

  <div class="tablewrap">
    <table id="sectorTable">
      <thead><tr><th>Sector</th><th>Direction</th><th>The evidence</th><th>Ten-year call</th></tr></thead>
      <tbody>
        <tr data-cat="exp"><td><strong>Oil and gas</strong></td><td><span class="tag t-exp">Expanding</span></td>
          <td>Industry revenue estimated at $210bn for 2026, up from $167bn — a 25% jump driven by the price surge after the Strait of Hormuz disruption. Analysts have raised 2026 forecasts three times, to roughly US$85 WTI and US$90 Brent.</td>
          <td>Strong, with a caveat. Capex is running flat despite the revenue windfall — producers are returning cash to shareholders rather than drilling. That is the single most telling fact about Canadian business investment culture.</td></tr>

        <tr data-cat="exp"><td><strong>Critical minerals and mining</strong></td><td><span class="tag t-exp">Expanding</span></td>
          <td>Red Chris expansion alone would lift Canadian copper output more than 15%. Foran's McIlvenna Bay copper project, Sisson tungsten and molybdenum in New Brunswick, plus nickel and graphite files all sit in the Major Projects Office queue.</td>
          <td>Structural winner if permitting holds. Copper, nickel, graphite, tungsten and uranium all sit at the intersection of defence, grid build-out and the AI power story. The risk is execution time, not demand.</td></tr>

        <tr data-cat="exp"><td><strong>Defence and aerospace</strong></td><td><span class="tag t-exp">Expanding</span></td>
          <td>Canada hit NATO's 2% of GDP in 2025–26 with over $63bn spent, the largest year-over-year increase in generations. The alliance commitment is 3.5% core plus 1.5% ancillary by 2035. The PBO estimates that path needs roughly $33.5bn a year in extra spending.</td>
          <td>The most reliable ten-year growth story on this page, because it is legislated rather than cyclical. Shipbuilding, submarines, drones, munitions, MRO and Arctic infrastructure. Atlantic Canada holds about 20% of the industry's employment.</td></tr>

        <tr data-cat="exp"><td><strong>AI infrastructure and compute</strong></td><td><span class="tag t-exp">Expanding</span></td>
          <td>Canada has roughly 0.3 GW of AI data-centre capacity today and needs about 1.3 GW by 2030 just to serve domestic workloads. Plans for 3.5–4 GW are on the books. The Sovereign AI Compute Strategy totals about $2.4bn, with $890m under SCIP for a Canadian-owned supercomputer, and the June 2026 "AI for All" strategy adds roughly $2bn more.</td>
          <td>Genuinely large, and the export case is bigger than the domestic one — estimates range from 1.7 GW to 6.7 GW of exportable capacity. Cheap clean power and a cold climate are real advantages. The constraint is grid interconnection speed.</td></tr>

        <tr data-cat="exp"><td><strong>Nuclear and SMRs</strong></td><td><span class="tag t-exp">Expanding</span></td>
          <td>Darlington New Nuclear is under construction and would make Canada the first G7 country with an operational small modular reactor.</td>
          <td>Slow-burn but high-value. If the first unit lands on schedule, Canada owns a genuine export franchise in a technology every AI-power-hungry jurisdiction wants.</td></tr>

        <tr data-cat="exp"><td><strong>LNG</strong></td><td><span class="tag t-exp">Expanding</span></td>
          <td>LNG Canada Phase 1 is complete; Phase 2 would double output and make Kitimat the second-largest facility of its kind globally. Cedar LNG is progressing under Haisla Nation leadership.</td>
          <td>Well-timed. European and Asian buyers are actively de-risking away from Middle Eastern and Russian supply. Canada's window is roughly this decade.</td></tr>

        <tr data-cat="exp"><td><strong>Construction and infrastructure</strong></td><td><span class="tag t-exp">Expanding</span></td>
          <td>+16,000 jobs in July. The Major Projects Office is advancing 23 initiatives worth over $135bn and more than 150,000 projected jobs, against roughly $125bn of federal capital commitments. Team Canada Strong puts $6bn behind recruiting 80,000–100,000 skilled trades workers by 2030–31.</td>
          <td>Non-residential and infrastructure boom, residential slump. Do not read the aggregate number — the composition is what matters.</td></tr>

        <tr data-cat="exp"><td><strong>Healthcare and social assistance</strong></td><td><span class="tag t-exp">Expanding</span></td>
          <td>Around 85,000 jobs added over the past year on pure demographic demand. The Canadian Nurses Association projects a shortfall of 117,600 nurses by 2030 on current trends, and there are more than 23,000 unfilled family physician positions.</td>
          <td>Demand is demographically locked in for the full ten years. Note the wrinkle: health vacancies actually fell to 62,700 in Q1 2026, the lowest since early 2020 — budget constraints are now capping hiring even where need is acute.</td></tr>

        <tr data-cat="mix"><td><strong>Finance, insurance and real estate</strong></td><td><span class="tag t-mix">Mixed</span></td>
          <td>+18,000 jobs in July, the strongest percentage gain of any major sector that month. But the underlying real estate transaction volume is weak.</td>
          <td>Employment resilient, revenue mix shifting from mortgage origination toward wealth and capital markets. Watch the mortgage renewal cycle.</td></tr>

        <tr data-cat="mix"><td><strong>Professional, scientific and technical</strong></td><td><span class="tag t-mix">Mixed</span></td>
          <td>+17,000 in July, yet vacancies for jobs requiring a bachelor's degree or higher fell 6.9% year over year. Self-employment is up 2.7% since April, which often signals involuntary contracting rather than entrepreneurship.</td>
          <td>Bifurcating hard. AI-adjacent, defence-adjacent and energy-adjacent professional services grow; generalist consulting, back-office analysis and routine software work compress.</td></tr>

        <tr data-cat="mix"><td><strong>Agriculture and agri-food</strong></td><td><span class="tag t-mix">Mixed</span></td>
          <td>Lost 9,600 jobs in July, a 4.3% monthly drop. But the China deal cut canola seed duties toward 15% and lifted them entirely on canola meal, peas, lobster and crab. Chinese pork tariffs remain.</td>
          <td>Prices and access improving, employment still falling — the sector is consolidating and mechanizing. Prairie farm incomes up, farm employment down. Both are true.</td></tr>

        <tr data-cat="mix"><td><strong>Wholesale and retail trade</strong></td><td><span class="tag t-mix">Mixed</span></td>
          <td>+21,000 in July, the largest single-sector gain. Household spending rose 0.8% in Q2.</td>
          <td>Follows the consumer, and the consumer follows real income. Counter-tariffs on US appliances, electronics and food will show up in shelf prices this autumn.</td></tr>

        <tr data-cat="con"><td><strong>Manufacturing, broadly</strong></td><td><span class="tag t-con">Contracting</span></td>
          <td>More than 50,000 positions lost over the year to early 2026, with employment still down about 50,000 (1.7%) year over year as of July. Over 60% of the sector has substantial US trade exposure.</td>
          <td>The core structural loss of this decade. Some of it comes back if tariffs ease; a meaningful share does not, because supply chains that relocate rarely relocate again.</td></tr>

        <tr data-cat="con"><td><strong>Autos and parts</strong></td><td><span class="tag t-con">Contracting</span></td>
          <td>Parts employment fell 8.7% year over year by February 2026, roughly 6,200 jobs — the sharpest decline of any automotive category. GM's Oshawa plant went from three shifts to two, cutting about 500 jobs. Stellantis Brampton has produced nothing for nearly two years with 2,200 workers on layoff and a possible sale under discussion.</td>
          <td>Structurally impaired. Parts cross the border multiple times before final assembly, so tariffs compound at every crossing and suppliers have the least pricing power. The Chinese EV quota adds domestic competition on top.</td></tr>

        <tr data-cat="con"><td><strong>Steel</strong></td><td><span class="tag t-con">Contracting</span></td>
          <td>About 2,000 layoffs since the US 50% steel tariff took effect, including 300 at Algoma in March 2026. The United Steelworkers warn of thousands more.</td>
          <td>Survives only with sustained Buy Canadian procurement and genuine domestic demand from the infrastructure build-out. Sault Ste. Marie and Hamilton are the communities to watch.</td></tr>

        <tr data-cat="con"><td><strong>Aluminum</strong></td><td><span class="tag t-con">Contracting</span></td>
          <td>Canada is the largest supplier to the US and faces the same 50% wall. Producers including Rio Tinto have been exploring a European pivot.</td>
          <td>Better long-run odds than steel — the product is more fungible, the power cost advantage in Quebec is real, and European demand is rising with defence and grid spending.</td></tr>

        <tr data-cat="con"><td><strong>Softwood lumber and forestry</strong></td><td><span class="tag t-con">Contracting</span></td>
          <td>Named by Finance Canada as one of the least-diversified, most tariff-exposed sectors, alongside steel and motor vehicles.</td>
          <td>A forty-year dispute that trade agreements have never solved. Compounded now by a weakening domestic housing start pipeline.</td></tr>

        <tr data-cat="con"><td><strong>Residential construction and condos</strong></td><td><span class="tag t-con">Contracting</span></td>
          <td>Housing starts forecast to fall 6.8% to 241,400 units in 2026, with further declines expected through 2028. Condo presale activity has collapsed and Toronto inventory is heavy.</td>
          <td>Multi-year contraction. Fewer people arriving means less household formation, and the projects that get built shift toward purpose-built rental and infrastructure.</td></tr>

        <tr data-cat="con"><td><strong>International education</strong></td><td><span class="tag t-con">Contracting</span></td>
          <td>New study permit targets are down roughly half. Total new temporary resident arrivals drop from 673,650 in 2025 to 385,000 in 2026.</td>
          <td>A sector deliberately shrunk by policy. The second-order damage lands on college towns, student housing, and the retail and food service employers who staffed themselves with student labour.</td></tr>

        <tr data-cat="con"><td><strong>Public administration</strong></td><td><span class="tag t-con">Contracting</span></td>
          <td>−15,000 jobs in July, a 1.2% drop, and public sector employment fell 27,000 overall that month while private sector rose 58,000.</td>
          <td>Restraint is intentional and continues. Federal spending review pressure plus a defence build-out means resources shift from administration toward procurement and capital.</td></tr>
      </tbody>
    </table>
  </div>
  <p class="src">Sources: Statistics Canada Labour Force Survey July 2026 and job vacancies Q1 2026; CAPP data centre estimates, April 2026; BCG on Canadian AI data-centre capacity, July 2026; Prime Minister's Office announcements on the Major Projects Office, July 2026; PBO on NATO 5% commitment, February 2026; CMHC Summer 2026 Housing Market Outlook; DesRosiers Automotive Consultants; United Steelworkers; IRCC 2026–2028 Immigration Levels Plan.</p>
</section>

<!-- ============ LABOUR ============ -->
<section id="labour">
  <h2 class="sec">Labour market</h2>
  <p class="deck">The headline is genuinely good. The composition is where the story lives: private sector and self-employment up, public sector down, and a vacancy rate well below its historical norm — which means employers have the upper hand even as unemployment falls.</p>

  <figure>
    <svg viewBox="0 0 720 348" role="img" aria-label="Diverging bar chart of the largest employment changes by industry in July 2026, in thousands of jobs. Gains: wholesale and retail trade plus 21.0; finance, insurance and real estate plus 18.0; professional, scientific and technical plus 17.0; construction plus 16.0. Losses: agriculture minus 9.6; public administration minus 15.0.">
      <g id="jobsBars"></g>
    </svg>
    <figcaption>Largest employment changes by industry, July 2026, seasonally adjusted, thousands of jobs. Employment rose in six of sixteen industries and fell in six, but only public administration lost more than 10,000 — the most broad-based month in two years. Industries with changes too small to chart are omitted.</figcaption>
  </figure>

  <h3>The structural read, beneath the monthly noise</h3>
  <div class="panel spine-s">
    <p style="margin:0 0 12px"><strong>Job growth is modest, not booming.</strong> Average monthly job creation across 2026 to date is roughly 10,000. That looks better than it is only because slowing population growth and rising retirements have lowered the number of jobs needed to hold unemployment steady. Canada is not creating jobs faster; it is needing fewer of them.</p>
    <p style="margin:0 0 12px"><strong>Vacancies are scarce by historical standards.</strong> The 2.8% vacancy rate sits nearly a full point below the long-run average near 3.5%. Vacancies fell year over year for three of four education levels, including a 6.9% drop for roles requiring a bachelor's degree or higher. Job seekers face more competition than the unemployment rate implies.</p>
    <p style="margin:0"><strong>The mismatch is the real problem.</strong> Displaced manufacturing workers in Windsor and Sault Ste. Marie are not the people who fill nursing vacancies in Ontario or electrician shortages in Alberta. Retraining takes years, costs money, and often requires credential recognition that Canadian regulators are notoriously slow at. This is why unemployment and shortage coexist.</p>
  </div>

  <h3>Where the demand actually is</h3>
  <div class="tablewrap">
    <table>
      <thead><tr><th>Occupation cluster</th><th>Demand signal</th><th>Why it holds for ten years</th></tr></thead>
      <tbody>
        <tr><td>Registered nurses, PSWs, allied health</td><td><span class="tag t-exp">Acute, national</span></td><td>Projected 117,600-nurse shortfall by 2030. Aging demographics guarantee demand regardless of the business cycle. Nova Scotia and New Brunswick have both declared staffing crises.</td></tr>
        <tr><td>Skilled trades — electricians, welders, pipefitters, millwrights</td><td><span class="tag t-exp">Acute, rising</span></td><td>The $135bn project pipeline, defence build-out, grid expansion and data centres all require the same people. Ottawa is funding 80,000–100,000 new trades workers by 2030–31 because the shortage is binding.</td></tr>
        <tr><td>Power engineering, grid and utility</td><td><span class="tag t-exp">Emerging, underrated</span></td><td>Every AI data centre, SMR, LNG train and electrified mine needs interconnection. This is the quiet bottleneck across the entire growth story.</td></tr>
        <tr><td>Defence engineering, shipbuilding, MRO</td><td><span class="tag t-exp">Policy-locked</span></td><td>A commitment to 3.5% of GDP by 2035 is a decade-long hiring mandate with cross-party support. Very unusual visibility.</td></tr>
        <tr><td>Mining engineers, geologists, heavy equipment</td><td><span class="tag t-exp">Strong</span></td><td>Critical minerals projects moving to final investment decision on a two-year MPO clock.</td></tr>
        <tr><td>AI, security and data infrastructure</td><td><span class="tag t-mix">Strong but narrowing</span></td><td>Real demand at the infrastructure and applied layer. Generalist software roles are competing with both offshore labour and the tools themselves.</td></tr>
        <tr><td>Long-haul and logistics</td><td><span class="tag t-mix">Steady</span></td><td>Trade-corridor investment supports volumes, but rerouting away from the US border changes which corridors matter.</td></tr>
        <tr><td>Manufacturing production, auto assembly</td><td><span class="tag t-con">Declining</span></td><td>Tariff structure plus automation. Recovery requires a trade settlement that no longer looks likely on a short horizon.</td></tr>
        <tr><td>Entry-level office, admin, generalist analysis</td><td><span class="tag t-con">Declining</span></td><td>Youth unemployment at 12.6% is the clearest evidence. Public administration cuts and AI-assisted workflow compression hit the same rungs of the ladder.</td></tr>
      </tbody>
    </table>
  </div>

  <div class="panel spine-a">
    <h4>The one demographic fact worth flagging</h4>
    <p style="margin:0">Core-aged women hit a record-low 5.2% unemployment rate in July with an employment rate of 81.2%, more than two points above the pre-pandemic norm. Core-aged men sit at 5.8%. Youth remain at 12.6%. The labour market is not weak overall — it is weak specifically at the entry point, which is a much harder problem to fix and has a longer tail of consequences.</p>
  </div>
  <p class="src">Sources: Statistics Canada Labour Force Survey, July 2026; Statistics Canada job vacancies, Q1 2026; Indeed Hiring Lab Canada; RBC Economics; Canadian Nurses Association projections.</p>
</section>

<!-- ============ PEOPLE + HOUSING ============ -->
<section id="people">
  <h2 class="sec">People and housing</h2>
  <p class="deck">Canada is running the largest deliberate reduction in population growth in its modern history. This is the most under-discussed variable in every ten-year forecast, and it cuts both ways.</p>

  <figure>
    <svg viewBox="0 0 720 280" role="img" aria-label="Bar chart comparing new temporary resident arrival targets and permanent resident admissions from 2025 to 2028. Temporary resident arrivals fall from 673,650 in 2025 to 385,000 in 2026 and 370,000 in 2027 and 2028. Permanent residents hold near 380,000 to 393,500.">
      <g id="immBars"></g>
    </svg>
    <figcaption>New temporary resident arrival targets against permanent resident admissions. The permanent stream is stable; the temporary stream is being cut by 43% in a single year.</figcaption>
  </figure>

  <h3>What the policy is doing</h3>
  <ul class="clean">
    <li>Permanent resident admissions hold at <strong>380,000 a year through 2028</strong>, with about 64% in economic categories. That is down from a 2024 target of 465,000.</li>
    <li>New temporary resident arrivals fall to <strong>385,000 in 2026</strong> from 673,650 in 2025, then 370,000 in 2027 and 2028. New study permits are cut by roughly half.</li>
    <li>The non-permanent resident share of the population has already fallen from a 7.6% peak to <strong>6.5%</strong>, with a target of under 5% by end-2027. The PBO judged that target achievable in February 2026.</li>
    <li>Population fell by <strong>55,025 in Q1 2026</strong>, a third consecutive quarterly decline. Statistics Canada has flagged these as preliminary and will revise in September.</li>
    <li>A one-time measure grants permanent residence to up to 33,000 established work permit holders across 2026 and 2027.</li>
    <li>The <strong>2027–2029 Immigration Levels Plan is due in fall 2026</strong> — the next real signal on whether this trajectory continues.</li>
  </ul>

  <div class="panel spine-a">
    <h4>Why this matters more than it appears</h4>
    <p style="margin:0 0 10px">A shrinking population flatters GDP per capita arithmetically — which is exactly what happened in Q2, when per-capita output rose 3.8% annualized partly because the denominator fell. Nobody's living standard improved by 3.8% in three months. Be very careful reading per-capita improvements over the next two years.</p>
    <p style="margin:0">It also removes the crutch Canada has leaned on for a decade. Headline GDP growth was propped up by adding people. With that gone, growth has to come from output per worker — which is the thing Canada has been worst at. The policy is defensible and probably correct on housing and services grounds. It also removes every remaining excuse on productivity.</p>
  </div>

  <h3>Housing, as of the summer 2026 outlook</h3>
  <div class="tablewrap">
    <table>
      <thead><tr><th>Indicator</th><th>2026 forecast</th><th>Direction</th><th>Note</th></tr></thead>
      <tbody>
        <tr><td>Home sales</td><td class="n">457,200</td><td><span class="tag t-con">−2.8%</span></td><td>Downgraded from February, when CMHC still expected growth.</td></tr>
        <tr><td>Average price</td><td class="n">$675,200</td><td><span class="tag t-con">−0.6%</span></td><td>CREA is more optimistic at roughly $686,710 and +1.1%. Take the range, not either point.</td></tr>
        <tr><td>Housing starts</td><td class="n">241,400</td><td><span class="tag t-con">−6.8%</span></td><td>Further declines expected in 2027 and 2028 as condo presales stay weak.</td></tr>
        <tr><td>Shelter inflation</td><td class="n">1.3% y/y</td><td><span class="tag t-exp">Cooling</span></td><td>Homeowners' replacement cost is down 2.1% and is now the biggest single drag on national CPI.</td></tr>
        <tr><td>Rental market</td><td class="n">Easing</td><td><span class="tag t-exp">Improving</span></td><td>Vacancy up as construction completes and demand falls. Rents remain high relative to income at turnover.</td></tr>
      </tbody>
    </table>
  </div>
  <p>The regional split matters more than the national number. The Prairies and Quebec lead on sales and price growth, helped by affordability and commodity income. Ontario and British Columbia stay constrained. Atlantic Canada is the weakest. The affordability improvement now underway is coming from stalled prices and falling population rather than rising incomes or supply — which is a real improvement for buyers and a bad sign for everything else.</p>
  <p class="src">Sources: IRCC 2026–2028 Immigration Levels Plan and supplementary information; Statistics Canada quarterly demographic estimates, Q1 2026; CMHC Summer 2026 Housing Market Outlook update, 22 July 2026; CREA July 2026 forecast; Statistics Canada CPI, July 2026.</p>
</section>

<!-- ============ CAPITAL ============ -->
<section id="capital">
  <h2 class="sec">Where the capital is going</h2>
  <p class="deck">If you want to know what Canada looks like in 2035, follow the committed money rather than the speeches. Roughly $135 billion of project pipeline, a legislated defence ramp, and a sovereign compute build-out are the three concrete bets on the table.</p>

  <div class="tablewrap">
    <table>
      <thead><tr><th>Programme</th><th>Scale</th><th>Contents</th><th>Confidence</th></tr></thead>
      <tbody>
        <tr><td><strong>Major Projects Office</strong><br><span style="color:var(--ink-3)">Building Canada Act</span></td><td class="n">$135bn+<br>150,000 jobs</td>
          <td>23 initiatives across nuclear, LNG, critical minerals and transport. Two-year maximum federal review, "one project, one review". Named files include LNG Canada Phase 2, Darlington SMRs, Contrecœur at the Port of Montreal, Foran McIlvenna Bay, Red Chris expansion, Sisson tungsten, and the proposed West Coast oil pipeline submitted by Alberta on 2 July 2026.</td>
          <td><span class="tag t-mix">Medium-high</span> Real money and real legislative backing. The risk is Indigenous consent processes, provincial coordination and construction labour supply — not political will.</td></tr>
        <tr><td><strong>Defence</strong><br><span style="color:var(--ink-3)">NATO commitment</span></td><td class="n">$63bn now<br>~$150bn by 2035</td>
          <td>2% of GDP reached in 2025–26, the first time since 1990. Commitment to 3.5% core plus 1.5% ancillary by 2035. Submarine procurement shortlisted, Canada joined the EU's SAFE initiative in February 2026, and a Defence, Security and Resilience Bank is in development.</td>
          <td><span class="tag t-mix">High on intent, low on plan</span> The PBO puts the incremental cost at roughly $33.5bn a year and estimates it adds $63bn to the 2035–36 deficit. C.D. Howe notes there is no credible five-year funding path published.</td></tr>
        <tr><td><strong>Sovereign AI compute</strong></td><td class="n">~$2.4bn<br>+~$2bn AI for All</td>
          <td>SCIP provides about $890m over seven years for a Canadian-owned supercomputer. $700m aims to mobilise private data-centre investment above 100 MW. A $300m Access Fund subsidises compute for researchers and firms. The June 2026 "AI for All" strategy adds a national public supercomputer and data-residency rules.</td>
          <td><span class="tag t-exp">High</span> Small in dollar terms next to the projects pipeline, but it unlocks a much larger private build-out. Watch grid interconnection queues in BC, Quebec and Alberta.</td></tr>
        <tr><td><strong>Canada Strong Fund</strong></td><td class="n">$25bn initial</td>
          <td>A sovereign wealth vehicle for strategic domestic projects, with a retail investment channel proposed.</td>
          <td><span class="tag t-neu">Unproven</span> Governance and mandate details still thin. Worth watching, not yet worth counting.</td></tr>
        <tr><td><strong>Build Communities Strong Fund</strong></td><td class="n">$51bn</td>
          <td>Municipal and community infrastructure capital.</td>
          <td><span class="tag t-mix">Medium</span> Delivery depends on municipal capacity, historically the weak link.</td></tr>
        <tr><td><strong>Team Canada Strong</strong></td><td class="n">$6bn</td>
          <td>Recruit, train and hire 80,000–100,000 skilled trades workers by 2030–31.</td>
          <td><span class="tag t-exp">Necessary</span> Without this, the rest of the pipeline is uncertifiable. Trades capacity is the binding physical constraint on the entire build-out.</td></tr>
      </tbody>
    </table>
  </div>

  <div class="panel spine-r">
    <h4>The counterweight nobody should ignore</h4>
    <p style="margin:0">Announced capital is not deployed capital. Oil and gas revenue is up 25% this year while capex stays flat. Real machinery and equipment investment has moved sideways in Canada since 2009 while more than doubling in the United States. Business investment intentions surveys for 2026 signal that capital deployment is unlikely at scale. Government can commit $135 billion; it cannot make the private sector match it. Whether it does is the hinge of the entire ten-year outlook.</p>
  </div>
  <p class="src">Sources: Prime Minister's Office, 2 July 2026; Blakes and BLG project tranche summaries; Finance Canada Spring Economic Update; PBO fiscal implications of the NATO 5% commitment; ISED Sovereign AI Compute Strategy; C.D. Howe Institute; Statistics Canada productivity and investment data.</p>
</section>

<!-- ============ PRODUCTIVITY ============ -->
<section id="productivity">
  <h2 class="sec">The productivity problem</h2>
  <p class="deck">Strip away tariffs, oil prices and immigration policy, and this is the number that determines whether Canadians are meaningfully better off in 2035. It has been going the wrong way for over a decade.</p>

  <figure>
    <svg viewBox="0 0 720 230" role="img" aria-label="Comparison of cumulative real GDP per capita growth from Q4 2014 to Q2 2026: Canada 5 percent, United States 23 percent.">
      <g id="prodBars"></g>
    </svg>
    <figcaption>Cumulative real GDP per capita growth, Q4 2014 to Q2 2026. Canada has recorded the weakest real GDP-per-capita growth in the G7 since 2013 and fell below the OECD average for the first time on record in 2024.</figcaption>
  </figure>

  <ul class="clean">
    <li>Business labour productivity fell 0.5% in Q1 2026 after a 0.3% decline in Q4 2025, with declines in 10 of 16 major sectors. Unit labour costs rose 1.4%.</li>
    <li>Investment drives roughly 80% of productivity growth. Investment in extractive sectors fell 15% between 2010 and 2023, and multiple energy projects were cancelled or deferred after 2014.</li>
    <li>The OECD published a dedicated review in June 2026 arguing the fix is worker-oriented — skills, job mobility and easing structural change — as much as it is capital.</li>
    <li>McKinsey estimates that seizing the available growth opportunities would leave households roughly $16,000 better off by 2035. That is the size of the prize, and the size of the loss if nothing changes.</li>
  </ul>

  <div class="panel spine-s">
    <h4>Why it stayed broken for so long</h4>
    <p style="margin:0 0 10px">Three mutually reinforcing reasons. First, the 2014 oil boom masked weak performance everywhere else — the aggregate looked fine, so nothing was fixed. Second, capital drifted into domestically oriented, lower-productivity sectors, above all residential real estate, where returns were reliable and competition was limited. Third, population growth let firms expand output by adding workers instead of adding capital per worker, which is the cheaper choice every year and the wrong one over twenty.</p>
    <p style="margin:0">All three of those props are now gone simultaneously. That is uncomfortable, and it is also the most genuinely optimistic thing on this page.</p>
  </div>
  <p class="src">Sources: Statistics Canada labour productivity, Q1 2026; OECD, "Reviving Productivity Growth in Canada", June 2026; C.D. Howe Institute on the investment shortfall; McKinsey on Canada's productivity gap; Globe and Mail analysis of business investment intentions.</p>
</section>

<!-- ============ PROVINCES ============ -->
<section id="provinces">
  <h2 class="sec">The provincial split is widening</h2>
  <p class="deck">National averages are hiding two different economies. The oil and mineral west is having a good year. Manufacturing central Canada is absorbing the tariff damage. That divergence has political consequences well beyond economics.</p>

  <div class="tablewrap">
    <table>
      <thead><tr><th>Region</th><th>2026 position</th><th>Ten-year read</th></tr></thead>
      <tbody>
        <tr><td><strong>Alberta</strong></td><td><span class="tag t-exp">Strongest</span> Oil revenue surge, largely insulated from the 50% tariff list, West Coast pipeline proposal advancing, Pathways carbon capture in motion, and provincial fiscal balance improving on royalties.</td><td>The clearest beneficiary of a world that prices energy security. Risk is a single-commodity exposure if oil normalises faster than expected.</td></tr>
        <tr><td><strong>Saskatchewan</strong></td><td><span class="tag t-exp">Strong</span> Potash, uranium, the Foran copper project, and canola relief from the China deal.</td><td>Uranium and potash both sit in structurally tight global markets. Small population means large per-capita effects.</td></tr>
        <tr><td><strong>British Columbia</strong></td><td><span class="tag t-mix">Mixed</span> LNG Canada, Red Chris, port expansion and the North Coast Transmission Line on the build side. Housing affordability and weak sales on the drag side.</td><td>The corridor province. Everything Canada wants to sell to Asia leaves through BC, which makes port and rail capacity a national issue.</td></tr>
        <tr><td><strong>Ontario</strong></td><td><span class="tag t-mix">Split</span> Added 52,000 jobs in July and 119,000 over four months — the national growth engine. Simultaneously carrying auto, steel and parts losses, and opposing the Chinese EV quota.</td><td>The outcome depends almost entirely on the trade file. Darlington SMRs, defence work and data centres are the offsetting bets.</td></tr>
        <tr><td><strong>Quebec</strong></td><td><span class="tag t-mix">Mixed</span> Aluminum exposed to the 50% tariff; furniture makers closing; but housing is balanced and affordable and the Contrecœur port expansion is proceeding.</td><td>Cheap hydro is a genuine long-run asset for aluminum, data centres and electrification. Better positioned than the tariff headlines suggest.</td></tr>
        <tr><td><strong>Prairies broadly</strong></td><td><span class="tag t-exp">Leading</span> CMHC expects the Prairies to lead the country in both housing sales and price growth.</td><td>Affordability plus commodity income is drawing internal migration. The quiet demographic story of the decade.</td></tr>
        <tr><td><strong>Atlantic Canada</strong></td><td><span class="tag t-con">Weakest</span> CMHC assesses conditions here as the softest in the country.</td><td>The offsets are real but narrow: about 20% of national defence industry employment, Wind West Atlantic Energy, and Sisson tungsten in New Brunswick. Healthcare staffing crises declared in both NS and NB.</td></tr>
        <tr><td><strong>North</strong></td><td><span class="tag t-neu">Emerging</span> Arctic economic and security corridor, Port of Churchill upgrades, all-weather roads, and Nunavut's first Inuit-owned hydro project at Iqaluit.</td><td>Small base, enormous strategic weight. Arctic sovereignty spending is a policy commitment that will not reverse.</td></tr>
      </tbody>
    </table>
  </div>
  <p class="src">Sources: Statistics Canada Labour Force Survey, July 2026; CMHC Summer 2026 Housing Market Outlook; Prime Minister's Office and Stikeman Elliott on the Canada–BC Cooperative Prosperity Agreement; Major Projects Office tranche announcements.</p>
</section>

<!-- ============ OUTLOOK ============ -->
<section id="outlook">
  <h2 class="sec">Ten-year outlook</h2>
  <p class="deck">Three paths. The scenarios below are my synthesis of the forces on this page, not a published institutional forecast — treat the numbers as shapes rather than predictions, and pay more attention to the trigger conditions than the digits.</p>

  <div class="controls" role="group" aria-label="Select scenario">
    <button class="pill" data-scen="base" aria-pressed="true">Managed divergence · 50%</button>
    <button class="pill" data-scen="down" aria-pressed="false">Rupture · 25%</button>
    <button class="pill" data-scen="up" aria-pressed="false">Build-out · 25%</button>
  </div>

  <div class="scen-grid">
    <div class="scen-cell"><div class="lab">Average real GDP growth, 2027–2035</div><div class="val" id="s-gdp">1.5–1.9%</div></div>
    <div class="scen-cell"><div class="lab">Unemployment range</div><div class="val" id="s-unemp">5.8–6.5%</div></div>
    <div class="scen-cell"><div class="lab">US share of exports by 2035</div><div class="val" id="s-us">60–63%</div></div>
    <div class="scen-cell"><div class="lab">Real GDP per capita growth</div><div class="val" id="s-pc">0.8–1.2%</div></div>
    <div class="scen-cell"><div class="lab">Canadian dollar range</div><div class="val" id="s-cad">68–75¢</div></div>
    <div class="scen-cell"><div class="lab">Federal debt-to-GDP by 2035</div><div class="val" id="s-debt">42–46%</div></div>
  </div>

  <div class="panel" id="scenNarr"></div>

  <figure>
    <svg viewBox="0 0 720 300" role="img" aria-label="Fan chart of illustrative real GDP growth paths to 2035 under three scenarios: build-out, managed divergence, and rupture.">
      <g id="fanChart"></g>
    </svg>
    <figcaption>Illustrative annual real GDP growth paths. The bands are wide on purpose — the honest uncertainty here is larger than any point forecast implies.</figcaption>
  </figure>

  <h3>The six forces that decide which path Canada takes</h3>
  <details>
    <summary>1. Whether CUSMA survives its annual reviews</summary>
    <div class="body">
      <p>The agreement runs to 2036 regardless, but the annual review cycle means a permanent policy risk premium on every cross-border investment. If a stable settlement emerges by 2028 — even a narrower one — investment intentions recover quickly. If reviews become an annual leverage exercise, integrated manufacturing keeps quietly relocating south, and that is not reversible.</p>
      <p><em>Watch:</em> the 1 July 2027 review, and whether the US–Mexico bilateral track produces terms Canada is later handed.</p>
    </div>
  </details>
  <details>
    <summary>2. Whether the $135 billion project pipeline actually gets built</summary>
    <div class="body">
      <p>Announcement, referral to the Major Projects Office, final investment decision and shovels in the ground are four very different things. The two-year review clock is genuinely ambitious by Canadian standards. The failure modes are Indigenous consent processes done badly rather than properly, provincial coordination breaking down, and simply not having enough electricians.</p>
      <p><em>Watch:</em> FID announcements rather than referrals. LNG Canada Phase 2 and the West Coast pipeline proposal are the bellwethers.</p>
    </div>
  </details>
  <details>
    <summary>3. Whether private capital follows public capital</summary>
    <div class="body">
      <p>The central tension on this page. Oil and gas revenue is up 25% with flat capex. Machinery and equipment investment has been flat since 2009. Government cannot substitute for business investment at the scale required — it can only de-risk it. If the response to a $135bn pipeline and a defence ramp is another round of buybacks, Canada gets the debt without the productivity.</p>
      <p><em>Watch:</em> quarterly non-residential business investment, and the machinery and equipment line specifically.</p>
    </div>
  </details>
  <details>
    <summary>4. Whether the demographic squeeze becomes a discipline or a drag</summary>
    <div class="body">
      <p>Population is falling by policy design. The optimistic reading is that firms finally have to raise output per worker. The pessimistic reading is that a shrinking labour force, an aging population and rising health and pension costs simply lower potential growth while the tax base narrows. Both mechanisms are real; which dominates depends entirely on capital deployment.</p>
      <p><em>Watch:</em> the 2027–2029 Immigration Levels Plan this fall, and revised population estimates in September.</p>
    </div>
  </details>
  <details>
    <summary>5. Where oil settles after the Middle East shock</summary>
    <div class="body">
      <p>Middle East crude exports fell from about 18.3 million barrels a day to under 8.8 million after the crisis began. Analysts now see roughly US$85 WTI for 2026. A sustained US$10 increase adds an estimated 0.25–0.5% to Canadian GDP over 2026–27, concentrated regionally. But high oil also props up inflation, keeps the Bank of Canada on hold, and disguises weakness elsewhere — exactly as it did before 2014.</p>
      <p><em>Watch:</em> Strait of Hormuz throughput, and whether Canadian producers convert the windfall into capacity or dividends.</p>
    </div>
  </details>
  <details>
    <summary>6. Whether AI is a Canadian industry or a Canadian import</summary>
    <div class="body">
      <p>Canada has world-class research, 0.3 GW of AI data-centre capacity, and needs about 1.3 GW by 2030 for domestic workloads alone. Export potential runs from 1.7 GW to 6.7 GW. The advantages are clean power, cold climate and a stable legal regime. The constraint is grid interconnection and the fact that Canada has historically been excellent at inventing things and poor at scaling them.</p>
      <p><em>Watch:</em> announced data centre capacity reaching commercial operation, not just MOU signature.</p>
    </div>
  </details>
</section>

<!-- ============ EXPOSURE TOOL ============ -->
<section id="exposure">
  <h2 class="sec">Your exposure</h2>
  <p class="deck">Pick a sector and a province to see how this all lands in one place. Rough directional guidance, not advice.</p>

  <div class="tool">
    <div class="fields">
      <label class="f">Sector
        <select id="selSector">
          <option value="mfg">Manufacturing, general</option>
          <option value="auto">Automotive or parts</option>
          <option value="steel">Steel, aluminum or metal fabrication</option>
          <option value="energy">Oil, gas or pipelines</option>
          <option value="mining">Mining or critical minerals</option>
          <option value="trades">Skilled trades or construction</option>
          <option value="health">Healthcare</option>
          <option value="tech">Technology or software</option>
          <option value="defence">Defence or aerospace</option>
          <option value="finance">Finance, insurance or real estate</option>
          <option value="retail">Retail, hospitality or food service</option>
          <option value="public">Public sector</option>
          <option value="agri">Agriculture or agri-food</option>
          <option value="edu">Education or international students</option>
          <option value="forest">Forestry or lumber</option>
        </select>
      </label>
      <label class="f">Province or region
        <select id="selProv">
          <option value="on">Ontario</option>
          <option value="qc">Quebec</option>
          <option value="ab">Alberta</option>
          <option value="bc">British Columbia</option>
          <option value="sk">Saskatchewan</option>
          <option value="mb">Manitoba</option>
          <option value="atl">Atlantic Canada</option>
          <option value="north">Territories</option>
        </select>
      </label>
    </div>
    <div id="toolOut"></div>
  </div>
</section>

<!-- ============ CALENDAR ============ -->
<section id="calendar">
  <h2 class="sec">What's next</h2>
  <p class="deck">The dates that will move these numbers. Countdowns update against your device's clock.</p>
  <div class="cal" id="calList"></div>

  <h3>Leading indicators worth tracking yourself</h3>
  <ul class="clean">
    <li><strong>Bank of Canada Business Outlook Survey</strong> — investment and hiring intentions turn before the hard data does. Quarterly.</li>
    <li><strong>Non-residential business investment, machinery and equipment line</strong> — the single best test of whether the build-out is real.</li>
    <li><strong>Job vacancy rate versus unemployment</strong> — the ratio tells you whether the labour market is tightening or just shrinking.</li>
    <li><strong>Housing starts split between rental and condo</strong> — the aggregate is misleading; the composition tells you what's actually being built.</li>
    <li><strong>Exports to non-US destinations, excluding gold</strong> — the honest diversification scoreboard. Gold flows to London distort the headline badly.</li>
    <li><strong>Provincial electricity interconnection queues</strong> — the physical bottleneck on data centres, electrified mining and industrial growth. Almost nobody watches this and it matters enormously.</li>
    <li><strong>Announced projects reaching final investment decision</strong> — versus announced projects merely referred for review.</li>
  </ul>
</section>

<footer>
  <p>Built 31 August 2026 from public data, and reflecting figures available on that date. Sources are Statistics Canada, the Bank of Canada, CMHC, IRCC, Finance Canada, the Parliamentary Budget Officer, Global Affairs Canada, the OECD, and published bank and consultancy research, each cited beneath the relevant section. Scenario projections in the ten-year outlook are analytical synthesis and are labelled as such.</p>
  <p>Nothing here is financial, investment, legal or tax advice.</p>
</footer>

</main>
</div>

<script>
(function(){
  "use strict";
  var SVGNS = "http://www.w3.org/2000/svg";
  function el(name, attrs, text){
    var n = document.createElementNS(SVGNS, name);
    for (var k in attrs) n.setAttribute(k, attrs[k]);
    if (text != null) n.textContent = text;
    return n;
  }

  /* ---------- chart 1: export partners ---------- */
  (function(){
    var g = document.getElementById("partnerBars");
    if(!g) return;
    var data = [
      {n:"United States", v:68.0, c:"#215C8F"},
      {n:"United Kingdom", v:9.2, c:"#5E82A3"},
      {n:"China", v:5.0, c:"#8FA4B7"},
      {n:"European Union", v:5.0, c:"#B6C4D0"},
      {n:"All others", v:12.8, c:"#D8DFE5"}
    ];
    var x0 = 140, w = 520, rowH = 44, max = 70;
    data.forEach(function(d,i){
      var y = 14 + i*rowH;
      g.appendChild(el("text",{x:x0-12,y:y+18,"text-anchor":"end","font-size":"13",fill:"#5B6872"}, d.n));
      g.appendChild(el("rect",{x:x0,y:y,width:w,height:26,fill:"#F1F4F6"}));
      g.appendChild(el("rect",{x:x0,y:y,width:(d.v/max)*w,height:26,fill:d.c}));
      g.appendChild(el("text",{x:x0+(d.v/max)*w+9,y:y+18,"font-size":"13","font-weight":"650",fill:"#1B242C"}, d.v.toFixed(1)+"%"));
    });
    g.appendChild(el("line",{x1:x0,y1:14,x2:x0,y2:14+data.length*rowH-18,stroke:"#DCE2E7","stroke-width":"1"}));
  })();

  /* ---------- chart 2: employment change by industry ---------- */
  (function(){
    var g = document.getElementById("jobsBars");
    if(!g) return;
    var data = [
      {n:"Wholesale and retail trade", v:21.0},
      {n:"Finance and real estate",    v:18.0},
      {n:"Professional and technical", v:17.0},
      {n:"Construction",               v:16.0},
      {n:"Agriculture",                v:-9.6},
      {n:"Public administration",      v:-15.0}
    ];
    var gutter = 196,      /* right edge of the industry-name column */
        zeroX  = 420,      /* the zero line */
        scale  = 11,       /* px per thousand jobs */
        top    = 26,
        rowH   = 44,
        barH   = 26,
        plotBottom = top + data.length*rowH - (rowH - barH) + 8,
        axisY  = plotBottom + 16;

    /* gridlines behind the bars */
    [-15,-10,-5,0,5,10,15,20].forEach(function(t){
      var x = zeroX + t*scale;
      g.appendChild(el("line",{
        x1:x, y1:top-10, x2:x, y2:plotBottom,
        stroke: t===0 ? "#5B6872" : "#EAEEF1", "stroke-width":"1"
      }));
      g.appendChild(el("text",{
        x:x, y:axisY+4, "text-anchor":"middle", "font-size":"11",
        fill: t===0 ? "#5B6872" : "#8B97A1"
      }, (t>0?"+":"")+t));
    });
    g.appendChild(el("line",{x1:zeroX-15*scale, y1:plotBottom, x2:zeroX+20*scale, y2:plotBottom, stroke:"#DCE2E7","stroke-width":"1"}));
    g.appendChild(el("text",{x:zeroX, y:axisY+26, "text-anchor":"middle","font-size":"11.5", fill:"#8B97A1"}, "change in employment, thousands"));

    data.forEach(function(d,i){
      var y   = top + i*rowH;
      var pos = d.v >= 0;
      var len = Math.abs(d.v)*scale;

      /* industry name lives in its own column, clear of every bar */
      g.appendChild(el("text",{
        x:gutter, y:y+barH/2+5, "text-anchor":"end", "font-size":"12.5", fill:"#5B6872"
      }, d.n));

      g.appendChild(el("rect",{
        x: pos ? zeroX : zeroX-len, y:y, width:len, height:barH,
        fill: pos ? "#15704E" : "#B03A2E"
      }));

      /* value sits inside the bar, so it can never collide with anything */
      g.appendChild(el("text",{
        x: pos ? zeroX+len-10 : zeroX-len+10,
        y: y+barH/2+5,
        "text-anchor": pos ? "end" : "start",
        "font-size":"12.5", "font-weight":"650", fill:"#FFFFFF"
      }, (pos?"+":"−")+Math.abs(d.v).toFixed(1)));
    });
  })();

  /* ---------- chart 3: immigration targets ---------- */
  (function(){
    var g = document.getElementById("immBars");
    if(!g) return;
    var years = [
      {y:"2025", tr:673650, pr:393500},
      {y:"2026", tr:385000, pr:380000},
      {y:"2027", tr:370000, pr:380000},
      {y:"2028", tr:370000, pr:380000}
    ];
    var baseY = 216, maxV = 700000, h = 176, x0 = 70, groupW = 150, barW = 52;
    [0,200000,400000,600000].forEach(function(t){
      var y = baseY - (t/maxV)*h;
      g.appendChild(el("line",{x1:x0-14,y1:y,x2:660,y2:y,stroke:"#EAEEF1","stroke-width":"1"}));
      g.appendChild(el("text",{x:x0-22,y:y+4,"text-anchor":"end","font-size":"11",fill:"#8B97A1"}, (t/1000)+"k"));
    });
    years.forEach(function(d,i){
      var gx = x0 + i*groupW;
      var h1 = (d.tr/maxV)*h, h2 = (d.pr/maxV)*h;
      g.appendChild(el("rect",{x:gx,y:baseY-h1,width:barW,height:h1,fill:"#B03A2E"}));
      g.appendChild(el("rect",{x:gx+barW+8,y:baseY-h2,width:barW,height:h2,fill:"#215C8F"}));
      g.appendChild(el("text",{x:gx+barW/2,y:baseY-h1-7,"text-anchor":"middle","font-size":"11","font-weight":"650",fill:"#B03A2E"}, Math.round(d.tr/1000)+"k"));
      g.appendChild(el("text",{x:gx+barW+8+barW/2,y:baseY-h2-7,"text-anchor":"middle","font-size":"11","font-weight":"650",fill:"#215C8F"}, Math.round(d.pr/1000)+"k"));
      g.appendChild(el("text",{x:gx+barW+4,y:baseY+20,"text-anchor":"middle","font-size":"13",fill:"#5B6872"}, d.y));
    });
    g.appendChild(el("line",{x1:x0-14,y1:baseY,x2:660,y2:baseY,stroke:"#5B6872","stroke-width":"1"}));
    g.appendChild(el("rect",{x:x0,y:246,width:11,height:11,fill:"#B03A2E"}));
    g.appendChild(el("text",{x:x0+18,y:256,"font-size":"12",fill:"#5B6872"},"New temporary resident arrivals (target)"));
    g.appendChild(el("rect",{x:x0+272,y:246,width:11,height:11,fill:"#215C8F"}));
    g.appendChild(el("text",{x:x0+290,y:256,"font-size":"12",fill:"#5B6872"},"Permanent resident admissions"));
  })();

  /* ---------- chart 4: productivity gap ---------- */
  (function(){
    var g = document.getElementById("prodBars");
    if(!g) return;
    var data = [{n:"Canada", v:5, c:"#B03A2E"},{n:"United States", v:23, c:"#215C8F"}];
    var x0 = 150, w = 470, max = 26;
    data.forEach(function(d,i){
      var y = 34 + i*78;
      g.appendChild(el("text",{x:x0-14,y:y+30,"text-anchor":"end","font-size":"15","font-weight":"600",fill:"#1B242C"}, d.n));
      g.appendChild(el("rect",{x:x0,y:y,width:w,height:46,fill:"#F1F4F6"}));
      g.appendChild(el("rect",{x:x0,y:y,width:(d.v/max)*w,height:46,fill:d.c}));
      g.appendChild(el("text",{x:x0+(d.v/max)*w+12,y:y+30,"font-size":"20","font-weight":"600",fill:d.c}, "+"+d.v+"%"));
    });
    g.appendChild(el("text",{x:x0,y:206,"font-size":"12",fill:"#8B97A1"},"Cumulative real GDP per capita growth, Q4 2014 to Q2 2026"));
  })();

  /* ---------- chart 5: scenario fan ---------- */
  var fanPaths = {};
  (function(){
    var g = document.getElementById("fanChart");
    if(!g) return;
    var years = [2026,2027,2028,2029,2030,2031,2032,2033,2034,2035];
    var series = {
      up:   [1.1,2.4,2.6,2.5,2.4,2.3,2.3,2.2,2.2,2.2],
      base: [1.1,1.7,1.8,1.8,1.7,1.7,1.6,1.6,1.6,1.6],
      down: [1.1,-0.6,0.4,1.1,1.3,1.3,1.2,1.2,1.2,1.2]
    };
    var x0=64, x1=680, yTop=24, yBot=232, vMax=3, vMin=-1.2;
    function X(i){ return x0 + (i/(years.length-1))*(x1-x0); }
    function Y(v){ return yBot - ((v-vMin)/(vMax-vMin))*(yBot-yTop); }
    [-1,0,1,2,3].forEach(function(t){
      g.appendChild(el("line",{x1:x0,y1:Y(t),x2:x1,y2:Y(t),stroke: t===0?"#5B6872":"#EAEEF1","stroke-width":"1"}));
      g.appendChild(el("text",{x:x0-10,y:Y(t)+4,"text-anchor":"end","font-size":"11",fill:"#8B97A1"}, t+"%"));
    });
    years.forEach(function(y,i){
      if(i%2===0 || i===years.length-1)
        g.appendChild(el("text",{x:X(i),y:yBot+20,"text-anchor":"middle","font-size":"11",fill:"#8B97A1"}, y));
    });
    var meta = {up:{c:"#15704E",l:"Build-out"}, base:{c:"#215C8F",l:"Managed divergence"}, down:{c:"#B03A2E",l:"Rupture"}};
    ["up","base","down"].forEach(function(k){
      var d = series[k].map(function(v,i){ return (i?"L":"M")+X(i).toFixed(1)+" "+Y(v).toFixed(1); }).join(" ");
      var p = el("path",{d:d,fill:"none",stroke:meta[k].c,"stroke-width":"2.5","stroke-linejoin":"round",opacity: k==="base"?"1":"0.32"});
      p.setAttribute("data-scen",k);
      g.appendChild(p);
      fanPaths[k]=p;
    });
    var lx = x0;
    ["down","base","up"].forEach(function(k){
      g.appendChild(el("rect",{x:lx,y:262,width:11,height:11,fill:meta[k].c}));
      g.appendChild(el("text",{x:lx+17,y:272,"font-size":"12",fill:"#5B6872"}, meta[k].l));
      lx += 168;
    });
  })();

  /* ---------- sector filter ---------- */
  (function(){
    var btns = document.querySelectorAll('[data-filter]');
    var rows = document.querySelectorAll('#sectorTable tbody tr');
    btns.forEach(function(b){
      b.addEventListener('click', function(){
        btns.forEach(function(o){ o.setAttribute('aria-pressed','false'); });
        b.setAttribute('aria-pressed','true');
        var f = b.getAttribute('data-filter');
        rows.forEach(function(r){
          r.style.display = (f==='all' || r.getAttribute('data-cat')===f) ? '' : 'none';
        });
      });
    });
  })();

  /* ---------- scenarios ---------- */
  (function(){
    var S = {
      base: {
        gdp:"1.5–1.9%", unemp:"5.8–6.5%", us:"60–63%", pc:"0.8–1.2%", cad:"68–75¢", debt:"42–46%",
        title:"Managed divergence",
        body:"CUSMA survives its annual reviews in a narrowed form, with sectoral carve-outs negotiated one at a time and periodic flare-ups. Most of the $135bn project pipeline proceeds but late and over budget. Defence spending rises toward 3% rather than 3.5% of GDP. Non-US exports grow substantially in percentage terms — perhaps 30 to 40 percent higher by 2035 — while the US share still sits above 60 percent because the base is so much larger. Manufacturing employment settles at a permanently lower level. Productivity growth resumes at around one percent a year, helped as much by a shrinking labour force as by rising investment. Living standards improve slowly and unevenly, with Alberta, Saskatchewan and BC pulling ahead of Ontario and the Atlantic provinces. This is not a good outcome. It is a survivable one, and it is the most likely."
      },
      down: {
        gdp:"0.6–1.1%", unemp:"7.0–8.5%", us:"55–60%", pc:"−0.2–0.4%", cad:"62–70¢", debt:"48–54%",
        title:"Rupture",
        body:"Escalation continues, the tariff perimeter widens beyond the current C$28bn list, and CUSMA either lapses at an annual review or is hollowed out to the point of irrelevance. Roughly 90,000 jobs go in the exposed sectors — machinery, electronics, plastics, textiles — concentrated in Ontario and Quebec, with the auto supply chain hit hardest because parts cross the border repeatedly. Canada enters recession in 2027. The dollar falls toward 62 to 65 cents, which cushions exporters and punishes every household buying imported food, fuel and equipment. Deficits widen well past $80bn as stabilisers kick in alongside defence commitments. The lasting damage is not the recession; it is that relocated supply chains do not come back, and Canada emerges structurally smaller in tradeable manufacturing."
      },
      up: {
        gdp:"2.2–2.6%", unemp:"5.0–5.8%", us:"55–58%", pc:"1.6–2.1%", cad:"73–80¢", debt:"38–42%",
        title:"Build-out",
        body:"Project after project reaches final investment decision on the two-year clock. LNG Canada Phase 2, the West Coast pipeline, Darlington SMRs and the critical minerals tranche all deliver. Private capital matches public commitment instead of returning it to shareholders. Data-centre capacity scales past domestic need into genuine export volume. Interprovincial trade barriers actually fall rather than being announced as falling. Defence spending builds a real industrial base rather than buying finished foreign kit. Immigration stabilises at a sustainable level and credential recognition speeds up. Productivity growth returns to roughly two percent and real GDP per capita starts closing the gap with peers for the first time since 2014. Every element of this is already announced. None of it is yet delivered, and that distinction is the whole story."
      }
    };
    var out = {gdp:"s-gdp",unemp:"s-unemp",us:"s-us",pc:"s-pc",cad:"s-cad",debt:"s-debt"};
    var narr = document.getElementById("scenNarr");
    function render(k){
      var s = S[k];
      for (var f in out) document.getElementById(out[f]).textContent = s[f];
      narr.className = "panel " + (k==="up"?"spine-g":k==="down"?"spine-r":"spine-s");
      narr.innerHTML = "<h4>"+s.title+"</h4><p style='margin:0'>"+s.body+"</p>";
      for (var p in fanPaths) fanPaths[p].setAttribute("opacity", p===k ? "1" : "0.22");
    }
    var btns = document.querySelectorAll('[data-scen]');
    btns.forEach(function(b){
      b.addEventListener('click', function(){
        btns.forEach(function(o){ o.setAttribute('aria-pressed','false'); });
        b.setAttribute('aria-pressed','true');
        render(b.getAttribute('data-scen'));
      });
    });
    render("base");
  })();

  /* ---------- exposure tool ---------- */
  (function(){
    var sec = {
      mfg:{s:-2,t:"Directly exposed. Over 60% of Canadian manufacturing has substantial US trade exposure, and the sector has shed more than 50,000 jobs over the past year."},
      auto:{s:-3,t:"The most damaged sector in the country. Parts employment fell 8.7% year over year, Oshawa dropped a shift, and Brampton has been idle for nearly two years. Chinese EV quotas add domestic competition on top of tariffs."},
      steel:{s:-3,t:"Under a 50% US tariff with roughly 2,000 layoffs already. Survival depends on Buy Canadian procurement and domestic infrastructure demand actually materialising."},
      energy:{s:3,t:"The strongest position in the economy. Industry revenue is up about 25% this year on the post-Hormuz price surge, and Canada is being repriced as a secure supplier."},
      mining:{s:3,t:"Structural winner. Critical minerals sit at the intersection of defence, grid build-out and AI power demand, with federal fast-tracking behind them."},
      trades:{s:3,t:"The binding constraint on the entire national build-out. Ottawa is funding 80,000 to 100,000 new trades workers by 2030–31 because it cannot find them."},
      health:{s:2,t:"Demographically locked-in demand for the full decade. The caveat is fiscal: health vacancies fell to their lowest level since early 2020 as budgets, not need, now cap hiring."},
      tech:{s:1,t:"Bifurcating. AI infrastructure, security and defence-adjacent work is expanding; generalist software and analysis roles face pressure from both offshoring and the tools themselves. Vacancies requiring a degree fell 6.9% year over year."},
      defence:{s:3,t:"The most predictable growth path available, because it is a treaty commitment rather than a market forecast. The route from 2% to 3.5% of GDP by 2035 implies roughly $33.5bn a year in additional spending."},
      finance:{s:1,t:"Employment resilient — up 18,000 in July — but the revenue mix is shifting away from mortgage origination as transaction volumes stay weak."},
      retail:{s:0,t:"Follows real household income. Counter-tariffs on US appliances, electronics and food will lift shelf prices this autumn, and reduced student and temporary worker inflows shrink both the customer base and the labour pool."},
      public:{s:-1,t:"Under sustained restraint. Public administration lost 15,000 jobs in July and public sector employment fell 27,000 that month. Resources are shifting toward defence procurement and capital projects."},
      agri:{s:1,t:"Improving access, shrinking employment. The China deal cut canola duties sharply and lifted them on peas, lobster and crab, but the sector still lost 9,600 jobs in July as it consolidates."},
      edu:{s:-3,t:"Deliberately shrunk by policy. New study permits are being cut roughly in half, and the damage extends to student housing, college-town retail and any employer that staffed itself with student labour."},
      forest:{s:-2,t:"Named by Finance Canada as one of the least diversified and most tariff-exposed sectors, and now facing a weaker domestic housing start pipeline as well."}
    };
    var prov = {
      on:{s:-1,t:"Ontario is the national job engine — 119,000 added over four months — while simultaneously absorbing the auto, steel and parts losses. Your sector determines which Ontario you live in."},
      qc:{s:0,t:"Quebec has aluminum exposure and furniture closures, offset by cheap hydro that is a genuine long-run asset for aluminum, data centres and electrification, plus the Contrecœur port expansion."},
      ab:{s:2,t:"Alberta is the strongest provincial economy this year, largely insulated from the current tariff list, with the West Coast pipeline proposal and Pathways carbon capture advancing."},
      bc:{s:1,t:"British Columbia is the corridor province: LNG, Red Chris, port expansion and transmission on the build side, weighed against the country's toughest housing affordability."},
      sk:{s:2,t:"Saskatchewan benefits from potash, uranium, the Foran copper project and canola relief, with a small population magnifying per-capita effects."},
      mb:{s:1,t:"Manitoba added 5,900 jobs in July and stands to gain from Port of Churchill upgrades and Arctic corridor investment."},
      atl:{s:-1,t:"Atlantic Canada has the softest conditions in the country per CMHC, partly offset by holding about 20% of national defence industry employment and the Sisson tungsten project in New Brunswick."},
      north:{s:1,t:"The territories have a small base but disproportionate strategic weight, with Arctic security corridor spending, Churchill upgrades and Nunavut's first Inuit-owned hydro project."}
    };
    var sS = document.getElementById("selSector"), sP = document.getElementById("selProv"), out = document.getElementById("toolOut");
    function verdict(n){
      if (n >= 4) return {t:"Well positioned", c:"var(--spruce)"};
      if (n >= 2) return {t:"Favourable", c:"var(--spruce)"};
      if (n >= 0) return {t:"Broadly neutral", c:"var(--slate)"};
      if (n >= -2) return {t:"Under pressure", c:"var(--amber)"};
      return {t:"Highly exposed", c:"var(--rust)"};
    }
    function render(){
      var a = sec[sS.value], b = prov[sP.value];
      var v = verdict(a.s + b.s);
      out.innerHTML =
        '<div class="score" style="color:'+v.c+'">'+v.t+'</div>'+
        '<p style="margin:0 0 10px"><strong>Sector.</strong> '+a.t+'</p>'+
        '<p style="margin:0 0 10px"><strong>Region.</strong> '+b.t+'</p>'+
        '<p style="margin:0;color:var(--ink-3);font-size:13px">Directional guidance built from the data on this page, not personal advice. Individual employers vary far more than sector averages.</p>';
    }
    sS.addEventListener("change", render);
    sP.addEventListener("change", render);
    render();
  })();

  /* ---------- calendar with live countdown ---------- */
  (function(){
    var items = [
      {d:"2026-09-02", t:"Bank of Canada rate decision", n:"Held at 2.25% for six meetings. Markets expect no change, but the counter-tariff inflation impulse complicates the path."},
      {d:"2026-09-04", t:"Labour Force Survey, August", n:"Tests whether the three-month hiring streak survives the tariff announcement."},
      {d:"2026-09-08", t:"Canadian counter-tariffs take effect", n:"15%, 25% and 50% on roughly $20bn of US goods: steel, dairy, appliances, farm equipment, pulp and paper, electronics."},
      {d:"2026-09-14", t:"Consumer Price Index, August", n:"First read on whether gasoline pressure is fading before counter-tariffs arrive in the data."},
      {d:"2026-09-30", t:"Revised population estimates", n:"Statistics Canada updates the preliminary Q1 decline. Could revise smaller, larger, or into growth."},
      {d:"2026-10-28", t:"Bank of Canada Monetary Policy Report", n:"First full forecast incorporating the August tariffs and the September countermeasures."},
      {d:"2026-11-15", t:"2027–2029 Immigration Levels Plan", n:"Due in the fall. The signal on whether population contraction is a phase or a policy direction."},
      {d:"2026-11-30", t:"Federal budget or fall economic statement", n:"Watch for a credible defence funding path — its absence has been the standing criticism."},
      {d:"2027-07-01", t:"First annual CUSMA joint review", n:"The new recurring event. Repeats every year until extension is agreed or the agreement expires."},
      {d:"2036-07-01", t:"CUSMA expiry, if never extended", n:"The outer boundary of the current trade architecture."}
    ];
    var wrap = document.getElementById("calList");
    var now = new Date(); now.setHours(0,0,0,0);
    var fmt = new Intl.DateTimeFormat("en-CA",{month:"short", day:"numeric", year:"numeric"});
    items.forEach(function(it){
      var dt = new Date(it.d + "T00:00:00");
      var days = Math.round((dt - now)/86400000);
      var past = days < 0;
      var row = document.createElement("div");
      row.className = "row" + (past ? " past" : "");
      var cLabel = past ? "in effect" : days === 0 ? "today" : days === 1 ? "tomorrow" : days < 400 ? "in " + days + " days" : "in " + Math.round(days/365.25) + " years";
      row.innerHTML =
        '<div class="d">'+fmt.format(dt)+'</div>'+
        '<div><strong>'+it.t+'</strong><br><span style="color:var(--ink-2)">'+it.n+'</span></div>'+
        '<div class="c" style="color:'+(past?"var(--ink-3)":(days<14?"var(--rust)":"var(--ink-2)"))+'">'+cLabel+'</div>';
      wrap.appendChild(row);
    });
  })();

  /* ---------- scrollspy ---------- */
  (function(){
    var links = Array.prototype.slice.call(document.querySelectorAll('nav.rail a'));
    var map = {};
    links.forEach(function(a){ map[a.getAttribute('href').slice(1)] = a; });
    var secs = Array.prototype.slice.call(document.querySelectorAll('section[id]'));
    if(!("IntersectionObserver" in window)) return;
    var io = new IntersectionObserver(function(entries){
      entries.forEach(function(e){
        if(e.isIntersecting){
          links.forEach(function(a){ a.classList.remove('on'); });
          if(map[e.target.id]) map[e.target.id].classList.add('on');
        }
      });
    }, {rootMargin:"-15% 0px -70% 0px", threshold:0});
    secs.forEach(function(s){ io.observe(s); });
  })();
})();
</script>
</body>
</html>
