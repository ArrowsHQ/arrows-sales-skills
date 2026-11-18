# Report template

This is the report page for the arrows-agentic-playbook-builder skill, as one HTML page in the code block below. Copy the whole page in that code block exactly, and fill in only the data, as the skill's steps describe.

```html
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Sales playbook</title>
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
.hero .sub{margin-bottom:4px}
.tag{display:inline-block;font-size:12px;font-weight:600;border-radius:2px;padding:1px 6px;white-space:nowrap;margin:2px 6px 0 0}
.lede{font-size:15px;line-height:1.55;margin:4px 0 0;max-width:760px}
.start{margin-top:16px;display:grid;grid-template-columns:30px 1fr;gap:10px;align-items:start;background:var(--card);border:1px solid var(--line);border-left:3px solid var(--ink);border-radius:4px;padding:16px 20px}
.start .num-badge{margin-top:2px}
.start b{font-weight:700}
.facts{display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:12px 24px;margin-top:8px}
.fact .k{font-size:12px;color:var(--ink-50);font-weight:600}
.fact .v{font-size:14px;margin-top:2px}
.sublabel{font-size:13px;font-weight:600;padding:14px 0 2px;border-top:1px solid var(--line);margin-top:6px}
.lbl{font-size:12px;color:var(--ink-50);font-weight:600;margin-right:4px}
.line2{font-size:13px;color:var(--ink-70);margin-top:2px}
.qs{margin:4px 0 0;padding-left:18px;font-size:13px;color:var(--ink-70)}
.qs li+li{margin-top:3px}
.para{font-size:13px;color:var(--ink-70);margin:8px 0 0;max-width:760px}
.para b{color:var(--ink);font-weight:600}
.callout{margin-top:12px;padding:12px 14px;background:var(--chip);border-radius:4px;font-size:13px}
.callout b{font-weight:600}
.glance{width:100%;border-collapse:collapse;font-size:13px}
.glance th{text-align:left;font-size:12px;color:var(--ink-50);font-weight:600;padding:6px 10px 6px 0;border-bottom:1px solid var(--line)}
.glance td{padding:8px 10px 8px 0;border-bottom:1px solid var(--line);vertical-align:top}
.glance td:first-child{font-weight:600}
.glance a{color:inherit;text-decoration:none}
.glance a:hover{text-decoration:underline;text-underline-offset:2px}
.tablewrap{overflow-x:auto}
.play .detail .blk+.blk{margin-top:8px}
.play .detail ol{margin:2px 0 0;padding-left:18px}
.play .detail .q{color:var(--ink);font-style:italic}
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
  team: true,
  updated: "[date]",
  basis: { closed: 0, months: 0, readWins: 0, readLosses: 0, readStalled: 0, calls: 0, callsFull: 0, emails: 0, docs: 0 },
  startHere: { action: "", why: "" },
  whatWeSell: { product: "", problem: "", whyBuy: "", whyUs: "" },
  fit: [],
  notFit: [],
  buyingGroup: [],
  glance: [],
  plays: [],
  stages: [],
  pricing: [],
  handoffs: [],
  rhythm: [],
  say: { pitch: "", questions: [], objections: [], competitors: [] },
  ai: [],
  human: [],
  gaps: [],
  playbookCheck: [],
  openQuestions: [],
  howBuilt: "[What was read, how it was sampled, what couldn't be measured]"
};

const esc = s => String(s ?? "").replace(/[&<>"]/g, c => ({ "&": "&amp;", "<": "&lt;", ">": "&gt;", '"': "&quot;" })[c]);
const list = a => (a || []).filter(Boolean);
const D = DATA, B = D.basis || {}, P = list(D.plays);
const go = id => `href="#${id}" onclick="const t=document.getElementById('${id}');if(t){t.scrollIntoView({behavior:'smooth'});if(t.tagName==='DETAILS')t.open=true;}return false;"`;
const cols = items => items.length ? `<div class="cols">${items.join("")}</div>` : "";
const detailBox = d => {
  const lines = Array.isArray(d) ? list(d) : d ? [d] : [];
  return lines.length ? `<div class="detail"><ul>${lines.map(l => `<li>${esc(l)}</li>`).join("")}</ul></div>` : "";
};
const item = (mark, title, sub, detail, box0, cls, id) => {
  const body = `<div class="row">${mark}<div>${title}${sub ? `<div class="sub2">${sub}</div>` : ""}</div></div>`;
  const box = box0 || detailBox(detail);
  const idAttr = id ? ` id="${id}"` : "";
  return box ? `<details class="item ${cls || ""}"${idAttr}><summary>${body}</summary>${box}</details>` : `<div class="item ${cls || ""}"${idAttr}>${body}</div>`;
};
const card = (id, title, hint, inner) => inner ? `<section class="card"${id ? ` id="${id}"` : ""}><div class="head"><span class="chip">${title}</span>${hint ? `<span class="hint">${hint}</span>` : ""}</div>${inner}</section>` : "";
const pid = (p, i) => "play-" + i;
const playBox = p => {
  const b = [];
  if (list(p.steps).length) b.push(`<div class="blk"><span class="lbl">Steps</span><ol>${list(p.steps).map(s => `<li>${esc(s)}</li>`).join("")}</ol></div>`);
  if (p.say) b.push(`<div class="blk"><span class="lbl">What we say</span><span class="q">${esc(p.say)}</span></div>`);
  if (p.handoff) b.push(`<div class="blk"><span class="lbl">Hand off when</span>${esc(p.handoff)}</div>`);
  if (p.done) b.push(`<div class="blk"><span class="lbl">Done when</span>${esc(p.done)}</div>`);
  if (p.seen) b.push(`<div class="blk"><span class="lbl">Seen in</span>${esc(p.seen)}</div>`);
  return b.length ? `<div class="detail">${b.join("")}</div>` : "";
};
const playRow = (p, i, n) => item(n ? `<span class="num-badge">${n}</span>` : `<span class="mark dot g"></span>`,
  `<span class="title">${esc(p.when)}</span><div class="qline">${p.appliesTo ? `<span class="tag n">${esc(p.appliesTo)}</span>` : ""}${p.owner ? `<span class="tag n">${esc(p.owner)}</span>` : ""}${p.speed ? `<span class="tag n">${esc(p.speed)}</span>` : ""}</div>`,
  p.goal ? `<span class="lbl">Goal</span>${esc(p.goal)}` : "", null, playBox(p), "play", pid(p, i));
const group = g => P.map((p, i) => [p, i]).filter(([p]) => p.group === g);
const owner = D.team ? esc(D.company || "Our team") : esc(D.name) + "'s";

let h = "";
h += `<section class="hero"><h1>How ${D.team ? esc(D.company || "our team") : esc(D.name)} sells</h1><p class="sub">${esc([D.team ? "Sales playbook" : "Personal sales playbook", D.updated].filter(Boolean).join(" · "))}</p>`;
h += `<div class="stats num">
  <a class="stat" ${go("plays")}><div class="n">${P.length}</div><div class="l">Plays the team runs</div></a>
  <a class="stat" ${go("moments")}><div class="n">${list(D.stages).length}</div><div class="l">Stages, each with what moves a deal on</div></a>
  <a class="stat" ${go("gaps")}><div class="n">${list(D.gaps).length}</div><div class="l">Gaps to decide</div></a>
  <div class="stat"><div class="n">${B.readWins + B.readLosses + B.readStalled}</div><div class="l">Deals read in full, out of ${B.closed} closed over ${B.months} months</div></div>
