

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
<title>GRAPHSTR — Nostr Social Graph Navigator</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/d3/7.8.5/d3.min.js"></script>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #080b0f;
  --surface: #0d1117;
  --surface2: #131920;
  --border: #1e2d3d;
  --border2: #243040;
  --accent: #00ff9d;
  --accent2: #00c8ff;
  --accent3: #ff6b35;
  --zap: #f7931a;
  --text: #e2eaf4;
  --muted: #5a7a9a;
  --danger: #ff4455;
  --mono: 'Space Mono', monospace;
  --display: 'Syne', sans-serif;
  --header-h: 56px;
  --sidebar-w: 320px;
}

*, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }
html, body { height:100%; overflow:hidden; }

body {
background: var(–bg);
color: var(–text);
font-family: var(–mono);
font-size: 13px;
}

body::before {
content:’’;
position:fixed; inset:0;
background:
linear-gradient(rgba(0,255,157,.025) 1px, transparent 1px),
linear-gradient(90deg, rgba(0,255,157,.025) 1px, transparent 1px);
background-size: 48px 48px;
pointer-events:none; z-index:0;
}

/* ── SCROLLBAR ── */
::-webkit-scrollbar { width:4px; height:4px; }
::-webkit-scrollbar-track { background:transparent; }
::-webkit-scrollbar-thumb { background:var(–border2); border-radius:2px; }

/* ══════════════════════════════════════
LAYOUT
══════════════════════════════════════ */
.app { position:relative; z-index:1; height:100vh; display:flex; flex-direction:column; }

/* HEADER */
header {
height: var(–header-h);
flex-shrink:0;
display:flex; align-items:center; justify-content:space-between;
padding: 0 20px;
border-bottom: 1px solid var(–border);
background: rgba(8,11,15,.97);
backdrop-filter: blur(16px);
z-index:200;
gap: 12px;
}

.logo {
font-family: var(–display);
font-size: 20px; font-weight:800;
display:flex; align-items:center; gap:8px;
flex-shrink:0;
}
.logo-mark {
width:26px; height:26px;
border:2px solid var(–accent); border-radius:6px;
display:flex; align-items:center; justify-content:center;
position:relative;
}
.logo-mark::before {
content:’’;
width:8px; height:8px;
background:var(–accent); border-radius:50%;
box-shadow: 0 0 10px var(–accent);
}

.header-search {
flex:1; max-width:440px;
display:flex; gap:6px;
}
.header-search input {
flex:1;
font-family:var(–mono); font-size:11px;
padding:7px 12px;
background:var(–surface2); border:1px solid var(–border2);
border-radius:4px; color:var(–text); outline:none;
transition: border-color .2s;
}
.header-search input:focus { border-color:var(–accent); }
.header-search input::placeholder { color:var(–muted); }

.header-right { display:flex; align-items:center; gap:8px; flex-shrink:0; }

.status-pill {
font-size:9px; letter-spacing:.5px;
padding:4px 8px; border-radius:20px;
border:1px solid var(–border2); color:var(–muted);
display:flex; align-items:center; gap:5px;
white-space:nowrap;
}
.status-dot {
width:5px; height:5px; border-radius:50%;
background:var(–accent);
animation: blink 2s infinite;
}
@keyframes blink { 0%,100%{opacity:1} 50%{opacity:.4} }

/* NAV BUTTONS */
.icon-btn {
width:34px; height:34px;
background:var(–surface2); border:1px solid var(–border);
border-radius:4px; color:var(–muted);
font-size:15px; cursor:pointer;
display:flex; align-items:center; justify-content:center;
transition: all .15s; position:relative;
}
.icon-btn:hover { color:var(–text); border-color:var(–border2); }
.icon-btn.active { color:var(–accent); border-color:var(–accent); }
.icon-btn .badge {
position:absolute; top:-4px; right:-4px;
width:14px; height:14px; border-radius:50%;
background:var(–zap); color:#000;
font-size:8px; font-weight:700;
display:flex; align-items:center; justify-content:center;
}

