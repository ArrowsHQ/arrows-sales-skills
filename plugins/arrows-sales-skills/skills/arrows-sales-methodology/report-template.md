# Report template

This is the report page for the arrows-sales-methodology skill, as one HTML page in the code block below. Copy the whole page in that code block exactly, and fill in only the data, as the skill's steps describe.

```html
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Methodology check</title>
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
.rate .bar{grid-column:1/3;display:flex;height:8px;border-radius:2px;overflow:hidden;background:var(--track)}
.sublabel{font-size:13px;font-weight:600;padding:14px 0 2px;border-top:1px solid var(--line);margin-top:6px}
.head + .sublabel{border-top:0;margin-top:0;padding-top:4px}
.callout{margin-top:12px;padding:12px 14px;background:var(--chip);border-radius:4px;font-size:13px}
.callout b{font-weight:600}
.qs{margin:4px 0 0;padding-left:18px;font-size:13px;color:var(--ink-70)}
.qs li+li{margin-top:3px}
.n-fill{background:var(--ink-30)}
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
  methodology: "[Methodology]",
  recommended: false,
  period: "Open deals now · closed [month year] – [month year]",
  updated: "[date]",
  numbers: { open: 0, openValue: 0, behind: 0, behindValue: 0, won: 0, lost: 0, wonFull: 0, lostFull: 0 },
  basis: { closedRead: 0, calls: 0, callsFull: 0, emails: 0 },
  fixes: [],
  elements: [],
  closedDeals: [],
  gates: [],
  dropped: [],
  behind: [],
  reps: [],
  openQuestions: [],
  howBuilt: "[What was read, how it was sampled, what couldn't be measured]"
};

const esc = s => String(s ?? "").replace(/[&<>"]/g, c => ({ "&": "&amp;", "<": "&lt;", ">": "&gt;", '"': "&quot;" })[c]);
const money = n => !n ? "" : n >= 1e6 ? "$" + (n / 1e6).toFixed(1).replace(/\.0$/, "") + "M" : n >= 1e3 ? "$" + Math.round(n / 1e3) + "k" : "$" + n;
const pct = (a, b) => b > 0 ? Math.max(0, Math.min(100, a / b * 100)) : 0;
const list = a => (a || []).filter(Boolean);
const D = DATA, N = D.numbers || {}, B = D.basis || {}, team = list(D.reps).length > 0;
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
const lvl = (a, b) => { const p = pct(a, b); return !b ? "" : p >= 75 ? "g" : p >= 50 ? "y" : "r"; };
const rateRow = (title, a, b, sub, detail, meta) => item(`<span class="mark dot ${lvl(a, b)}"></span>`, `<div class="rate"><div><span class="title">${title}</span>${meta ? `<span class="who">${meta}</span>` : ""}</div><div class="r-al num"><b>${Math.round(pct(a, b))}%</b> <span class="meta">${a} of ${b}</span></div><div class="bar"><span class="${lvl(a, b) || "n"}-fill" style="width:${pct(a, b)}%"></span></div></div>`, sub, detail);
const early = x => (x.winsOf && x.winsOf < 5) || (x.lossesOf && x.lossesOf < 5);
const gap = x => pct(x.wins, x.winsOf) - pct(x.losses, x.lossesOf);
const vs = x => `<div class="vs num"><span>Wins</span><div class="bar"><span class="g-fill" style="width:${pct(x.wins, x.winsOf)}%"></span></div><span class="v">${x.wins} of ${x.winsOf}</span><span>Losses</span><div class="bar"><span class="r-fill" style="width:${pct(x.losses, x.lossesOf)}%"></span></div><span class="v">${x.losses} of ${x.lossesOf}</span></div>`;
const tags = (a, cls) => list(a).map(x => `<span class="tag ${cls}">${esc(x)}</span>`).join("");
const meta = d => [money(d.amount), d.stage, team ? d.owner : ""].filter(Boolean).map(esc).join(" · ");

const M = esc(D.methodology || "the methodology");
const fullClosed = (N.wonFull || 0) + (N.lostFull || 0);
const missWon = (N.won || 0) - (N.wonFull || 0), missClosed = (N.won || 0) + (N.lost || 0) - fullClosed;
const rateFull = Math.round(pct(N.wonFull, fullClosed)), rateMiss = Math.round(pct(missWon, missClosed));

let h = "";
h += `<section class="hero"><h1>${team ? esc(D.company || "Sales team") + " methodology check" : esc(D.name) + "'s methodology check"}</h1><p class="sub">${esc([D.methodology + (D.recommended ? " (suggested)" : ""), D.period, team ? `Team view · ${list(D.reps).length} reps` : "Own deals"].filter(Boolean).join(" · "))}</p>`;
h += `<div class="health"><span class="g-fill" style="width:${pct((N.open || 0) - (N.behind || 0), N.open)}%"></span><span class="r-fill" style="width:${pct(N.behind, N.open)}%"></span></div>`;
h += `<div class="stats num">
  <a class="stat" ${go("closed")}><div class="n">${N.wonFull || 0} of ${N.won || 0}</div><div class="l"><span class="key g-fill"></span>Wins that followed ${M}</div></a>
  <a class="stat" ${go("closed")}><div class="n">${(N.lost || 0) - (N.lostFull || 0)} of ${N.lost || 0}</div><div class="l"><span class="key r-fill"></span>Losses that didn't follow ${M}</div></a>
  <a class="stat" ${go("closed")}><div class="n">${fullClosed && missClosed ? rateFull + "% vs " + rateMiss + "%" : "–"}</div><div class="l">Win rate when a deal followed ${M} vs. when it didn't</div></a>
  <a class="stat" ${go("behind")}><div class="n">${N.behind || 0} of ${N.open || 0}</div><div class="l">Open deals not following ${M} yet${N.behindValue ? " · " + money(N.behindValue) : ""}</div></a>
