# Report template

This is the report page for the arrows-win-loss-analysis skill, as one HTML page in the code block below. Copy the whole page in that code block exactly, and fill in only the data, as the skill's steps describe.

```html
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Win-loss analysis</title>
<style>
:root{
  color-scheme:light;
  --paper:#F7F6F3; --card:#FFFFFF; --ink:#171614; --ink-70:rgba(23,22,20,.7); --ink-50:rgba(23,22,20,.58); --ink-30:rgba(23,22,20,.3);
  --line:#E9E8E4; --chip:#F3F2EF; --track:#ECEAE6;
  --green:#1F8A4C; --green-soft:#E8F4EC;
  --red:#D33A24; --red-soft:#FCEAE6;
  --gold:#FEBC22; --gold-soft:#FFF4D6; --gold-text:#8A5A00;
  --display:'Plus Jakarta Sans',system-ui,-apple-system,'Segoe UI',sans-serif;
}
*{box-sizing:border-box}
body{margin:0;background:var(--paper);color:var(--ink);font:14px/1.5 "Plus Jakarta Sans",system-ui,-apple-system,"Segoe UI","Helvetica Neue",Arial,sans-serif;-webkit-font-smoothing:antialiased}
.wrap{max-width:960px;margin:0 auto;padding:16px 16px 40px}
.num{font-variant-numeric:tabular-nums}
.chip{display:block;font-family:var(--display);font-size:18px;font-weight:700;letter-spacing:-.2px;color:var(--ink)}
.hero{background:#171614;color:#FFFFFF;position:relative;border-radius:4px;padding:20px 24px 18px}
.hero h1{font-family:var(--display);font-feature-settings:"lnum","tnum";color:#FFFFFF;font-size:32px;line-height:1.12;letter-spacing:-.6px;font-weight:700;margin:0 0 4px;max-width:760px}
.hero .sub{color:rgba(255,255,255,.75);font-size:15px;margin:0 0 16px}
.health{display:flex;height:10px;border-radius:2px;overflow:hidden;background:rgba(250,248,245,.15)}
.g-fill{background:var(--green)}
.r-fill{background:var(--red)}
.stats{display:grid;grid-template-columns:repeat(4,1fr);margin-top:14px;border-top:1px solid rgba(250,248,245,.16)}
.stat{padding:14px 12px 0 0}
.stat+.stat{padding-left:16px;border-left:1px solid rgba(250,248,245,.16)}
.stat .n{font-family:var(--display);font-feature-settings:"lnum","tnum";font-size:28px;font-weight:700;letter-spacing:-.5px}
.stat .l{font-size:12px;color:rgba(255,255,255,.75)}
.stat .key{display:inline-block;width:8px;height:8px;border-radius:2px;margin-right:6px;vertical-align:1px}
.card{background:var(--card);border:1px solid var(--line);border-radius:4px;padding:20px 22px;margin-top:16px}
.head{display:flex;justify-content:space-between;align-items:baseline;margin-bottom:6px;padding-bottom:10px;border-bottom:1px solid var(--line)}
.hint{font-size:12px;color:var(--ink-50)}
.item{border-top:1px solid var(--line)}
.head + .item{border-top:0}
.row{display:grid;grid-template-columns:26px 1fr 14px;gap:6px;padding:10px 0;align-items:start}
details.item summary{list-style:none;cursor:pointer}
details.item summary::-webkit-details-marker{display:none}
details.item summary .row::after{content:"";width:7px;height:7px;border-right:1.5px solid var(--ink-30);border-bottom:1.5px solid var(--ink-30);transform:rotate(-45deg);margin-top:7px;transition:transform .15s}
details.item[open] summary .row::after{transform:rotate(45deg)}
details.item summary:hover .row::after{border-color:var(--ink-70)}
.mark.dot::before{content:"";display:inline-block;width:8px;height:8px;border-radius:50%;background:var(--ink-30);margin-top:6px}
.mark.dot.r::before{background:var(--red)}
.mark.dot.g::before{background:var(--green)}
.tick{width:16px;height:16px;border-radius:50%;background:var(--green);color:#fff;font-size:10px;font-weight:700;display:flex;align-items:center;justify-content:center;margin-top:2px}
.title{font-weight:600}
.who{font-size:12px;color:var(--ink-50);font-weight:400;margin-left:6px}
.sub2{font-size:13px;color:var(--ink-70)}
.detail{margin:0 20px 12px 28px;padding:10px 12px;background:#F5F4F1;border-radius:6px;font-size:13px;color:var(--ink-70)}
.detail ul,.detail ol{margin:0;padding-left:18px}
.detail ol li{color:var(--ink)}
.detail .ctx{margin-top:8px;font-size:12px;color:var(--ink-50)}
a.stat{display:block;color:inherit;text-decoration:none;cursor:pointer}
a.stat:hover .l{text-decoration:underline;text-underline-offset:2px}
section[id]{scroll-margin-top:12px}
.cols{display:grid;grid-template-columns:1fr 1fr}
.cols > .item:nth-child(odd){padding-right:22px;border-right:1px solid var(--line)}
.cols > .item:nth-child(even){padding-left:22px}
.num-badge{width:22px;height:22px;border-radius:50%;background:var(--ink);color:#fff;font-size:12px;font-weight:700;display:flex;align-items:center;justify-content:center;margin-top:-1px}
.cols > .item:nth-child(-n+2){border-top:0}
.detail li+li{margin-top:3px}
.next{color:var(--ink);font-size:13px}
.next::before{content:"→ ";color:var(--ink-30)}
.qline{margin:3px 0 2px}
.tag.r{background:var(--red-soft);color:var(--red)}
.tag.g{background:var(--green-soft);color:var(--green)}
.tag.n{background:var(--chip);color:var(--ink-70)}
.empty{font-size:13px;color:var(--ink-50);padding:6px 0}
.rep-row{display:grid;grid-template-columns:190px 1fr;gap:12px}
.minibar{display:flex;height:8px;border-radius:2px;overflow:hidden;background:var(--track);margin-top:6px;max-width:220px}
.more{font-size:12px;color:var(--ink-50);padding-top:10px;border-top:1px solid var(--line)}
.r-al{text-align:right}
.meta{font-size:12px;color:var(--ink-50)}
footer{display:flex;justify-content:space-between;gap:12px;flex-wrap:wrap;margin-top:20px;font-size:12px;color:var(--ink-50)}
footer details summary{cursor:pointer}
footer a{color:var(--ink-70);text-decoration:underline;text-underline-offset:2px}
footer a:hover{color:var(--ink)}
.about{max-width:680px;margin-top:6px;padding:12px 14px;background:var(--card);border:1px solid var(--line);border-radius:4px;color:var(--ink-70);font-size:13px}
.about p{margin:0 0 8px}
.about p:last-child{margin:0}
.about b{color:var(--ink);font-weight:600}
.tag.g{color:#127A3E!important}
.y-fill{background:var(--gold)}
.mark.dot.y::before{background:var(--gold)}
.tag.y{background:var(--gold-soft);color:var(--gold-text)}
.tag{display:inline-block;font-size:12px;font-weight:600;border-radius:2px;padding:1px 6px;white-space:nowrap;margin:2px 6px 0 0}
.vs{display:grid;grid-template-columns:62px 1fr 84px;gap:2px 10px;align-items:center;margin-top:6px;max-width:520px;font-size:12px;color:var(--ink-50)}
.vs .bar{display:flex;height:8px;border-radius:2px;overflow:hidden;background:var(--track)}
.vs .v{text-align:right;color:var(--ink-70)}
.rate{display:grid;grid-template-columns:1fr 110px;gap:4px 14px;align-items:center}
.rate .bar{grid-column:1/3;position:relative;display:flex;height:8px;border-radius:2px;overflow:hidden;background:var(--track)}
.n-fill{background:var(--ink-30)}
.rate .avg{position:absolute;top:0;bottom:0;width:2px;background:var(--ink)}
.sublabel{font-size:13px;font-weight:600;padding:14px 0 2px;border-top:1px solid var(--line);margin-top:6px}
.head + .sublabel{border-top:0;margin-top:0;padding-top:4px}
.callout{margin-top:12px;padding:12px 14px;background:var(--chip);border-radius:4px;font-size:13px}
.callout b{font-weight:600}
.para{font-size:13px;color:var(--ink-70);margin:8px 0 0}
.para b{color:var(--ink);font-weight:600}
.qs{margin:4px 0 0;padding-left:18px;font-size:13px;color:var(--ink-70)}
.qs li+li{margin-top:3px}
@media (max-width:720px){
  .hero{padding:22px 18px 18px}
  .hero h1{font-size:25px}
  .stats{grid-template-columns:repeat(2,1fr)}
  .stat:nth-child(3){padding-left:0;border-left:0}
  .stat:nth-child(n+3){margin-top:10px}
  .cols{grid-template-columns:1fr}
  .cols > .item:nth-child(2){border-top:1px solid var(--line)}
  .cols > .item:nth-child(odd){padding-right:0;border-right:0}
  .cols > .item:nth-child(even){padding-left:0}
  .card{padding:16px}
  .detail{margin:0 0 12px 28px}
  .head{flex-direction:column;align-items:flex-start;gap:2px}
  .vs{grid-template-columns:54px 1fr 74px}
  .rate{grid-template-columns:1fr 90px}
}
</style>
</head>
<body>
<div class="wrap" id="app"></div>
<script>
/* Fill in DATA only. Leave everything else as is. */
const DATA = {
  name: "[First name]",
  company: "[Company]",
  period: "Closed [month year] – [month year]",
  pipeline: "[pipeline name]",
  updated: "[date]",
  numbers: { closed: 0, won: 0, lost: 0, excluded: 0, winCycle: 0, lossCycle: 0, wonValue: 0, lostValue: 0 },
  basis: { readWins: 0, readLosses: 0, readStalled: 0, calls: 0, callsFull: 0, emails: 0 },
  changes: [],
  segments: [],
  moves: [],
  noise: [],
  lossStages: [],
  timing: "",
  reasons: [],
  noReason: 0,
  buyingGroup: [],
  methodology: { name: "", onPaper: "", inPractice: "", recommended: false, elements: [] },
  stalled: "",
  reps: [],
  topRep: "",
  profileCheck: [],
  openQuestions: [],
  howBuilt: "[What was read, how it was sampled, what was left out, what couldn't be measured]"
};

const esc = s => String(s ?? "").replace(/[&<>"]/g, c => ({ "&": "&amp;", "<": "&lt;", ">": "&gt;", '"': "&quot;" })[c]);
const money = n => !n ? "" : n >= 1e6 ? "$" + (n / 1e6).toFixed(1).replace(/\.0$/, "") + "M" : n >= 1e3 ? "$" + Math.round(n / 1e3) + "k" : "$" + n;
const pct = (a, b) => b > 0 ? Math.max(0, Math.min(100, a / b * 100)) : 0;
const list = a => (a || []).filter(Boolean);
const D = DATA, N = D.numbers || {}, B = D.basis || {}, team = list(D.reps).length > 0;
const rate = Math.round(pct(N.won, N.closed));
const go = id => `href="#${id}" onclick="const t=document.getElementById('${id}');if(t){t.scrollIntoView({behavior:'smooth'});}return false;"`;
const cols = items => items.length ? `<div class="cols">${items.join("")}</div>` : "";
const detailBox = d => {
  const lines = Array.isArray(d) ? list(d) : d ? [d] : [];
  return lines.length ? `<div class="detail"><ul>${lines.map(l => `<li>${esc(l)}</li>`).join("")}</ul></div>` : "";
};
const stepsBox = (steps, context) => {
  const st = list(steps);
  if (!st.length && !context) return "";
  return `<div class="detail">${st.length ? `<ol>${st.map(x => `<li>${esc(x)}</li>`).join("")}</ol>` : ""}${context ? `<div class="ctx">${esc(context)}</div>` : ""}</div>`;
};
const item = (mark, title, sub, detail, box0) => {
  const body = `<div class="row">${mark}<div>${title}${sub ? `<div class="sub2">${sub}</div>` : ""}</div></div>`;
  const box = box0 || detailBox(detail);
  return box ? `<details class="item"><summary>${body}</summary>${box}</details>` : `<div class="item">${body}</div>`;
};
const card = (id, title, hint, inner) => inner ? `<section class="card"${id ? ` id="${id}"` : ""}><div class="head"><span class="chip">${title}</span>${hint ? `<span class="hint">${hint}</span>` : ""}</div>${inner}</section>` : "";
const early = x => (x.winsOf && x.winsOf < 5) || (x.lossesOf && x.lossesOf < 5);
const vs = x => `<div class="vs num"><span>Wins</span><div class="bar"><span class="g-fill" style="width:${pct(x.wins, x.winsOf)}%"></span></div><span class="v">${x.wins} of ${x.winsOf}</span><span>Losses</span><div class="bar"><span class="r-fill" style="width:${pct(x.losses, x.lossesOf)}%"></span></div><span class="v">${x.losses} of ${x.lossesOf}</span></div>`;
const gap = x => pct(x.wins, x.winsOf) - pct(x.losses, x.lossesOf);
const earlyTag = `<span class="tag n">Early signal</span>`;

let h = "";
h += `<section class="hero"><h1>${team ? esc(D.company || "Sales team") + " win-loss analysis" : esc(D.name) + "'s win-loss analysis"}</h1><p class="sub">${esc([D.period, team ? `Team view · ${list(D.reps).length} reps` : "Own deals", D.pipeline].filter(Boolean).join(" · "))}</p>`;
h += `<div class="health"><span class="g-fill" style="width:${pct(N.won, N.closed)}%"></span><span class="r-fill" style="width:${pct(N.lost, N.closed)}%"></span></div>`;
const topStage = list(D.lossStages).slice().sort((a, b) => b.lost - a.lost)[0];
h += `<div class="stats num">
  <a class="stat" ${go("who")}><div class="n">${rate}%</div><div class="l"><span class="key g-fill"></span>Win rate · ${N.won} won of ${N.closed} closed${N.wonValue ? " · " + money(N.wonValue) + " won" : ""}</div></a>
  <a class="stat" ${go("moves")}><div class="n">${list(D.moves).length}</div><div class="l">Moves seen far more on wins than losses, from ${B.readWins} wins and ${B.readLosses} losses read in full</div></a>
  <a class="stat" ${go("die")}><div class="n">${topStage ? topStage.lost : N.lost}</div><div class="l"><span class="key r-fill"></span>${topStage ? `of the ${N.lost} losses ended at ${esc(topStage.stage)}` : "Deals lost"}</div></a>
  <div class="stat"><div class="n">${N.winCycle ? N.winCycle + "d" : "–"}</div><div class="l">Median days to win${N.lossCycle ? ` · losses take ${N.lossCycle}d` : ""}</div></div>
