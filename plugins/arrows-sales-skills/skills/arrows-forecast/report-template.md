# Report template

This is the report page for the arrows-forecast skill, as one HTML page in the code block below. Copy the whole page in that code block exactly, and fill in only the data, as the skill's steps describe.

```html
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Objective forecast</title>
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
:root{--blue:#2F6FD1; --blue-soft:#E7EFFB;}
.hero .sub{color:rgba(255,255,255,.75);font-size:15px;margin:0 0 6px}
.hero .explain{color:rgba(255,255,255,.85);font-size:13px;margin:0 0 14px;max-width:760px}
.b-fill{background:var(--blue)}
.hero .legend{color:rgba(255,255,255,.75)}
.head{display:flex;justify-content:space-between;align-items:baseline;gap:12px;margin-bottom:6px;padding-bottom:10px;border-bottom:1px solid var(--line)}
.hint{font-size:12px;color:var(--ink-50);text-align:right}
.mark{font-weight:700;color:var(--ink-30);font-size:14px}
.mark.dot.b::before{background:var(--blue)}
.tag{display:inline-block;font-size:12px;font-weight:600;border-radius:2px;padding:1px 6px;white-space:nowrap;margin-left:6px}
.tag.g{background:var(--green-soft);color:#127A3E}
.tag.b{background:var(--blue-soft);color:var(--blue)}
.cmp{display:flex;gap:14px;flex-wrap:wrap;margin:3px 0 2px;font-size:13px}
.cmp .k{color:var(--ink-50);font-size:12px}
.cmp .v{font-weight:600}
.cmp .arrow{color:var(--ink-30);margin:0 4px}
.cmp .up{color:#127A3E}
.cmp .down{color:var(--red)}
.need::before{content:"Still needed: ";color:var(--ink-50)}
.need{color:var(--ink-70);font-size:12px}
.move{display:block;margin-top:6px;padding:1px 0 1px 10px;border-left:2px solid var(--gold);color:var(--ink);font-size:13px;font-weight:600;line-height:1.4}
.move::before{content:"To move it · ";font-weight:600;color:var(--ink-50)}
.dl{list-style:none;padding-left:0!important;margin:0}
.dl li{display:grid;grid-template-columns:16px 1fr;gap:4px;color:var(--ink)}
.legend{display:flex;gap:16px;font-size:12px;color:var(--ink-50);margin-top:10px;flex-wrap:wrap}
.legend i{display:inline-block;width:10px;height:10px;border-radius:2px;margin-right:5px;vertical-align:-1px}
.about table{border-collapse:collapse;margin:6px 0 8px;font-size:12px}
.about td{padding:3px 10px 3px 0;vertical-align:top;border-top:1px solid var(--line)}
.about td:first-child{font-weight:600;color:var(--ink);white-space:nowrap}
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
  .rep-row{grid-template-columns:1fr;gap:4px}
  .head{flex-direction:column;align-items:flex-start;gap:2px}
  .hint{text-align:left}
}
</style>
</head>
<body>
<div class="wrap" id="app"></div>
<script>
/* Fill in DATA only. Leave everything else as is. */
const DATA = {
  period: "Q4 2026",
  periodEnd: "Dec 31",
  view: "[My deals | Team view · N owners]",
  pipeline: "[pipeline name]",
  updated: "[date, time]",
  crmLabel: "stage probability",
  name: "[First name]",
  company: "[Company name]",
  numbers: { dealCount: 0, noAmountCount: 0, pipelineValue: 0, crmValue: 0, objectiveValue: 0, goal: null, commitValue: 0, likelyValue: 0, possibleValue: 0, unlikelyValue: 0, slipValue: 0, slipCount: 0 },
  deals: [],
  ahead: [],
  further: [],
  slip: [],
  reps: [],
  howBuilt: "[What was read, where the CRM number came from, any sampling, anything missing, how many deals had no amount]"
};

const esc = s => String(s ?? "").replace(/[&<>"]/g, c => ({ "&": "&amp;", "<": "&lt;", ">": "&gt;", '"': "&quot;" })[c]);
const money = n => n == null || n === "" ? "" : n >= 1e6 ? "$" + (n / 1e6).toFixed(1).replace(/\.0$/, "") + "M" : n >= 1e3 ? "$" + Math.round(n / 1e3) + "k" : "$" + n;
const amt = d => d.amount == null || d.amount === 0 ? "no amount" : money(d.amount);
const pct = (a, b) => b > 0 ? Math.max(0, Math.min(100, a / b * 100)) : 0;
const list = a => (a || []).filter(Boolean);
const P = v => v == null ? "—" : Math.round(v) + "%";
const lvl = d => d.label === "slip" ? "r" : (d.objPct ?? 0) >= 75 ? "g" : (d.objPct ?? 0) >= 60 ? "b" : (d.objPct ?? 0) >= 25 ? "y" : "r";
const labelText = d => d.label === "slip" ? "Likely to slip" : (d.objPct ?? 0) >= 75 ? "Commit" : (d.objPct ?? 0) >= 60 ? "Likely" : (d.objPct ?? 0) >= 25 ? "Possible" : (d.objPct ?? 0) > 0 ? "Unlikely" : "Not this period";
const evidenceBox = d => {
  const lines = Array.isArray(d) ? list(d) : d ? [d] : [];
  return lines.length ? `<div class="detail"><ul>${lines.map(l => `<li>${esc(l)}</li>`).join("")}</ul></div>` : "";
};
const D = DATA, N = D.numbers, team = list(D.reps).length > 0;
const hasCrm = N.crmValue != null && N.crmValue !== 0;
const hasGoal = N.goal != null && N.goal > 0;
const cov = hasGoal ? (N.pipelineValue / N.goal) : 0;
const crmName = D.crmLabel || "stage probability";
const cmp = d => {
  const diff = d.crmPct != null && d.objPct != null ? d.objPct - d.crmPct : null;
  const cls = diff == null ? "" : diff < 0 ? "down" : diff > 0 ? "up" : "";
  const dateCls = d.objDate && d.crmDate && d.objDate !== d.crmDate ? "down" : "";
  return `<div class="cmp num"><span><span class="k">CRM </span><span class="v">${P(d.crmPct)}</span><span class="arrow">→</span><span class="k">evidence </span><span class="v ${cls}">${P(d.objPct)}</span></span><span><span class="k">CRM date </span><span class="v">${esc(d.crmDate || "—")}</span><span class="arrow">→</span><span class="k">evidence </span><span class="v ${dateCls}">${esc(d.objDate || "—")}</span></span>${d.buyerDate ? `<span><span class="k">Buyer's own date </span><span class="v">${esc(d.buyerDate)}</span></span>` : `<span class="k">No date from the buyer</span>`}</div>`;
};
const item = (mark, title, sub, box) => {
  const body = `<div class="row">${mark}<div>${title}${sub ? `<div class="sub2">${sub}</div>` : ""}</div></div>`;
  return box ? `<details class="item"><summary>${body}</summary>${box}</details>` : `<div class="item">${body}</div>`;
};
const dealItem = (d, markHtml) => item(markHtml || `<span class="mark dot ${lvl(d)}"></span>`,
  `<span class="title">${esc(d.deal)}</span><span class="who num">${esc([amt(d), d.owner, d.stage].filter(Boolean).join(" · "))}</span><span class="tag ${lvl(d)}">${labelText(d)}</span>${cmp(d)}`,
  `${d.blocker ? `<div class="need">${esc(d.blocker)}</div>` : esc(d.why)}${d.move ? `<div class="move">${esc(d.move)}</div>` : ""}`, evidenceBox(d.why ? [d.why, ...list(d.evidence)] : d.evidence));
const go = id => `href="#${id}" onclick="const t=document.getElementById('${id}');if(t){t.scrollIntoView({behavior:'smooth'});}return false;"`;
const cols = items => items.length ? `<div class="cols">${items.join("")}</div>` : "";

let h = "";
h += `<section class="hero"><h1>${team ? esc(D.company || "Sales team") : esc(D.name) + "'s"} objective forecast</h1><p class="sub">${esc([D.period, D.view, D.pipeline].filter(Boolean).join(" · "))}</p>`;
h += `<p class="explain">Every deal the CRM has dated ${esc(D.period)}, scored only on what the buyer said and did. <b>CRM says</b> is each deal's amount × its ${esc(crmName)}. <b>Evidence says</b> is the same amount × a likelihood earned by buyer actions: a date they gave, a budget holder on a call, paper in motion.</p>`;
h += `<div class="health"><span class="g-fill" style="width:${pct(N.commitValue, N.objectiveValue)}%"></span><span class="b-fill" style="width:${pct(N.likelyValue, N.objectiveValue)}%"></span><span class="y-fill" style="width:${pct(N.possibleValue, N.objectiveValue)}%"></span><span class="r-fill" style="width:${pct(N.unlikelyValue, N.objectiveValue)}%"></span></div>`;
h += `<div class="legend"><span><i class="g-fill"></i>Commit ${money(N.commitValue)}</span><span><i class="b-fill"></i>Likely ${money(N.likelyValue)}</span><span><i class="y-fill"></i>Possible ${money(N.possibleValue)}</span><span><i class="r-fill"></i>Unlikely ${money(N.unlikelyValue)}</span></div>`;
h += `<div class="stats num">
  <a class="stat" ${go("deals")}><div class="n">${N.dealCount}</div><div class="l">Deals the CRM has dated ${esc(D.period)} · ${money(N.pipelineValue)}${N.noAmountCount ? ` · ${N.noAmountCount} with no amount` : ""}</div></a>
  <div class="stat"><div class="n">${hasCrm ? money(N.crmValue) : "—"}</div><div class="l">CRM says · amount × ${esc(crmName)}</div></div>
  <a class="stat" ${go("ahead")}><div class="n">${money(N.objectiveValue)}</div><div class="l">Evidence says${hasCrm ? ` · ${N.objectiveValue < N.crmValue ? "−" : "+"}${money(Math.abs(N.crmValue - N.objectiveValue))} vs. the CRM` : ""}</div></a>
  ${hasGoal ? `<div class="stat"><div class="n">${money(N.goal)}</div><div class="l">Goal · ${cov.toFixed(1)}x pipeline coverage · ${Math.round(pct(N.objectiveValue, N.goal))}% likely</div></div>` : `<a class="stat" ${go("slip")}><div class="n">${money(N.slipValue)}</div><div class="l">Likely to slip past ${esc(D.periodEnd)} · ${N.slipCount} deals</div></a>`}
</div></section>`;