</div></section>`;

h += card("fixes", "Three things to fix first", "The changes most likely to raise the win rate · open one for the steps",
  list(D.fixes).map((c, i) => item(`<span class="num-badge">${i + 1}</span>`, `<span class="title">${esc(c.fix)}</span>${c.owner ? `<span class="who">${esc(c.owner)}</span>` : ""}`, esc(c.why), null, stepsBox(c.steps, c.context))).join(""));

let cl = "";
if (list(D.elements).some(e => e.winsOf || e.lossesOf)) cl += `<div class="sublabel">Which parts of ${M} show up on wins</div>` + list(D.elements).filter(e => e.winsOf || e.lossesOf).map(e => {
  const p = !early(e) && gap(e) >= 25;
  return item(`<span class="mark dot ${p ? "g" : ""}"></span>`, `<span class="title">${esc(e.element)}</span>${e.byStage ? `<span class="who">by ${esc(e.byStage)}</span>` : ""} <span class="tag ${early(e) ? "n" : p ? "g" : "n"}">${early(e) ? "Early signal" : p ? "Wins have it far more" : "Same on wins and losses"}</span>${vs(e)}`, esc(e.note), e.detail);
}).join("");
const dealRow = d => item(`<span class="mark dot ${d.outcome === "won" ? "g" : "r"}"></span>`, `<span class="title">${esc(d.company)}</span><span class="who">${esc([d.outcome === "won" ? "Won" : "Lost", money(d.amount), team ? d.owner : ""].filter(Boolean).join(" · "))}</span><div class="qline">${list(d.missing).length ? tags(d.missing.map(m => "Missed: " + m), "r") : `<span class="tag g">Followed ${M}</span>`}</div>`, esc(d.note), d.detail);
const wonD = list(D.closedDeals).filter(d => d.outcome === "won"), lostD = list(D.closedDeals).filter(d => d.outcome !== "won");
if (wonD.length) cl += `<div class="sublabel">Won deals read in full</div>` + cols(wonD.map(dealRow));
if (lostD.length) cl += `<div class="sublabel">Lost deals read in full</div>` + cols(lostD.map(dealRow));
h += card("closed", `Won and lost deals: did they follow ${M}?`, `Followed ${M} means every part its stage needed was known, with proof · ${N.won || 0} wins and ${N.lost || 0} losses counted, ${B.closedRead || 0} read in full`, cl);

h += card("upheld", `Is each part of ${M} getting done?`, "Of the open deals that have reached the stage that needs it, how many have it, with proof",
  list(D.elements).filter(e => e.of).map(e => rateRow(esc(e.element), e.known, e.of, esc(e.note), null, e.byStage ? "needed by " + esc(e.byStage) : "")).join(""));

let ft = "";
if (list(D.gates).length) ft += `<div class="sublabel">Moved to the next stage without what it needs</div>` + list(D.gates).map(g => item(`<span class="mark dot r"></span>`, `<div class="rate"><div><span class="title">${esc(g.stage)}</span>${g.value ? `<span class="who">${money(g.value)}</span>` : ""}</div><div class="r-al num"><b>${g.skipped}</b> <span class="meta">of ${g.of} moved ahead without it</span></div><div class="bar"><span class="r-fill" style="width:${pct(g.skipped, g.of)}%"></span></div></div>`, g.missing ? "Usually missing: " + esc(g.missing) : "", g.detail)).join("");
if (list(D.dropped).length) ft += `<div class="sublabel">Found, then acted on</div>` + list(D.dropped).map(x => rateRow(esc(x.what), x.done, x.of, esc(x.note), x.detail)).join("");
h += card("follow", "Is the team following through?", "Whether reps act on what they learn, or move deals ahead without it", ft);

const behind = list(D.behind), shown = team ? behind.slice(0, 8) : behind;
const behindRow = d => item(`<span class="mark dot r"></span>`, `<span class="title">${esc(d.company)}</span><span class="who">${meta(d)}</span><div class="qline">${tags(list(d.missing).map(m => "Missing: " + m), "r")}</div>`, d.ask ? `Ask: "${esc(d.ask)}"` : "", d.detail);
let bh = cols(shown.map(behindRow));
if (behind.length > shown.length) bh += `<div class="more">${behind.length - shown.length} more, grouped by rep below.</div>`;
h += card("behind", `Open deals not following ${M} yet`, "Missing a part their stage needs, most value first, with the question to ask", bh);

if (team) h += card("reps", "By rep", `How much of ${M} each rep's open deals have, with proof · open a rep for their deals`,
  list(D.reps).map(r => {
    const mine = behind.filter(d => d.owner === r.name);
    const box = mine.length ? `<div class="detail"><ul>${mine.map(d => `<li><b>${esc(d.company)}</b> ${esc([money(d.amount), d.stage].filter(Boolean).join(" · "))}: missing ${esc(list(d.missing).join(", "))}</li>`).join("")}</ul></div>` : "";
    return item(`<span class="mark dot ${lvl(r.known, r.of)}"></span>`, `<div class="rate"><div><span class="title">${esc(r.name)}</span><span class="who num">${r.skipped || 0} deals moved ahead without it · ${r.wonFull || 0} of ${r.won || 0} wins followed ${M}</span></div><div class="r-al num"><b>${Math.round(pct(r.known, r.of))}%</b> <span class="meta">${r.known} of ${r.of}</span></div><div class="bar"><span class="${lvl(r.known, r.of) || "n"}-fill" style="width:${pct(r.known, r.of)}%"></span></div></div>`, esc([r.missesMost ? "Misses most: " + r.missesMost : "", r.note].filter(Boolean).join(" · ")), null, box);
  }).join(""));