</div></section>`;

h += card("changes", "Three things to change this quarter", "The changes most likely to raise the win rate · open one for the steps",
  list(D.changes).map((c, i) => item(`<span class="num-badge">${i + 1}</span>`, `<span class="title">${esc(c.change)}</span>${c.owner ? `<span class="who">${esc(c.owner)}</span>` : ""}`, esc(c.why), null, stepsBox(c.steps, c.context))).join(""));

let mv = list(D.moves).map((m, i) => item(`<span class="num-badge">${i + 1}</span>`, `<span class="title">${esc(m.move)}</span>${early(m) ? " " + earlyTag : ""}${vs(m)}`, esc(m.why), m.detail)).join("");
if (list(D.noise).length) mv += `<div class="sublabel">Noise: happens on most deals, won or lost, so it doesn't decide anything</div>` + cols(list(D.noise).map(n => item(`<span class="mark dot"></span>`, `<span class="title">${esc(n.what)}</span>${n.winsOf ? vs(n) : ""}`, "", n.detail)));
h += card("moves", "The moves that win", "How often each happened on wins and on losses", mv || `<div class="empty">Not enough closed deals to compare wins and losses yet.</div>`);

const dims = [...new Set(list(D.segments).map(s => s.dimension || "Segment"))];
const who = dims.map(dim => `<div class="sublabel">${esc(dim)}</div>` + cols(list(D.segments).filter(s => (s.dimension || "Segment") === dim).map(s => {
  const r = Math.round(pct(s.won, s.closed)), lvl = s.closed < 5 ? "" : r >= rate ? "g" : "r";
  return item(`<span class="mark dot ${lvl}"></span>`, `<div class="rate"><div><span class="title">${esc(s.name)}</span>${s.closed < 5 ? " " + earlyTag : ""}</div><div class="r-al num"><b>${r}%</b> <span class="meta">${s.won} of ${s.closed}</span></div><div class="bar"><span class="${lvl || "n"}-fill" style="width:${r}%"></span><span class="avg" style="left:${rate}%"></span></div></div>`, esc(s.note), s.detail);
}))).join("");
h += card("who", "Who wins", `Win rate by segment · the black line is the ${rate}% overall rate`, who);