.btn-sm {
font-family:var(–mono); font-size:10px; font-weight:700;
letter-spacing:.8px; text-transform:uppercase;
padding:7px 14px; border-radius:4px; cursor:pointer;
transition: all .2s; white-space:nowrap;
}
.btn-outline { background:transparent; border:1px solid var(–accent); color:var(–accent); }
.btn-outline:hover { background:var(–accent); color:var(–bg); }
.btn-primary-sm { background:var(–zap); border:none; color:#000; }
.btn-primary-sm:hover { background:#ffaa33; }

/* BODY AREA */
.body { flex:1; display:flex; overflow:hidden; }

/* SIDEBAR */
.sidebar {
width: var(–sidebar-w);
flex-shrink:0;
border-right:1px solid var(–border);
background:var(–surface);
display:flex; flex-direction:column;
overflow:hidden;
transition: transform .3s ease, width .3s ease;
z-index:100;
}

.sidebar.hidden { display:none; }

.sidebar-tabs {
display:flex; border-bottom:1px solid var(–border);
flex-shrink:0;
}
.stab {
flex:1; padding:10px 4px;
font-size:9px; letter-spacing:1px; text-transform:uppercase;
color:var(–muted); background:none; border:none;
border-bottom:2px solid transparent;
cursor:pointer; transition: all .2s;
}
.stab.active { color:var(–accent); border-bottom-color:var(–accent); }
.stab:hover { color:var(–text); }

.sidebar-pane { display:none; flex-direction:column; flex:1; overflow:hidden; }
.sidebar-pane.active { display:flex; }

/* METRICS */
.metrics-section { padding:16px; border-bottom:1px solid var(–border); flex-shrink:0; }
.metrics-grid { display:grid; grid-template-columns:1fr 1fr; gap:6px; }
.metric-card {
background:var(–surface2); border:1px solid var(–border);
border-radius:6px; padding:10px;
}
.metric-label { font-size:8px; letter-spacing:1.5px; text-transform:uppercase; color:var(–muted); margin-bottom:4px; }
.metric-val {
font-family:var(–display); font-size:20px; font-weight:700; line-height:1;
}
.metric-val.g { color:var(–accent); }
.metric-val.b { color:var(–accent2); }
.metric-val.z { color:var(–zap); }
.metric-val.o { color:var(–accent3); }
.metric-sub { font-size:8px; color:var(–muted); margin-top:3px; }

/* REC LIST */
.section-head {
padding:12px 16px 8px;
font-size:9px; letter-spacing:2px; text-transform:uppercase; color:var(–muted);
flex-shrink:0;
}
.rec-scroll { flex:1; overflow-y:auto; padding:0 8px 8px; }
.rec-item {
display:flex; align-items:center; gap:10px;
padding:9px 10px; border-radius:6px;
border:1px solid transparent; cursor:pointer;
transition: all .15s;
}
.rec-item:hover { background:var(–surface2); border-color:var(–border); }
.rec-item.locked { opacity:.45; pointer-events:none; }
.rec-avatar {
width:32px; height:32px; border-radius:7px;
background:var(–surface2); border:1px solid var(–border2);
display:flex; align-items:center; justify-content:center;
font-size:13px; flex-shrink:0; overflow:hidden;
}
.rec-avatar img { width:100%; height:100%; object-fit:cover; }
.rec-info { flex:1; min-width:0; }
.rec-name { font-family:var(–display); font-size:12px; font-weight:600; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
.rec-meta { font-size:9px; color:var(–muted); margin-top:1px; }
.rec-score { font-size:10px; font-weight:700; color:var(–accent); flex-shrink:0; }

.zap-gate {
margin:10px 12px;
padding:12px; border-radius:6px;
background:rgba(247,147,26,.08); border:1px solid rgba(247,147,26,.25);
text-align:center; flex-shrink:0;
}
.zap-gate strong { display:block; font-size:11px; color:var(–zap); margin-bottom:4px; }
.zap-gate span { font-size:9px; color:var(–muted); display:block; margin-bottom:10px; }
.btn-zap { width:100%; padding:8px; background:var(–zap); color:#000; border:none; border-radius:4px; font-family:var(–mono); font-size:10px; font-weight:700; letter-spacing:1px; text-transform:uppercase; cursor:pointer; transition: all .2s; }
.btn-zap:hover { background:#ffaa33; }

/* WATCHLIST PANE */
.watch-scroll { flex:1; overflow-y:auto; padding:8px; }
.watch-item {
display:flex; align-items:center; gap:10px;
padding:10px; border-radius:6px; border:1px solid var(–border);
background:var(–surface2); margin-bottom:6px; cursor:pointer;
transition: border-color .15s;
}
.watch-item:hover { border-color:var(–border2); }
.watch-info { flex:1; min-width:0; }
.watch-name { font-family:var(–display); font-size:12px; font-weight:600; }
.watch-npub { font-size:9px; color:var(–muted); margin-top:2px; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
.watch-remove { color:var(–muted); background:none; border:none; cursor:pointer; font-size:14px; padding:4px; transition: color .15s; }
.watch-remove:hover { color:var(–danger); }
.watch-empty { padding:40px 20px; text-align:center; color:var(–muted); font-size:11px; line-height:1.7; }

.btn-add-watch {
margin:10px 12px 12px;
width:calc(100% - 24px);
padding:9px; background:transparent;
border:1px dashed var(–border2); border-radius:4px;
color:var(–muted); font-family:var(–mono); font-size:10px;
cursor:pointer; transition: all .2s; flex-shrink:0;
}
.btn-add-watch:hover { border-color:var(–accent); color:var(–accent); }

/* RELAY PANE */
.relay-scroll { flex:1; overflow-y:auto; padding:8px; }
.relay-item {
display:flex; align-items:center; gap:8px;
padding:9px 10px; border-radius:6px; border:1px solid var(–border);
background:var(–surface2); margin-bottom:5px;
}
.relay-dot { width:7px; height:7px; border-radius:50%; flex-shrink:0; }
.relay-dot.live { background:var(–accent); box-shadow:0 0 6px var(–accent); }
.relay-dot.dead { background:var(–muted); }
.relay-url { flex:1; font-size:10px; color:var(–muted); overflow:hidden; text-overflow:ellipsis; white-space:nowrap; }
.relay-ping { font-size:9px; color:var(–accent); flex-shrink:0; }
.relay-remove { background:none; border:none; color:var(–muted); cursor:pointer; font-size:12px; padding:2px; }
.relay-remove:hover { color:var(–danger); }
.relay-add { display:flex; gap:6px; padding:10px 12px; flex-shrink:0; }
.relay-add input { flex:1; font-family:var(–mono); font-size:10px; padding:7px 10px; background:var(–surface2); border:1px solid var(–border2); border-radius:4px; color:var(–text); outline:none; }
.relay-add input:focus { border-color:var(–accent); }
.relay-add button { padding:7px 12px; background:var(–accent); color:var(–bg); border:none; border-radius:4px; font-family:var(–mono); font-size:10px; font-weight:700; cursor:pointer; }

/* CONTENT AREA */
.content { flex:1; display:flex; flex-direction:column; overflow:hidden; position:relative; }

.view-tabs {
display:flex; border-bottom:1px solid var(–border);
padding:0 20px; background:var(–surface); flex-shrink:0;
}
.vtab {
font-family:var(–mono); font-size:9px; letter-spacing:1px; text-transform:uppercase;
padding:13px 16px; border-bottom:2px solid transparent;
cursor:pointer; color:var(–muted); background:none;
border-top:none; border-left:none; border-right:none;
transition: all .2s;
}
.vtab:hover { color:var(–text); }
.vtab.active { color:var(–accent); border-bottom-color:var(–accent); }

/* GRAPH */
.graph-wrap { flex:1; position:relative; overflow:hidden; }
#graph-svg { width:100%; height:100%; display:block; }

.graph-controls {
position:absolute; bottom:20px; right:20px;
display:flex; flex-direction:column; gap:4px;
}
.graph-btn {
width:30px; height:30px;
background:var(–surface); border:1px solid var(–border2);
color:var(–text); font-size:14px; border-radius:4px;
cursor:pointer; display:flex; align-items:center; justify-content:center;
transition: all .15s;
}
.graph-btn:hover { border-color:var(–accent); color:var(–accent); }

.graph-legend {
position:absolute; bottom:20px; left:20px;
display:flex; flex-direction:column; gap:5px;
}
.leg { display:flex; align-items:center; gap:7px; font-size:9px; color:var(–muted); letter-spacing:.5px; text-transform:uppercase; }
.leg-dot { width:7px; height:7px; border-radius:50%; flex-shrink:0; }

/* NICHE GRID */
.niche-wrap { flex:1; overflow-y:auto; padding:24px; }
.niche-grid { display:grid; grid-template-columns:repeat(auto-fill, minmax(240px,1fr)); gap:14px; }
.niche-card {
background:var(–surface); border:1px solid var(–border);
border-radius:8px; padding:18px; cursor:pointer;
transition: all .2s; position:relative; overflow:hidden;
}
.niche-card::before { content:’’; position:absolute; top:0; left:0; right:0; height:2px; background:var(–nc, var(–accent)); }
.niche-card:hover { border-color:var(–border2); transform:translateY(-2px); box-shadow:0 8px 24px rgba(0,0,0,.4); }
.niche-name { font-family:var(–display); font-size:15px; font-weight:700; margin-bottom:4px; }
.niche-tag { font-size:9px; color:var(–muted); margin-bottom:14px; }
.niche-stats { display:flex; gap:16px; }
.ns-val { font-family:var(–display); font-size:18px; font-weight:700; color:var(–nc, var(–accent)); }
.ns-lbl { font-size:8px; color:var(–muted); letter-spacing:1px; text-transform:uppercase; margin-top:2px; }
.niche-bar { margin-top:12px; height:2px; background:var(–border); border-radius:1px; overflow:hidden; }
.niche-bar-fill { height:100%; background:var(–nc, var(–accent)); border-radius:1px; transition:width 1s ease; width:0; }

/* ACTIVITY */
.activity-wrap { flex:1; overflow-y:auto; padding:24px; }
.activity-list { max-width:680px; }
.act-item {
display:grid; grid-template-columns:120px 1fr auto;
gap:14px; padding:12px 0;
border-bottom:1px solid var(–border);
font-size:11px;
animation: fadeUp .3s ease forwards; opacity:0;
}
@keyframes fadeUp { to { opacity:1; transform:translateY(0); } from { opacity:0; transform:translateY(6px); } }
.act-time { color:var(–muted); }
.act-content { color:var(–text); line-height:1.5; }
.act-actor { color:var(–accent2); font-weight:700; }
.act-zap { color:var(–zap); font-weight:700; white-space:nowrap; }

/* EMPTY STATE */
.empty-state {
flex:1; display:flex; flex-direction:column;
align-items:center; justify-content:center;
gap:14px; color:var(–muted); padding:40px;
}
.empty-icon {
width:72px; height:72px; border-radius:50%;
border:1px solid var(–border2);
display:flex; align-items:center; justify-content:center;
font-size:28px; position:relative;
}
.empty-icon::before {
content:’’; position:absolute; inset:-10px; border-radius:50%;
border:1px solid var(–border); animation:spin 8s linear infinite;
}
.empty-icon::after {
content:’’; position:absolute; inset:-20px; border-radius:50%;
border:1px dashed rgba(30,45,61,.6); animation:spin 14s linear infinite reverse;
}
@keyframes spin { to { transform:rotate(360deg); } }
.empty-title { font-family:var(–display); font-size:18px; font-weight:700; color:var(–text); }
.empty-sub { font-size:11px; text-align:center; max-width:300px; line-height:1.7; }

/* LOADING BAR */
.load-bar { height:2px; background:var(–border); overflow:hidden; flex-shrink:0; }
.load-bar.hidden { display:none; }
.load-bar::after {
content:’’; display:block; height:100%;
background:linear-gradient(90deg, transparent, var(–accent), transparent);
animation: sweep 1.2s infinite;
width:40%; margin-left:-40%;
}
@keyframes sweep { to { margin-left:100%; } }

/* ══════════════════════════════════════
PROFILE PANEL (slide-in from right)
══════════════════════════════════════ */
.profile-panel {
position:absolute; top:0; right:0; bottom:0;
width:360px; max-width:100%;
background:var(–surface); border-left:1px solid var(–border);
display:flex; flex-direction:column;
transform:translateX(100%); transition:transform .3s ease;
z-index:150; overflow:hidden;
}
.profile-panel.open { transform:translateX(0); }

.pp-header {
display:flex; align-items:center; gap:12px;
padding:16px; border-bottom:1px solid var(–border); flex-shrink:0;
}
.pp-avatar {
width:48px; height:48px; border-radius:10px;
background:var(–surface2); border:1px solid var(–border2);
display:flex; align-items:center; justify-content:center;
font-size:22px; flex-shrink:0; overflow:hidden;
}
.pp-avatar img { width:100%; height:100%; object-fit:cover; }
.pp-name { font-family:var(–display); font-size:16px; font-weight:700; }
.pp-npub { font-size:9px; color:var(–muted); margin-top:2px; font-family:var(–mono); }
.pp-close {
margin-left:auto; width:28px; height:28px;
background:var(–surface2); border:1px solid var(–border);
border-radius:4px; color:var(–muted); cursor:pointer;
font-size:14px; display:flex; align-items:center; justify-content:center;
flex-shrink:0; transition:all .15s;
}
.pp-close:hover { color:var(–text); }

.pp-stats {
display:grid; grid-template-columns:1fr 1fr 1fr;
gap:1px; background:var(–border); flex-shrink:0;
}
.pp-stat { padding:12px; background:var(–surface); text-align:center; }
.pp-stat-val { font-family:var(–display); font-size:16px; font-weight:700; color:var(–text); }
.pp-stat-lbl { font-size:8px; color:var(–muted); letter-spacing:1px; text-transform:uppercase; margin-top:2px; }

.pp-bio { padding:14px 16px; font-size:11px; color:var(–muted); line-height:1.6; border-bottom:1px solid var(–border); flex-shrink:0; max-height:80px; overflow-y:auto; }

.pp-actions { display:flex; gap:8px; padding:12px 16px; border-bottom:1px solid var(–border); flex-shrink:0; }
.pp-btn {
flex:1; padding:8px; border-radius:4px;
font-family:var(–mono); font-size:10px; font-weight:700;
letter-spacing:.5px; cursor:pointer; transition:all .2s; text-align:center;
}
.pp-btn-follow { background:var(–accent); color:var(–bg); border:none; }
.pp-btn-follow:hover { background:#00e88a; }
.pp-btn-watch { background:transparent; border:1px solid var(–border2); color:var(–muted); }
.pp-btn-watch:hover { border-color:var(–zap); color:var(–zap); }
.pp-btn-watch.watching { border-color:var(–zap); color:var(–zap); background:rgba(247,147,26,.08); }

.pp-notes { flex:1; overflow-y:auto; padding:0; }
.pp-note {
padding:14px 16px; border-bottom:1px solid var(–border);
font-size:11px; line-height:1.6; color:var(–text);
}
.pp-note-time { font-size:9px; color:var(–muted); margin-bottom:6px; }
.pp-note-text { word-break:break-word; }

.pp-loading { padding:40px; text-align:center; color:var(–muted); font-size:11px; }

/* ══════════════════════════════════════
SHARE CARD MODAL
══════════════════════════════════════ */
.modal-overlay {
display:none; position:fixed; inset:0;
background:rgba(0,0,0,.85); z-index:500;
align-items:center; justify-content:center;
backdrop-filter:blur(10px);
}
.modal-overlay.open { display:flex; }

.modal {
background:var(–surface); border:1px solid var(–border2);
border-radius:12px; width:520px; max-width:95vw;
max-height:92vh; overflow-y:auto;
animation: modalIn .25s ease;
}
@keyframes modalIn {
from { opacity:0; transform:translateY(12px) scale(.97); }
to   { opacity:1; transform:translateY(0) scale(1); }
}
.modal-hdr {
display:flex; align-items:center; justify-content:space-between;
padding:20px 24px 16px; border-bottom:1px solid var(–border);
}
.modal-title { font-family:var(–display); font-size:17px; font-weight:800; }
.modal-x {
width:26px; height:26px; background:var(–surface2); border:1px solid var(–border);
border-radius:4px; color:var(–muted); cursor:pointer; font-size:14px;
display:flex; align-items:center; justify-content:center; transition:all .15s;
}
.modal-x:hover { color:var(–text); }
.modal-body { padding:24px; }

/* Share card preview */
.share-preview {
background:linear-gradient(135deg, #0a0f14 0%, #0d1a24 100%);
border:1px solid var(–border2); border-radius:10px;
padding:28px; margin-bottom:20px; position:relative; overflow:hidden;
}
.share-preview::before {
content:’’;
position:absolute; inset:0;
background:
linear-gradient(rgba(0,255,157,.04) 1px, transparent 1px),
linear-gradient(90deg, rgba(0,255,157,.04) 1px, transparent 1px);
background-size:32px 32px;
}
.sc-logo { font-family:var(–display); font-size:13px; font-weight:800; color:var(–muted); margin-bottom:20px; position:relative; }
.sc-logo span { color:var(–accent); }
.sc-name { font-family:var(–display); font-size:22px; font-weight:800; color:var(–text); margin-bottom:4px; position:relative; }
.sc-npub { font-size:10px; color:var(–muted); margin-bottom:20px; position:relative; }
.sc-stats { display:grid; grid-template-columns:repeat(4,1fr); gap:16px; position:relative; }
.sc-stat-val { font-family:var(–display); font-size:20px; font-weight:700; }
.sc-stat-lbl { font-size:8px; color:var(–muted); letter-spacing:1px; text-transform:uppercase; margin-top:3px; }
.sc-footer { margin-top:20px; padding-top:16px; border-top:1px solid rgba(255,255,255,.06); font-size:9px; color:var(–muted); position:relative; display:flex; justify-content:space-between; }

.share-actions { display:flex; gap:8px; }
.btn-share {
flex:1; padding:10px; border-radius:4px; border:none;
font-family:var(–mono); font-size:10px; font-weight:700; letter-spacing:.8px; text-transform:uppercase;
cursor:pointer; transition:all .2s;
}
.btn-share-nostr { background:var(–accent); color:var(–bg); }
.btn-share-nostr:hover { background:#00e88a; }
.btn-share-copy { background:var(–surface2); border:1px solid var(–border2); color:var(–muted); }
.btn-share-copy:hover { border-color:var(–border2); color:var(–text); }

/* ══════════════════════════════════════
ZAP GATE MODAL
══════════════════════════════════════ */
.zg-steps { display:flex; gap:5px; justify-content:center; margin-bottom:20px; }
.zg-dot { width:6px; height:6px; border-radius:50%; background:var(–border2); transition: background .3s; }
.zg-dot.active { background:var(–zap); }
.zg-dot.done { background:var(–accent); }

.zg-step { display:none; }
.zg-step.active { display:block; }

.pay-opts { display:grid; grid-template-columns:1fr 1fr; gap:10px; margin-bottom:18px; }
.pay-opt {
padding:16px 12px; background:var(–surface2); border:1px solid var(–border);
border-radius:8px; cursor:pointer; transition:all .2s; text-align:center;
}
.pay-opt:hover, .pay-opt.sel { border-color:var(–zap); background:rgba(247,147,26,.08); }
.pay-opt-ico { font-size:22px; margin-bottom:6px; }
.pay-opt-lbl { font-family:var(–display); font-size:12px; font-weight:700; margin-bottom:2px; }
.pay-opt-sub { font-size:9px; color:var(–muted); }

.pay-status { text-align:center; padding:8px 0; font-size:11px; }
.pay-status.pending { color:var(–muted); }
.pay-status.ok { color:var(–accent); }
.pay-status.err { color:var(–danger); }
.dots::after { content:’’; animation: dotanim 1.5s infinite; }
@keyframes dotanim { 0%{content:’.’} 33%{content:’..’} 66%{content:’…’} 100%{content:’’} }

.invoice-box {
background:var(–surface2); border:1px solid var(–border2); border-radius:6px;
padding:12px; margin-bottom:12px; font-size:9px; color:var(–muted);
word-break:break-all; line-height:1.5; max-height:72px; overflow:hidden;
position:relative;
}
.invoice-box::after { content:’’; position:absolute; bottom:0; left:0; right:0; height:28px; background:linear-gradient(transparent, var(–surface2)); }

.qr-wrap { display:flex; justify-content:center; margin:12px 0; }
.qr-wrap img { border-radius:8px; background:#fff; padding:6px; }

.btn-full {
width:100%; padding:11px; border-radius:4px; border:none;
font-family:var(–mono); font-size:11px; font-weight:700; letter-spacing:1px; text-transform:uppercase;
cursor:pointer; transition:all .2s; margin-bottom:8px;
}
.btn-full-zap { background:var(–zap); color:#000; }
.btn-full-zap:hover { background:#ffaa33; }
.btn-full-zap:disabled { opacity:.4; cursor:not-allowed; }
.btn-full-ghost { background:transparent; border:1px solid var(–border); color:var(–muted); }
.btn-full-ghost:hover { border-color:var(–border2); color:var(–text); }

.success-ico { font-size:44px; text-align:center; margin:4px 0 14px; animation:pop .4s cubic-bezier(.175,.885,.32,1.275); }
@keyframes pop { from{transform:scale(0);opacity:0} to{transform:scale(1);opacity:1} }
.success-title { font-family:var(–display); font-size:20px; font-weight:800; text-align:center; color:var(–accent); margin-bottom:8px; }
.success-sub { font-size:11px; color:var(–muted); text-align:center; line-height:1.6; margin-bottom:20px; }

/* ══════════════════════════════════════
TOOLTIP
══════════════════════════════════════ */
.tooltip {
position:fixed; background:var(–surface2); border:1px solid var(–border2);
border-radius:6px; padding:10px 14px; font-size:11px; color:var(–text);
pointer-events:none; z-index:999; max-width:190px;
box-shadow:0 8px 24px rgba(0,0,0,.5); display:none;
}
.tt-name { font-family:var(–display); font-weight:700; font-size:13px; margin-bottom:4px; }
.tt-stat { color:var(–muted); margin-top:2px; }
.tt-stat span { color:var(–accent); }

/* MOBILE BOTTOM NAV */
.mobile-nav {
display:none;
position:fixed; bottom:0; left:0; right:0;
height:56px; background:var(–surface);
border-top:1px solid var(–border);
z-index:300;
grid-template-columns:repeat(5,1fr);
}
.mnav-btn {
display:flex; flex-direction:column; align-items:center; justify-content:center;
gap:3px; background:none; border:none; color:var(–muted); cursor:pointer;
font-size:9px; letter-spacing:.5px; text-transform:uppercase; transition: color .15s;
padding:4px 0;
}
.mnav-btn.active { color:var(–accent); }
.mnav-ico { font-size:18px; line-height:1; }

/* MOBILE SIDEBAR OVERLAY */
.sidebar-overlay {
display:none;
position:fixed; inset:0; background:rgba(0,0,0,.6); z-index:99;
}

/* ══════════════════════════════════════
RESPONSIVE
══════════════════════════════════════ */
@media (max-width: 768px) {
:root { –sidebar-w: 100vw; }

.app { height:calc(100vh - 56px); }

/* Header collapses */
header { padding:0 12px; }
.status-pill { display:none; }
.logo { font-size:17px; }

/* Sidebar becomes a sheet */
.sidebar {
position:fixed; top:var(–header-h); bottom:56px; left:0;
transform:translateX(-100%); z-index:100;
width:90vw; max-width:360px;
box-shadow:4px 0 24px rgba(0,0,0,.5);
}
.sidebar.mobile-open { transform:translateX(0); }
.sidebar-overlay { display:none; }
.sidebar-overlay.show { display:block; }

/* Content fills full width */
.body { flex-direction:column; }
.content { height:100%; }

/* Profile panel */
.profile-panel { width:100%; max-width:100%; }

/* Graph legend smaller */
.graph-legend { display:none; }

/* Mobile nav shows */
.mobile-nav { display:grid; }

/* View tabs scroll */
.view-tabs { overflow-x:auto; }
.vtab { padding:13px 12px; white-space:nowrap; }

/* Hide desktop sidebar toggle */
#desktop-sidebar-toggle { display:none; }

/* Niche grid single col */
.niche-grid { grid-template-columns:1fr; }

/* Activity 2-col instead of 3 */
.act-item { grid-template-columns:80px 1fr; }
.act-zap { display:none; }
}

@media (max-width:480px) {
.header-search { max-width:180px; }
.share-preview .sc-stats { grid-template-columns:repeat(2,1fr); }
}
</style>

</head>
<body>
<div class="app">

<!-- HEADER -->

<header>
  <div class="logo">
    <div class="logo-mark"></div>
    <span>GRAPH</span><span style="color:var(--accent)">STR</span>
  </div>

  <div class="header-search">
    <input id="npub-input" type="text" placeholder="npub1... or hex pubkey" autocomplete="off" />
    <button class="btn-sm btn-outline" id="analyze-btn" onclick="analyzeProfile()">MAP</button>
  </div>

  <div class="header-right">
    <div class="status-pill">
      <div class="status-dot"></div>
      <span id="relay-status">CONNECTING</span>
    </div>
    <button class="icon-btn" id="desktop-sidebar-toggle" onclick="toggleDesktopSidebar()" title="Toggle sidebar">☰</button>
    <button class="icon-btn" id="watchlist-badge-btn" onclick="openMobilePanel('watch')" title="Watchlist">
      👁
      <span class="badge" id="watch-count" style="display:none">0</span>
    </button>
    <button class="icon-btn" onclick="openShareModal()" title="Share graph">📤</button>
    <button class="btn-sm btn-outline" onclick="connectNIP07()">⚡ CONNECT</button>
  </div>
</header>

<!-- BODY -->

<div class="body">

  <!-- SIDEBAR -->

  <aside class="sidebar" id="sidebar">
    <div class="sidebar-tabs">
      <button class="stab active" onclick="switchSideTab('graph')">Graph</button>
      <button class="stab" onclick="switchSideTab('watch')">Watchlist</button>
      <button class="stab" onclick="switchSideTab('relays')">Relays</button>
    </div>

```
<!-- GRAPH PANE -->
<div class="sidebar-pane active" id="spane-graph">
  <div class="metrics-section" id="metrics-section" style="display:none">
    <div class="metrics-grid">
      <div class="metric-card">
        <div class="metric-label">Following</div>
        <div class="metric-val g" id="m-following">—</div>
        <div class="metric-sub" id="m-relay-sub">across relays</div>
      </div>
      <div class="metric-card">
        <div class="metric-label">2nd Degree</div>
        <div class="metric-val b" id="m-reach">—</div>
        <div class="metric-sub">network reach</div>
      </div>
      <div class="metric-card">
        <div class="metric-label">Zap Weight</div>
        <div class="metric-val z" id="m-zapscore">—</div>
        <div class="metric-sub">economic score</div>
      </div>
      <div class="metric-card">
        <div class="metric-label">Niches</div>
        <div class="metric-val o" id="m-niches">—</div>
        <div class="metric-sub">communities</div>
      </div>
    </div>
  </div>

  <div class="section-head" id="rec-head" style="display:none">Recommended Follows</div>
  <div class="rec-scroll" id="rec-list"></div>

  <div class="zap-gate" id="zap-gate" style="display:none">
    <strong>⚡ UNLOCK FULL LIST</strong>
    <span>Top 5 free · All + deep graph: 1,000 sats</span>
    <button class="btn-zap" onclick="openZapGate()">ZAP TO UNLOCK</button>
  </div>
</div>

<!-- WATCHLIST PANE -->
<div class="sidebar-pane" id="spane-watch">
  <div class="section-head">Watching</div>
  <div class="watch-scroll" id="watch-list">
    <div class="watch-empty" id="watch-empty">No profiles watched yet.<br>Click a node in the graph and tap "Watch" to track someone.</div>
  </div>
  <button class="btn-add-watch" onclick="promptAddWatch()">+ Add npub to watchlist</button>
</div>

<!-- RELAY PANE -->
<div class="sidebar-pane" id="spane-relays">
  <div class="section-head">Active Relays</div>
  <div class="relay-scroll" id="relay-list"></div>
  <div class="relay-add">
    <input id="relay-input" type="text" placeholder="wss://relay.example.com" />
    <button onclick="addRelay()">Add</button>
  </div>
</div>
```

  </aside>

  <!-- SIDEBAR OVERLAY (mobile) -->

  <div class="sidebar-overlay" id="sidebar-overlay" onclick="closeMobileSidebar()"></div>

  <!-- CONTENT -->

  <div class="content">
    <div class="load-bar hidden" id="load-bar"></div>

```
<!-- EMPTY STATE -->
<div class="empty-state" id="empty-state">
  <div class="empty-icon">⬡</div>
  <div class="empty-title">No graph loaded</div>
  <div class="empty-sub">Paste an npub above or connect your Nostr extension to map your social graph and find who you should follow.</div>
</div>

<!-- VIEW TABS -->
<div class="view-tabs" id="view-tabs" style="display:none">
  <button class="vtab active" onclick="switchView('graph')">Graph</button>
  <button class="vtab" onclick="switchView('niches')">Niches</button>
  <button class="vtab" onclick="switchView('activity')">Activity</button>
</div>

<!-- GRAPH VIEW -->
<div class="graph-wrap" id="view-graph" style="display:none">
  <svg id="graph-svg"></svg>
  <div class="graph-controls">
    <button class="graph-btn" onclick="zoomIn()">+</button>
    <button class="graph-btn" onclick="zoomOut()">−</button>
    <button class="graph-btn" onclick="resetZoom()" style="font-size:10px">⟳</button>
  </div>
  <div class="graph-legend">
    <div class="leg"><div class="leg-dot" style="background:#00ff9d"></div>You</div>
    <div class="leg"><div class="leg-dot" style="background:#f7931a"></div>High Zap</div>
    <div class="leg"><div class="leg-dot" style="background:#00c8ff"></div>Following</div>
    <div class="leg"><div class="leg-dot" style="background:#2a3f55"></div>2nd Degree</div>
  </div>
</div>

<!-- NICHES VIEW -->
<div class="niche-wrap" id="view-niches" style="display:none">
  <div class="niche-grid" id="niche-grid"></div>
</div>

<!-- ACTIVITY VIEW -->
<div class="activity-wrap" id="view-activity" style="display:none">
  <div class="activity-list" id="activity-list"></div>
</div>

<!-- PROFILE PANEL -->
<div class="profile-panel" id="profile-panel">
  <div class="pp-header" id="pp-header">
    <div class="pp-avatar" id="pp-avatar">?</div>
    <div>
      <div class="pp-name" id="pp-name">—</div>
      <div class="pp-npub" id="pp-npub">—</div>
    </div>
    <button class="pp-close" onclick="closeProfilePanel()">✕</button>
  </div>
  <div class="pp-stats" id="pp-stats">
    <div class="pp-stat"><div class="pp-stat-val" id="pp-zaps">—</div><div class="pp-stat-lbl">Zap Score</div></div>
    <div class="pp-stat"><div class="pp-stat-val" id="pp-follows">—</div><div class="pp-stat-lbl">Following</div></div>
    <div class="pp-stat"><div class="pp-stat-val" id="pp-degree">—</div><div class="pp-stat-lbl">Degree</div></div>
  </div>
  <div class="pp-bio" id="pp-bio"></div>
  <div class="pp-actions">
    <button class="pp-btn pp-btn-follow" onclick="followProfile()" id="pp-follow-btn">+ Follow</button>
    <button class="pp-btn pp-btn-watch" onclick="toggleWatch()" id="pp-watch-btn">👁 Watch</button>
  </div>
  <div class="pp-notes" id="pp-notes">
    <div class="pp-loading">Loading notes...</div>
  </div>
</div>
```

  </div>
</div>

<!-- MOBILE BOTTOM NAV -->

<nav class="mobile-nav">
  <button class="mnav-btn active" id="mnav-graph" onclick="mobileNav('graph')"><span class="mnav-ico">⬡</span>Graph</button>
  <button class="mnav-btn" id="mnav-niches" onclick="mobileNav('niches')"><span class="mnav-ico">⊞</span>Niches</button>
  <button class="mnav-btn" id="mnav-activity" onclick="mobileNav('activity')"><span class="mnav-ico">⚡</span>Activity</button>
  <button class="mnav-btn" id="mnav-sidebar" onclick="toggleMobileSidebar()"><span class="mnav-ico">☰</span>Menu</button>
  <button class="mnav-btn" id="mnav-share" onclick="openShareModal()"><span class="mnav-ico">📤</span>Share</button>
</nav>

</div><!-- .app -->

<!-- TOOLTIP -->

<div class="tooltip" id="tooltip">
  <div class="tt-name" id="tt-name"></div>
  <div class="tt-stat">Zap score: <span id="tt-zap">—</span></div>
  <div class="tt-stat">Degree: <span id="tt-deg">—</span></div>
</div>

<!-- SHARE MODAL -->

<div class="modal-overlay" id="share-modal">
  <div class="modal">
    <div class="modal-hdr">
      <div class="modal-title">📤 Share Your Graph</div>
      <button class="modal-x" onclick="closeModal('share-modal')">✕</button>
    </div>
    <div class="modal-body">
      <div class="share-preview" id="share-preview">
        <div class="sc-logo">GRAPH<span>STR</span></div>
        <div class="sc-name" id="sc-name">—</div>
        <div class="sc-npub" id="sc-npub">—</div>
        <div class="sc-stats">
          <div><div class="sc-stat-val g" id="sc-following">—</div><div class="sc-stat-lbl">Following</div></div>
          <div><div class="sc-stat-val b" id="sc-reach">—</div><div class="sc-stat-lbl">Reach</div></div>
          <div><div class="sc-stat-val z" id="sc-zap">—</div><div class="sc-stat-lbl">Zap Weight</div></div>
          <div><div class="sc-stat-val o" id="sc-niches">—</div><div class="sc-stat-lbl">Niches</div></div>
        </div>
        <div class="sc-footer">
          <span>graphstr.app</span>
          <span id="sc-date"></span>
        </div>
      </div>
      <div class="share-actions">
        <button class="btn-share btn-share-nostr" onclick="shareToNostr()">⚡ Post to Nostr</button>
        <button class="btn-share btn-share-copy" onclick="copyShareText()">📋 Copy Text</button>
      </div>
      <div id="share-status" style="margin-top:10px;font-size:10px;text-align:center;color:var(--muted)"></div>
    </div>
  </div>
</div>

<!-- ZAP GATE MODAL -->

<div class="modal-overlay" id="zap-modal">
  <div class="modal">
    <div class="modal-hdr">
      <div class="modal-title">⚡ Unlock Full Graph</div>
      <button class="modal-x" onclick="closeModal('zap-modal')">✕</button>
    </div>
    <div class="modal-body">
      <div class="zg-steps">
        <div class="zg-dot active" id="zgd1"></div>
        <div class="zg-dot" id="zgd2"></div>
        <div class="zg-dot" id="zgd3"></div>
      </div>

```
  <!-- Step 1: Choose -->
  <div class="zg-step active" id="zgs-choose">
    <div style="font-size:9px;letter-spacing:2px;text-transform:uppercase;color:var(--muted);margin-bottom:8px">Choose Payment Method</div>
    <div style="font-size:11px;color:var(--muted);line-height:1.6;margin-bottom:18px">Unlock your full recommendation list + deep 2nd-degree graph for 1,000 sats. One-time payment, saved to this device.</div>
    <div class="pay-opts">
      <div class="pay-opt" id="opt-nwc" onclick="selectPay('nwc')">
        <div class="pay-opt-ico">🔌</div>
        <div class="pay-opt-lbl">Wallet Connect</div>
        <div class="pay-opt-sub">NWC auto-pay</div>
      </div>
      <div class="pay-opt" id="opt-inv" onclick="selectPay('invoice')">
        <div class="pay-opt-ico">⚡</div>
        <div class="pay-opt-lbl">Lightning Invoice</div>
        <div class="pay-opt-sub">QR or copy</div>
      </div>
    </div>
    <div id="nwc-section" style="display:none">
      <div style="font-size:9px;color:var(--muted);margin-bottom:6px">NWC string from Alby Hub → Developer → Wallet Connect</div>
      <input class="input-field" id="nwc-str" type="text" placeholder="nostr+walletconnect://..." style="width:100%;font-family:var(--mono);font-size:10px;padding:9px 12px;background:var(--surface2);border:1px solid var(--border2);border-radius:4px;color:var(--text);outline:none;margin-bottom:12px;" />
      <button class="btn-full btn-full-zap" onclick="doNWCPay()">→ Connect & Pay 1,000 sats</button>
    </div>
    <button class="btn-full btn-full-zap" id="btn-gen-inv" style="display:none" onclick="doInvoicePay()">→ Generate Invoice</button>
  </div>

  <!-- Step 2: Pay -->
  <div class="zg-step" id="zgs-pay">
    <div id="inv-display" style="display:none">
      <div class="qr-wrap" id="qr-wrap"></div>
      <div class="invoice-box" id="inv-text"></div>
      <button class="btn-full btn-full-ghost" onclick="copyInvoice()">📋 Copy Invoice</button>
      <div class="pay-status pending" id="pay-status"><span class="dots">Waiting for payment</span></div>
    </div>
    <div id="nwc-paying" style="display:none">
      <div class="pay-status pending" id="nwc-status"><span class="dots">Sending payment via NWC</span></div>
    </div>
    <button class="btn-full btn-full-ghost" onclick="zgStep('choose')" style="margin-top:14px">← Back</button>
  </div>

  <!-- Step 3: Success -->
  <div class="zg-step" id="zgs-success">
    <div class="success-ico">✅</div>
    <div class="success-title">Unlocked</div>
    <div class="success-sub">Full recommendations and deep graph analysis active. Saved to this device.</div>
    <button class="btn-full btn-full-zap" onclick="closeModal('zap-modal')">→ View Full Graph</button>
  </div>
</div>
```

  </div>
</div>

<script>
// ══════════════════════════════════════════════
// GRAPHSTR v2 — Full production build
// ══════════════════════════════════════════════

// ── CONFIG
const DEFAULT_RELAYS = [
  'wss://relay.damus.io',
  'wss://relay.nostr.band',
  'wss://nos.lol',
  'wss://relay.primal.net',
  'wss://nostr.wine'
];
const LN_ADDRESS = 'contra@rizful.com';
const ZAP_SATS = 1000;
const ZAP_MSATS = ZAP_SATS * 1000;
const BECH32 = 'qpzry9x8gf2tvdw0s3jn54khce6mua7l';

// ── STATE
let relays = loadRelays();
let graphData = null;
let simulation = null;
let svgZoom = null;
let currentView = 'graph';
let currentSideTab = 'graph';
let openProfilePubkey = null;
let watchlist = loadWatchlist();
let unlocked = loadUnlocked();
let pollInterval = null;
let nwcWs = null;
let currentInvoice = null;
let selectedPayMethod = null;
let connectedRelays = 0;
let openSockets = [];

// ══════════════════════════════════════════════
// STORAGE
// ══════════════════════════════════════════════
function loadRelays() {
  try { const r = JSON.parse(localStorage.getItem('gs_relays')); if (Array.isArray(r) && r.length) return r; } catch(e) {}
  return [...DEFAULT_RELAYS];
}
function saveRelays() { try { localStorage.setItem('gs_relays', JSON.stringify(relays)); } catch(e) {} }
function loadWatchlist() {
  try { const w = JSON.parse(localStorage.getItem('gs_watchlist')); if (Array.isArray(w)) return w; } catch(e) {}
  return [];
}
function saveWatchlist() {
  try { localStorage.setItem('gs_watchlist', JSON.stringify(watchlist)); } catch(e) {}
  updateWatchBadge();
}
function loadUnlocked() { try { return localStorage.getItem('gs_unlocked') === 'true'; } catch(e) { return false; } }
function saveUnlocked() { try { localStorage.setItem('gs_unlocked', 'true'); } catch(e) {} unlocked = true; }

// ══════════════════════════════════════════════
// BECH32 / NPUB
// ══════════════════════════════════════════════
function npubToHex(npub) {
  if (!npub.startsWith('npub1')) return null;
  try {
    const data = npub.slice(5).toLowerCase();
    let bits = 0, value = 0; const bytes = [];
    for (const c of data) {
      const idx = BECH32.indexOf(c);
      if (idx < 0) continue;
      value = (value << 5) | idx; bits += 5;
      if (bits >= 8) { bits -= 8; bytes.push((value >> bits) & 0xff); }
    }
    return bytes.slice(0, 32).map(b => b.toString(16).padStart(2, '0')).join('');
  } catch(e) { return null; }
}
function shortHex(hex) { return hex ? hex.slice(0,8) + '...' + hex.slice(-6) : ''; }
function resolveHex(input) {
  input = input.trim();
  if (input.startsWith('npub1')) return npubToHex(input);
  if (/^[0-9a-f]{64}$/i.test(input)) return input.toLowerCase();
  return null;
}
function esc(s) { return String(s||'').replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;'); }

// ══════════════════════════════════════════════
// RELAY ENGINE
// ══════════════════════════════════════════════
const profileCache = {};

function closeAllSockets() { openSockets.forEach(ws => { try { ws.close(); } catch(e){} }); openSockets = []; }

function queryRelay(url, filters, onEvent, timeoutMs = 8000) {
  return new Promise(resolve => {
    let done = false, ws;
    const subId = 'gs_' + Math.random().toString(36).slice(2,9);
    const events = [];
    const finish = () => {
      if (done) return; done = true;
      try { ws.send(JSON.stringify(['CLOSE', subId])); } catch(e) {}
      resolve(events);
    };
    const timer = setTimeout(finish, timeoutMs);
    try { ws = new WebSocket(url); openSockets.push(ws); } catch(e) { resolve([]); return; }
    ws.onopen = () => ws.send(JSON.stringify(['REQ', subId, ...filters]));
    ws.onmessage = msg => {
      try {
        const d = JSON.parse(msg.data);
        if (d[0]==='EVENT' && d[1]===subId) { events.push(d[2]); if (onEvent) onEvent(d[2]); }
        else if (d[0]==='EOSE') { clearTimeout(timer); finish(); }
      } catch(e) {}
    };
    ws.onerror = () => { clearTimeout(timer); finish(); };
    ws.onclose = () => { clearTimeout(timer); finish(); };
  });
}

async function queryAll(filters, onEvent, timeoutMs=8000) {
  const results = await Promise.allSettled(relays.slice(0,4).map(r => queryRelay(r, filters, onEvent, timeoutMs)));
  const all = []; const seen = new Set();
  results.forEach(r => { if (r.status==='fulfilled') r.value.forEach(e => { if (!seen.has(e.id)) { seen.add(e.id); all.push(e); } }); });
  return all;
}

async function fetchProfiles(pubkeys) {
  const missing = pubkeys.filter(p => !profileCache[p]);
  if (!missing.length) return;
  const events = await queryAll([{ kinds:[0], authors:missing, limit:missing.length }], null, 6000);
  events.forEach(e => {
    if (!profileCache[e.pubkey] || (profileCache[e.pubkey]?.created_at||0) < e.created_at) {
      try { profileCache[e.pubkey] = { ...JSON.parse(e.content), created_at: e.created_at }; } catch(err) {}
    }
  });
}

function displayName(pk) { const p = profileCache[pk]; return p?.display_name || p?.name || shortHex(pk); }
function avatarUrl(pk) { return profileCache[pk]?.picture || null; }
function bio(pk) { return profileCache[pk]?.about || ''; }

// ══════════════════════════════════════════════
// RELAY STATUS
// ══════════════════════════════════════════════
async function initRelayStatus() {
  document.getElementById('relay-status').textContent = 'CONNECTING...';
  renderRelayList();
  let live = 0;
  await Promise.all(relays.map(url => new Promise(res => {
    try {
      const ws = new WebSocket(url); const t = setTimeout(() => { try{ws.close()}catch(e){} res(); }, 3000);
      ws.onopen = () => { clearTimeout(t); live++; connectedRelays = live; document.getElementById('relay-status').textContent = live+'/'+relays.length+' LIVE'; ws.close(); res(); };
      ws.onerror = () => { clearTimeout(t); res(); };
    } catch(e) { res(); }
  })));
  document.getElementById('relay-status').textContent = live+'/'+relays.length+' RELAYS LIVE';
  renderRelayList();
}

// ══════════════════════════════════════════════
// NIP-07
// ══════════════════════════════════════════════
async function connectNIP07() {
  if (!window.nostr) { alert('No Nostr extension found. Install Alby or nos2x, or paste your npub.'); return; }
  try {
    const pk = await window.nostr.getPublicKey();
    document.getElementById('npub-input').value = pk;
    analyzeProfile();
  } catch(e) { alert('Extension declined access.'); }
}

// ══════════════════════════════════════════════
// MAIN ANALYSIS
// ══════════════════════════════════════════════
async function analyzeProfile() {
  const input = document.getElementById('npub-input').value.trim();
  if (!input) return;
  const hex = resolveHex(input);
  if (!hex) { alert('Invalid npub or pubkey.'); return; }

  closeAllSockets();
  const btn = document.getElementById('analyze-btn');
  btn.disabled = true; btn.textContent = '...';

  document.getElementById('empty-state').style.display = 'none';
  document.getElementById('load-bar').classList.remove('hidden');
  document.getElementById('view-tabs').style.display = 'none';
  document.getElementById('view-graph').style.display = 'none';

  setStatus('Fetching follows...');

  try {
    // Kind 3 — contact list
    const contactEvts = await queryAll([{ kinds:[3], authors:[hex], limit:1 }], null, 7000);
    contactEvts.sort((a,b) => b.created_at - a.created_at);
    const ce = contactEvts[0];
    let follows = ce ? ce.tags.filter(t=>t[0]==='p').map(t=>t[1]).filter(p=>/^[0-9a-f]{64}$/i.test(p)).slice(0,60) : [];
    const followSet = new Set(follows);

    setStatus('Loading profiles...');
    await fetchProfiles([hex, ...follows.slice(0,40)]);

    setStatus('Analyzing zap flows...');
    const zapEvts = await queryAll([{ kinds:[9735], '#p':follows.slice(0,30), limit:200 }], null, 7000);
    const zapCount = {}; const zapSats = {};
    zapEvts.forEach(e => {
      const pt = e.tags.find(t=>t[0]==='p');
      if (pt) {
        zapCount[pt[1]] = (zapCount[pt[1]]||0) + 1;
        const b11 = (e.tags.find(t=>t[0]==='bolt11')||[])[1];
        if (b11) zapSats[pt[1]] = (zapSats[pt[1]]||0) + parseBolt11(b11);
      }
    });

    setStatus('Detecting niches...');
    const noteEvts = await queryAll([{ kinds:[1], authors:follows.slice(0,25), limit:150, since:Math.floor(Date.now()/1000)-7*86400 }], null, 7000);
    const tagCount = {};
    noteEvts.forEach(e => e.tags.filter(t=>t[0]==='t').forEach(t => {
      const tag = t[1].toLowerCase().trim();
      if (tag.length>2 && tag.length<30) tagCount[tag] = (tagCount[tag]||0)+1;
    }));

    setStatus('Mapping 2nd degree...');
    const sdEvts = await queryAll([{ kinds:[3], authors:follows.slice(0,15), limit:30 }], null, 7000);
    const sdMap = {}; const sdSet = new Set();
    sdEvts.forEach(e => {
      if (!followSet.has(e.pubkey)) return;
      e.tags.filter(t=>t[0]==='p').slice(0,10).forEach(t => {
        const pk = t[1];
        if (pk!==hex && !followSet.has(pk) && /^[0-9a-f]{64}$/.test(pk)) {
          sdSet.add(pk);
          if (!sdMap[pk]) sdMap[pk]=[];
          sdMap[pk].push(e.pubkey);
        }
      });
    });
    const sdPubkeys = [...sdSet].slice(0,30);
    await fetchProfiles(sdPubkeys.slice(0,20));

    setStatus('Loading activity...');
    const actZaps = await queryAll([{ kinds:[9735], '#p':follows.slice(0,20), limit:30, since:Math.floor(Date.now()/1000)-3*3600 }], null, 5000);
    const actReposts = await queryAll([{ kinds:[6,7], authors:follows.slice(0,20), limit:20, since:Math.floor(Date.now()/1000)-3*3600 }], null, 5000);

    // Build graph data
    const nodes=[], links=[];
    nodes.push({ id:'user', pubkey:hex, label:displayName(hex), picture:avatarUrl(hex), type:'user', zapScore:zapCount[hex]||0, degree:0 });
    follows.slice(0,40).forEach(pk => {
      const zs = zapCount[pk]||0;
      nodes.push({ id:pk, pubkey:pk, label:displayName(pk), picture:avatarUrl(pk), type:zs>3?'zapper':'follow', zapScore:zs, zapSats:zapSats[pk]||0, degree:1 });
      links.push({ source:'user', target:pk, strength:0.4+Math.min(zs*.05,.5) });
    });
    sdPubkeys.slice(0,25).forEach(pk => {
      const parents = sdMap[pk]||[];
      nodes.push({ id:pk, pubkey:pk, label:displayName(pk), picture:avatarUrl(pk), type:'second', zapScore:zapCount[pk]||0, degree:2, mutualCount:parents.length });
      const parent = parents.find(p=>followSet.has(p));
      if (parent && follows.includes(parent)) links.push({ source:parent, target:pk, strength:0.2 });
    });

    const nicheColors = ['#f7931a','#00ff9d','#00c8ff','#ff6b35','#9b59b6','#e74c3c'];
    const topTags = Object.entries(tagCount).sort((a,b)=>b[1]-a[1]).slice(0,6);
    const niches = topTags.map(([tag,count],i) => ({
      name: tag.charAt(0).toUpperCase()+tag.slice(1), tag, color:nicheColors[i%nicheColors.length],
      count, zap:Math.round(count*(zapEvts.length/Math.max(noteEvts.length,1))*1000),
      pct: count/Math.max(...Object.values(tagCount),1)
    }));

    const recs = sdPubkeys
      .map(pk=>({ pubkey:pk, name:displayName(pk), picture:avatarUrl(pk), zapScore:zapCount[pk]||0, mutual:(sdMap[pk]||[]).length, niche:topTags[0]?topTags[0][0]:'nostr' }))
      .sort((a,b)=>(b.mutual*3+b.zapScore)-(a.mutual*3+a.zapScore))
      .map((r,i)=>({...r, locked:!unlocked && i>=5}))
      .slice(0,12);

    const activity=[];
    actZaps.slice(0,12).forEach(e => {
      const pt=e.tags.find(t=>t[0]==='p'); if(!pt) return;
      const sats=parseBolt11((e.tags.find(t=>t[0]==='bolt11')||[])[1]||'');
      activity.push({ actor:displayName(e.pubkey), action:'zapped', target:displayName(pt[1]), sats:sats||21, minsAgo:Math.round((Date.now()/1000-e.created_at)/60) });
    });
    actReposts.slice(0,8).forEach(e => {
      const pt=e.tags.find(t=>t[0]==='p');
      activity.push({ actor:displayName(e.pubkey), action:e.kind===6?'boosted':'reacted to', target:pt?displayName(pt[1]):'a note', sats:null, minsAgo:Math.round((Date.now()/1000-e.created_at)/60) });
    });
    activity.sort((a,b)=>a.minsAgo-b.minsAgo);

    graphData = { hex, nodes, links, niches, recs, activity, followCount:follows.length, reach:follows.length*12, zapScore:Object.values(zapCount).reduce((a,b)=>a+b,0) };

    // Render
    document.getElementById('load-bar').classList.add('hidden');
    document.getElementById('metrics-section').style.display = 'block';
    document.getElementById('rec-head').style.display = 'block';
    document.getElementById('view-tabs').style.display = 'flex';
    switchView('graph');

    animateNum('m-following', graphData.followCount);
    animateNum('m-reach', graphData.reach);
    animateNum('m-zapscore', graphData.zapScore);
    animateNum('m-niches', graphData.niches.length);
    document.getElementById('m-relay-sub').textContent = `across ${connectedRelays} relays`;

    renderRecs(graphData.recs);
    renderGraph(graphData);
    renderNiches(graphData.niches);
    renderActivity(graphData.activity);

    // Populate share card
    document.getElementById('sc-name').textContent = displayName(hex);
    document.getElementById('sc-npub').textContent = shortHex(hex);
    document.getElementById('sc-following').textContent = graphData.followCount;
    document.getElementById('sc-reach').textContent = graphData.reach;
    document.getElementById('sc-zap').textContent = graphData.zapScore;
    document.getElementById('sc-niches').textContent = graphData.niches.length;
    document.getElementById('sc-date').textContent = new Date().toLocaleDateString();

  } catch(err) {
    console.error(err);
    document.getElementById('load-bar').classList.add('hidden');
    document.getElementById('empty-state').style.display = 'flex';
  }

  btn.disabled = false; btn.textContent = 'MAP';
}

function setStatus(msg) { document.getElementById('analyze-btn').textContent = msg.slice(0,8); }
function parseBolt11(b) { if(!b) return 0; try { const m=b.toLowerCase().match(/^lnbc(\d+)([munp])/); if(!m) return 0; return Math.round(parseInt(m[1])*({m:100000,u:100,n:.1,p:.0001}[m[2]]||1)); } catch(e){return 0;} }

// ══════════════════════════════════════════════
// GRAPH RENDERER
// ══════════════════════════════════════════════
function renderGraph(data) {
  const container = document.getElementById('view-graph');
  const svg = d3.select('#graph-svg');
  svg.selectAll('*').remove();
  if (simulation) { simulation.stop(); simulation = null; }

  const W = container.clientWidth || 600;
  const H = container.clientHeight || 400;
  const g = svg.append('g');

  svgZoom = d3.zoom().scaleExtent([.2,4]).on('zoom', e => g.attr('transform', e.transform));
  svg.call(svgZoom);

  const nodeColor = t => ({ user:'#00ff9d', zapper:'#f7931a', follow:'#00c8ff', second:'#2a3f55' })[t]||'#2a3f55';
  const nodeR = d => ({ user:16, zapper:9, follow:6, second:4 })[d.type]||4;

  const defs = svg.append('defs');
  const fl = defs.append('filter').attr('id','glow');
  fl.append('feGaussianBlur').attr('stdDeviation','3').attr('result','blur');
  const fm = fl.append('feMerge');
  fm.append('feMergeNode').attr('in','blur');
  fm.append('feMergeNode').attr('in','SourceGraphic');

  const link = g.append('g').selectAll('line').data(data.links).enter().append('line')
    .attr('stroke','#1e2d3d').attr('stroke-width', d => d.strength*2);

  const node = g.append('g').selectAll('g').data(data.nodes).enter().append('g')
    .style('cursor','pointer')
    .call(d3.drag().on('start',dragS).on('drag',dragD).on('end',dragE));

  node.append('circle')
    .attr('r', nodeR)
    .attr('fill', d => nodeColor(d.type))
    .attr('fill-opacity', d => d.type==='second'?.4:.9)
    .attr('stroke', d => d.type==='user'?'#00ff9d':'none')
    .attr('stroke-width', 2)
    .attr('filter', d => d.type!=='second'?'url(#glow)':'none');

  node.filter(d => d.type!=='second').append('text')
    .text(d => (d.label||'').split(' ')[0])
    .attr('dy', d => nodeR(d)+11)
    .attr('text-anchor','middle')
    .attr('font-size', d => d.type==='user'?'11px':'9px')
    .attr('font-family','Space Mono,monospace')
    .attr('fill', d => d.type==='user'?'#00ff9d':'#5a7a9a');

  node.on('click', (event, d) => { event.stopPropagation(); openProfilePanel(d); })
    .on('mouseover', (event, d) => {
      const tt = document.getElementById('tooltip');
      document.getElementById('tt-name').textContent = d.label||'Unknown';
      document.getElementById('tt-zap').textContent = d.zapScore||0;
      document.getElementById('tt-deg').textContent = d.type==='user'?'You':d.degree===1?'1st degree':'2nd degree';
      tt.style.display='block';
    })
    .on('mousemove', event => {
      const tt = document.getElementById('tooltip');
      tt.style.left=(event.clientX+14)+'px'; tt.style.top=(event.clientY-10)+'px';
    })
    .on('mouseout', () => { document.getElementById('tooltip').style.display='none'; });

  simulation = d3.forceSimulation(data.nodes)
    .force('link', d3.forceLink(data.links).id(d=>d.id).distance(80))
    .force('charge', d3.forceManyBody().strength(-180))
    .force('center', d3.forceCenter(W/2, H/2))
    .force('collision', d3.forceCollide().radius(d=>nodeR(d)+6))
    .on('tick', () => {
      link.attr('x1',d=>d.source.x).attr('y1',d=>d.source.y).attr('x2',d=>d.target.x).attr('y2',d=>d.target.y);
      node.attr('transform', d=>`translate(${d.x},${d.y})`);
    });

  svg.on('click', () => closeProfilePanel());

  function dragS(event,d) { if(!event.active) simulation.alphaTarget(.3).restart(); d.fx=d.x; d.fy=d.y; }
  function dragD(event,d) { d.fx=event.x; d.fy=event.y; }
  function dragE(event,d) { if(!event.active) simulation.alphaTarget(0); d.fx=null; d.fy=null; }
}

function zoomIn() { d3.select('#graph-svg').transition().call(svgZoom.scaleBy,1.4); }
function zoomOut() { d3.select('#graph-svg').transition().call(svgZoom.scaleBy,.7); }
function resetZoom() { d3.select('#graph-svg').transition().call(svgZoom.transform,d3.zoomIdentity); }

// ══════════════════════════════════════════════
// PROFILE PANEL
// ══════════════════════════════════════════════
async function openProfilePanel(d) {
  if (d.type === 'user') return;
  openProfilePubkey = d.pubkey;

  const panel = document.getElementById('profile-panel');
  const av = document.getElementById('pp-avatar');
  const pic = d.picture||avatarUrl(d.pubkey);

  document.getElementById('pp-name').textContent = d.label||shortHex(d.pubkey);
  document.getElementById('pp-npub').textContent = shortHex(d.pubkey);
  document.getElementById('pp-zaps').textContent = d.zapScore||0;
  document.getElementById('pp-follows').textContent = '—';
  document.getElementById('pp-degree').textContent = d.degree===1?'1st':'2nd';
  document.getElementById('pp-bio').textContent = bio(d.pubkey)||'No bio available.';
  document.getElementById('pp-notes').innerHTML = '<div class="pp-loading">Loading notes...</div>';

  if (pic) {
    av.innerHTML = `<img src="${pic}" onerror="this.parentElement.textContent='👤'">`;
  } else { av.textContent = '👤'; }

  // Update watch button
  const isWatching = watchlist.some(w=>w.pubkey===d.pubkey);
  const wb = document.getElementById('pp-watch-btn');
  wb.textContent = isWatching ? '👁 Watching' : '👁 Watch';
  wb.classList.toggle('watching', isWatching);

  panel.classList.add('open');

  // Fetch recent notes
  const notes = await queryAll([{ kinds:[1], authors:[d.pubkey], limit:10, since:Math.floor(Date.now()/1000)-7*86400 }], null, 5000);
  notes.sort((a,b)=>b.created_at-a.created_at);

  const notesEl = document.getElementById('pp-notes');
  if (!notes.length) { notesEl.innerHTML='<div class="pp-loading">No recent notes found.</div>'; return; }
  notesEl.innerHTML = notes.slice(0,8).map(n => `
    <div class="pp-note">
      <div class="pp-note-time">${timeAgo(n.created_at)}</div>
      <div class="pp-note-text">${esc(n.content).slice(0,280)}${n.content.length>280?'…':''}</div>
    </div>
  `).join('');
}

function closeProfilePanel() {
  document.getElementById('profile-panel').classList.remove('open');
  openProfilePubkey = null;
}

async function followProfile() {
  if (!openProfilePubkey) return;
  if (!window.nostr) { alert('Connect your Nostr extension to follow.'); return; }
  try {
    // Get current follows
    const pk = await window.nostr.getPublicKey();
    const evts = await queryAll([{ kinds:[3], authors:[pk], limit:1 }], null, 5000);
    evts.sort((a,b)=>b.created_at-a.created_at);
    const currentTags = evts[0]?.tags || [];
    const alreadyFollowing = currentTags.some(t=>t[0]==='p' && t[1]===openProfilePubkey);
    if (alreadyFollowing) { alert('Already following this person.'); return; }

    const newTags = [...currentTags, ['p', openProfilePubkey]];
    const event = { kind:3, created_at:Math.floor(Date.now()/1000), tags:newTags, content:evts[0]?.content||'' };
    const signed = await window.nostr.signEvent(event);

    // Broadcast to relays
    relays.slice(0,3).forEach(url => {
      try {
        const ws = new WebSocket(url);
        ws.onopen = () => { ws.send(JSON.stringify(['EVENT', signed])); setTimeout(()=>ws.close(),2000); };
      } catch(e) {}
    });

    const btn = document.getElementById('pp-follow-btn');
    btn.textContent = '✓ Following'; btn.style.background = '#1a3a2a'; btn.style.color = 'var(--accent)';
  } catch(e) { alert('Failed to follow: '+e.message); }
}

function toggleWatch() {
  if (!openProfilePubkey) return;
  const idx = watchlist.findIndex(w=>w.pubkey===openProfilePubkey);
  if (idx >= 0) {
    watchlist.splice(idx,1);
  } else {
    watchlist.push({ pubkey:openProfilePubkey, name:displayName(openProfilePubkey), picture:avatarUrl(openProfilePubkey), added:Date.now() });
  }
  saveWatchlist();
  renderWatchlist();
  const isNow = watchlist.some(w=>w.pubkey===openProfilePubkey);
  const wb = document.getElementById('pp-watch-btn');
  wb.textContent = isNow ? '👁 Watching' : '👁 Watch';
  wb.classList.toggle('watching', isNow);
}

// ══════════════════════════════════════════════
// WATCHLIST
// ══════════════════════════════════════════════
function renderWatchlist() {
  const list = document.getElementById('watch-list');
  const empty = document.getElementById('watch-empty');
  updateWatchBadge();

  if (!watchlist.length) { list.innerHTML=''; empty.style.display='block'; return; }
  empty.style.display='none';

  list.innerHTML = watchlist.map((w,i) => `
    <div class="watch-item" onclick="loadWatchedProfile('${w.pubkey}')">
      <div class="rec-avatar">${w.picture?`<img src="${w.picture}" onerror="this.parentElement.textContent='👤'">`:' 👤'}</div>
      <div class="watch-info">
        <div class="watch-name">${esc(w.name)}</div>
        <div class="watch-npub">${shortHex(w.pubkey)}</div>
      </div>
      <button class="watch-remove" onclick="event.stopPropagation();removeWatch(${i})">✕</button>
    </div>
  `).join('');
}

function removeWatch(idx) { watchlist.splice(idx,1); saveWatchlist(); renderWatchlist(); }

function updateWatchBadge() {
  const badge = document.getElementById('watch-count');
  if (watchlist.length > 0) { badge.style.display='flex'; badge.textContent=watchlist.length; }
  else { badge.style.display='none'; }
}

function promptAddWatch() {
  const input = prompt('Enter npub or hex pubkey to watch:');
  if (!input) return;
  const hex = resolveHex(input.trim());
  if (!hex) { alert('Invalid npub or pubkey.'); return; }
  if (watchlist.some(w=>w.pubkey===hex)) { alert('Already watching this profile.'); return; }
  watchlist.push({ pubkey:hex, name:shortHex(hex), picture:null, added:Date.now() });
  saveWatchlist();
  fetchProfiles([hex]).then(() => {
    const idx = watchlist.findIndex(w=>w.pubkey===hex);
    if (idx>=0) { watchlist[idx].name=displayName(hex); watchlist[idx].picture=avatarUrl(hex)||null; }
    saveWatchlist(); renderWatchlist();
  });
  renderWatchlist();
}

function loadWatchedProfile(pubkey) {
  document.getElementById('npub-input').value = pubkey;
  analyzeProfile();
  closeMobileSidebar();
}

// ══════════════════════════════════════════════
// RELAY MANAGER
// ══════════════════════════════════════════════
function renderRelayList() {
  const list = document.getElementById('relay-list');
  list.innerHTML = relays.map((r,i) => `
    <div class="relay-item">
      <div class="relay-dot" id="rdot-${i}"></div>
      <div class="relay-url">${r.replace('wss://','')}</div>
      <button class="relay-remove" onclick="removeRelay(${i})">✕</button>
    </div>
  `).join('');
  // Ping each
  relays.forEach((r,i) => pingRelay(r,i));
}

async function pingRelay(url, idx) {
  const dot = document.getElementById('rdot-'+idx);
  if (!dot) return;
  try {
    const ws = new WebSocket(url);
    const t = setTimeout(() => { dot.className='relay-dot dead'; ws.close(); }, 3000);
    ws.onopen = () => { clearTimeout(t); dot.className='relay-dot live'; ws.close(); };
    ws.onerror = () => { clearTimeout(t); dot.className='relay-dot dead'; };
  } catch(e) { if(dot) dot.className='relay-dot dead'; }
}

function addRelay() {
  const input = document.getElementById('relay-input');
  let url = input.value.trim();
  if (!url) return;
  if (!url.startsWith('wss://')) url = 'wss://' + url;
  if (relays.includes(url)) { alert('Already added.'); return; }
  relays.push(url); saveRelays(); input.value=''; renderRelayList();
}

function removeRelay(idx) {
  if (relays.length <= 1) { alert('Need at least one relay.'); return; }
  relays.splice(idx,1); saveRelays(); renderRelayList();
}

// ══════════════════════════════════════════════
// RECOMMENDATIONS
// ══════════════════════════════════════════════
function renderRecs(recs) {
  const list = document.getElementById('rec-list');
  const emojis = ['⚡','🔑','🟠','🌊','🔗','🏔','⛓','🌐','💡','🗡','🛡','🔭'];
  list.innerHTML = recs.map((r,i) => {
    const av = r.picture ? `<img src="${esc(r.picture)}" onerror="this.parentElement.textContent='${emojis[i%emojis.length]}'">` : emojis[i%emojis.length];
    return `<div class="rec-item${r.locked?' locked':''}" onclick="${r.locked?'openZapGate()':'openRecProfile(\''+r.pubkey+'\')'}">
      <div class="rec-avatar">${av}</div>
      <div class="rec-info">
        <div class="rec-name">${esc(r.name)}</div>
        <div class="rec-meta">${r.mutual} mutual follows · #${esc(r.niche)}</div>
      </div>
      <div class="rec-score">${r.locked?'<span style="color:var(--zap)">⚡</span>':(r.zapScore||'—')}</div>
    </div>`;
  }).join('');
  document.getElementById('zap-gate').style.display = (recs.some(r=>r.locked)) ? 'block' : 'none';
}

function openRecProfile(pubkey) {
  const node = graphData?.nodes.find(n=>n.pubkey===pubkey);
  if (node) openProfilePanel(node);
}

// ══════════════════════════════════════════════
// NICHES
// ══════════════════════════════════════════════
function renderNiches(niches) {
  const grid = document.getElementById('niche-grid');
  grid.innerHTML = niches.map(n => `
    <div class="niche-card" style="--nc:${n.color}">
      <div class="niche-name">#${esc(n.tag)}</div>
      <div class="niche-tag">${esc(n.name)}</div>
      <div class="niche-stats">
        <div><div class="ns-val">${n.count}</div><div class="ns-lbl">Active</div></div>
        <div><div class="ns-val">${(n.zap/1000).toFixed(1)}k</div><div class="ns-lbl">Sats/wk</div></div>
      </div>
      <div class="niche-bar"><div class="niche-bar-fill" data-pct="${Math.round(n.pct*100)}"></div></div>
    </div>
  `).join('');
  setTimeout(() => {
    document.querySelectorAll('.niche-bar-fill').forEach(el => { el.style.width = el.dataset.pct+'%'; });
  }, 100);
}

// ══════════════════════════════════════════════
// ACTIVITY
// ══════════════════════════════════════════════
function renderActivity(activity) {
  const list = document.getElementById('activity-list');
  list.innerHTML = activity.map((item,i) => `
    <div class="act-item" style="animation-delay:${i*.04}s">
      <div class="act-time">${timeAgo2(item.minsAgo)}</div>
      <div class="act-content"><span class="act-actor">${esc(item.actor)}</span> ${item.action} <span class="act-actor">${esc(item.target)}</span></div>
      ${item.sats?`<div class="act-zap">+${item.sats} sats</div>`:'<div></div>'}
    </div>
  `).join('');
}

// ══════════════════════════════════════════════
// SHARE
// ══════════════════════════════════════════════
function openShareModal() {
  if (!graphData) { alert('Map a profile first.'); return; }
  openModal('share-modal');
  document.getElementById('share-status').textContent='';
}

async function shareToNostr() {
  if (!window.nostr) { alert('Connect your Nostr extension to post.'); return; }
  const name = displayName(graphData.hex);
  const text = `📊 My Nostr Graph via GRAPHSTR\n\n` +
    `Following: ${graphData.followCount}\n` +
    `Network reach: ${graphData.reach}\n` +
    `Zap weight: ${graphData.zapScore}\n` +
    `Active niches: ${graphData.niches.map(n=>'#'+n.tag).join(' ')}\n\n` +
    `Map your graph → graphstr.app`;
  try {
    const event = { kind:1, created_at:Math.floor(Date.now()/1000), tags:[], content:text };
    const signed = await window.nostr.signEvent(event);
    relays.slice(0,3).forEach(url => {
      try { const ws=new WebSocket(url); ws.onopen=()=>{ws.send(JSON.stringify(['EVENT',signed]));setTimeout(()=>ws.close(),2000);}; } catch(e){}
    });
    document.getElementById('share-status').textContent='✓ Posted to Nostr!';
    document.getElementById('share-status').style.color='var(--accent)';
  } catch(e) { document.getElementById('share-status').textContent='Failed: '+e.message; document.getElementById('share-status').style.color='var(--danger)'; }
}

function copyShareText() {
  if (!graphData) return;
  const text = `📊 My Nostr Graph via GRAPHSTR\n\nFollowing: ${graphData.followCount} | Reach: ${graphData.reach} | Zap weight: ${graphData.zapScore}\nNiches: ${graphData.niches.map(n=>'#'+n.tag).join(' ')}\n\ngraphstr.app`;
  navigator.clipboard.writeText(text).then(() => {
    document.getElementById('share-status').textContent='✓ Copied to clipboard!';
    document.getElementById('share-status').style.color='var(--accent)';
  });
}

// ══════════════════════════════════════════════
// ZAP GATE
// ══════════════════════════════════════════════
function openZapGate() {
  if (unlocked) { doUnlock(); return; }
  openModal('zap-modal'); zgStep('choose');
}

function zgStep(name) {
  ['choose','pay','success'].forEach(s => {
    const el=document.getElementById('zgs-'+s);
    if(el) el.classList.toggle('active', s===name);
  });
  const steps=['choose','pay','success'];
  const idx=steps.indexOf(name);
  steps.forEach((s,i) => {
    const d=document.getElementById('zgd'+(i+1));
    if(d) d.className='zg-dot'+(i<idx?' done':i===idx?' active':'');
  });
}

function selectPay(method) {
  selectedPayMethod=method;
  document.getElementById('opt-nwc').classList.toggle('sel', method==='nwc');
  document.getElementById('opt-inv').classList.toggle('sel', method==='invoice');
  document.getElementById('nwc-section').style.display = method==='nwc'?'block':'none';
  document.getElementById('btn-gen-inv').style.display = method==='invoice'?'block':'none';
}

async function doInvoicePay() {
  zgStep('pay');
  document.getElementById('inv-display').style.display='block';
  document.getElementById('nwc-paying').style.display='none';
  setPS('pending','Generating invoice...');
  try {
    const [user,domain]=LN_ADDRESS.split('@');
    const lnurl=await(await fetch(`https://${domain}/.well-known/lnurlp/${user}`)).json();
    if(lnurl.status==='ERROR') throw new Error(lnurl.reason);
    const inv=await(await fetch(`${lnurl.callback}?amount=${ZAP_MSATS}`)).json();
    if(inv.status==='ERROR') throw new Error(inv.reason);
    currentInvoice=inv.pr;
    document.getElementById('inv-text').textContent=currentInvoice;
    renderQR(currentInvoice);
    setPS('pending','Waiting for payment');
    startPoll();
  } catch(err) {
    setPS('err','Could not auto-generate. Send '+ZAP_SATS+' sats to: '+LN_ADDRESS);
    document.getElementById('inv-text').textContent='Send '+ZAP_SATS+' sats to:\n'+LN_ADDRESS;
    addManualBtn();
  }
}

async function doNWCPay() {
  const str=document.getElementById('nwc-str').value.trim();
  if(!str.startsWith('nostr+walletconnect://')) { alert('Invalid NWC string.'); return; }
  zgStep('pay');
  document.getElementById('inv-display').style.display='none';
  document.getElementById('nwc-paying').style.display='block';
  setNS('pending','Connecting...');
  try {
    const parsed=parseNWC(str); if(!parsed) throw new Error('Cannot parse NWC URI');
    setNS('pending','Generating invoice...');
    const [user,domain]=LN_ADDRESS.split('@');
    const lnurl=await(await fetch(`https://${domain}/.well-known/lnurlp/${user}`)).json();
    const inv=await(await fetch(`${lnurl.callback}?amount=${ZAP_MSATS}`)).json();
    const invoice=inv.pr;
    setNS('pending','Sending to wallet...');
    await sendNWC(parsed,invoice);
  } catch(err) { setNS('err',err.message||'NWC failed'); }
}

function parseNWC(uri) {
  try {
    const s=uri.replace('nostr+walletconnect://','');
    const [pk,qs]=s.split('?'); const p=new URLSearchParams(qs);
    return { walletPubkey:pk, relay:p.get('relay'), secret:p.get('secret') };
  } catch(e){return null;}
}

async function sendNWC(np,invoice) {
  if(!window.nostr?.nip04) throw new Error('NIP-07 extension with nip04 required');
  const enc=await window.nostr.nip04.encrypt(np.walletPubkey,JSON.stringify({method:'pay_invoice',params:{invoice}}));
  const event={ kind:23194, created_at:Math.floor(Date.now()/1000), tags:[['p',np.walletPubkey]], content:enc, pubkey:await window.nostr.getPublicKey() };
  const signed=await window.nostr.signEvent(event);
  return new Promise((res,rej) => {
    const ws=new WebSocket(np.relay); nwcWs=ws;
    const t=setTimeout(()=>rej(new Error('NWC timeout')),30000);
    ws.onopen=()=>ws.send(JSON.stringify(['EVENT',signed]));
    ws.onmessage=msg=>{
      try {
        const d=JSON.parse(msg.data);
        if(d[0]==='OK') { setNS('pending','Processing...'); const sid='nwc_'+Math.random().toString(36).slice(2,8); ws.send(JSON.stringify(['REQ',sid,{kinds:[23195],authors:[np.walletPubkey],'#e':[signed.id],limit:1}])); }
        else if(d[0]==='EVENT' && d[2]?.kind===23195) { clearTimeout(t); ws.close(); res(d[2]); onPaid(); }
      } catch(e){}
    };
    ws.onerror=()=>{clearTimeout(t);rej(new Error('WebSocket error'));};
  });
}

function startPoll() {
  if(pollInterval) clearInterval(pollInterval);
  let n=0;
  pollInterval=setInterval(()=>{ n++; if(n>60){clearInterval(pollInterval);setPS('err','Timeout');} if(n===5)addManualBtn(); },2000);
}

function addManualBtn() {
  if(document.getElementById('manual-btn')) return;
  const b=document.createElement('button');
  b.id='manual-btn'; b.className='btn-full btn-full-ghost'; b.style.marginTop='12px';
  b.textContent='✓ I sent the payment'; b.onclick=onPaid;
  document.getElementById('inv-display').appendChild(b);
}

function onPaid() {
  if(pollInterval){clearInterval(pollInterval);pollInterval=null;}
  saveUnlocked(); zgStep('success');
  setTimeout(doUnlock,400);
}

function doUnlock() {
  unlocked=true;
  document.querySelectorAll('.rec-item.locked').forEach(el=>el.classList.remove('locked'));
  document.getElementById('zap-gate').style.display='none';
  if(graphData) renderRecs(graphData.recs.map(r=>({...r,locked:false})));
}

function copyInvoice() {
  if(!currentInvoice) return;
  navigator.clipboard.writeText(currentInvoice).then(()=>{
    const b=document.querySelector('.btn-full-ghost');
    if(b){b.textContent='✓ Copied!';setTimeout(()=>b.textContent='📋 Copy Invoice',2000);}
  });
}

function renderQR(text) {
  const c=document.getElementById('qr-wrap'); c.innerHTML='';
  const img=document.createElement('img');
  img.width=160; img.height=160;
  img.style.cssText='border-radius:6px;background:#fff;padding:5px;';
  img.src='https://chart.googleapis.com/chart?cht=qr&chs=160x160&chl='+encodeURIComponent(text)+'&choe=UTF-8';
  img.onerror=()=>{c.innerHTML='<div style="color:var(--muted);font-size:10px;padding:16px">QR unavailable — copy invoice</div>';};
  c.appendChild(img);
}

function setPS(t,m){const e=document.getElementById('pay-status');if(!e)return;e.className='pay-status '+t;e.innerHTML=t==='pending'?'<span class="dots">'+m+'</span>':m;}
function setNS(t,m){const e=document.getElementById('nwc-status');if(!e)return;e.className='pay-status '+t;e.innerHTML=t==='pending'?'<span class="dots">'+m+'</span>':m;}

// ══════════════════════════════════════════════
// VIEW / TAB SWITCHING
// ══════════════════════════════════════════════
function switchView(name) {
  currentView=name;
  const views=['graph','niches','activity'];
  views.forEach(v => {
    const el=document.getElementById('view-'+v);
    if(el) el.style.display=v===name?'block':'none';
  });
  document.querySelectorAll('.vtab').forEach((t,i)=>t.classList.toggle('active',views[i]===name));
  document.querySelectorAll('.mnav-btn').forEach(b=>b.classList.remove('active'));
  const mb=document.getElementById('mnav-'+name);
  if(mb) mb.classList.add('active');
  if(name==='graph'&&graphData) setTimeout(()=>renderGraph(graphData),30);
}

function switchSideTab(name) {
  currentSideTab=name;
  ['graph','watch','relays'].forEach(t=>{
    const p=document.getElementById('spane-'+t);
    if(p) p.classList.toggle('active', t===name);
  });
  document.querySelectorAll('.stab').forEach((t,i)=>t.classList.toggle('active',['graph','watch','relays'][i]===name));
}

// ══════════════════════════════════════════════
// MOBILE NAV
// ══════════════════════════════════════════════
function mobileNav(name) {
  if(name==='graph'||name==='niches'||name==='activity') {
    closeMobileSidebar();
    if(graphData) switchView(name);
    document.querySelectorAll('.mnav-btn').forEach(b=>b.classList.remove('active'));
    document.getElementById('mnav-'+name)?.classList.add('active');
  }
}

function toggleMobileSidebar() {
  const sidebar=document.getElementById('sidebar');
  const overlay=document.getElementById('sidebar-overlay');
  const isOpen=sidebar.classList.contains('mobile-open');
  sidebar.classList.toggle('mobile-open',!isOpen);
  overlay.classList.toggle('show',!isOpen);
  document.getElementById('mnav-sidebar').classList.toggle('active',!isOpen);
}

function closeMobileSidebar() {
  document.getElementById('sidebar').classList.remove('mobile-open');
  document.getElementById('sidebar-overlay').classList.remove('show');
  document.getElementById('mnav-sidebar').classList.remove('active');
}

function openMobilePanel(pane) { switchSideTab(pane); toggleMobileSidebar(); }

function toggleDesktopSidebar() {
  const s=document.getElementById('sidebar');
  s.classList.toggle('hidden');
}

// ══════════════════════════════════════════════
// MODAL HELPERS
// ══════════════════════════════════════════════
function openModal(id) { document.getElementById(id).classList.add('open'); }
function closeModal(id) {
  document.getElementById(id).classList.remove('open');
  if(id==='zap-modal') { if(pollInterval){clearInterval(pollInterval);pollInterval=null;} if(nwcWs){try{nwcWs.close();}catch(e){} nwcWs=null;} }
}
document.querySelectorAll('.modal-overlay').forEach(m=>m.addEventListener('click',e=>{if(e.target===m)m.classList.remove('open');}));

// ══════════════════════════════════════════════
// UTILS
// ══════════════════════════════════════════════
function animateNum(id, target) {
  const el=document.getElementById(id); if(!el) return;
  let c=0; const step=target/28;
  const iv=setInterval(()=>{ c=Math.min(c+step,target); el.textContent=Math.floor(c).toLocaleString(); if(c>=target)clearInterval(iv); },25);
}
function timeAgo(ts) {
  const m=Math.round((Date.now()/1000-ts)/60);
  if(m<60) return m+'m ago'; if(m<1440) return Math.floor(m/60)+'h ago'; return Math.floor(m/1440)+'d ago';
}
function timeAgo2(minsAgo) { if(minsAgo<60) return minsAgo+'m ago'; return Math.floor(minsAgo/60)+'h ago'; }

// ── INIT
renderRelayList();
renderWatchlist();
updateWatchBadge();
initRelayStatus();

// Handle enter key in search
document.getElementById('npub-input').addEventListener('keydown', e => { if(e.key==='Enter') analyzeProfile(); });
document.getElementById('relay-input').addEventListener('keydown', e => { if(e.key==='Enter') addRelay(); });
</script>

</body>
</html>