const ALL = list(D.deals), AH = list(D.ahead), FU = list(D.further), S = list(D.slip);

h += `<section class="card" id="deals"><div class="head"><span class="chip">What will really close, and when</span><span class="hint">Most likely first · the buyer's own date when there is one · what the buyer still hasn't done and the move that would get it done · open a deal for the evidence</span></div>`;
h += ALL.length ? ALL.map(d => dealItem(d)).join("") : `<div class="empty">No open deals with a close date in ${esc(D.period)}.</div>`;
h += `</section>`;

h += `<section class="card" id="ahead"><div class="head"><span class="chip">CRM ahead of the evidence</span><span class="hint">Stage or close date is further along than what the buyer has done, by money at stake</span></div>`;
h += AH.length ? cols(AH.map((d, i) => dealItem(d, `<span class="num-badge">${i + 1}</span>`))) : `<div class="empty">${hasCrm ? "The CRM and the evidence agree on every deal." : "No CRM numbers to compare against."}</div>`;
h += `</section>`;

h += `<section class="card" id="further"><div class="head"><span class="chip">Further along than the CRM shows</span><span class="hint">The buyer has done more than the stage suggests</span></div>`;
h += FU.length ? cols(FU.map(d => dealItem(d))) : `<div class="empty">No deals ahead of their stage.</div>`;
h += `</section>`;