let die = "";
if (list(D.lossStages).length) die += `<div class="sublabel">Where losses happen</div>` + list(D.lossStages).map(s => item(`<span class="mark dot r"></span>`, `<div class="rate"><span class="title">${esc(s.stage)}</span><div class="r-al num"><b>${s.lost}</b> <span class="meta">of ${N.lost}</span></div><div class="bar"><span class="r-fill" style="width:${pct(s.lost, N.lost)}%"></span></div></div>`, esc(s.note), s.detail)).join("");
if (D.timing) die += `<div class="callout"><b>Timing:</b> ${esc(D.timing)}</div>`;
if (list(D.reasons).length) die += `<div class="sublabel">Why they really lost, and what the CRM says</div>` + cols(list(D.reasons).map(r => item(`<span class="mark dot r"></span>`, `<span class="title">${esc(r.reason)}</span><div class="qline"><span class="tag r">Found on ${r.found} of ${r.foundOf} read</span><span class="tag n">${r.crm == null ? "No CRM option" : `CRM: ${r.crm} of ${r.crmOf}`}</span></div>`, esc(r.note), r.detail)));
if (D.noReason) die += `<div class="more">${D.noReason} of ${N.lost} losses have no reason in the CRM.</div>`;
if (D.stalled) die += `<div class="callout"><b>Stalled deals now:</b> ${esc(D.stalled)}</div>`;
h += card("die", "Where and why deals die", "The stage, the timing and the real reasons, from reading each lost deal", die);

