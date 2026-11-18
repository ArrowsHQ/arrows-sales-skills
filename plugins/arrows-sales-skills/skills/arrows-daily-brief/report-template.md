# Report template

This is the report page for the arrows-daily-brief skill, as one HTML page in the code block below. Copy the whole page in that code block exactly, and fill in only the data, as the skill's steps describe.

```html
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Daily brief</title>
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
.grid2{display:grid;grid-template-columns:1fr 1fr;gap:16px;margin-top:16px;align-items:start}
.grid2 .card,.grid3 .card{margin-top:0}
.grid3{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-top:16px;align-items:start}
.card.won{border-top:3px solid var(--green)}
.card.lost{border-top:3px solid var(--red)}
.card.won .head,.card.lost .head{border-bottom:0}
.mark{font-weight:700;color:var(--ink-30);font-size:14px}
.tag{display:inline-block;font-size:12px;font-weight:600;border-radius:2px;padding:1px 6px;white-space:nowrap;margin-left:6px}
.qline .tag{margin-left:0}
.stage{display:grid;grid-template-columns:170px 1fr 100px;gap:14px;align-items:center;padding:9px 0;border-top:1px solid var(--line)}
.head + .stage{border-top:0}
.stage .bar{display:flex;height:12px;border-radius:2px;overflow:hidden}
.stage .gap{grid-column:2/4;font-size:12px;color:var(--ink-50);margin-top:-6px}
.legend{display:flex;gap:16px;font-size:12px;color:var(--ink-50);margin-top:10px}
.legend i{display:inline-block;width:10px;height:10px;border-radius:2px;margin-right:5px;vertical-align:-1px}
footer details p{max-width:640px;margin:6px 0 0}
@media (max-width:720px){
  .hero{padding:22px 18px 18px}
  .hero h1{font-size:25px}
  .stats{grid-template-columns:repeat(2,1fr)}
  .stat:nth-child(3){padding-left:0;border-left:0}
  .stat:nth-child(n+3){margin-top:10px}
  .grid2,.grid3,.cols{grid-template-columns:1fr}
  .cols > .item:nth-child(2){border-top:1px solid var(--line)}
  .cols > .item:nth-child(odd){padding-right:0;border-right:0}
  .cols > .item:nth-child(even){padding-left:0}
  .card{padding:16px}
  .detail{margin:0 0 12px 28px}
  .rep-row{grid-template-columns:1fr;gap:4px}
  .stage{grid-template-columns:1fr 90px}
  .stage .bar{grid-column:1/3}
  .stage .gap{grid-column:1/3;margin-top:0}
}
.row.t{grid-template-columns:52px 1fr 14px}
.time{font-weight:700;font-size:13px;color:var(--ink);margin-top:1px}
</style>
</head>
<body>
<div class="wrap" id="app"></div>
<script>
/* Fill in DATA only. Leave everything else as is. */
const DATA = {
  name: "[First name]",
  company: "[Company, for the team view]",
  date: "[Weekday, Month Day]",
  view: "[My day | My day + team · N reps]",
  updated: "[date, time]",
  numbers: { calls: 0, replies: 0, atRisk: 0, changes: 0 },
  doFirst: [],
  sinceYesterday: [],
  atRisk: [],
  closeOut: [],
  calls: [],
  otherMeetings: "",
  replies: [],
  team: [],
  openTime: [],
  howBuilt: "[What was read, any sampling, anything missing]"
};

const esc = s => String(s ?? "").replace(/[&<>"]/g, c => ({ "&": "&amp;", "<": "&lt;", ">": "&gt;", '"': "&quot;" })[c]);
const money = n => n == null || n === "" ? "" : n >= 1e6 ? "$" + (n / 1e6).toFixed(1).replace(/\.0$/, "") + "M" : n >= 1e3 ? "$" + Math.round(n / 1e3) + "k" : "$" + n;
const list = a => (a || []).filter(Boolean);
const detailBox = d => {
  const lines = Array.isArray(d) ? list(d) : d ? [d] : [];
  return lines.length ? `<div class="detail"><ul>${lines.map(l => `<li>${esc(l)}</li>`).join("")}</ul></div>` : "";
};
const stepsBox = (steps, context) => {
  const st = list(steps);
  if (!st.length && !context) return "";
  return `<div class="detail">${st.length ? `<ol>${st.map(x => `<li>${esc(x)}</li>`).join("")}</ol>` : ""}${context ? `<div class="ctx">${esc(context)}</div>` : ""}</div>`;
};
const item = (mark, title, sub, detail, box0, cls) => {
  const body = `<div class="row${cls ? " " + cls : ""}">${mark}<div>${title}${sub ? `<div class="sub2">${sub}</div>` : ""}</div></div>`;
  const box = box0 || detailBox(detail);
  return box ? `<details class="item"><summary>${body}</summary>${box}</details>` : `<div class="item">${body}</div>`;
};
const quiet = d => d.quietDays == null ? `<span class="tag r">no touch logged</span>` : `<span class="tag ${d.quietDays >= 14 ? "r" : "n"}">${d.quietDays === 0 ? "today" : d.quietDays + "d quiet"}${d.channel ? " · " + esc(d.channel) : ""}</span>`;
const kindMark = k => k === "good" ? `<span class="tick">✓</span>` : `<span class="mark dot ${k === "bad" ? "r" : ""}"></span>`;
const D = DATA, N = D.numbers, team = list(D.team).length > 0;

const go = id => `href="#${id}" onclick="const t=document.getElementById('${id}');if(t){t.scrollIntoView({behavior:'smooth'});}return false;"`;
const cols = items => items.length ? `<div class="cols">${items.join("")}</div>` : "";
const AR = list(D.atRisk), cap = team ? 6 : 5;

let h = "";
h += `<section class="hero"><h1>${team ? esc(D.company || "Sales team") + " daily brief" : esc(D.name) + "'s daily brief"}</h1><p class="sub">${esc([D.date, D.view].filter(Boolean).join(" · "))}</p>`;
h += `<div class="stats num">
  <a class="stat" ${go("calls")}><div class="n">${N.calls}</div><div class="l">Sales calls today</div></a>
  <a class="stat" ${go("replies")}><div class="n">${N.replies}</div><div class="l">Replies waiting</div></a>
  <a class="stat" ${go("at-risk")}><div class="n">${N.atRisk}</div><div class="l"><span class="key r-fill"></span>Deals at risk</div></a>
  <a class="stat" ${go("since")}><div class="n">${N.changes}</div><div class="l">New since yesterday</div></a>