</div></section>`;

if (D.startHere && D.startHere.action) h += `<div class="start"><span class="num-badge">1</span><div><b>Start here:</b> ${esc(D.startHere.action)}${D.startHere.why ? `<div class="sub2">${esc(D.startHere.why)}</div>` : ""}</div></div>`;

const W = D.whatWeSell || {};
let ws = "";
if (W.product) ws += `<p class="lede">${esc(W.product)}</p>`;
if (W.problem) ws += `<p class="para"><b>The problem we solve:</b> ${esc(W.problem)}</p>`;
if (W.whyBuy) ws += `<p class="para"><b>Why customers buy:</b> ${esc(W.whyBuy)}</p>`;
if (W.whyUs) ws += `<p class="para"><b>Why us:</b> ${esc(W.whyUs)}</p>`;
h += card("what", "What we sell, and why", "", ws);

let who = "";
if (list(D.fit).length) who += cols(list(D.fit).map(f => item(`<span class="mark dot g"></span>`, `<span class="title">${esc(f.who)}</span>`, esc(f.note), f.detail)));
if (list(D.notFit).length) who += `<div class="sublabel">Not a fit: say no kindly, early</div>` + cols(list(D.notFit).map(f => item(`<span class="mark dot r"></span>`, `<span class="title">${esc(f.who)}</span>`, esc(f.note), f.detail)));
if (list(D.buyingGroup).length) who += `<div class="sublabel">Who's involved in a deal</div>` + cols(list(D.buyingGroup).map(b => item(`<span class="mark dot"></span>`, `<span class="title">${esc(b.role)}</span>${b.when ? `<span class="who">${esc(b.when)}</span>` : ""}`, esc(b.cares), b.detail)));
h += card("who", "Who we sell to", "Who's a fit, who isn't, and who's involved", who);