h += `<section class="card" id="slip"><div class="head"><span class="chip">Likely to slip past ${esc(D.periodEnd)}</span><span class="hint">Evidence date lands after the period${S.length ? ` · ${S.length} deals · ${money(N.slipValue)}` : ""}</span></div>`;
h += S.length ? cols(S.map(d => dealItem({ ...d, label: "slip" }))) : `<div class="empty">No deals likely to slip past ${esc(D.periodEnd)}.</div>`;
h += `</section>`;

if (team) {
  const repBox = r => {
    const mine = ALL.filter(d => d.owner === r.name);
    const lines = mine.map(d => `<li><span class="mark dot ${lvl(d)}"></span><span><b>${esc(d.deal)}</b> <span class="meta num">${esc([amt(d), d.stage].filter(Boolean).join(" · "))} · CRM ${P(d.crmPct)} → evidence ${P(d.objPct)}</span><br>${esc(d.blocker || d.why)}${d.move ? ` · <i>${esc(d.move)}</i>` : ""}</span></li>`);
    const extra = evidenceBox(r.detail);
    return lines.length || extra ? `<div class="detail">${lines.length ? `<ul class="dl">${lines.join("")}</ul>` : ""}${extra ? extra.replace('<div class="detail">', '<div class="ctx">') : ""}</div>` : "";
  };
  h += `<section class="card" id="by-rep"><div class="head"><span class="chip">By rep</span><span class="hint">Each rep's deals, CRM vs. evidence, and the question for their 1:1 · open a rep for their deals</span></div>`;
  h += list(D.reps).map(r => item(`<span class="mark dot ${r.objValue < r.crmValue ? "y" : "g"}"></span>`,
      `<div class="rep-row"><div><span class="title">${esc(r.name)}</span><div class="meta num">${r.dealCount} deals · CRM ${money(r.crmValue)} · evidence ${money(r.objValue)}</div></div><div><span class="sub2">${esc(r.ask)}</span></div></div>`,
      "", repBox(r))).join("");
  h += `</section>`;
}