h += card("open", "Open questions", "Unresolved, with the evidence", list(D.openQuestions).length ? `<ul class="qs">${list(D.openQuestions).map(q => `<li>${esc(q)}</li>`).join("")}</ul>` : "");

h += `<footer><details><summary>How this report works</summary><div class="about">
<p>This page checks the team's deals against the saved methodology file (arrows-methodology.md): the parts of ${M}, what each stage needs and what counts as proof. It reads the CRM, call recordings and email, and only reads them: nothing in the CRM, inboxes or calendars was changed.</p>
<p>A deal <b>followed ${M}</b> when every part of ${M} its stage needed was known, with proof: a CRM field backed by a call or email, the buyer's own answer on a call, or an email that shows it (a CFO on the thread, say). A field that just says "yes" doesn't count. Missing any one part means the deal <b>didn't follow ${M}</b>. <b>Getting done</b> is the share of open deals that have a part once their stage needs it: green at 75% or more, gold from 50%, red below. <b>Moved ahead without it</b> means a deal reached the next stage without what the stage before it needs. <b>Wins have it far more</b> means wins had that part at least 25 points more often than losses; <b>early signal</b> means fewer than 5 deals on a side.</p>
<p>Open the arrow on any row for the evidence and the deals behind each count.</p>
<p><b>This time:</b> ${esc(D.howBuilt)}</p></div></details><span>Updated ${esc(D.updated)} · Built with Sales Skills by <a href="https://skills.arrows.to" target="_blank" rel="noopener">Arrows</a></span></footer>`;
document.getElementById("app").innerHTML = h;
</script>
</body>
</html>
```