h += card("group", "The buying group", "Who was involved on wins, and who was missing on losses", list(D.buyingGroup).map(b => item(`<span class="mark dot ${gap(b) >= 25 ? "g" : ""}"></span>`, `<span class="title">${esc(b.role)}</span>${early(b) ? " " + earlyTag : ""}${vs(b)}`, esc(b.note), b.detail)).join(""));

const M = D.methodology || {};
let me = "";
if (M.onPaper || M.inPractice) me += `<p class="para"><b>On paper:</b> ${esc(M.onPaper)}</p><p class="para"><b>In practice:</b> ${esc(M.inPractice)}</p>`;
if (list(M.elements).length) me += `<div class="sublabel">What was known, and by when, on wins and losses</div>` + list(M.elements).map(e => {
  const p = !early(e) && gap(e) >= 25;
  return item(`<span class="mark dot ${p ? "g" : ""}"></span>`, `<span class="title">${esc(e.element)}</span>${e.byStage ? `<span class="who">by ${esc(e.byStage)}</span>` : ""} ${early(e) ? earlyTag : `<span class="tag ${p ? "g" : "n"}">${p ? "Predicts a win" : "Doesn't separate wins"}</span>`}${e.winsOf ? vs(e) : ""}`, esc(e.note), e.detail);
}).join("");
h += card("method", `Methodology${M.name ? ": " + esc(M.name) : ""}`, M.recommended ? "Suggested, based on what the wins already show" : "Found in the CRM, docs and calls", me);