h += `<footer><details><summary>How the forecast works</summary><div class="about">
<p>This page is rebuilt from the CRM, calls, email and calendar each time it runs, in the same layout and order. It only reads those tools: nothing in the CRM was changed. The evidence number for each deal comes only from what the buyer said and did; the stage, the CRM close date and the seller's notes don't move it. A gap is about the CRM record, not about the person working the deal.</p>
<p><b>CRM says</b> is each deal's amount × its ${esc(crmName)} in the CRM, including deals likely to slip. <b>Evidence says</b> is amount × the tier below, with slipping deals counted at zero for this period.</p>
<p><b>Tiers.</b> Each deal gets the highest tier whose evidence it has:</p>
<table>
<tr><td>90% Commit</td><td>Paper with the buyer and the buyer named a signature date, or a verbal yes from the budget holder with paper in motion</td></tr>
<tr><td>75% Commit</td><td>Budget holder agreed pricing or terms; legal, security or procurement started</td></tr>
<tr><td>60% Likely</td><td>Budget holder met, buyer gave a decision date or process, next step booked</td></tr>
<tr><td>40% Possible</td><td>Champion replying, next step booked, two or more buyer contacts or the budget holder engaged, but no date from the buyer</td></tr>
<tr><td>25% Possible</td><td>Two-way contact in the last 14 days, but nothing booked, or single-threaded, or the timeline exists only in the CRM</td></tr>
<tr><td>10% Unlikely</td><td>No buyer reply in 14+ days, or no next step and no reply in the last 7</td></tr>
<tr><td>0%</td><td>Buyer said no budget or chose someone else; or quiet 30+ days</td></tr>
</table>
<p><b>Caps.</b> No budget holder from buyer-side evidence: at most 40%. Quiet 14+ days: at most 25%. Close date moved twice: at most 40%. Competitor named with no stated preference: at most 60%. New deal with no call yet: at most 25%. Every cap that applied is listed in the deal's evidence.</p>
<p><b>Dates.</b> The evidence close date is the later of the date the buyer gave and the date the remaining steps could finish at this team's usual pace. A deal whose evidence date lands after the period counts as likely to slip and adds nothing to this period's number, while the CRM number still counts it.</p>
<p><b>Still needed</b> on each row is the one thing the buyer hasn't done that would move the deal up a tier. <b>To move it</b> is the one thing on the seller's side that would get the buyer to do it, or a plain "close it out" when nothing would.</p>
<p><b>This run:</b> ${esc(D.howBuilt)}</p></div></details><span>Updated ${esc(D.updated)} · Built with Sales Skills by <a href="https://skills.arrows.to" target="_blank" rel="noopener">Arrows</a></span></footer>`;
document.getElementById("app").innerHTML = h;
</script>
</body>
</html>
```