</div></section>`;

h += `<section class="card" id="do-first"><div class="head"><span class="chip">Do first</span><span class="hint">Open any item for the steps</span></div>`;
h += list(D.doFirst).length ? cols(list(D.doFirst).map((t, i) => item(`<span class="num-badge">${i + 1}</span>`, `<span class="title">${esc(t.deal)}</span><span class="who num">${esc([money(t.amount), t.owner].filter(Boolean).join(" · "))}</span><div>${esc(t.action)}</div>`, esc(t.why), null, stepsBox(t.steps, t.context) || detailBox(t.detail) || detailBox(t.why ? [t.why] : [])))) : `<div class="empty">Nothing urgent today.</div>`;
h += `</section>`;

h += `<section class="card" id="since"><div class="head"><span class="chip">New since yesterday</span><span class="hint">Replies, stage moves, wins and losses</span></div>`;
h += list(D.sinceYesterday).length ? cols(list(D.sinceYesterday).map(s => item(kindMark(s.kind), `<span class="title">${esc(s.deal)}</span><span class="who">${esc([money(s.amount), s.owner].filter(Boolean).join(" · "))}</span>`, esc(s.what), s.detail))) : `<div class="empty">Nothing changed since yesterday.</div>`;
h += `</section>`;

h += `<section class="card" id="at-risk"><div class="head"><span class="chip">${team ? "Biggest at risk" : "At risk"}</span><span class="hint">${AR.length > cap || N.atRisk > cap ? `Top ${Math.min(cap, AR.length)} of ${Math.max(N.atRisk, AR.length)}` : ""}</span></div>`;
if (AR.length) {
  h += cols(AR.slice(0, cap).map(d => item(`<span class="mark dot r"></span>`,
    `<span class="title">${esc(d.deal)}</span><span class="who num">${esc([money(d.amount), d.owner, d.stage].filter(Boolean).join(" · "))}</span><div class="qline">${quiet(d)}</div>`,
    `${esc(d.why)}<div class="next">${esc(d.next)}</div>`, d.detail)));
  const rest = AR.slice(cap);
  if (rest.length) h += `<div class="more">${rest.length} more${team ? ", grouped by rep in Team below" : ": " + esc(rest.map(d => d.deal).join(", "))}</div>`;
} else h += `<div class="empty">No deals at risk today.</div>`;
if (list(D.closeOut).length) h += `<div class="more">Close out (${list(D.closeOut).length}, no activity in 60+ days): ${esc(list(D.closeOut).join(", "))}</div>`;
h += `</section>`;

if (team) {
  const repBox = r => {
    const mine = AR.filter(d => d.owner === r.name).map(d => [d.deal, money(d.amount), d.stage].filter(Boolean).join(" · ") + ": " + (d.why || ""));
    return detailBox([...mine, ...(Array.isArray(r.detail) ? r.detail : r.detail ? [r.detail] : [])]);
  };
  h += `<section class="card" id="team"><div class="head"><span class="chip">Team</span><span class="hint">Most at risk first · open a rep for their deals</span></div>`;
  h += list(D.team).map(r => item(`<span class="mark dot ${r.atRiskCount ? "r" : "g"}"></span>`,
    `<div class="rep-row"><div><span class="title">${esc(r.name)}</span><div class="meta num">${r.closingCount || 0} closing this week</div></div><div><span class="sub2">${esc(r.ask)}</span>${r.atRiskCount ? `<span class="tag r">${r.atRiskCount} at risk</span>` : `<span class="tag g">On track</span>`}</div></div>`,
    "", null, repBox(r))).join("");
  h += `</section>`;
}

h += `<section class="card" id="calls"><div class="head"><span class="chip">Today's calls</span><span class="hint">${list(D.calls).length ? list(D.calls).length + " sales calls" : ""}</span></div>`;
h += list(D.calls).length ? list(D.calls).map(c => item(`<span class="time num">${esc(c.time)}</span>`,
  `<span class="title">${esc(c.company)}</span><span class="who">${esc(c.type)}</span><div class="meta">${esc(c.people)}</div><div class="meta num">${esc(c.deal)}</div>`,
  `${esc(c.open)}${c.prep ? `<div class="next">${esc(c.prep)}</div>` : ""}`, c.detail, "", "t")).join("") : `<div class="empty">No sales calls today.</div>`;