if (team) {
  let rp = list(D.reps).map(r => {
    const rr = Math.round(pct(r.won, r.closed)), lvl = r.closed < 5 ? "" : rr >= rate ? "g" : "r";
    return item(`<span class="mark dot ${lvl}"></span>`, `<div class="rate"><div><span class="title">${esc(r.name)}</span>${r.cycle ? `<span class="who num">${esc(r.cycle)} days to win</span>` : ""}${r.closed < 5 ? " " + earlyTag : ""}</div><div class="r-al num"><b>${rr}%</b> <span class="meta">${r.won} of ${r.closed}</span></div><div class="bar"><span class="${lvl || "n"}-fill" style="width:${rr}%"></span><span class="avg" style="left:${rate}%"></span></div></div>`, esc(r.note), r.detail);
  }).join("");
  if (D.topRep) rp += `<div class="callout"><b>What the top rep does differently:</b> ${esc(D.topRep)}</div>`;
  h += card("reps", "By rep", "Win rate and cycle on each rep's closed deals", rp);
}

h += card("profile", "What the sales profile says, against the deals", "Where the written process and the data disagree", list(D.profileCheck).length ? `<ul class="qs">${list(D.profileCheck).map(q => `<li>${esc(q)}</li>`).join("")}</ul>` : "");
h += card("open", "Open questions", "Unresolved, with the evidence", list(D.openQuestions).length ? `<ul class="qs">${list(D.openQuestions).map(q => `<li>${esc(q)}</li>`).join("")}</ul>` : "");