h += card("glance", "How we sell, at a glance", "", list(D.glance).length ? `<div class="facts">${list(D.glance).map(g => `<div class="fact"><div class="k">${esc(g.label)}</div><div class="v">${esc(g.value)}</div></div>`).join("")}</div>` : "");

h += card("plays", "The plays at a glance", "Open any play below for the steps", P.length ? `<div class="tablewrap"><table class="glance"><thead><tr><th>When</th><th>Who it's for</th><th>What we do</th><th>Owner</th><th>How fast</th></tr></thead><tbody>${P.map((p, i) => `<tr><td><a ${go(pid(p, i))}>${esc(p.when)}</a></td><td>${esc(p.appliesTo || "Every deal")}</td><td>${esc(p.short || p.goal)}</td><td>${esc(p.owner)}</td><td>${esc(p.speed)}</td></tr>`).join("")}</tbody></table></div>` : "");

h += card("who-books", "By who books and what the company looks like", "Different buyers, different first moves", group("who").map(([p, i]) => playRow(p, i)).join(""));

let mo = group("moment").map(([p, i], n) => playRow(p, i, n + 1)).join("");
if (list(D.stages).length) mo += `<div class="sublabel">Stages: what has to be true to move on</div><div class="tablewrap"><table class="glance"><thead><tr><th>Stage</th><th>To move on</th><th>Update in the CRM</th><th>Typical time</th></tr></thead><tbody>${list(D.stages).map(s => `<tr><td>${esc(s.stage)}</td><td>${esc(s.exit)}</td><td>${esc(s.update)}</td><td class="num">${esc(s.time)}</td></tr>`).join("")}</tbody></table></div>`;
h += card("moments", "Moment by moment", "From the first booking to signed, in order", mo);

h += card("situations", "When things happen", "Competitors, new people, quiet deals, slipping dates", group("situation").map(([p, i]) => playRow(p, i)).join(""));

h += card("pricing", "Pricing, paperwork and closing", "", list(D.pricing).map(c => item(`<span class="mark dot"></span>`, `<span class="title">${esc(c.topic)}</span>`, esc(c.text), c.detail)).join(""));

h += card("handoffs", "Handoffs", "Who passes what to whom", list(D.handoffs).map(x => item(`<span class="mark dot"></span>`, `<span class="title">${esc(x.from)} → ${esc(x.to)}</span>${x.when ? `<span class="who">${esc(x.when)}</span>` : ""}`, esc(x.what), x.detail)).join(""));