if (D.otherMeetings) h += `<div class="more">Also: ${esc(D.otherMeetings)}</div>`;
h += `</section>`;

h += `<section class="card" id="replies"><div class="head"><span class="chip">Replies waiting</span><span class="hint">${list(D.replies).length || ""}</span></div>`;
h += list(D.replies).length ? cols(list(D.replies).map(r => item(`<span class="mark dot ${r.waitingDays >= 2 ? "r" : "y"}"></span>`, `<span class="title">${esc(r.name)}</span><span class="who">${esc([r.company, r.channel].filter(Boolean).join(" · "))}</span>`, `${esc(r.ask)} <span class="tag ${r.waitingDays >= 2 ? "r" : "y"}">${r.waitingDays === 0 ? "today" : r.waitingDays + "d waiting"}</span>`, r.detail))) : `<div class="empty">No buyer is waiting on a reply.</div>`;
h += `</section>`;

h += `<section class="card" id="open-time"><div class="head"><span class="chip">Open time</span></div>`;
h += list(D.openTime).length ? cols(list(D.openTime).map(o => `<div class="item"><div class="row"><span class="mark dot g"></span><div><span class="title num">${esc(o.start)}–${esc(o.end)}</span><span class="who">${esc(o.length)}</span></div></div></div>`)) : `<div class="empty">No open blocks of 30+ minutes.</div>`;
h += `</section>`;

h += `<footer><details><summary>How this report works</summary><div class="about">
<p>This page is rebuilt from the calendar, CRM, email and calls each time it runs, in the same layout and order, so every section is always in the same place. It only reads those tools: nothing in the CRM, inboxes or calendars was changed.</p>
<p><b>New since yesterday</b> covers buyer replies, stage changes, wins, losses and signed contracts since the start of the previous working day. <b>At risk</b> means one of three things: no two-way contact in 14+ days, no dated next step, or a promised next step that didn't happen. <b>Slipped</b> means the close date has passed and the deal is still open. <b>Close out</b> names deals with no activity in 60+ days: close them with a reason or restart them. <b>Replies waiting</b> are buyers who wrote last and haven't heard back. <b>Today's calls</b> lists sales calls only; other meetings are on one line below them.</p>
<p>Open the arrow on any row for the details and where they came from.</p>
<p><b>Today:</b> ${esc(D.howBuilt)}</p></div></details><span>Updated ${esc(D.updated)} · Built with Sales Skills by <a href="https://skills.arrows.to" target="_blank" rel="noopener">Arrows</a></span></footer>`;
document.getElementById("app").innerHTML = h;
</script>
</body>
</html>
```