h += `<footer><details><summary>How this report works</summary><div class="about">
<p>This page is built from the team's closed deals: every won and lost deal in the period counted, a sample of wins, losses and stalled open deals read start to finish, plus call recordings and email. Deals that were never real opportunities (test records, no-shows, research or stray bookings) are left out. It only reads those tools: nothing in the CRM, inboxes or calendars was changed.</p>
<p><b>Moves that win</b> happened on far more won deals than lost ones, with both counts shown. <b>Noise</b> happens on most deals either way. <b>Real loss reasons</b> come from reading each lost deal's calls and emails, shown next to how often the CRM records them. A methodology element <b>predicts a win</b> when wins had it at least 25 points more often than losses. <b>Early signal</b> means fewer than 5 deals on a side, so treat it as a lead, not a rule. Green is above the overall win rate or a winning move; red is below it or a loss.</p>
<p>Open the arrow on any row for the evidence and the deals behind each count.</p>
<p><b>This time:</b> ${esc(D.howBuilt)}${N.excluded ? ` ${N.excluded} deals left out as not real opportunities.` : ""}</p></div></details><span>Updated ${esc(D.updated)} · Built with Sales Skills by <a href="https://skills.arrows.to" target="_blank" rel="noopener">Arrows</a></span></footer>`;
document.getElementById("app").innerHTML = h;
</script>
</body>
</html>
```