h += card("rhythm", "How we run the team", "Meetings, reviews and the numbers we watch", list(D.rhythm).map(x => item(`<span class="mark dot"></span>`, `<span class="title">${esc(x.what)}</span><span class="who">${esc([x.when, x.who].filter(Boolean).join(" · "))}</span>`, esc(x.note), x.detail)).join(""));

const S = D.say || {};
let sy = "";
if (S.pitch) sy += `<p class="lede">${esc(S.pitch)}</p>`;
if (list(S.questions).length) sy += `<div class="sublabel">Discovery questions that show up on wins</div><ol class="qs">${list(S.questions).map(q => `<li>${esc(q)}</li>`).join("")}</ol>`;
if (list(S.objections).length) sy += `<div class="sublabel">Objections, and what keeps deals alive</div>` + cols(list(S.objections).map(o => item(`<span class="mark dot"></span>`, `<span class="title">"${esc(o.objection)}"</span>`, esc(o.response), o.detail)));
if (list(S.competitors).length) sy += `<div class="sublabel">Competitors, in a line</div>` + cols(list(S.competitors).map(c => item(`<span class="mark dot"></span>`, `<span class="title">${esc(c.name)}</span>`, esc(c.line), c.detail)));
h += card("say", "What we say", "The pitch, the questions, the answers", sy);

let ai = "";
if (list(D.ai).length) ai += `<ul class="qs">${list(D.ai).map(x => `<li>${esc(x)}</li>`).join("")}</ul>`;
if (list(D.human).length) ai += `<div class="sublabel">Stays with a person</div><ul class="qs">${list(D.human).map(x => `<li>${esc(x)}</li>`).join("")}</ul>`;
h += card("ai", "Working with AI", "Every play here is written so an AI assistant can follow it too", ai);

h += card("gaps", "Gaps to decide", "Moments where the team has no consistent way yet", list(D.gaps).map(g => item(`<span class="mark dot y"></span>`, `<span class="title">${esc(g.moment)}</span>`, esc(g.note), g.detail)).join(""));

const vTag = { Keep: "g", Change: "y", Drop: "r", Add: "n" };
h += card("check", "The old playbook against real deals", "Each rule, how often it happened, and what to do with it", list(D.playbookCheck).map(r => item(`<span class="mark dot ${vTag[r.verdict] === "n" ? "" : vTag[r.verdict] || ""}"></span>`,
  `<span class="title">${esc(r.rule)}</span><span class="who num">${r.of ? `${r.followed} of ${r.of} deals` : ""}</span><div class="qline"><span class="tag ${vTag[r.verdict] || "n"}">${esc(r.verdict)}</span></div>`, esc(r.note), r.detail)).join(""));

h += card("open", "Open questions", "", list(D.openQuestions).length ? `<ul class="qs">${list(D.openQuestions).map(q => `<li>${esc(q)}</li>`).join("")}</ul>` : "");

h += `<footer><details><summary>How this playbook works</summary><div class="about">
<p>This playbook describes how the team runs its sales process, written from the team's own deals: every closed deal counted, a sample of wins, losses and stalled deals read start to finish, plus call recordings, email and documents. It only reads those tools: nothing in the CRM, inboxes or documents was changed.</p>
<p>Each <b>play</b> says when it applies, who it's for, the goal, the steps with an owner and timing, what to say, when to hand off, and how to know it's done. <b>Seen in</b> shows how often the team's winning deals followed it. <b>Gaps to decide</b> are moments where the team doesn't yet have one way of doing things; they're questions for the team, not rules. Every play is written plainly enough for a new hire, a consultant or an AI assistant to follow.</p>
<p>Open the arrow on any play for the steps. A written copy of this playbook sits alongside this page and can be loaded into any AI tool.</p>
<p><b>This time:</b> ${esc(D.howBuilt)}</p></div></details><span>Updated ${esc(D.updated)} · Built with Sales Skills by <a href="https://skills.arrows.to" target="_blank" rel="noopener">Arrows</a></span></footer>`;
document.getElementById("app").innerHTML = h;
</script>
</body>
</html>
```
