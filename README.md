<!doctype html>
<html lang="id">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>ClassCash XI V5 — Bubble Confirmation</title>
<style>
:root{--bg:#f4f6fa;--panel:#fff;--text:#172033;--muted:#6b7280;--line:#e6eaf0;--nav:#11162a;--nav2:#1a2140;--accent:#5b5ce2;--accent2:#7c3aed;--green:#15803d;--greenbg:#eaf7ee;--red:#b91c1c;--redbg:#fdecec;--orange:#c2410c;--orangebg:#fff0e7;--yellow:#b58100;--yellowbg:#fff7cf;--bluebg:#eef3f9;--shadow:0 14px 30px rgba(27,36,60,.07)}
*{box-sizing:border-box}html,body{margin:0;min-height:100%;font-family:Inter,Segoe UI,Arial,sans-serif;background:var(--bg);color:var(--text)}button,input,select{font:inherit}.app{min-height:100vh;display:flex}
.sidebar{position:fixed;inset:0 auto 0 0;width:250px;background:linear-gradient(180deg,var(--nav),#0d1222);color:#fff;padding:22px 15px;display:flex;flex-direction:column;z-index:10}.brand{display:flex;gap:12px;align-items:center;padding:8px 10px 28px}.logo{width:42px;height:42px;border-radius:13px;background:linear-gradient(135deg,#6366f1,#8b5cf6);display:grid;place-items:center;font-weight:900;box-shadow:0 10px 24px rgba(99,102,241,.25)}.brand h1{font-size:18px;margin:0}.brand small{font-size:11px;color:#a6adc0}.nav{display:grid;gap:6px}.nav button{border:0;background:transparent;color:#b7bfd2;text-align:left;padding:12px 13px;border-radius:11px;cursor:pointer}.nav button:hover,.nav button.active{background:#ffffff12;color:#fff}.side-note{margin-top:auto;padding:10px;color:#8e97ab;font-size:11px;line-height:1.55}
.main{margin-left:250px;flex:1;padding:24px;max-width:1700px;min-width:0}.topbar{display:flex;justify-content:space-between;align-items:flex-start;gap:16px;margin-bottom:18px}.topbar h2{margin:0;font-size:28px}.sub{font-size:12px;color:var(--muted);margin-top:4px}.actions{display:flex;gap:8px;flex-wrap:wrap}.btn{border:1px solid var(--line);background:var(--panel);color:var(--text);padding:10px 13px;border-radius:10px;cursor:pointer}.btn.primary{background:var(--accent);border-color:var(--accent);color:#fff}.btn:hover{filter:brightness(.985)}
.hero{display:flex;justify-content:space-between;align-items:center;gap:18px;padding:23px 24px;border-radius:20px;color:#fff;background:linear-gradient(135deg,#111a33,#2c3471 62%,#5b4db0);box-shadow:0 16px 34px rgba(44,52,113,.17);margin-bottom:16px}.hero h1{font-size:24px;margin:3px 0 6px}.hero p{margin:0;color:#dfe6ff;font-size:12px}.hero-pill{padding:10px 13px;border-radius:12px;background:#ffffff16;border:1px solid #ffffff2b;font-size:11px;font-weight:800;white-space:nowrap}
.cards{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:14px}.metric{position:relative;overflow:hidden}.metric:after{content:"";position:absolute;right:-28px;top:-28px;width:95px;height:95px;border-radius:50%;background:#5b5ce214}.metric-icon{width:34px;height:34px;border-radius:10px;display:grid;place-items:center;background:#eef0ff;color:var(--accent);font-weight:900}.metric-icon.green{background:var(--greenbg);color:var(--green)}.metric-icon.red{background:var(--redbg);color:var(--red)}.metric-title{font-size:11px;font-weight:800;color:var(--muted);letter-spacing:.4px;margin-top:10px}.metric-value{font-size:29px;font-weight:900;margin-top:5px}.card{background:var(--panel);border:1px solid var(--line);border-radius:16px;padding:18px;box-shadow:var(--shadow)}
.grid2{display:grid;grid-template-columns:1.55fr 1fr;gap:14px;margin-top:14px}.section-head{display:flex;justify-content:space-between;align-items:center;gap:12px;margin-bottom:13px}.section-head h3{margin:0;font-size:17px}.tiny{font-size:10px;color:var(--muted)}.table-scroll{overflow:auto;border:1px solid var(--line);border-radius:12px}.table{width:100%;border-collapse:separate;border-spacing:0;min-width:760px}.table th,.table td{padding:10px 9px;border-right:1px solid var(--line);border-bottom:1px solid var(--line);font-size:12px;vertical-align:top}.table th:last-child,.table td:last-child{border-right:0}.table tr:last-child td{border-bottom:0}.table th{background:#f8fafc;color:#566174;font-size:10px;letter-spacing:.2px;position:sticky;top:0;z-index:3}.matrix{min-width:1050px}.matrix .label-col{min-width:160px;text-align:left;font-weight:900;position:sticky;left:0;z-index:4;background:var(--panel)}.matrix th{text-align:center}.matrix td{text-align:center}.row-income td{background:var(--greenbg);font-weight:800}.row-expense td{background:var(--orangebg)}.row-net td{background:var(--yellowbg);font-weight:900}.neg{color:var(--red)}
.progress-row{display:grid;gap:6px;padding:10px 0;border-bottom:1px solid var(--line)}.progress-row:last-child{border-bottom:0}.progress-top{display:flex;justify-content:space-between;font-size:11px}.bar{height:8px;border-radius:999px;background:#eef1f6;overflow:hidden}.bar span{display:block;height:100%;border-radius:999px;background:linear-gradient(90deg,#6366f1,#8b5cf6)}
.search-row{display:flex;gap:9px;flex-wrap:wrap;margin-bottom:12px}.search-row input,.search-row select{padding:10px 11px;border:1px solid var(--line);border-radius:10px;background:var(--panel);color:var(--text)}.search-row input{flex:1;min-width:220px}.badge{display:inline-flex;align-items:center;justify-content:center;padding:5px 8px;border-radius:999px;font-size:10px;font-weight:800;white-space:nowrap}.paid{background:var(--greenbg);color:var(--green)}.unpaid{background:var(--redbg);color:var(--red)}.neutral{background:#eef0f4;color:#5b6473}
.payment-table{min-width:1600px}.payment-table th:first-child,.payment-table td:first-child{position:sticky;left:0;z-index:5;background:var(--panel)}.payment-table th:nth-child(2),.payment-table td:nth-child(2){position:sticky;left:44px;z-index:5;background:var(--panel);min-width:235px;text-align:left}.payment-cell{min-width:175px;display:flex;flex-direction:column;align-items:center;gap:6px}.payment-period{font-size:10px;color:var(--accent);font-weight:900}.day-list{display:flex;flex-wrap:wrap;justify-content:center;gap:3px;max-width:165px}.day{font-size:9px;padding:3px 5px;border-radius:5px;background:#f1f3ff;color:#4f46e5;border:1px solid #dfe2ff;font-weight:800}.pay-btn{border:0;background:transparent;padding:0;cursor:pointer}.pay-btn:disabled{cursor:default}.pay-ok,.pay-no{display:inline-flex;padding:5px 8px;border-radius:999px;font-size:10px;font-weight:900}.pay-ok{background:var(--greenbg);color:var(--green)}.pay-no{background:var(--redbg);color:var(--red)}
.expense-grid{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:10px}.expense-box{border:1px solid var(--line);border-radius:12px;padding:12px;background:var(--panel)}.expense-box h4{margin:0 0 6px;font-size:12px}.expense-total{font-size:15px;font-weight:900;color:var(--red);margin-bottom:8px}.expense-list{display:grid;gap:5px}.expense-list div{font-size:10px;color:var(--muted);padding-bottom:4px;border-bottom:1px dashed var(--line)}
.toast{position:fixed;right:20px;bottom:20px;background:#111827;color:#fff;padding:11px 14px;border-radius:10px;opacity:0;transform:translateY(8px);transition:.25s;z-index:50}.toast.show{opacity:1;transform:none}.modal{position:fixed;inset:0;background:#0008;display:none;align-items:center;justify-content:center;padding:18px;z-index:30}.modal.show{display:flex}.modal-box{width:min(430px,100%);background:var(--panel);color:var(--text);padding:20px;border-radius:16px;box-shadow:0 25px 70px rgba(0,0,0,.2)}.close{float:right;border:0;background:#eef1f6;border-radius:9px;width:32px;height:32px;cursor:pointer}.form{display:grid;gap:10px;margin-top:14px}.form label{font-size:11px;font-weight:800;color:var(--muted)}.form input,.form select{width:100%;padding:10px 11px;border:1px solid var(--line);border-radius:10px;background:var(--panel);color:var(--text)}
.dark{--bg:#0a0f1c;--panel:#111827;--text:#eef2ff;--muted:#a5aec1;--line:#2a3448}.dark .table th{background:#151d2d}.dark .bar{background:#212a3a}.dark .day{background:#1d2341;border-color:#313d74;color:#bac3ff}.dark .nav button:hover,.dark .nav button.active{background:#ffffff12}
@media(max-width:1100px){.grid2{grid-template-columns:1fr}.expense-grid{grid-template-columns:repeat(2,minmax(0,1fr))}}
@media(max-width:820px){.sidebar{width:74px;padding:16px 8px}.brand div:not(.logo),.nav span,.side-note{display:none}.nav button{text-align:center}.main{margin-left:74px;padding:15px}.topbar{flex-direction:column}.actions{width:100%}.actions .btn{flex:1}.cards{grid-template-columns:1fr}.expense-grid{grid-template-columns:1fr}.hero{align-items:flex-start;flex-direction:column}.hero-pill{align-self:flex-start}}

/* ===== BUBBLE UI REVISION ===== */
:root{--bubble-shadow:0 18px 45px rgba(60,72,110,.10);--bubble-border:1px solid rgba(255,255,255,.75)}
body{background:radial-gradient(circle at 8% 8%,rgba(124,92,246,.10),transparent 28%),radial-gradient(circle at 92% 14%,rgba(99,102,241,.09),transparent 24%),var(--bg)}
.sidebar{border-top-right-radius:30px;border-bottom-right-radius:30px;box-shadow:14px 0 35px rgba(17,24,39,.12)}
.logo{border-radius:18px}.nav button{border-radius:999px;padding:11px 15px}.nav{gap:9px}.nav button.active{box-shadow:inset 0 0 0 1px rgba(255,255,255,.08),0 10px 25px rgba(0,0,0,.10)}
.main{padding-top:28px}.hero{position:relative;overflow:hidden;border-radius:32px;padding:28px 30px;box-shadow:0 22px 45px rgba(53,61,132,.17)}
.hero:before,.hero:after{content:"";position:absolute;border-radius:50%;background:rgba(255,255,255,.10);pointer-events:none}.hero:before{width:170px;height:170px;right:90px;top:-80px}.hero:after{width:110px;height:110px;right:-25px;bottom:-45px}.hero>*{position:relative;z-index:1}.hero-pill{border-radius:999px;padding:12px 17px;backdrop-filter:blur(6px)}
.card{border-radius:26px;box-shadow:var(--bubble-shadow);border-color:rgba(224,229,240,.9);transition:transform .2s ease,box-shadow .2s ease}.card:hover{transform:translateY(-2px);box-shadow:0 22px 50px rgba(39,51,83,.12)}
.metric{min-height:150px;padding:21px}.metric:after{width:125px;height:125px;right:-34px;top:-34px;background:rgba(91,92,226,.10)}.metric-icon{width:42px;height:42px;border-radius:15px}.metric-value{font-size:31px}.btn{border-radius:999px;padding:10px 16px;box-shadow:0 6px 18px rgba(36,44,74,.05)}.btn.primary{box-shadow:0 9px 22px rgba(91,92,226,.24)}
.table-scroll{border-radius:20px;padding:3px;background:linear-gradient(135deg,rgba(255,255,255,.9),rgba(239,243,250,.8))}.table{border-collapse:separate;border-spacing:4px;min-width:760px}.table th,.table td{border:0;border-radius:12px}.table th{background:#eef1f7}.table td{background:rgba(255,255,255,.72)}.matrix .label-col{border-radius:14px}.row-income td{background:#eaf8ee}.row-expense td{background:#fff0e7}.row-net td{background:#fff8d9}
.badge{padding:6px 10px;border-radius:999px}.search-row input,.search-row select,#studentSearch{border-radius:999px;box-shadow:inset 0 1px 2px rgba(15,23,42,.03)}
.payment-table{min-width:1680px}.payment-cell{padding:9px 7px;border-radius:20px;background:linear-gradient(180deg,#fbfcff,#f2f5fb);box-shadow:inset 0 0 0 1px rgba(225,229,238,.8)}.payment-period{padding:4px 8px;border-radius:999px;background:#eceeff}.day{border-radius:999px;background:#f4f5ff}.pay-ok,.pay-no{padding:7px 11px}.pay-btn{border-radius:999px}.expense-grid{gap:14px}.expense-box{border-radius:20px;box-shadow:0 10px 24px rgba(32,42,69,.06)}
.modal-box{border-radius:28px;box-shadow:0 30px 80px rgba(15,23,42,.24)}.close{border-radius:50%}.form input,.form select{border-radius:999px}.toast{border-radius:999px;box-shadow:0 16px 35px rgba(15,23,42,.2)}
@media(max-width:820px){.sidebar{border-radius:0 22px 22px 0}.hero{border-radius:24px}.card{border-radius:22px}}

/* Desktop click-and-drag horizontal scrolling for wide tables */
.table-scroll{cursor:grab;overflow-x:auto;overscroll-behavior-x:contain;-webkit-overflow-scrolling:touch;scrollbar-width:thin}
.table-scroll.is-dragging{cursor:grabbing;user-select:none;scroll-behavior:auto}
.table-scroll.is-dragging *{user-select:none!important}
.table-scroll.drag-enabled .payment-table{cursor:inherit}
@media (hover:hover) and (pointer:fine){.table-scroll:has(.payment-table){cursor:grab}.table-scroll:has(.payment-table):active{cursor:grabbing}}

/* Fixes requested: drag-to-scroll, wrapped student names, symmetric date cards, and proper dark theme. */
.table-scroll:has(.payment-table){overflow:auto;overscroll-behavior-x:contain;scrollbar-gutter:stable;cursor:grab;touch-action:pan-x pan-y;}
.table-scroll:has(.payment-table).is-dragging{cursor:grabbing;user-select:none;-webkit-user-select:none;}
.table-scroll.is-dragging,.table-scroll.is-dragging *{cursor:grabbing!important;user-select:none!important;-webkit-user-select:none!important;}
.table-scroll:has(.payment-table){scrollbar-width:thin;scrollbar-color:#9da6bb #edf0f6;}
.dark .table-scroll:has(.payment-table){scrollbar-color:#59657d #1a2437;}
.table-scroll.is-dragging *{user-select:none;-webkit-user-select:none;}
.payment-table{table-layout:fixed;min-width:0;width:max-content;}
.payment-table th:first-child,.payment-table td:first-child{width:44px;min-width:44px;max-width:44px;text-align:center;}
.payment-table th:nth-child(2),.payment-table td:nth-child(2){width:165px;min-width:165px;max-width:165px;white-space:normal;overflow-wrap:break-word;word-break:normal;line-height:1.25}.payment-table td:nth-child(2) b{display:block;max-width:108px;white-space:normal;overflow-wrap:normal;word-break:normal;line-height:1.3}
.payment-table th:nth-child(3),.payment-table td:nth-child(3){width:120px;min-width:120px;max-width:120px;}
.payment-table th:nth-child(n+4):nth-child(-n+9),.payment-table td:nth-child(n+4):nth-child(-n+9){width:165px;min-width:165px;max-width:165px;}
.payment-table th:nth-last-child(2),.payment-table td:nth-last-child(2){width:125px;min-width:125px;max-width:125px;}
.payment-table th:last-child,.payment-table td:last-child{width:110px;min-width:110px;max-width:110px;}
.payment-table .payment-cell{width:100%;min-width:0;min-height:146px;padding:9px 6px;gap:7px;border-radius:18px;display:flex;flex-direction:column;align-items:center;justify-content:flex-start;}
.payment-table .payment-period{width:100%;min-height:34px;display:flex;align-items:center;justify-content:center;text-align:center;white-space:normal;overflow-wrap:anywhere;line-height:1.2;padding:5px 7px;border-radius:999px;font-size:10px;}
.payment-table .day-list{width:138px;max-width:138px;min-height:54px;display:grid;grid-template-columns:repeat(3,minmax(0,1fr));align-content:start;justify-content:center;gap:3px;}
.payment-table .day{white-space:nowrap;text-align:center;padding:3px 2px;font-size:9px;line-height:1.15;min-width:0;overflow:hidden;}
.payment-table .pay-btn{margin-top:auto;min-height:25px;}
.payment-hint{font-size:11px;color:var(--muted);padding:8px 11px;border:1px solid var(--line);background:var(--panel);border-radius:999px;white-space:nowrap;}
.dark{--bg:#0b1020;--panel:#141b2b;--text:#edf2ff;--muted:#a2aec4;--line:#2a354b;--green:#4ade80;--greenbg:#123524;--red:#fca5a5;--redbg:#3a2029;--orange:#fdba74;--orangebg:#3a291d;--yellow:#fde68a;--yellowbg:#3c3417;--bluebg:#202d42;--shadow:0 18px 45px rgba(0,0,0,.22);}
body.dark{background:radial-gradient(circle at 8% 8%,rgba(124,92,246,.035),transparent 28%),radial-gradient(circle at 92% 14%,rgba(99,102,241,.025),transparent 24%),var(--bg);color:var(--text)}
.dark .card,.dark .table-scroll,.dark .expense-box,.dark .payment-cell{background:var(--panel);border-color:var(--line);box-shadow:0 12px 30px rgba(0,0,0,.18);}
.dark .table th{background:#1a2437;color:#c3cee2;}
.dark .table td{background:var(--panel);color:var(--text);border-color:var(--line);}
.dark .row-income td{background:var(--greenbg);color:var(--green);}
.dark .row-expense td{background:var(--orangebg);color:#fed7aa;}
.dark .row-net td{background:var(--yellowbg);color:var(--yellow);}
.dark .payment-table th:first-child,.dark .payment-table td:first-child,.dark .payment-table th:nth-child(2),.dark .payment-table td:nth-child(2){background:var(--panel);}
.dark .payment-table .payment-period{background:#252b4c;color:#c7ccff;}
.dark .payment-table .day{background:#20283c;color:#d0d9ef;border-color:#34415b;}
.dark .payment-table .pay-ok{background:#123524;color:#86efac;}
.dark .payment-table .pay-no{background:#3a2029;color:#fecaca;}
.dark .metric-icon{background:#252b4c;color:#c7ccff;}
.dark .metric-icon.green{background:#123524;color:#86efac;}
.dark .metric-icon.red{background:#3a2029;color:#fecaca;}
.dark .hero{box-shadow:0 18px 45px rgba(0,0,0,.35);}
.dark .hero-pill{background:#ffffff0d;border-color:#ffffff1c;}
.dark .close{background:#263247;color:#edf2ff;}
@media(max-width:820px){.payment-table th:nth-child(2),.payment-table td:nth-child(2){width:145px;min-width:145px;max-width:145px;left:44px}.payment-table th:nth-child(n+4):nth-child(-n+9),.payment-table td:nth-child(n+4):nth-child(-n+9){width:155px;min-width:155px;max-width:155px}.payment-hint{white-space:normal;}}


.dark .payment-cell{background:linear-gradient(180deg,#151f31,#121a2a);box-shadow:inset 0 0 0 1px #2b3850;}
.dark .payment-period{background:#252c4a;color:#d0d4ff;}
.dark .payment-hint{background:#151f31;border-color:#2a354b;color:#c1cadb;}
.dark .hero:before,.dark .hero:after{background:rgba(255,255,255,.035);}
.dark .table-scroll:has(.payment-table){background:#111827;border-color:#2a354b;}
.dark .expense-list div{color:#aeb8cc;border-color:#2a354b;}
.dark .search-row input,.dark .search-row select,#studentSearch{background:#141b2b;color:#eef2ff;border-color:#34405a;}
.payment-table tbody tr:hover td{filter:brightness(.985)}
.dark .payment-table tbody tr:hover td{filter:brightness(1.08)}
@media(hover:hover) and (pointer:fine){.table-scroll:has(.payment-table){cursor:grab}.table-scroll:has(.payment-table).is-dragging{cursor:grabbing}}


/* Transaction controls + simplified payment bubbles */
.payment-table .payment-cell-simple{min-height:94px;justify-content:center;padding:12px 8px;gap:12px}
.payment-table .payment-cell-simple .payment-period{min-height:46px;font-size:12px;font-weight:900;line-height:1.25;border-radius:14px;padding:8px 10px;overflow-wrap:normal;word-break:normal}
.day-list,.day{display:none!important}
.tx-filters{align-items:end}.date-filter{display:flex;flex-direction:column;gap:5px;font-size:10px;color:var(--muted);font-weight:800}.date-filter input{min-width:140px;padding:10px;border:1px solid var(--line);border-radius:999px;background:var(--panel);color:var(--text)}.filter-note{margin:-2px 0 12px;line-height:1.45}.filtered-summary{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:10px;margin:10px 0 14px}.summary-chip{background:var(--panel);border:1px solid var(--line);border-radius:16px;padding:12px 14px;box-shadow:0 7px 18px rgba(32,42,69,.04)}.summary-chip span{display:block;font-size:10px;color:var(--muted);font-weight:800}.summary-chip b{display:block;font-size:16px;margin-top:5px}.summary-chip.income b{color:var(--green)}.summary-chip.expense b{color:var(--red)}.summary-chip.balance b{color:var(--accent)}.tx-table{min-width:930px}.action-delete{border:1px solid #fecaca;background:#fff1f2;color:#be123c;padding:6px 10px;border-radius:999px;font-weight:800;font-size:10px;cursor:pointer}.action-delete:hover{background:#ffe4e6}.action-locked{font-size:10px;color:var(--muted)}
.dark .date-filter input,.dark .search-row input,.dark .search-row select{background:#111827;color:var(--text);border-color:var(--line)}.dark .summary-chip{background:#111827;border-color:#2a3448;box-shadow:0 8px 22px rgba(0,0,0,.15)}.dark .action-delete{background:#351b27;color:#fecdd3;border-color:#6b263b}.dark .payment-table .payment-cell-simple{background:linear-gradient(180deg,#151d2c,#111827);box-shadow:inset 0 0 0 1px #2a3448}.dark .payment-table .payment-period{background:#252b4c;color:#c7ccff}
@media(max-width:820px){.tx-filters{align-items:stretch}.date-filter{flex:1}.date-filter input{width:100%;min-width:0}.filtered-summary{grid-template-columns:1fr}.tx-table{min-width:760px}}


/* Compact weekly expense cards + animated detail popup */
.expense-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(205px,1fr));gap:13px;align-items:stretch}
.expense-week-card{appearance:none;text-align:left;display:flex;flex-direction:column;align-items:flex-start;gap:10px;min-height:153px;width:100%;padding:16px;border:1px solid var(--line);border-radius:22px;background:linear-gradient(145deg,var(--panel),color-mix(in srgb,var(--panel) 86%,var(--accent) 14%));color:var(--text);box-shadow:0 10px 24px rgba(32,42,69,.055);cursor:pointer;transition:transform .22s ease,box-shadow .22s ease,border-color .22s ease}
.expense-week-card:hover{transform:translateY(-3px);box-shadow:0 17px 32px rgba(61,70,132,.12);border-color:rgba(91,92,226,.35)}
.expense-week-card:focus-visible{outline:3px solid rgba(91,92,226,.35);outline-offset:3px}
.expense-week-icon{display:grid;place-items:center;width:34px;height:34px;border-radius:13px;background:var(--orangebg);color:var(--orange);font-size:18px;font-weight:900}
.expense-week-date{font-size:12px;line-height:1.35;font-weight:800;color:var(--muted);min-height:31px}
.expense-week-amount{font-size:22px;line-height:1.15;font-weight:900;color:var(--red);letter-spacing:-.4px}
.expense-week-hint{display:flex;justify-content:space-between;align-items:center;width:100%;margin-top:auto;font-size:10px;font-weight:800;color:var(--accent)}
.expense-detail-modal{position:fixed;inset:0;z-index:100;display:none;align-items:center;justify-content:center;padding:20px}
.expense-detail-modal.show{display:flex}
.expense-detail-backdrop{position:absolute;inset:0;width:100%;height:100%;border:0;background:rgba(10,15,30,.56);backdrop-filter:blur(7px);animation:expenseFadeIn .22s ease both;cursor:pointer}
.expense-detail-card{position:relative;z-index:1;width:min(490px,100%);max-height:min(82vh,720px);overflow:auto;padding:23px;border-radius:28px;border:1px solid rgba(255,255,255,.65);background:var(--panel);color:var(--text);box-shadow:0 30px 90px rgba(0,0,0,.25);animation:expensePopIn .32s cubic-bezier(.18,.85,.25,1.18) both}
.expense-detail-head{display:flex;justify-content:space-between;align-items:flex-start;gap:15px;margin-bottom:18px}
.expense-detail-eyebrow{font-size:10px;font-weight:900;letter-spacing:1.4px;color:var(--accent)}
.expense-detail-head h3{font-size:21px;margin:7px 0 5px;line-height:1.25}
.expense-detail-head p{font-size:11px;color:var(--muted);margin:0}
.expense-detail-close{flex:0 0 auto;width:36px;height:36px;border:0;border-radius:50%;background:var(--bg);color:var(--text);font-size:23px;line-height:1;cursor:pointer;transition:transform .2s ease,background .2s ease}
.expense-detail-close:hover{transform:rotate(90deg);background:var(--redbg);color:var(--red)}
.expense-detail-totalbox{display:flex;justify-content:space-between;align-items:center;gap:12px;padding:16px;border-radius:18px;background:var(--orangebg);margin-bottom:14px}
.expense-detail-totalbox span{font-size:12px;font-weight:800;color:var(--orange)}.expense-detail-totalbox strong{font-size:22px;font-weight:900;color:var(--red)}
.expense-detail-list{display:grid;gap:8px}
.expense-detail-row{display:grid;grid-template-columns:24px minmax(0,1fr) auto;align-items:center;gap:8px;padding:12px 13px;border:1px solid var(--line);border-radius:15px;background:var(--panel)}
.expense-detail-dot{display:grid;place-items:center;width:23px;height:23px;border-radius:8px;background:var(--orangebg);color:var(--orange);font-size:18px;font-weight:900}
.expense-detail-name{font-size:12px;font-weight:700;overflow-wrap:anywhere}.expense-detail-row strong{font-size:12px;white-space:nowrap}
.expense-detail-empty{display:grid;justify-items:center;gap:6px;padding:24px 12px;border:1px dashed var(--line);border-radius:16px;color:var(--muted);text-align:center}.expense-detail-empty span{display:grid;place-items:center;width:36px;height:36px;border-radius:50%;background:var(--greenbg);color:var(--green)}.expense-detail-empty b{font-size:13px}.expense-detail-empty small{font-size:11px}
.expense-detail-foot{display:flex;justify-content:space-between;align-items:center;gap:12px;margin-top:18px;padding-top:14px;border-top:1px solid var(--line)}.expense-detail-foot>span{font-size:10px;color:var(--muted)}
body.modal-open{overflow:hidden}
.dark .expense-week-card{background:linear-gradient(145deg,#141d2d,#171a31);border-color:#2b354b;box-shadow:0 12px 28px rgba(0,0,0,.18)}.dark .expense-week-card:hover{border-color:#5a60a7;box-shadow:0 18px 34px rgba(0,0,0,.28)}.dark .expense-week-icon{background:#39261f;color:#fdba74}.dark .expense-detail-backdrop{background:rgba(0,0,0,.72)}.dark .expense-detail-card{background:#111827;border-color:#2a354b;box-shadow:0 30px 90px rgba(0,0,0,.48)}.dark .expense-detail-close{background:#202a3b}.dark .expense-detail-totalbox{background:#38241e}.dark .expense-detail-totalbox span{color:#fdba74}.dark .expense-detail-totalbox strong{color:#fca5a5}.dark .expense-detail-row{background:#151f2e;border-color:#2a354b}.dark .expense-detail-dot{background:#39261f;color:#fdba74}
@keyframes expenseFadeIn{from{opacity:0}to{opacity:1}}
@keyframes expensePopIn{from{opacity:0;transform:translateY(18px) scale(.94)}to{opacity:1;transform:translateY(0) scale(1)}}
@media(prefers-reduced-motion:reduce){.expense-detail-backdrop,.expense-detail-card{animation:none}.expense-week-card,.expense-detail-close{transition:none}}
@media(max-width:560px){.expense-grid{grid-template-columns:repeat(2,minmax(0,1fr));gap:9px}.expense-week-card{min-height:143px;padding:13px;border-radius:18px}.expense-week-amount{font-size:18px}.expense-detail-card{padding:18px;border-radius:22px}.expense-detail-totalbox strong{font-size:18px}}


/* Dashboard contrast + overall balance + draggable daily ledger */
:root{--income-soft:#e3f1e7;--income-ink:#285c39;--expense-soft:#fae9dd;--expense-ink:#87451e;--net-soft:#fff5ce;--net-ink:#71540d}
body:not(.dark) .row-income td{background:var(--income-soft);color:var(--income-ink);font-weight:800}
body:not(.dark) .row-expense td{background:var(--expense-soft);color:var(--expense-ink);font-weight:700}
body:not(.dark) .row-expense td.red{color:var(--expense-ink)}
body:not(.dark) .row-net td{background:var(--net-soft);color:var(--net-ink)}
body:not(.dark) .metric .metric-value.red{color:#a94343}
body:not(.dark) .pay-no{background:#f8e4e4;color:#9f3030}
.grand-total-box{margin-top:14px;padding:24px 22px;border-radius:24px;background:linear-gradient(135deg,#edf7ef,#e3f0e7);border:1px solid #cfe4d4;box-shadow:0 12px 28px rgba(40,92,57,.08);display:grid;grid-template-columns:minmax(0,1fr) auto;align-items:center;gap:12px;position:relative;overflow:hidden}
.grand-total-box:after{content:"";position:absolute;right:-34px;bottom:-66px;width:170px;height:170px;border-radius:50%;background:rgba(45,119,68,.07);pointer-events:none}
.grand-total-box.balance-negative{background:linear-gradient(135deg,#fff0f0,#fbe4e4);border-color:#efcaca;box-shadow:0 12px 28px rgba(155,55,55,.08)}
.grand-total-box.balance-negative .grand-label{color:#8e3d3d}.grand-total-box.balance-negative .grand-description{color:#8d5555}.grand-total-box.balance-negative .grand-value{color:#b42332}.grand-total-box.balance-negative .grand-component{color:#8e3d3d;border-color:#f0cccc}
.grand-total-box.balance-positive .grand-value{color:#24643a}.grand-total-box.balance-zero{background:linear-gradient(135deg,#f0f2f5,#e8ebf0);border-color:#d6dbe4;box-shadow:0 12px 28px rgba(52,64,84,.06)}.grand-total-box.balance-zero .grand-label,.grand-total-box.balance-zero .grand-description,.grand-total-box.balance-zero .grand-value,.grand-total-box.balance-zero .grand-component{color:#596273}.grand-total-box.balance-zero .grand-component{border-color:#d5dbe5}
.dark .grand-total-box.balance-negative{background:linear-gradient(135deg,#351b24,#3b202b);border-color:#683340}.dark .grand-total-box.balance-negative .grand-label,.dark .grand-total-box.balance-negative .grand-description,.dark .grand-total-box.balance-negative .grand-component{color:#f1b4bd}.dark .grand-total-box.balance-negative .grand-value{color:#ff8998}.dark .grand-total-box.balance-negative .grand-component{background:#482530;border-color:#71404b}.dark .grand-total-box.balance-zero{background:linear-gradient(135deg,#202838,#1b2332);border-color:#384356}.dark .grand-total-box.balance-zero .grand-label,.dark .grand-total-box.balance-zero .grand-description,.dark .grand-total-box.balance-zero .grand-value,.dark .grand-total-box.balance-zero .grand-component{color:#cbd5e1}.dark .grand-total-box.balance-zero .grand-component{background:#263142;border-color:#3a4659}
.dark #balanceTotal.balance-negative,.dark #balanceTotal.negative{color:#ff8998!important}.dark #balanceTotal.balance-positive,.dark #balanceTotal.positive{color:#98e2ad!important}
.grand-label{font-size:11px;font-weight:900;letter-spacing:.7px;color:#416c4d}.grand-description{font-size:11px;color:#557361;line-height:1.5;margin-top:5px;max-width:460px}.grand-value{position:relative;z-index:1;font-size:clamp(25px,3vw,38px);font-weight:950;letter-spacing:-.7px;color:#24643a;text-align:right;white-space:nowrap}.grand-components{display:flex;gap:8px;flex-wrap:wrap;margin-top:10px}.grand-component{padding:6px 9px;border-radius:999px;background:#ffffffb8;color:#3e6b4a;font-size:10px;font-weight:800;border:1px solid #d4e6d8}
.daily-ledger-card{margin-top:14px}.daily-help{font-size:11px;line-height:1.5;color:var(--muted);margin-top:4px}.daily-ledger{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:12px;margin-top:12px}.daily-ledger-empty{border:1px dashed var(--line);border-radius:18px;padding:24px;text-align:center;color:var(--muted);font-size:12px;grid-column:1/-1;background:rgba(255,255,255,.35)}
.daily-entry{border:1px solid var(--line);border-radius:20px;padding:14px;background:var(--panel);box-shadow:0 9px 24px rgba(24,35,60,.05);cursor:grab;transition:transform .18s ease,box-shadow .18s ease,border-color .18s ease;min-width:0;user-select:none}.daily-entry:hover{transform:translateY(-2px);box-shadow:0 14px 29px rgba(24,35,60,.09)}.daily-entry.dragging{opacity:.5;transform:scale(.98)}.daily-entry.drag-over{border-color:var(--accent);box-shadow:0 0 0 3px rgba(91,92,226,.12)}.daily-entry-head{display:flex;justify-content:space-between;align-items:center;gap:8px;margin-bottom:12px}.daily-entry-date{font-size:12px;font-weight:900;line-height:1.35;overflow-wrap:anywhere}.drag-grip{color:var(--muted);font-size:18px;letter-spacing:-2px;cursor:grab}.daily-values{display:grid;grid-template-columns:1fr 1fr;gap:8px}.daily-value-box{padding:10px;border-radius:13px;background:#f2f7f3;min-width:0}.daily-value-box.out{background:#fbefe7}.daily-value-box span{display:block;font-size:9px;font-weight:900;color:var(--muted);letter-spacing:.35px}.daily-value-box strong{display:block;font-size:14px;margin-top:5px;overflow-wrap:anywhere;color:#2e6940}.daily-value-box.out strong{color:#98512a}.daily-net{display:flex;justify-content:space-between;align-items:center;gap:8px;padding-top:11px;margin-top:10px;border-top:1px solid var(--line);font-size:10px;color:var(--muted)}.daily-net strong{font-size:13px;color:var(--text)}.daily-entry-items{margin-top:9px;display:grid;gap:4px}.daily-entry-items span{font-size:10px;color:var(--muted);overflow-wrap:anywhere}.daily-entry-items span b{color:var(--text)}
.dark .grand-total-box{background:linear-gradient(135deg,#152a21,#183326);border-color:#294c39;box-shadow:0 14px 30px rgba(0,0,0,.18)}.dark .grand-total-box:after{background:rgba(112,190,139,.06)}.dark .grand-label{color:#a7d8b5}.dark .grand-description{color:#a7c6b0}.dark .grand-value{color:#98e2ad}.dark .grand-component{background:#1c3929;color:#b7e7c3;border-color:#2a533a}.dark .daily-entry{background:#141b2b;border-color:#2a354b;box-shadow:0 10px 24px rgba(0,0,0,.17)}.dark .daily-entry:hover{box-shadow:0 15px 32px rgba(0,0,0,.28)}.dark .daily-value-box{background:#172b22}.dark .daily-value-box.out{background:#33241e}.dark .daily-value-box strong{color:#9de0ae}.dark .daily-value-box.out strong{color:#efb18c}.dark .daily-net{border-color:#2a354b}.dark .daily-net strong{color:#edf2ff}.dark .daily-entry-items span{color:#a2aec4}.dark .daily-entry-items span b{color:#edf2ff}.dark .daily-ledger-empty{background:#111827;border-color:#34405a}
@media(max-width:1100px){.daily-ledger{grid-template-columns:repeat(2,minmax(0,1fr))}}
@media(max-width:700px){.grand-total-box{grid-template-columns:1fr;padding:18px}.grand-value{text-align:left;white-space:normal}.daily-ledger{grid-template-columns:1fr}.daily-values{grid-template-columns:1fr 1fr}}


/* Login feedback and custom bubble delete confirmation */
.login-error{padding:10px 12px;border-radius:14px;background:var(--redbg);color:var(--red);font-size:11px;font-weight:800;line-height:1.45;border:1px solid color-mix(in srgb,var(--red) 18%,transparent)}
.login-error[hidden]{display:none!important}
.bubble-confirm-overlay{position:fixed;inset:0;z-index:150;display:none;align-items:center;justify-content:center;padding:20px;isolation:isolate}
.bubble-confirm-overlay.show{display:flex}
.bubble-confirm-backdrop{position:absolute;inset:0;border:0;background:rgba(15,20,39,.46);backdrop-filter:blur(7px);animation:bubbleBackdropIn .2s ease both;cursor:pointer}
.bubble-confirm-card{position:relative;isolation:isolate;overflow:hidden;width:min(410px,100%);padding:26px 24px 20px;border-radius:30px;border:1px solid rgba(255,255,255,.72);background:radial-gradient(circle at 15% 0%,rgba(124,92,246,.12),transparent 42%),radial-gradient(circle at 100% 85%,rgba(91,92,226,.10),transparent 40%),var(--panel);color:var(--text);box-shadow:0 26px 90px rgba(10,15,30,.25),inset 0 1px 0 rgba(255,255,255,.55);text-align:center;animation:bubbleCardIn .38s cubic-bezier(.16,.9,.25,1.2) both}
.bubble-confirm-card>*:not(.bubble-confirm-orb){position:relative;z-index:2}
.bubble-confirm-orb{position:absolute;border-radius:50%;pointer-events:none;z-index:0;background:linear-gradient(135deg,rgba(255,255,255,.60),rgba(122,111,255,.09));border:1px solid rgba(125,131,220,.12)}
.bubble-confirm-orb.orb-one{width:116px;height:116px;top:-65px;right:-35px}.bubble-confirm-orb.orb-two{width:65px;height:65px;bottom:28px;left:-37px}
.bubble-confirm-icon{width:62px;height:62px;margin:0 auto 12px;display:grid;place-items:center;border-radius:22px;background:linear-gradient(145deg,#f0efff,#e2e1ff);box-shadow:inset 0 1px 0 #fff,0 10px 22px rgba(91,92,226,.13);font-size:28px;animation:bubbleIconFloat 2.8s ease-in-out infinite}
.bubble-confirm-eyebrow{font-size:9px;font-weight:900;letter-spacing:1.5px;color:var(--accent)}.bubble-confirm-card h3{font-size:21px;line-height:1.2;margin:8px 0}.bubble-confirm-message{margin:0 auto;color:var(--muted);font-size:12px;line-height:1.6;max-width:320px;overflow-wrap:anywhere}.bubble-confirm-message strong{color:var(--text)}
.bubble-confirm-actions{display:flex;justify-content:center;gap:9px;flex-wrap:wrap;margin-top:21px}.bubble-confirm-actions .btn{border-radius:999px;padding:10px 16px;font-size:11px;font-weight:900;box-shadow:0 7px 17px rgba(20,30,60,.07)}.bubble-keep{background:var(--panel);color:var(--text)}.bubble-delete{color:#fff;background:linear-gradient(135deg,#d94a62,#b42343);border-color:#d94a62;box-shadow:0 8px 18px rgba(180,35,67,.22)!important}.bubble-delete:hover{filter:brightness(1.04);transform:translateY(-1px)}.bubble-confirm-foot{font-size:9px;color:var(--muted);margin-top:14px}
.bubble-particles{position:absolute;inset:0;display:none;align-items:center;justify-content:center;pointer-events:none;z-index:4}.bubble-particles i{position:absolute;width:12px;height:12px;border-radius:50%;background:radial-gradient(circle at 28% 25%,#fff,#b7b9ff 45%,#7a75ee);border:1px solid rgba(255,255,255,.8);box-shadow:0 3px 10px rgba(91,92,226,.18);opacity:0}.bubble-confirm-overlay.bursting .bubble-particles{display:flex}.bubble-confirm-overlay.bursting .bubble-particles i{animation:bubbleParticleBurst .42s ease-out forwards}.bubble-confirm-overlay.bursting .bubble-particles i:nth-child(1){--dx:-110px;--dy:-88px;--sz:.7}.bubble-confirm-overlay.bursting .bubble-particles i:nth-child(2){--dx:112px;--dy:-92px;--sz:1.15}.bubble-confirm-overlay.bursting .bubble-particles i:nth-child(3){--dx:-140px;--dy:10px;--sz:.85}.bubble-confirm-overlay.bursting .bubble-particles i:nth-child(4){--dx:142px;--dy:8px;--sz:.65}.bubble-confirm-overlay.bursting .bubble-particles i:nth-child(5){--dx:-92px;--dy:95px;--sz:1.05}.bubble-confirm-overlay.bursting .bubble-particles i:nth-child(6){--dx:88px;--dy:103px;--sz:.75}.bubble-confirm-overlay.bursting .bubble-particles i:nth-child(7){--dx:0px;--dy:-130px;--sz:.8}.bubble-confirm-overlay.bursting .bubble-particles i:nth-child(8){--dx:8px;--dy:128px;--sz:1.2}.bubble-confirm-overlay.bursting .bubble-particles i:nth-child(9){--dx:-58px;--dy:-52px;--sz:.55}.bubble-confirm-overlay.bursting .bubble-particles i:nth-child(10){--dx:58px;--dy:50px;--sz:.6}
.bubble-confirm-overlay.bursting .bubble-confirm-card{animation:bubbleCardBurst .35s cubic-bezier(.4,0,.9,.45) forwards}.bubble-confirm-overlay.bursting .bubble-confirm-backdrop{animation:bubbleBackdropOut .35s ease forwards}
@keyframes bubbleBackdropIn{from{opacity:0}to{opacity:1}}@keyframes bubbleBackdropOut{to{opacity:0}}@keyframes bubbleCardIn{0%{opacity:0;transform:translateY(18px) scale(.72)}70%{opacity:1;transform:translateY(-2px) scale(1.025)}100%{opacity:1;transform:translateY(0) scale(1)}}@keyframes bubbleCardBurst{0%{opacity:1;transform:scale(1)}45%{opacity:1;transform:scale(1.07)}100%{opacity:0;transform:scale(.66);filter:blur(5px)}}@keyframes bubbleParticleBurst{0%{opacity:0;transform:translate(0,0) scale(.1)}18%{opacity:1}100%{opacity:0;transform:translate(var(--dx),var(--dy)) scale(var(--sz))}}@keyframes bubbleIconFloat{0%,100%{transform:translateY(0)}50%{transform:translateY(-3px)}}
.dark .bubble-confirm-card{background:radial-gradient(circle at 15% 0%,rgba(124,92,246,.16),transparent 42%),radial-gradient(circle at 100% 85%,rgba(91,92,226,.14),transparent 40%),#111827;border-color:#35405a;box-shadow:0 28px 90px rgba(0,0,0,.46),inset 0 1px 0 rgba(255,255,255,.04)}.dark .bubble-confirm-orb{background:linear-gradient(135deg,rgba(170,174,255,.11),rgba(122,111,255,.025));border-color:#303b54}.dark .bubble-confirm-icon{background:linear-gradient(145deg,#28294a,#1d2341);box-shadow:inset 0 1px 0 #34365e,0 10px 22px rgba(0,0,0,.2)}.dark .bubble-keep{background:#1a2434;border-color:#34405a;color:#e8edfa}.dark .login-error{background:#351e29;color:#ffc0cc;border-color:#693346}
@media(prefers-reduced-motion:reduce){.bubble-confirm-card,.bubble-confirm-backdrop,.bubble-confirm-icon,.bubble-confirm-overlay.bursting .bubble-particles i{animation:none!important;transition:none!important}}


/* Compact date fields + animated full-screen calendar picker */
.calendar-panel{margin:0;padding:20px;border:1px solid var(--line);border-radius:24px;background:var(--panel);box-shadow:0 8px 22px rgba(32,42,69,.045);width:100%;max-width:none}
.calendar-trigger{display:inline-flex;align-items:center;justify-content:space-between;gap:20px;min-width:226px;max-width:100%;margin:14px 0;padding:10px 15px;border:1px solid var(--line);border-radius:16px;background:var(--panel);color:var(--text);cursor:pointer;text-align:left;box-shadow:0 5px 16px rgba(32,42,69,.045);transition:transform .2s ease,border-color .2s ease,box-shadow .2s ease}
.calendar-trigger:hover{transform:translateY(-2px);border-color:var(--accent);box-shadow:0 10px 24px rgba(91,92,226,.12)}.calendar-trigger:focus-visible{outline:3px solid rgba(91,92,226,.32);outline-offset:3px}
.calendar-trigger-left{display:flex;align-items:center;gap:11px}.calendar-trigger-icon{display:grid;place-items:center;width:39px;height:39px;flex:none;border-radius:13px;background:var(--bg);color:var(--accent);font-size:20px}.calendar-trigger-copy{display:grid;gap:3px}.calendar-trigger-label{font-size:9px;letter-spacing:.7px;font-weight:900;color:var(--muted)}.calendar-trigger-date{font-size:16px;letter-spacing:.25px;line-height:1.1}.calendar-trigger-chevron{font-size:20px;color:var(--muted);transition:transform .2s ease}.calendar-trigger[aria-expanded="true"] .calendar-trigger-chevron{transform:rotate(180deg)}
body.calendar-modal-open{overflow:hidden}.calendar-modal-overlay{position:fixed;inset:0;z-index:180;display:none;align-items:center;justify-content:center;padding:22px;isolation:isolate}.calendar-modal-overlay.show,.calendar-modal-overlay.closing{display:flex}
.calendar-modal-backdrop{position:absolute;inset:0;border:0;background:rgba(12,19,36,.58);backdrop-filter:blur(9px);cursor:pointer;animation:calendarBackdropIn .22s ease both}
.calendar-modal-card{position:relative;z-index:1;width:min(760px,100%);max-height:min(90vh,900px);overflow-y:auto;padding:20px;border:1px solid rgba(255,255,255,.66);border-radius:30px;background:var(--panel);color:var(--text);box-shadow:0 28px 100px rgba(8,14,30,.30),inset 0 1px 0 rgba(255,255,255,.5);animation:calendarModalIn .42s cubic-bezier(.16,.9,.25,1.15) both;scrollbar-width:thin}
.calendar-modal-top{display:flex;align-items:center;justify-content:space-between;gap:14px;margin:0 2px 15px}.calendar-modal-kicker{font-size:9px;letter-spacing:1.6px;font-weight:900;color:var(--accent)}.calendar-modal-top h3{font-size:20px;line-height:1.25;margin:5px 0 0}.calendar-modal-close{display:grid;place-items:center;flex:none;width:42px;height:42px;border:1px solid var(--line);border-radius:15px;background:var(--bg);color:var(--text);font-size:25px;cursor:pointer;transition:transform .18s ease,background .18s ease}.calendar-modal-close:hover{transform:rotate(90deg);background:var(--redbg)}
.calendar-modal-panel .calendar-head{gap:14px;margin-bottom:16px}.calendar-head strong{font-size:20px;text-align:center}.calendar-head .btn{padding:9px 16px;font-size:23px;line-height:1.1;min-width:48px;border-radius:14px}.calendar-weekdays,.calendar-days{display:grid;grid-template-columns:repeat(7,minmax(0,1fr));gap:8px}.calendar-weekdays span{text-align:center;font-size:11px;font-weight:900;color:var(--muted);padding:9px 0}.calendar-day{min-width:0;aspect-ratio:1;border:1px solid transparent;border-radius:15px;background:var(--bg);color:var(--text);font-size:16px;font-weight:800;cursor:pointer;transition:background .17s,border-color .17s,transform .17s,box-shadow .17s}.calendar-day:hover{border-color:var(--accent);transform:translateY(-2px) scale(1.025);box-shadow:0 7px 17px rgba(91,92,226,.12)}.calendar-day.outside{opacity:.35}.calendar-day.selected{background:var(--accent);color:#fff;border-color:var(--accent);box-shadow:0 7px 18px rgba(91,92,226,.24)}.calendar-day.period-day:not(.selected){box-shadow:inset 0 -4px 0 #a5b4fc}.calendar-note{font-size:12px;line-height:1.55;color:var(--muted);margin-top:16px;min-height:18px;padding:12px 14px;border-radius:14px;background:var(--bg)}
.dark .calendar-trigger{background:var(--panel);border-color:var(--line);box-shadow:0 8px 20px rgba(0,0,0,.15)}.dark .calendar-trigger-icon{background:#1a2437}.dark .calendar-day{background:#1a2437;color:var(--text)}.dark .calendar-day.selected{background:var(--accent);color:white}.dark .calendar-panel{background:var(--panel);border-color:var(--line)}.dark .calendar-modal-card{background:#111827;border-color:#35405a;box-shadow:0 28px 100px rgba(0,0,0,.52),inset 0 1px 0 rgba(255,255,255,.03)}.dark .calendar-modal-close{background:#1a2434;border-color:#34405a;color:#e8edfa}.dark .calendar-note{background:#1a2434}
.payment-cell-simple{cursor:pointer;transition:transform .16s ease,box-shadow .16s ease}.payment-cell-simple:hover{transform:translateY(-2px);box-shadow:0 8px 18px rgba(91,92,226,.12)}.payment-cell-simple:focus-visible{outline:3px solid rgba(91,92,226,.45);outline-offset:2px}.payment-cell-simple .pay-btn{pointer-events:none}
@keyframes calendarBackdropIn{from{opacity:0}to{opacity:1}}@keyframes calendarModalIn{0%{opacity:0;transform:translateY(24px) scale(.88);filter:blur(5px)}70%{opacity:1;transform:translateY(-3px) scale(1.01);filter:blur(0)}100%{opacity:1;transform:translateY(0) scale(1);filter:blur(0)}}@keyframes calendarModalOut{to{opacity:0;transform:translateY(12px) scale(.94);filter:blur(3px)}}@keyframes calendarBackdropOut{to{opacity:0}}
.calendar-modal-overlay.closing .calendar-modal-card{animation:calendarModalOut .18s ease both}.calendar-modal-overlay.closing .calendar-modal-backdrop{animation:calendarBackdropOut .18s ease both}
@media(max-width:560px){.calendar-trigger{width:100%;min-width:0;max-width:320px}.calendar-modal-overlay{padding:10px}.calendar-modal-card{padding:13px;border-radius:23px;max-height:94vh}.calendar-modal-top{margin-bottom:11px}.calendar-modal-top h3{font-size:17px}.calendar-modal-close{width:38px;height:38px}.calendar-modal-panel{padding:13px;border-radius:18px}.calendar-head strong{font-size:16px}.calendar-head .btn{min-width:40px;padding:7px 12px}.calendar-weekdays,.calendar-days{gap:4px}.calendar-weekdays span{font-size:9px;padding:6px 0}.calendar-day{border-radius:9px;font-size:12px}.calendar-note{font-size:10px;padding:10px}.calendar-trigger-date{font-size:15px}}
@media(prefers-reduced-motion:reduce){.calendar-modal-card,.calendar-modal-backdrop,.calendar-trigger,.calendar-trigger-chevron,.calendar-day,.calendar-modal-close{animation:none!important;transition:none!important}}


/* Consistent section sizing and dynamic weekly management */
#dashboardTab,#paymentsTab,#financeTab,#transactionsTab{width:100%;min-width:0}
#dashboardTab>.cards,#dashboardTab>.grid2,#dashboardTab>.card{width:100%;min-width:0}
.cards{align-items:stretch}
.cards>.metric{height:100%;min-height:160px;display:flex;flex-direction:column}
.grid2{align-items:stretch;grid-auto-rows:1fr}
.grid2>.card{height:100%;min-width:0}
#paymentsTab>.card,#financeTab>.card,#transactionsTab>.card{width:100%;min-width:0}
.section-head{min-height:48px}
.payment-section-head{align-items:center;flex-wrap:wrap}
.payment-head-actions{display:flex;align-items:center;justify-content:flex-end;gap:8px;flex:0 1 auto;flex-wrap:wrap;min-width:0}
.payment-head-actions .search{width:min(260px,100%);min-width:180px;max-width:260px;padding:10px 11px;border:1px solid var(--line);border-radius:10px;background:var(--panel);color:var(--text)}
.payment-head-actions .btn{white-space:nowrap}
.expense-grid{align-items:stretch}
.expense-week-card{height:100%;min-height:164px}
.payment-table th:not(:first-child),.payment-table td:not(:first-child){min-width:150px}
#paymentWeekModal .form{gap:12px}
#paymentWeekModal .login-error:not([hidden]){display:block}
@media(max-width:650px){.payment-section-head{align-items:stretch}.payment-head-actions{width:100%;justify-content:stretch}.payment-head-actions .search{min-width:0;flex:1;width:auto;max-width:none}.payment-head-actions .btn{flex:1}.section-head{min-height:0}.cards>.metric{min-height:145px}}

</style>
</head>
<body>
<div class="app">
<aside class="sidebar">
  <div class="brand"><div class="logo">XI</div><div><h1>ClassCash XI</h1><small>Keuangan Kelas</small></div></div>
  <nav class="nav">
    <button class="active" data-tab="dashboard">⌂ <span>Dashboard</span></button>
    <button data-tab="payments">✓ <span>Pembayaran</span></button>
    <button data-tab="finance">▤ <span>Rekap Keuangan</span></button>
    <button data-tab="transactions">☷ <span>Transaksi</span></button>
  </nav>
  <div class="side-note">Data pembayaran dan rekap keuangan sudah digabung dari dua foto yang diberikan.</div>
</aside>
<main class="main">
<div class="topbar"><div><div class="tiny">SISTEM INFORMASI KEUANGAN KELAS XI</div><h2 id="title">Dashboard Kas Kelas</h2><div class="sub">Tampilan revisi: lebih rapi, angka diperiksa kembali, dan data pembayaran diperbaiki sesuai foto.</div></div><div class="actions"><button class="btn" id="themeBtn">🌙 Mode</button><button class="btn" id="loginBtn">🔐 Admin Login</button><button class="btn primary" id="addBtn">＋ Tambah Transaksi</button></div></div>
<section class="hero"><div><div class="tiny" style="color:#b9c6ff">CLASSCASH XI • DASHBOARD</div><h1>Transparansi Keuangan Kelas</h1><p>Rekap pembayaran siswa dan laporan kas kelas berada dalam satu sistem.</p></div><div class="hero-pill">Saldo Akhir • Rp703.000</div></section>

<section id="dashboardTab">
<div class="cards">
 <div class="card metric"><div class="metric-icon">↗</div><div class="metric-title">TOTAL PEMASUKAN</div><div class="metric-value accent" id="incomeTotal">Rp0</div><div class="sub">Uang kas awal + iuran mingguan</div></div>
 <div class="card metric"><div class="metric-icon red">↘</div><div class="metric-title">TOTAL PENGELUARAN</div><div class="metric-value red" id="expenseTotal">Rp0</div><div class="sub">Seluruh pengeluaran pada foto</div></div>
 <div class="card metric"><div class="metric-icon green">✓</div><div class="metric-title">SALDO AKHIR</div><div class="metric-value green" id="balanceTotal">Rp0</div><div class="sub">Pemasukan − pengeluaran</div></div>
</div>
<div class="grid2">
 <div class="card"><div class="section-head"><div><h3>Ringkasan Keuangan</h3><div class="tiny">Tabel dibuat ulang agar lebih mudah dibaca.</div></div><span class="badge paid">Sesuai Foto</span></div><div class="table-scroll"><table class="table matrix"><thead><tr><th class="label-col">KOMPONEN</th><th>UANG KAS AWAL</th><th>3–7 AGUSTUS 2026</th><th>10–14 AGUSTUS 2026</th><th>17–21 AGUSTUS 2026</th><th>24–28 AGUSTUS 2026</th><th>29 AGU–04 SEP 2026</th><th>7–11 SEPTEMBER 2026</th><th>TOTAL</th></tr></thead><tbody id="financeBody"></tbody></table></div><div id="grandTotalDashboard" class="grand-total-box"></div></div>
 <div class="card"><div class="section-head"><div><h3>Status Pembayaran</h3><div class="tiny">Jumlah siswa yang tercatat membayar</div></div><span class="badge paid">36 siswa</span></div><div id="statusBars"></div></div>
</div>
<div class="card daily-ledger-card"><div class="section-head"><div><h3>Catatan Harian</h3><div class="daily-help">Tambahkan pemasukan dan pengeluaran dengan tanggal yang sama untuk membentuk ringkasan satu hari. Kartu dapat diseret untuk mengubah urutan tampilan; saldo utama tetap dihitung dari seluruh transaksi yang digabungkan.</div></div><span class="badge neutral">Drag &amp; drop</span></div><div class="daily-ledger" id="dailyLedger"></div></div>
</section>

<section id="paymentsTab" style="display:none">
<div class="card"><div class="section-head payment-section-head"><div><h3>Rekap Pembayaran 36 Siswa</h3><div class="tiny">Tanggal periode ditampilkan di atas status pembayaran. <span class="payment-hint">🖱️ PC: klik-tahan, lalu geser ← →</span></div></div><div class="payment-head-actions"><input id="studentSearch" class="search" placeholder="Cari nama siswa..." aria-label="Cari siswa"><button type="button" class="btn primary" id="addPaymentWeekBtn">＋ Tambah Minggu</button></div></div><div class="calendar-panel" id="paymentCalendar"><div class="calendar-head"><button type="button" class="btn calendar-prev" aria-label="Bulan sebelumnya">‹</button><strong class="calendar-title"></strong><button type="button" class="btn calendar-next" aria-label="Bulan berikutnya">›</button></div><div class="calendar-weekdays"><span>Min</span><span>Sen</span><span>Sel</span><span>Rab</span><span>Kam</span><span>Jum</span><span>Sab</span></div><div class="calendar-days"></div><div class="calendar-note">Pilih tanggal untuk melihat periode pembayaran yang mencakup tanggal tersebut.</div></div><div class="table-scroll"><table class="table payment-table"><thead><tr><th>No</th><th>Nama Siswa</th><th>Uang Kas Awal</th></tr></thead><tbody id="paymentBody"></tbody></table></div><div class="tiny" style="margin-top:12px">Status pada tabel mengikuti tanda pembayaran pada foto. Karena sumber hanya memberikan rentang mingguan, tanggal harian di dalam rentang ditampilkan sebagai tanggal periode, bukan sebagai klaim bahwa pembayaran dilakukan setiap hari.</div></div>
</section>

<section id="financeTab" style="display:none">
<div class="card"><div class="section-head"><div><h3>Rekap Keuangan & Pengeluaran</h3><div class="tiny">Angka asli dipertahankan, tampilan diperbaiki.</div></div><span class="badge paid">Saldo Rp703.000</span></div><div class="table-scroll"><table class="table matrix"><thead><tr><th class="label-col">KOMPONEN</th><th>UANG KAS AWAL</th><th>3–7 AGUSTUS</th><th>10–14 AGUSTUS</th><th>17–21 AGUSTUS</th><th>24–28 AGUSTUS</th><th>31 AGU–04 SEP</th><th>7–11 SEPTEMBER</th><th>TOTAL</th></tr></thead><tbody id="financeBody2"></tbody></table></div><div id="grandTotalFinance" class="grand-total-box"></div><div style="margin-top:16px"><div class="section-head"><div><h3>Pengeluaran per Periode</h3><div class="tiny">Ringkasan tanggal dan total saja. Klik kartu untuk membuka rincian pengeluaran.</div></div></div><div class="expense-grid" id="expenseGrid"></div></div></div>
</section>

<section id="transactionsTab" style="display:none">
<div class="card"><div class="section-head"><div><h3>Semua Transaksi</h3><div class="tiny">Transaksi terbaru ditampilkan lebih dahulu. Admin dapat menghapus entri yang keliru.</div></div></div><div class="calendar-panel" id="transactionCalendar"><div class="calendar-head"><button type="button" class="btn calendar-prev" aria-label="Bulan sebelumnya">‹</button><strong class="calendar-title"></strong><button type="button" class="btn calendar-next" aria-label="Bulan berikutnya">›</button></div><div class="calendar-weekdays"><span>Min</span><span>Sen</span><span>Sel</span><span>Rab</span><span>Kam</span><span>Jum</span><span>Sab</span></div><div class="calendar-days"></div><div class="calendar-note">Pilih tanggal untuk memfilter transaksi pada hari itu.</div></div><div class="search-row tx-filters"><input id="search" placeholder="Cari transaksi..."><select id="filter"><option value="all">Semua jenis</option><option value="in">Pemasukan</option><option value="out">Pengeluaran</option></select><select id="periodFilter"><option value="all">Semua periode</option></select><label class="date-filter"><span>Dari</span><input id="dateFrom" type="date" aria-label="Tanggal mulai"></label><label class="date-filter"><span>Sampai</span><input id="dateTo" type="date" aria-label="Tanggal akhir"></label><button class="btn" id="clearDateFilters" type="button">Reset tanggal</button></div><div id="rangeNote" class="tiny filter-note">Data dari foto tercatat per periode mingguan. Untuk transaksi foto, filter rentang memakai tanggal awal periode; nominal yang tampil tetap nominal periode lengkap.</div><div class="filtered-summary" id="filteredSummary"></div><div class="table-scroll"><table class="table tx-table"><thead><tr><th>Tanggal / Periode</th><th>Jenis</th><th>Deskripsi</th><th>Nominal</th><th>Admin</th><th>Aksi</th></tr></thead><tbody id="txBody"></tbody></table></div></div>
</section>
<div class="tiny" style="margin-top:14px">Data telah direvisi berdasarkan dua gambar sumber: total pemasukan Rp1.420.000, pengeluaran Rp717.000, saldo Rp703.000.</div>
</main></div>

<div class="expense-detail-modal" id="expenseDetailModal" aria-hidden="true" role="dialog" aria-modal="true" aria-labelledby="expenseDetailTitle">
 <button class="expense-detail-backdrop" type="button" aria-label="Tutup rincian" onclick="closeExpenseDetail()"></button>
 <section class="expense-detail-card">
  <div class="expense-detail-head"><div><span class="expense-detail-eyebrow">REKAP PENGELUARAN</span><h3 id="expenseDetailTitle">Periode</h3><p>Rincian pengeluaran pada periode terpilih</p></div><button class="expense-detail-close" type="button" aria-label="Tutup" onclick="closeExpenseDetail()">×</button></div>
  <div class="expense-detail-totalbox"><span>Total pengeluaran</span><strong id="expenseDetailTotal">Rp0</strong></div>
  <div id="expenseDetailList" class="expense-detail-list"></div>
  <div class="expense-detail-foot"><span>ClassCash XI • Transparansi Keuangan</span><button type="button" class="btn primary" onclick="closeExpenseDetail()">Selesai</button></div>
 </section>
</div>
<div class="modal" id="loginModal"><div class="modal-box"><button class="close" id="loginClose">×</button><h3>Login Admin</h3><form class="form" id="loginForm"><div><label>Username</label><input id="username" autocomplete="username" required></div><div><label>Password</label><input id="password" type="password" autocomplete="current-password" required></div><div class="login-error" id="loginError" role="status" aria-live="polite" hidden>Username atau password belum sesuai. Silakan coba lagi.</div><button class="btn primary">Masuk</button></form></div></div>
<div class="modal" id="addModal"><div class="modal-box"><button class="close" id="addClose">×</button><h3>Tambah Transaksi</h3><form class="form" id="addForm"><div class="daily-help">Untuk satu hari, simpan pemasukan dan pengeluaran sebagai transaksi terpisah dengan tanggal yang sama. Dashboard akan menjumlahkan semuanya secara keseluruhan.</div><div><label>Tanggal transaksi</label><input id="newPeriod" type="date" required></div><div><label>Jenis</label><select id="newType"><option value="in">Pemasukan</option><option value="out">Pengeluaran</option></select></div><div><label>Deskripsi</label><input id="newDesc" required></div><div><label>Nominal</label><input id="newAmount" type="number" min="1" required></div><button class="btn primary">Simpan</button></form></div></div>
<div class="modal" id="paymentWeekModal"><div class="modal-box"><button class="close" id="paymentWeekClose" type="button" aria-label="Tutup">×</button><h3>Tambah Minggu Pembayaran</h3><div class="tiny" style="margin-top:5px;line-height:1.6">Periode baru akan ditambahkan ke tabel pembayaran dan ringkasan dashboard. Semua siswa dimulai dengan status “Belum bayar”.</div><form class="form" id="paymentWeekForm"><div><label>Tanggal mulai</label><input id="paymentWeekStart" type="date" required></div><div><label>Tanggal selesai</label><input id="paymentWeekEnd" type="date" required></div><div class="login-error" id="paymentWeekError" role="status" aria-live="polite" hidden></div><button class="btn primary" type="submit">＋ Buat Minggu</button></form></div></div>
<div class="bubble-confirm-overlay" id="deleteConfirmModal" aria-hidden="true" role="dialog" aria-modal="true" aria-labelledby="deleteConfirmTitle">
  <button type="button" class="bubble-confirm-backdrop" id="deleteConfirmBackdrop" aria-label="Batalkan hapus"></button>
  <section class="bubble-confirm-card" id="deleteConfirmCard" role="document" tabindex="-1">
    <div class="bubble-confirm-orb orb-one"></div><div class="bubble-confirm-orb orb-two"></div>
    <div class="bubble-confirm-icon" aria-hidden="true">🫧</div>
    <div class="bubble-confirm-eyebrow">CLASSCASH XI • KONFIRMASI ADMIN</div>
    <h3 id="deleteConfirmTitle">Hapus transaksi ini?</h3>
    <p class="bubble-confirm-message" id="deleteConfirmMessage">Periksa transaksi sebelum dihapus.</p>
    <div class="bubble-confirm-actions">
      <button class="btn bubble-keep" type="button" id="deleteConfirmCancel">Jangan hapus</button>
      <button class="btn bubble-delete" type="button" id="deleteConfirmAccept">Ya, hapus</button>
    </div>
    <div class="bubble-confirm-foot">Gelembung akan pecah setelah kamu memilih.</div>
  </section>
  <div class="bubble-particles" id="deleteBubbleParticles" aria-hidden="true"><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i><i></i></div>
</div>
<div class="toast" id="toast"></div>
<script>
const rupiah=n=>new Intl.NumberFormat('id-ID',{style:'currency',currency:'IDR',maximumFractionDigits:0}).format(n);
const esc=s=>String(s).replace(/[&<>"']/g,m=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[m]));
const shortDate=d=>d.replace('Agustus','Agu').replace('September','Sep');
const BASE_WEEK_INFO=[
{label:'3–7 Agustus 2026',start:'2026-08-03',end:'2026-08-07',days:['03 Agustus 2026','04 Agustus 2026','05 Agustus 2026','06 Agustus 2026','07 Agustus 2026']},
{label:'10–14 Agustus 2026',start:'2026-08-10',end:'2026-08-14',days:['10 Agustus 2026','11 Agustus 2026','12 Agustus 2026','13 Agustus 2026','14 Agustus 2026']},
{label:'17–21 Agustus 2026',start:'2026-08-17',end:'2026-08-21',days:['17 Agustus 2026','18 Agustus 2026','19 Agustus 2026','20 Agustus 2026','21 Agustus 2026']},
{label:'24–28 Agustus 2026',start:'2026-08-24',end:'2026-08-28',days:['24 Agustus 2026','25 Agustus 2026','26 Agustus 2026','27 Agustus 2026','28 Agustus 2026']},
{label:'29 Agustus–04 September 2026',start:'2026-08-29',end:'2026-09-04',days:['29 Agustus 2026','30 Agustus 2026','31 Agustus 2026','01 September 2026','02 September 2026','03 September 2026','04 September 2026']},
{label:'7–11 September 2026',start:'2026-09-07',end:'2026-09-11',days:['07 September 2026','08 September 2026','09 September 2026','10 September 2026','11 September 2026']}
];
const PAYMENT_WEEKS_KEY='classcash_extra_payment_weeks_v1';
let extraPaymentWeeks=[];
try{const savedWeeks=JSON.parse(localStorage.getItem(PAYMENT_WEEKS_KEY)||'[]');if(Array.isArray(savedWeeks))extraPaymentWeeks=savedWeeks.filter(w=>w&&/^\d{4}-\d{2}-\d{2}$/.test(w.start||'')&&/^\d{4}-\d{2}-\d{2}$/.test(w.end||'')&&w.start<=w.end).map((w,i)=>({...w,id:w.id||`payment-week-${i+1}`,label:w.label||formatWeekLabel(w.start,w.end)}));}catch(_){extraPaymentWeeks=[];}
const WEEK_INFO=[...BASE_WEEK_INFO,...extraPaymentWeeks];
const STUDENTS=['Anggi Maria Mangkey','Axel Imanuel Laikun','Benedicta Lovea Jenive Suwuh','Berliana Jelova Hartiono','Berry Ignazio Manoppo','Carissa Cristabella Lasiro','Cheryl Angelyca Aprilliani Razak','Clay Richard Pangaila','Demetria Angelique Pangemanan','Devano Ezra Rondonuwu','Fabio Keith Hontong','Felicia Mareyke Lelengboto','Gabriel Yohanes Budiawan','Gabriela Syalom Patadungan','Gratia Beatrix Rei','Gregorio Leonard Roring','Irene Carissa Putri Purwanto','Jesslyn Theresia Yudono','Keyla Fenisia Wawolumaya','Keyza Celomitha Zefanya Rambing','Kirsten Faith Davina Patty','Kylan Gazil Xavier Tumbel','Lisa Pangemanan','Marcelo Ludong','Margareth Tia Maniku','Meyuri Tesalonika Rory','Miquel Dimitri Johanis','Nicole Bernadeth Thieyssen','Pricillia Litschia Sinaulan','Rafajireh Abel Mongkaren','Scarlett Leonetta Indra','Theresia Monique Putri Rumyantenan','Verren Dealova Samuri','Vigili Cecilia Pangkey','Vivelle Liesbianto','Windy Triyana Simanjuntak'];
// Revisi pola pembayaran agar sama dengan foto: Week 3 Axel tidak membayar; Week 5 Axel, Irene, Kylan tidak membayar; Week 6 hanya Carissa membayar.
const DEFAULT_PAID=STUDENTS.map((_,i)=>WEEK_INFO.map((__,w)=>{if(w===0||w===1||w===3)return 1;if(w===2)return i!==1?1:0;if(w===4)return [1,16,21].includes(i)?0:1;if(w===5)return i===5?1:0;return 0;}));
const PAYMENT_KEY='classcash_payment_final_v2';let payments=JSON.parse(localStorage.getItem(PAYMENT_KEY)||'null')||DEFAULT_PAID;payments=payments.map(row=>{const next=Array.isArray(row)?row.slice(0,WEEK_INFO.length):[];while(next.length<WEEK_INFO.length)next.push(0);return next.map(v=>Number(v)?1:0);});if(localStorage.getItem(PAYMENT_KEY))localStorage.setItem(PAYMENT_KEY,JSON.stringify(payments));
const PERIODS=[
{label:'Uang Kas Awal',income:540000,expense:94400,descs:['Sapu (58.900)','Penghapus Papan (35.500)']},
{label:'3–7 Agustus 2026',income:180000,expense:289600,descs:['Banner (120.000)','Kain Merah Putih (97.500)','Print Dokumen 2 (18.000)','Paku, Gold Fox, Pin Karton (24.100)','Hiasan Kemerdekaan (8.000)','Print Dokumen 1 (22.000)']},
{label:'10–14 Agustus 2026',income:180000,expense:66000,descs:['Pita Plastik (18.000)','Hiasan Bulat (48.000)']},
{label:'17–21 Agustus 2026',income:175000,expense:83000,descs:['Buku Jurnal (39.000)','Stella (36.000)','Pembersih Lantai (8.000)']},
{label:'24–28 Agustus 2026',income:175000,expense:134000,descs:['Benang (10.000)','Karton Linen (10.000)','Push Pin (8.000)','Parkir dan Print (16.000)','Aqua (90.000)']},
{label:'29 Agustus–04 September 2026',income:165000,expense:50000,descs:['Derma Misa (50.000)']},
{label:'7–11 September 2026',income:5000,expense:0,descs:[]}
];
let custom=JSON.parse(localStorage.getItem('classcash_custom_tx_v2')||'[]');
const migratedCustom=custom.map((x,i)=>({...x,id:x.id||`legacy-${i}`}));
if(migratedCustom.some((x,i)=>x.id!==custom[i].id)){custom=migratedCustom;localStorage.setItem('classcash_custom_tx_v2',JSON.stringify(custom));}else{custom=migratedCustom;}
let deletedSource=JSON.parse(localStorage.getItem('classcash_deleted_source_tx_v1')||'[]');
let admin=localStorage.getItem('classcash_admin_final_v2')==='1';const USER='admin',PASS='classcashxi';
const PERIOD_STARTS=['2026-08-01','2026-08-03','2026-08-10','2026-08-17','2026-08-24','2026-08-29','2026-09-07'];
const PERIOD_ENDS=['2026-08-02','2026-08-07','2026-08-14','2026-08-21','2026-08-28','2026-09-04','2026-09-11'];
let currentExpenseGroups=[];
function amountOfDesc(d){return Number((d.match(/\(([-\d.]+)\)/)||[])[1]?.replaceAll('.','')||0)}
function sourceIncomeId(i){return `source-income-${i}`}
function sourceExpenseId(i,j){return `source-expense-${i}-${j}`}
function customPeriodIndex(x){
 const date=parsePeriodDate(x.period); if(!date)return -1;
 return PERIOD_STARTS.findIndex((start,i)=>date>=start&&date<=PERIOD_ENDS[i]);
}
function customInPeriod(i,type){return custom.filter(x=>x.type===type&&customPeriodIndex(x)===i).reduce((sum,x)=>sum+Number(x.amount||0),0)}
function periodIncomeAt(i){
 // Periode 0 adalah uang kas awal; periode 1–6 cocok dengan enam minggu awal.
 const recordedBase=deletedSource.includes(sourceIncomeId(i))?0:Number(PERIODS[i].income||0);
 const weeklyPaymentIncome=i===0?recordedBase:payments.reduce((sum,row)=>sum+(Number(row[i-1])===1?5000:0),0);
 return weeklyPaymentIncome+customInPeriod(i,'in');
}
function periodExpenseAt(i){return PERIODS[i].descs.reduce((sum,d,j)=>sum+(deletedSource.includes(sourceExpenseId(i,j))?0:amountOfDesc(d)),0)+customInPeriod(i,'out')}
function extraPaymentIncome(){let total=0;for(let wi=BASE_WEEK_INFO.length;wi<WEEK_INFO.length;wi++)total+=payments.reduce((sum,row)=>sum+(Number(row[wi])===1?5000:0),0);return total;}
function totals(){const income=PERIODS.reduce((a,p,i)=>a+periodIncomeAt(i),0)+custom.filter(x=>x.type==='in'&&customPeriodIndex(x)===-1).reduce((a,x)=>a+Number(x.amount||0),0)+extraPaymentIncome();const expense=PERIODS.reduce((a,p,i)=>a+periodExpenseAt(i),0)+custom.filter(x=>x.type==='out'&&customPeriodIndex(x)===-1).reduce((a,x)=>a+Number(x.amount||0),0);return{income,expense,balance:income-expense};}
function addIsoDays(iso,days){const d=new Date(iso+'T00:00:00Z');d.setUTCDate(d.getUTCDate()+days);return d.toISOString().slice(0,10);}
function dynamicWeekRange(date){let start=getMondayISO(date),end=getSundayISO(start);for(let i=0;i<PERIOD_STARTS.length;i++){const ps=PERIOD_STARTS[i],pe=PERIOD_ENDS[i];if(start<=pe&&end>=ps){if(pe>=start&&pe<end)start=addIsoDays(pe,1);else if(ps>start&&ps<=end)end=addIsoDays(ps,-1);}}return{start,end};}
function getDynamicWeekGroups(){
 const groups=new Map();
 for(let wi=BASE_WEEK_INFO.length;wi<WEEK_INFO.length;wi++){const w=WEEK_INFO[wi];groups.set(`payment-week-${w.id}`,{id:`payment-week-${w.id}`,label:w.label,start:w.start,end:w.end,paymentIndex:wi,items:[]});}
 custom.forEach((x,index)=>{
   const date=parsePeriodDate(x.period);if(customPeriodIndex(x)>=0)return;
   if(!date){const id='undated-transactions';if(!groups.has(id))groups.set(id,{id,label:'Tanggal tidak tercatat',start:'9999-12-31',end:'9999-12-31',paymentIndex:null,items:[]});groups.get(id).items.push(x);return;}
   const paymentIndex=WEEK_INFO.findIndex((w,wi)=>wi>=BASE_WEEK_INFO.length&&date>=w.start&&date<=w.end);
   if(paymentIndex>=0){groups.get(`payment-week-${WEEK_INFO[paymentIndex].id}`).items.push(x);return;}
   const monday=getMondayISO(date),id=`transaction-week-${monday}`;
   if(!groups.has(id)){const range=dynamicWeekRange(date);groups.set(id,{id,label:formatWeekLabel(range.start,range.end),start:range.start,end:range.end,monday,paymentIndex:null,items:[]});}
   groups.get(id).items.push(x);
 });
 return [...groups.values()].map(g=>({...g,sortKey:g.start||'9999-12-31'})).sort((a,b)=>a.sortKey.localeCompare(b.sortKey));
}
function dynamicGroupIncome(g){const paid=g.paymentIndex==null?0:payments.reduce((sum,row)=>sum+(Number(row[g.paymentIndex])===1?5000:0),0);return paid+g.items.filter(x=>x.type==='in').reduce((sum,x)=>sum+Number(x.amount||0),0);}
function dynamicGroupExpense(g){return g.items.filter(x=>x.type==='out').reduce((sum,x)=>sum+Number(x.amount||0),0);}
function matrixHeaderHtml(){const dynamic=getDynamicWeekGroups();const labels=[...PERIODS.map((p,i)=>i===0?'UANG KAS AWAL':p.label.toUpperCase()),...dynamic.map(g=>g.label.toUpperCase()),'TOTAL'];return `<tr><th class="label-col">KOMPONEN</th>${labels.map(label=>`<th>${esc(label)}</th>`).join('')}</tr>`;}
function matrixHtml(){const t=totals(),dynamic=getDynamicWeekGroups();const ins=[...PERIODS.map((p,i)=>periodIncomeAt(i)),...dynamic.map(dynamicGroupIncome),t.income],outs=[...PERIODS.map((p,i)=>periodExpenseAt(i)),...dynamic.map(dynamicGroupExpense),t.expense];return `<tr class="row-income"><td class="label-col">TOTAL / PEMASUKAN</td>${ins.map(v=>`<td>${rupiah(v)}</td>`).join('')}</tr><tr class="row-expense"><td class="label-col">PENGELUARAN</td>${outs.map(v=>`<td>${rupiah(v)}</td>`).join('')}</tr>`;}
function balanceTone(balance){return balance<0?'balance-negative':balance>0?'balance-positive':'balance-zero';}
function grandTotalMarkup(){const t=totals();return `<div><div class="grand-label">TOTAL SEMUA • KESELURUHAN CATATAN</div><div class="grand-description">Saldo bersih gabungan dari seluruh pemasukan dikurangi seluruh pengeluaran. Catatan harian tidak dihitung sebagai saldo terpisah—semua transaksi dijumlahkan bersama.</div><div class="grand-components"><span class="grand-component">Pemasukan ${rupiah(t.income)}</span><span class="grand-component">Pengeluaran ${rupiah(t.expense)}</span></div></div><div class="grand-value">${rupiah(t.balance)}</div>`;}
const DAILY_ORDER_KEY='classcash_daily_order_v1';
let dailyOrder=JSON.parse(localStorage.getItem(DAILY_ORDER_KEY)||'[]');
function dailySummaries(){const byDate=new Map();custom.forEach((x,index)=>{const date=parsePeriodDate(x.period);if(!date)return;if(!byDate.has(date))byDate.set(date,{date,items:[],income:0,expense:0});const g=byDate.get(date);g.items.push(x);if(x.type==='in')g.income+=Number(x.amount||0);else g.expense+=Number(x.amount||0);});let groups=[...byDate.values()];groups.sort((a,b)=>b.date.localeCompare(a.date));const rank=new Map(dailyOrder.map((date,i)=>[date,i]));groups.sort((a,b)=>{const ai=rank.has(a.date)?rank.get(a.date):Infinity,bi=rank.has(b.date)?rank.get(b.date):Infinity;if(ai!==bi)return ai-bi;return b.date.localeCompare(a.date)});return groups;}
function renderDailyLedger(){const el=document.getElementById('dailyLedger');if(!el)return;const groups=dailySummaries();if(!groups.length){el.innerHTML='<div class="daily-ledger-empty">Belum ada catatan harian tambahan. Login sebagai admin, lalu pilih <b>Tambah Transaksi</b> untuk memasukkan pemasukan atau pengeluaran pada tanggal yang tepat.</div>';return;}el.innerHTML=groups.map(g=>`<article class="daily-entry" draggable="true" data-daily-date="${g.date}"><div class="daily-entry-head"><div class="daily-entry-date">${prettyDate(g.date)}</div><span class="drag-grip" title="Seret untuk mengubah urutan">⠿</span></div><div class="daily-values"><div class="daily-value-box"><span>PEMASUKAN</span><strong>${rupiah(g.income)}</strong></div><div class="daily-value-box out"><span>PENGELUARAN</span><strong>${rupiah(g.expense)}</strong></div></div><div class="daily-net"><span>Saldo hari ini</span><strong>${rupiah(g.income-g.expense)}</strong></div><div class="daily-entry-items">${g.items.map(x=>`<span>• ${esc(x.type==='in'?'Masuk':'Keluar')}: <b>${esc(x.desc)}</b> — ${rupiah(Number(x.amount||0))}</span>`).join('')}</div></article>`).join('');
 let draggedDate=null;el.querySelectorAll('.daily-entry').forEach(card=>{card.addEventListener('dragstart',e=>{draggedDate=card.dataset.dailyDate;card.classList.add('dragging');e.dataTransfer.effectAllowed='move';e.dataTransfer.setData('text/plain',draggedDate);});card.addEventListener('dragend',()=>{card.classList.remove('dragging');el.querySelectorAll('.daily-entry').forEach(c=>c.classList.remove('drag-over'));});card.addEventListener('dragover',e=>{e.preventDefault();if(card.dataset.dailyDate!==draggedDate)card.classList.add('drag-over');e.dataTransfer.dropEffect='move';});card.addEventListener('dragleave',()=>card.classList.remove('drag-over'));card.addEventListener('drop',e=>{e.preventDefault();card.classList.remove('drag-over');const from=e.dataTransfer.getData('text/plain')||draggedDate,to=card.dataset.dailyDate;if(!from||from===to)return;const dates=dailySummaries().map(x=>x.date);const remaining=dates.filter(d=>d!==from);const target=remaining.indexOf(to);remaining.splice(target<0?remaining.length:target,0,from);dailyOrder=remaining;localStorage.setItem(DAILY_ORDER_KEY,JSON.stringify(dailyOrder));renderDailyLedger();});});}

function render(){const t=totals();document.querySelectorAll('.matrix thead').forEach(head=>head.innerHTML=matrixHeaderHtml());document.getElementById('incomeTotal').textContent=rupiah(t.income);document.getElementById('expenseTotal').textContent=rupiah(t.expense);const balanceEl=document.getElementById('balanceTotal');balanceEl.textContent=rupiah(t.balance);balanceEl.classList.remove('balance-negative','balance-positive','balance-zero','negative','positive');balanceEl.classList.add(balanceTone(t.balance));document.querySelector('.hero-pill').textContent='Saldo Akhir • '+rupiah(t.balance);document.getElementById('financeBody').innerHTML=matrixHtml();document.getElementById('financeBody2').innerHTML=matrixHtml();document.getElementById('grandTotalDashboard').className='grand-total-box '+balanceTone(t.balance);document.getElementById('grandTotalFinance').className='grand-total-box '+balanceTone(t.balance);document.getElementById('grandTotalDashboard').innerHTML=grandTotalMarkup();document.getElementById('grandTotalFinance').innerHTML=grandTotalMarkup();renderStatus();renderPayments();renderExpenses();renderDailyLedger();populatePeriodFilter();renderTransactions();updateLogin();}
function renderStatus(){const html=WEEK_INFO.map((w,wi)=>{const c=payments.reduce((a,r)=>a+r[wi],0);return `<div class="progress-row"><div class="progress-top"><b>${esc(w.label)}</b><span class="${c===STUDENTS.length?'green':'orange'}">${c}/${STUDENTS.length} siswa</span></div><div class="bar"><span style="width:${c/STUDENTS.length*100}%;background:${c===STUDENTS.length?'#15803d':'#c2410c'}"></span></div></div>`}).join('');document.getElementById('statusBars').innerHTML=html;}
function renderPayments(){const q=(document.getElementById('studentSearch').value||'').toLowerCase();const head='<tr><th>No</th><th>Nama Siswa</th><th>Uang Kas Awal</th>'+WEEK_INFO.map(w=>`<th>${esc(w.label)}</th>`).join('')+'<th>Total Dibayar</th><th>Status</th></tr>';let rows='';STUDENTS.map((name,i)=>({name,i})).filter(x=>x.name.toLowerCase().includes(q)).forEach(x=>{let row=payments[x.i],paidWeeks=row.reduce((a,b)=>a+b,0),total=15000+paidWeeks*5000;rows+=`<tr><td>${x.i+1}</td><td><b>${esc(x.name)}</b></td><td>${rupiah(15000)}</td>`+row.map((paid,wi)=>`<td><div class="payment-cell payment-cell-simple" role="button" tabindex="0" aria-label="${esc(x.name)} — ${esc(WEEK_INFO[wi].label)}: ${paid?'Sudah bayar':'Belum bayar'}${admin?'':'. Login admin untuk mengubah status'}" onclick="togglePayment(${x.i},${wi})" onkeydown="if(event.key===\'Enter\'||event.key===\' \'){event.preventDefault();togglePayment(${x.i},${wi})}"><div class="payment-period">${esc(WEEK_INFO[wi].label)}</div>${paid?'<span class="pay-ok">✓ Rp5.000 · Sudah bayar</span>':'<span class="pay-no">Belum bayar</span>'}</div></td>`).join('')+`<td class="green"><b>${rupiah(total)}</b></td><td><span class="badge ${paidWeeks===WEEK_INFO.length?'paid':'unpaid'}">${paidWeeks===WEEK_INFO.length?'Lengkap':paidWeeks+'/'+WEEK_INFO.length+' minggu'}</span></td></tr>`;});document.querySelector('#paymentsTab thead tr').outerHTML=head;document.getElementById('paymentBody').innerHTML=rows||`<tr><td colspan="11" style="text-align:center;color:var(--muted)">Nama siswa tidak ditemukan.</td></tr>`;}
window.togglePayment=(i,w)=>{if(!admin){toast('Login admin terlebih dahulu.');return;}payments[i][w]=payments[i][w]?0:1;localStorage.setItem(PAYMENT_KEY,JSON.stringify(payments));render();toast('Status pembayaran diperbarui');};
function formatISODateForLabel(iso){
 const d=new Date(iso+'T00:00:00Z');
 return d.toLocaleDateString('id-ID',{day:'2-digit',month:'long',year:'numeric',timeZone:'UTC'});
}
function getMondayISO(iso){
 const d=new Date(iso+'T00:00:00Z');const offset=(d.getUTCDay()+6)%7;d.setUTCDate(d.getUTCDate()-offset);return d.toISOString().slice(0,10);
}
function getSundayISO(mondayISO){const d=new Date(mondayISO+'T00:00:00Z');d.setUTCDate(d.getUTCDate()+6);return d.toISOString().slice(0,10)}
function formatWeekLabel(startISO,endISO){
 const a=new Date(startISO+'T00:00:00Z'),b=new Date(endISO+'T00:00:00Z');
 const dayA=String(a.getUTCDate()).padStart(2,'0'),dayB=String(b.getUTCDate()).padStart(2,'0');
 const monthA=a.toLocaleDateString('id-ID',{month:'long',timeZone:'UTC'}),monthB=b.toLocaleDateString('id-ID',{month:'long',timeZone:'UTC'}),yearB=b.getUTCFullYear();
 return monthA===monthB?`${dayA}–${dayB} ${monthB} ${yearB}`:`${dayA} ${monthA}–${dayB} ${monthB} ${yearB}`;
}
function buildExpenseGroups(){
 const groups=PERIODS.map((p,i)=>({id:`period-${i}`,label:p.label,sourceIndex:i,items:p.descs.map((desc,j)=>({desc,amount:amountOfDesc(desc),sourceId:sourceExpenseId(i,j)})).filter(item=>!deletedSource.includes(item.sourceId))}));
 const futureGroups=new Map();
 custom.filter(x=>x.type==='out').forEach((x,index)=>{
   const date=parsePeriodDate(x.period);const pIndex=customPeriodIndex(x);const item={desc:x.desc,amount:Number(x.amount||0),customId:x.id||`legacy-${index}`};
   if(pIndex>=0){groups[pIndex].items.push(item);return;}
   if(date){const monday=getMondayISO(date),sunday=getSundayISO(monday),id=`future-week-${monday}`;if(!futureGroups.has(id))futureGroups.set(id,{id,label:formatWeekLabel(monday,sunday),sourceIndex:null,items:[]});futureGroups.get(id).items.push(item);}
   else {const id=`undated-${String(x.period||'periode')}`;if(!futureGroups.has(id))futureGroups.set(id,{id,label:String(x.period||'Periode lainnya'),sourceIndex:null,items:[]});futureGroups.get(id).items.push(item);}
 });
 const all=[...groups,...futureGroups.values()];
 all.forEach(g=>g.total=g.items.reduce((sum,item)=>sum+Number(item.amount||0),0));
 return all;
}
function renderExpenses(){
 currentExpenseGroups=buildExpenseGroups();
 document.getElementById('expenseGrid').innerHTML=currentExpenseGroups.map(g=>`<button type="button" class="expense-week-card" data-expense-group="${esc(g.id)}" aria-label="Lihat rincian pengeluaran ${esc(g.label)}"><span class="expense-week-icon">↗</span><span class="expense-week-date">${esc(g.label)}</span><strong class="expense-week-amount">${rupiah(g.total)}</strong><span class="expense-week-hint">Lihat rincian <span aria-hidden="true">→</span></span></button>`).join('');
 document.getElementById('expenseGrid').querySelectorAll('[data-expense-group]').forEach(button=>button.addEventListener('click',()=>openExpenseDetail(button.dataset.expenseGroup)));
}
function openExpenseDetail(groupId){
 const group=currentExpenseGroups.find(g=>g.id===groupId);if(!group)return;
 const items=group.items;
 const total=items.reduce((sum,x)=>sum+Number(x.amount||0),0);
 document.getElementById('expenseDetailTitle').textContent=group.label;
 document.getElementById('expenseDetailTotal').textContent=rupiah(total);
 document.getElementById('expenseDetailList').innerHTML=items.length?items.map(item=>`<div class="expense-detail-row"><span class="expense-detail-dot">•</span><span class="expense-detail-name">${esc(item.desc.replace(/\s*\([\d.]+\)\s*$/,''))}</span><strong>${rupiah(item.amount)}</strong></div>`).join(''):`<div class="expense-detail-empty"><span>✓</span><b>Tidak ada pengeluaran</b><small>Belum ada rincian pengeluaran untuk periode ini.</small></div>`;
 document.getElementById('expenseDetailModal').classList.add('show');
 document.getElementById('expenseDetailModal').setAttribute('aria-hidden','false');
 document.body.classList.add('modal-open');
} 
function closeExpenseDetail(){const modal=document.getElementById('expenseDetailModal');modal.classList.remove('show');modal.setAttribute('aria-hidden','true');document.body.classList.remove('modal-open');}

function parsePeriodDate(text){
 if(!text)return '';
 if(/^\d{4}-\d{2}-\d{2}$/.test(text))return text;
 const m=text.match(/(\d{1,2})\s+(Jan(?:uary)?|Feb(?:ruary)?|Mar(?:ch)?|Apr(?:il)?|May|Jun(?:e)?|Jul(?:y)?|Aug(?:ust)?|Sep(?:tember)?|Oct(?:ober)?|Nov(?:ember)?|Dec(?:ember)?|Januari|Februari|Maret|April|Mei|Juni|Juli|Agustus|September|Oktober|November|Desember)\s+(\d{4})/i);
 if(!m)return '';
 const monthMap={jan:1,january:1,januari:1,feb:2,february:2,februari:2,mar:3,march:3,maret:3,apr:4,april:4,may:5,mei:5,jun:6,june:6,juni:6,jul:7,july:7,juli:7,aug:8,august:8,agustus:8,sep:9,september:9,oct:10,october:10,oktober:10,nov:11,november:11,des:12,dec:12,december:12,desember:12};
 const mm=monthMap[m[2].toLowerCase()]||monthMap[m[2].slice(0,3).toLowerCase()];return mm?`${m[3]}-${String(mm).padStart(2,'0')}-${String(Number(m[1])).padStart(2,'0')}`:'';
}
function prettyDate(iso){if(!iso)return '—';if(!/^\d{4}-\d{2}-\d{2}$/.test(iso))return iso;return new Date(iso+'T00:00:00').toLocaleDateString('id-ID',{day:'2-digit',month:'short',year:'numeric'});}
function allTransactions(){
 const source=PERIODS.flatMap((p,i)=>{
   const rows=[];
   if(!deletedSource.includes(sourceIncomeId(i)))rows.push({id:sourceIncomeId(i),period:p.label,type:'in',desc:'Total pemasukan periode',amount:p.income,admin:'Bendahara',sortDate:PERIOD_STARTS[i],source:true});
   p.descs.forEach((d,j)=>{if(!deletedSource.includes(sourceExpenseId(i,j)))rows.push({id:sourceExpenseId(i,j),period:p.label,type:'out',desc:d,amount:amountOfDesc(d),admin:'Bendahara',sortDate:PERIOD_STARTS[i],source:true});});
   return rows;
 });
 const customRows=custom.map((x,i)=>({...x,id:x.id||`legacy-${i}`,custom:true,sortDate:parsePeriodDate(x.period)||'0000-00-00'}));
 return [...source,...customRows].sort((a,b)=>b.sortDate.localeCompare(a.sortDate)||(a.type==='in'?-1:1));
}
function populatePeriodFilter(){const sel=document.getElementById('periodFilter');if(!sel)return;const current=sel.value||'all';const opts=[['all','Semua periode'],...PERIODS.map((p,i)=>[`period-${i}`,p.label])];sel.innerHTML=opts.map(([v,l])=>`<option value="${v}">${esc(l)}</option>`).join('');sel.value=opts.some(o=>o[0]===current)?current:'all';}
function renderTransactions(){
 const q=(document.getElementById('search').value||'').toLowerCase(),f=document.getElementById('filter').value,pf=document.getElementById('periodFilter').value,from=document.getElementById('dateFrom').value,to=document.getElementById('dateTo').value;
 let rows=allTransactions().filter(x=>{
   if(f!=='all'&&x.type!==f)return false;
   if(pf!=='all'){const idx=Number(pf.slice(7));if(x.source){if(x.period!==PERIODS[idx].label)return false;}else {const date=parsePeriodDate(x.period);if(!date||date<PERIOD_STARTS[idx]||date>(PERIODS[idx+1]?PERIOD_STARTS[idx+1]:'9999-12-31'))return false;}}
   if(from&&(!x.sortDate||x.sortDate<from))return false;
   if(to&&(!x.sortDate||x.sortDate>to))return false;
   if(!(`${x.period} ${x.desc}`).toLowerCase().includes(q))return false;
   return true;
 });
 const inc=rows.filter(x=>x.type==='in').reduce((a,x)=>a+Number(x.amount),0),exp=rows.filter(x=>x.type==='out').reduce((a,x)=>a+Number(x.amount),0);
 document.getElementById('filteredSummary').innerHTML=`<div class="summary-chip income"><span>PEMASUKAN TERFILTER</span><b>${rupiah(inc)}</b></div><div class="summary-chip expense"><span>PENGELUARAN TERFILTER</span><b>${rupiah(exp)}</b></div><div class="summary-chip balance"><span>SELISIH TERFILTER</span><b>${rupiah(inc-exp)}</b></div>`;
 document.getElementById('txBody').innerHTML=rows.map(x=>`<tr><td>${esc(x.custom?prettyDate(x.sortDate):x.period)}${x.source?`<div class="tiny">Awal periode: ${prettyDate(x.sortDate)}</div>`:''}</td><td><span class="badge ${x.type==='in'?'paid':'unpaid'}">${x.type==='in'?'Pemasukan':'Pengeluaran'}</span></td><td>${esc(x.desc)}</td><td class="${x.type==='in'?'green':'red'}"><b>${x.type==='in'?'+':'−'} ${rupiah(x.amount)}</b></td><td>${esc(x.admin||'Admin')}</td><td>${admin?`<button class="action-delete" onclick="deleteTransaction('${x.id}')">Hapus</button>`:'<span class="action-locked">Admin saja</span>'}</td></tr>`).join('')||`<tr><td colspan="6" style="text-align:center;color:var(--muted);padding:22px">Tidak ada transaksi yang cocok dengan filter.</td></tr>`;
}
let pendingDeleteId=null;
function openDeleteConfirm(id){
 if(!admin){toast('Login admin terlebih dahulu.');return;}
 const tx=allTransactions().find(x=>x.id===id);if(!tx)return;
 pendingDeleteId=id;
 const desc=String(tx.desc||'Transaksi');
 document.getElementById('deleteConfirmMessage').textContent=`Kamu akan menghapus “${desc}” senilai ${rupiah(tx.amount)}. Transaksi ini akan dihapus dari rekap. Yakin ingin melanjutkan?`;
 const overlay=document.getElementById('deleteConfirmModal');
 overlay.classList.remove('bursting');overlay.classList.add('show');overlay.setAttribute('aria-hidden','false');
 document.getElementById('deleteConfirmAccept').disabled=false;
 document.getElementById('deleteConfirmCancel').disabled=false;
 document.getElementById('deleteConfirmCancel').focus();
}
function finishDeleteBubble(shouldDelete){
 const overlay=document.getElementById('deleteConfirmModal');
 if(!overlay.classList.contains('show'))return;
 if(overlay.classList.contains('bursting'))return;
 overlay.classList.add('bursting');
 document.getElementById('deleteConfirmAccept').disabled=true;
 document.getElementById('deleteConfirmCancel').disabled=true;
 const complete=()=>{
   overlay.classList.remove('show','bursting');overlay.setAttribute('aria-hidden','true');
   document.getElementById('deleteConfirmAccept').disabled=false;document.getElementById('deleteConfirmCancel').disabled=false;
   const id=pendingDeleteId;pendingDeleteId=null;
   if(shouldDelete && id!==null){
     const tx=allTransactions().find(x=>String(x.id)===String(id));
     if(tx){
       if(tx.custom){custom=custom.filter(x=>String(x.id||'')!==String(id));localStorage.setItem('classcash_custom_tx_v2',JSON.stringify(custom));}
       else{if(!deletedSource.includes(id))deletedSource.push(id);localStorage.setItem('classcash_deleted_source_tx_v1',JSON.stringify(deletedSource));}
       render();toast('Transaksi berhasil dihapus.');
     }
   }
 };
 const reduced=window.matchMedia&&window.matchMedia('(prefers-reduced-motion: reduce)').matches;
 window.setTimeout(complete,reduced?20:430);
}
window.deleteTransaction=id=>openDeleteConfirm(id);
function showTab(name){['dashboard','payments','finance','transactions'].forEach(x=>document.getElementById(x+'Tab').style.display=x===name?'block':'none');document.getElementById('title').textContent=name==='dashboard'?'Dashboard Kas Kelas':name==='payments'?'Rekap Pembayaran Siswa':name==='finance'?'Rekap Keuangan':'Transaksi';document.querySelectorAll('.nav button').forEach(b=>b.classList.toggle('active',b.dataset.tab===name));}
function updateLogin(){document.getElementById('loginBtn').textContent=admin?'🚪 Logout':'🔐 Admin Login';}
function toast(t){const e=document.getElementById('toast');e.textContent=t;e.classList.add('show');setTimeout(()=>e.classList.remove('show'),1800);}
document.querySelectorAll('.nav button').forEach(b=>b.onclick=()=>showTab(b.dataset.tab));document.getElementById('studentSearch').oninput=renderPayments;document.getElementById('search').oninput=renderTransactions;document.getElementById('filter').onchange=renderTransactions;document.getElementById('periodFilter').onchange=renderTransactions;document.getElementById('dateFrom').onchange=renderTransactions;document.getElementById('dateTo').onchange=renderTransactions;document.getElementById('clearDateFilters').onclick=()=>{document.getElementById('dateFrom').value='';document.getElementById('dateTo').value='';document.getElementById('periodFilter').value='all';calendarState.transaction.selected='';renderCalendar('transaction');document.getElementById('transactionCalendar').querySelector('.calendar-note').textContent='Pilih tanggal untuk memfilter transaksi pada hari itu.';updateCalendarTrigger('transaction');closeCalendarModal('transaction');renderTransactions();};
const loginModal=document.getElementById('loginModal'),addModal=document.getElementById('addModal');document.getElementById('loginBtn').onclick=()=>{if(admin){admin=false;localStorage.removeItem('classcash_admin_final_v2');updateLogin();renderPayments();toast('Logout berhasil');}else{document.getElementById('loginError').hidden=true;document.getElementById('password').value='';loginModal.classList.add('show');document.getElementById('username').focus();}};document.getElementById('loginClose').onclick=()=>loginModal.classList.remove('show');document.getElementById('loginForm').onsubmit=e=>{e.preventDefault();if(document.getElementById('username').value===USER&&document.getElementById('password').value===PASS){admin=true;localStorage.setItem('classcash_admin_final_v2','1');loginModal.classList.remove('show');document.getElementById('loginError').hidden=true;updateLogin();renderPayments();renderTransactions();toast('Login admin berhasil');}else{document.getElementById('loginError').hidden=false;document.getElementById('password').focus();}};document.getElementById('addBtn').onclick=()=>{if(!admin){toast('Login admin terlebih dahulu.');return;}addModal.classList.add('show')};document.getElementById('addClose').onclick=()=>addModal.classList.remove('show');document.getElementById('addForm').onsubmit=e=>{e.preventDefault();custom.push({id:'custom-'+Date.now(),period:document.getElementById('newPeriod').value,type:document.getElementById('newType').value,desc:document.getElementById('newDesc').value,amount:Number(document.getElementById('newAmount').value),admin:'Admin'});localStorage.setItem('classcash_custom_tx_v2',JSON.stringify(custom));addModal.classList.remove('show');e.target.reset();render();toast('Transaksi ditambahkan');};
function openPaymentWeekModal(){if(!admin){toast('Login admin terlebih dahulu.');return;}const today=new Date(),todayISO=`${today.getFullYear()}-${String(today.getMonth()+1).padStart(2,'0')}-${String(today.getDate()).padStart(2,'0')}`;let start=getMondayISO(todayISO);const knownEnds=[...PERIOD_ENDS,...WEEK_INFO.slice(BASE_WEEK_INFO.length).map(w=>w.end)].filter(Boolean).sort();const latestEnd=knownEnds[knownEnds.length-1]||todayISO;if(start<=latestEnd)start=getMondayISO(addIsoDays(latestEnd,1));document.getElementById('paymentWeekStart').value=start;document.getElementById('paymentWeekEnd').value=addIsoDays(start,4);document.getElementById('paymentWeekError').hidden=true;document.getElementById('paymentWeekModal').classList.add('show');}
const paymentWeekModal=document.getElementById('paymentWeekModal');document.getElementById('addPaymentWeekBtn').onclick=openPaymentWeekModal;document.getElementById('paymentWeekClose').onclick=()=>paymentWeekModal.classList.remove('show');document.getElementById('paymentWeekStart').onchange=()=>{const start=document.getElementById('paymentWeekStart').value;if(start&&!document.getElementById('paymentWeekEnd').value)document.getElementById('paymentWeekEnd').value=addIsoDays(start,4);};document.getElementById('paymentWeekForm').onsubmit=e=>{e.preventDefault();if(!admin){paymentWeekModal.classList.remove('show');toast('Login admin terlebih dahulu.');return;}const start=document.getElementById('paymentWeekStart').value,end=document.getElementById('paymentWeekEnd').value,error=document.getElementById('paymentWeekError');if(!start||!end||start>end){error.textContent='Tanggal selesai harus sama dengan atau setelah tanggal mulai.';error.hidden=false;return;}const ranges=[...PERIOD_STARTS.map((value,i)=>({start:value,end:PERIOD_ENDS[i],label:PERIODS[i].label})),...WEEK_INFO.map(w=>({start:w.start,end:w.end,label:w.label}))];const overlap=ranges.find(r=>start<=r.end&&end>=r.start);if(overlap){error.textContent=`Periode ini bertabrakan dengan minggu yang sudah ada: ${overlap.label}. Pilih tanggal yang berbeda.`;error.hidden=false;return;}const week={id:'payment-week-'+Date.now(),start,end,label:formatWeekLabel(start,end),days:[]};extraPaymentWeeks.push(week);WEEK_INFO.push(week);localStorage.setItem(PAYMENT_WEEKS_KEY,JSON.stringify(extraPaymentWeeks));payments.forEach(row=>row.push(0));localStorage.setItem(PAYMENT_KEY,JSON.stringify(payments));paymentWeekModal.classList.remove('show');e.target.reset();render();renderCalendar('payment');toast('Minggu pembayaran baru ditambahkan');};

document.getElementById('expenseDetailModal').addEventListener('click',e=>{if(e.target.id==='expenseDetailModal')closeExpenseDetail();});
document.getElementById('deleteConfirmAccept').onclick=()=>finishDeleteBubble(true);
document.getElementById('deleteConfirmCancel').onclick=()=>finishDeleteBubble(false);
document.getElementById('deleteConfirmBackdrop').onclick=()=>finishDeleteBubble(false);
document.addEventListener('keydown',e=>{if(e.key==='Escape'){closeExpenseDetail();finishDeleteBubble(false);closeCalendarModal('payment');closeCalendarModal('transaction');document.getElementById('paymentWeekModal').classList.remove('show');document.getElementById('addModal').classList.remove('show');document.getElementById('loginModal').classList.remove('show');}});
document.getElementById('themeBtn').onclick=()=>{document.body.classList.toggle('dark');localStorage.setItem('classcash_theme_v2',document.body.classList.contains('dark')?'1':'0');};if(localStorage.getItem('classcash_theme_v2')==='1')document.body.classList.add('dark');

// Lightweight custom month calendars; transaction dates filter the table, payment dates identify the matching weekly period.
const calendarState={payment:{year:2026,month:8,selected:''},transaction:{year:2026,month:8,selected:''}};
const monthNamesID=['Januari','Februari','Maret','April','Mei','Juni','Juli','Agustus','September','Oktober','November','Desember'];
const calendarCloseTimers={};
function calendarFieldDate(iso){if(!iso)return 'dd/mm/yy';const [y,m,d]=iso.split('-');return `${d}/${m}/${y.slice(-2)}`;}
function updateCalendarTrigger(kind){const trigger=document.getElementById(kind+'CalendarTrigger');if(trigger){trigger.querySelector('.calendar-trigger-date').textContent=calendarFieldDate(calendarState[kind].selected);}}
function openCalendarModal(kind){const overlay=document.getElementById(kind+'CalendarOverlay'),trigger=document.getElementById(kind+'CalendarTrigger');if(!overlay)return;clearTimeout(calendarCloseTimers[kind]);overlay.classList.remove('closing');overlay.classList.add('show');overlay.setAttribute('aria-hidden','false');trigger?.setAttribute('aria-expanded','true');document.body.classList.add('calendar-modal-open');overlay.querySelector('.calendar-modal-close')?.focus();}
function closeCalendarModal(kind){const overlay=document.getElementById(kind+'CalendarOverlay'),trigger=document.getElementById(kind+'CalendarTrigger');if(!overlay||!overlay.classList.contains('show'))return;overlay.classList.add('closing');overlay.setAttribute('aria-hidden','true');trigger?.setAttribute('aria-expanded','false');document.body.classList.remove('calendar-modal-open');calendarCloseTimers[kind]=setTimeout(()=>{overlay.classList.remove('show','closing');trigger?.focus({preventScroll:true});},180);}
function setupCalendarModal(kind){const panel=document.getElementById(kind+'Calendar');if(!panel||document.getElementById(kind+'CalendarOverlay'))return;const isPayment=kind==='payment';const trigger=document.createElement('button');trigger.type='button';trigger.id=kind+'CalendarTrigger';trigger.className='calendar-trigger';trigger.setAttribute('aria-haspopup','dialog');trigger.setAttribute('aria-expanded','false');trigger.innerHTML=`<span class="calendar-trigger-left"><span class="calendar-trigger-icon" aria-hidden="true">▦</span><span class="calendar-trigger-copy"><span class="calendar-trigger-label">${isPayment?'TANGGAL PEMBAYARAN':'TANGGAL TRANSAKSI'}</span><strong class="calendar-trigger-date">dd/mm/yy</strong></span></span><span class="calendar-trigger-chevron" aria-hidden="true">⌄</span>`;panel.parentNode.insertBefore(trigger,panel);const overlay=document.createElement('div');overlay.id=kind+'CalendarOverlay';overlay.className='calendar-modal-overlay';overlay.setAttribute('aria-hidden','true');overlay.innerHTML=`<button type="button" class="calendar-modal-backdrop" aria-label="Tutup kalender"></button><section class="calendar-modal-card" role="dialog" aria-modal="true" aria-labelledby="${kind}CalendarModalTitle"><div class="calendar-modal-top"><div><div class="calendar-modal-kicker">PILIH TANGGAL</div><h3 id="${kind}CalendarModalTitle">${isPayment?'Kalender Pembayaran':'Kalender Transaksi'}</h3></div><button type="button" class="calendar-modal-close" aria-label="Tutup kalender">×</button></div></section>`;const modalCard=overlay.querySelector('.calendar-modal-card');panel.classList.add('calendar-modal-panel');modalCard.appendChild(panel);document.body.appendChild(overlay);trigger.addEventListener('click',()=>openCalendarModal(kind));overlay.querySelector('.calendar-modal-backdrop').addEventListener('click',()=>closeCalendarModal(kind));overlay.querySelector('.calendar-modal-close').addEventListener('click',()=>closeCalendarModal(kind));}
function isoLocal(y,m,d){return `${y}-${String(m+1).padStart(2,'0')}-${String(d).padStart(2,'0')}`;}
function renderCalendar(kind){
 const panel=document.getElementById(kind+'Calendar');if(!panel)return;
 const st=calendarState[kind],first=new Date(st.year,st.month,1),offset=first.getDay(),days=new Date(st.year,st.month+1,0).getDate(),prevDays=new Date(st.year,st.month,0).getDate();
 panel.querySelector('.calendar-title').textContent=`${monthNamesID[st.month]} ${st.year}`;
 let html='';
 for(let i=0;i<42;i++){
   let day,yy=st.year,mm=st.month,outside=false;
   if(i<offset){day=prevDays-offset+i+1;mm--;outside=true;if(mm<0){mm=11;yy--;}}
   else if(i>=offset+days){day=i-offset-days+1;mm++;outside=true;if(mm>11){mm=0;yy++;}}
   else day=i-offset+1;
   const iso=isoLocal(yy,mm,day);
   let periodDay=false;
   if(kind==='payment')periodDay=paymentWeekForDate(iso)>=0;
   html+=`<button type="button" class="calendar-day${outside?' outside':''}${st.selected===iso?' selected':''}${periodDay?' period-day':''}" data-date="${iso}" aria-pressed="${st.selected===iso}">${day}</button>`;
 }
 panel.querySelector('.calendar-days').innerHTML=html;
 updateCalendarTrigger(kind);
 panel.querySelectorAll('[data-date]').forEach(b=>b.addEventListener('click',()=>{
   st.selected=b.dataset.date;
   if(kind==='transaction'){
     document.getElementById('dateFrom').value=st.selected;document.getElementById('dateTo').value=st.selected;document.getElementById('periodFilter').value='all';renderTransactions();
     panel.querySelector('.calendar-note').textContent=`Transaksi difilter untuk ${prettyDate(st.selected)}. Gunakan Reset tanggal untuk menghapus filter.`;
   }else{
     const wi=paymentWeekForDate(st.selected);
     panel.querySelector('.calendar-note').textContent=wi>=0?`Tanggal ${prettyDate(st.selected)} termasuk periode pembayaran: ${WEEK_INFO[wi].label}. Status dapat diubah dengan mengeklik seluruh blok siswa pada kolom periode tersebut.`:`Tanggal ${prettyDate(st.selected)} tidak termasuk periode mingguan yang tercatat.`;
   }
   renderCalendar(kind);
   if(kind==='payment'){
     const wi=paymentWeekForDate(st.selected);
     panel.querySelector('.calendar-note').textContent=wi>=0?`Tanggal ${prettyDate(st.selected)} termasuk periode pembayaran: ${WEEK_INFO[wi].label}. Klik blok pembayaran siswa untuk mengubah status.`:`Tanggal ${prettyDate(st.selected)} tidak termasuk periode mingguan yang tercatat.`;
   }else panel.querySelector('.calendar-note').textContent=`Transaksi difilter untuk ${prettyDate(st.selected)}. Gunakan Reset tanggal untuk menghapus filter.`;
   closeCalendarModal(kind);
 }));
}
function paymentWeekForDate(iso){return WEEK_INFO.findIndex(w=>Boolean(w.start&&w.end&&iso>=w.start&&iso<=w.end));}
['payment','transaction'].forEach(setupCalendarModal);
['payment','transaction'].forEach(kind=>{
 const panel=document.getElementById(kind+'Calendar');
 panel.querySelector('.calendar-prev').onclick=()=>{const st=calendarState[kind];st.month--;if(st.month<0){st.month=11;st.year--;}renderCalendar(kind);};
 panel.querySelector('.calendar-next').onclick=()=>{const st=calendarState[kind];st.month++;if(st.month>11){st.month=0;st.year++;}renderCalendar(kind);};
 renderCalendar(kind);
});

render();

// Click-and-drag horizontal scrolling for wide tables. Mouse clicks on buttons still work.
(function enableMouseDragScroll(){
  document.querySelectorAll('.table-scroll').forEach(function(scroller){
    let pointerDown=false, startX=0, startScrollLeft=0, didDrag=false, pointerId=null;
    scroller.addEventListener('pointerdown',function(e){
      if(e.pointerType==='mouse' && e.button!==0) return;
      if(e.target.closest('button,input,select,textarea,a,label')) return;
      pointerDown=true; didDrag=false; startX=e.clientX; startScrollLeft=scroller.scrollLeft; pointerId=e.pointerId;
      scroller.classList.add('is-dragging');
    });
    window.addEventListener('pointermove',function(e){
      if(!pointerDown || (pointerId!==null && e.pointerId!==pointerId)) return;
      const dx=e.clientX-startX;
      if(Math.abs(dx)>4) didDrag=true;
      if(didDrag){ scroller.scrollLeft=startScrollLeft-dx; if(e.cancelable)e.preventDefault(); }
    },{passive:false});
    function endDrag(){pointerDown=false;pointerId=null;scroller.classList.remove('is-dragging');}
    window.addEventListener('pointerup',endDrag); window.addEventListener('pointercancel',endDrag);
    scroller.addEventListener('wheel',function(e){
      if(e.shiftKey && Math.abs(e.deltaY)>Math.abs(e.deltaX)){scroller.scrollLeft+=e.deltaY;e.preventDefault();}
    },{passive:false});
    scroller.addEventListener('dragstart',e=>e.preventDefault());
  });
})();
</script>
</body></html>
