<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>My Daily Routine – English Worksheet</title>
<link href="https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800;900&display=swap" rel="stylesheet">
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'Nunito',sans-serif;background:#F0EDFF;min-height:100vh;padding:24px 16px}
.page{max-width:780px;margin:0 auto}
 
.page-header{background:linear-gradient(135deg,#7C3AED,#4F46E5,#2563EB);border-radius:20px;padding:24px 32px;margin-bottom:22px;color:white;display:flex;align-items:center;gap:18px}
.header-icon{font-size:40px;line-height:1}
.page-header h1{font-size:26px;font-weight:900;letter-spacing:-0.5px}
.page-header p{font-size:14px;opacity:.85;margin-top:4px}
.progress-bar{background:rgba(255,255,255,.2);border-radius:20px;height:8px;margin-top:10px;overflow:hidden}
.progress-fill{background:white;height:100%;border-radius:20px;transition:width .5s ease;width:0%}
.progress-label{font-size:12px;opacity:.8;margin-top:4px}
 
.section{border-radius:18px;margin-bottom:22px;overflow:hidden;border:2.5px solid}
.s1{border-color:#7C3AED}.s2{border-color:#2563EB}.s3{border-color:#059669}
.sec-head{display:flex;align-items:center;gap:12px;padding:14px 22px;color:white}
.s1 .sec-head{background:#7C3AED}.s2 .sec-head{background:#2563EB}.s3 .sec-head{background:#059669}
.sec-num{width:34px;height:34px;border-radius:50%;background:rgba(255,255,255,.25);display:flex;align-items:center;justify-content:center;font-weight:900;font-size:17px;flex-shrink:0}
.sec-head h2{font-size:18px;font-weight:800}
.sec-head .hicon{font-size:24px;margin-left:auto;opacity:.85}
.sec-body{padding:20px 22px;background:white}
 
.instr{border-radius:10px;padding:10px 16px;font-size:13px;font-weight:700;margin-bottom:18px;display:flex;align-items:center;gap:8px}
.s1 .instr{background:#EDE9FE;color:#5B21B6}
.s2 .instr{background:#DBEAFE;color:#1E40AF}
.s3 .instr{background:#D1FAE5;color:#065F46}
 
/* EX1 */
.ex1-wrap{display:flex;gap:18px;align-items:flex-start;flex-wrap:wrap}
.illus{flex:0 0 320px;border-radius:14px;overflow:hidden;border:2px solid #DDD6FE}
.vocab-panel{flex:1;min-width:200px}
.vbank-label{font-size:11px;font-weight:800;color:#7C3AED;text-transform:uppercase;letter-spacing:.5px;margin-bottom:8px}
.word-bank{background:#EDE9FE;border-radius:10px;padding:10px 12px;margin-bottom:16px;display:flex;flex-wrap:wrap;gap:6px}
.word-pill{background:white;border:1.5px solid #C4B5FD;border-radius:20px;padding:4px 12px;font-size:12px;font-weight:700;color:#5B21B6}
.vocab-items{display:flex;flex-direction:column;gap:8px}
.vi{display:flex;align-items:center;gap:8px}
.vnum{width:22px;height:22px;border-radius:50%;background:#7C3AED;color:white;font-size:11px;font-weight:800;display:flex;align-items:center;justify-content:center;flex-shrink:0}
.vi select{flex:1;border:2px solid #C4B5FD;border-radius:8px;padding:5px 8px;font-family:'Nunito',sans-serif;font-size:12px;font-weight:700;color:#5B21B6;background:#FAFAFE;cursor:pointer;outline:none}
.vi select:focus{border-color:#7C3AED}
.vi select.correct{border-color:#059669;background:#D1FAE5;color:#065F46}
.vi select.wrong{border-color:#DC2626;background:#FEE2E2;color:#991B1B}
 
/* EX2 */
.clocks-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:14px}
.clock-card{border:1.5px solid #BFDBFE;border-radius:12px;padding:12px;text-align:center;background:#F0F7FF}
.clk-lbl{font-size:11px;font-weight:800;color:#1E40AF;background:#DBEAFE;border-radius:6px;padding:2px 8px;display:inline-block;margin-bottom:8px}
.opts{margin-top:10px;text-align:left}
.opt-btn{display:flex;align-items:center;gap:8px;margin-bottom:6px;cursor:pointer;padding:5px 8px;border-radius:8px;border:1.5px solid transparent;transition:.15s;width:100%}
.opt-btn:hover{background:#DBEAFE;border-color:#93C5FD}
.opt-btn.selected{background:#DBEAFE;border-color:#2563EB}
.opt-btn.correct{background:#D1FAE5;border-color:#059669}
.opt-btn.wrong{background:#FEE2E2;border-color:#DC2626}
.opt-circ{width:16px;height:16px;border-radius:50%;border:2px solid #93C5FD;background:white;flex-shrink:0;display:flex;align-items:center;justify-content:center;font-size:10px}
.opt-btn.selected .opt-circ{background:#2563EB;border-color:#2563EB;color:white}
.opt-btn.correct .opt-circ{background:#059669;border-color:#059669;color:white}
.opt-btn.wrong .opt-circ{background:#DC2626;border-color:#DC2626;color:white}
.opt-text{font-size:11.5px;color:#1E3A5F;font-weight:700}
 
/* EX3 */
.freq-chips{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:16px}
.fchip{padding:6px 16px;border-radius:20px;font-size:13px;font-weight:800}
.fc1{background:#D1FAE5;color:#065F46;border:1.5px solid #6EE7B7}
.fc2{background:#DBEAFE;color:#1E40AF;border:1.5px solid #93C5FD}
.fc3{background:#FEF3C7;color:#92400E;border:1.5px solid #FCD34D}
.fc4{background:#FEE2E2;color:#991B1B;border:1.5px solid #FCA5A5}
.sent-list{display:flex;flex-direction:column;gap:10px}
.sent-row{display:flex;align-items:center;gap:10px;background:#F9F9F9;border-radius:10px;padding:10px 14px;border:1.5px solid #E5E7EB}
.snum{width:26px;height:26px;border-radius:50%;background:#059669;color:white;font-size:13px;font-weight:800;display:flex;align-items:center;justify-content:center;flex-shrink:0}
.sent-text{font-size:13px;color:#1F2937;font-weight:600;line-height:1.6;flex:1}
.sent-row.correct-row{background:#D1FAE5;border-color:#6EE7B7}
.sent-row.wrong-row{background:#FEE2E2;border-color:#FCA5A5}
.inline-sel{border:2px solid #6EE7B7;border-radius:8px;padding:3px 6px;font-family:'Nunito',sans-serif;font-size:12px;font-weight:800;color:#065F46;background:#D1FAE5;cursor:pointer;outline:none;margin:0 3px}
.inline-sel:focus{border-color:#059669}
.inline-sel.correct{border-color:#059669;background:#D1FAE5;color:#065F46}
.inline-sel.wrong{border-color:#DC2626;background:#FEE2E2;color:#991B1B}
 
/* Submit button */
.submit-wrap{text-align:center;margin:26px 0 8px}
.submit-btn{background:linear-gradient(135deg,#7C3AED,#2563EB);color:white;border:none;padding:14px 40px;border-radius:40px;font-family:'Nunito',sans-serif;font-size:16px;font-weight:900;cursor:pointer;letter-spacing:.3px;transition:.2s}
.submit-btn:hover{transform:scale(1.04)}
.submit-btn:active{transform:scale(.97)}
.submit-btn:disabled{opacity:.5;cursor:not-allowed;transform:none}
 
/* Result */
.result-box{border-radius:18px;padding:24px 28px;margin-top:20px;text-align:center;border:3px solid}
.result-box.great{background:#D1FAE5;border-color:#059669}
.result-box.good{background:#DBEAFE;border-color:#2563EB}
.result-box.keep{background:#FEF3C7;border-color:#D97706}
.result-emoji{font-size:52px;margin-bottom:8px}
.result-score{font-size:36px;font-weight:900;margin-bottom:4px}
.result-box.great .result-score{color:#065F46}
.result-box.good .result-score{color:#1E40AF}
.result-box.keep .result-score{color:#92400E}
.result-msg{font-size:16px;font-weight:700;margin-bottom:12px}
.result-box.great .result-msg{color:#065F46}
.result-box.good .result-msg{color:#1E40AF}
.result-box.keep .result-msg{color:#92400E}
.breakdown{display:flex;gap:12px;justify-content:center;flex-wrap:wrap;margin-top:12px}
.bd-item{background:white;border-radius:12px;padding:10px 18px;font-size:13px;font-weight:700}
.bd-item span{display:block;font-size:22px;font-weight:900;text-align:center}
.retry-btn{margin-top:16px;background:white;border:2px solid;padding:10px 28px;border-radius:30px;font-family:'Nunito',sans-serif;font-size:14px;font-weight:800;cursor:pointer;transition:.2s}
.result-box.great .retry-btn{color:#065F46;border-color:#059669}
.result-box.good .retry-btn{color:#1E40AF;border-color:#2563EB}
.result-box.keep .retry-btn{color:#92400E;border-color:#D97706}
.retry-btn:hover{transform:scale(1.04)}
 
@media(max-width:600px){
  .ex1-wrap{flex-direction:column}
  .illus{flex:none;width:100%}
  .clocks-grid{grid-template-columns:repeat(2,1fr)}
  .page-header{padding:18px 20px}
  .sec-body{padding:16px}
}
</style>
</head>
<body>
<div class="page">
 
<div class="page-header">
  <div class="header-icon">🌟</div>
  <div style="flex:1">
    <h1>My Daily Routine</h1>
    <p>English Worksheet &nbsp;•&nbsp; Answer all questions and check your score!</p>
    <div class="progress-bar"><div class="progress-fill" id="progressFill"></div></div>
    <div class="progress-label" id="progressLabel">0 of 17 answered</div>
  </div>
</div>
 
<!-- SECTION 1 -->
<div class="section s1">
  <div class="sec-head">
    <div class="sec-num">1</div>
    <h2>Vocabulary Practice</h2>
    <div class="hicon">✏️</div>
  </div>
  <div class="sec-body">
    <div class="instr">👀 Look at the picture. Choose the correct word for each number.</div>
    <div class="ex1-wrap">
      <div class="illus">
        <svg width="320" viewBox="0 0 320 290" xmlns="http://www.w3.org/2000/svg">
          <rect width="320" height="290" fill="#E8F4FD"/>
          <rect x="0" y="220" width="320" height="70" fill="#E8E0F0"/>
          <rect x="0" y="0" width="320" height="222" fill="#FFF8F0"/>
          <rect x="250" y="18" width="58" height="58" rx="6" fill="#BAE6FD" stroke="#93C5FD" stroke-width="2"/>
          <line x1="279" y1="18" x2="279" y2="76" stroke="#93C5FD" stroke-width="1.5"/>
          <line x1="250" y1="47" x2="308" y2="47" stroke="#93C5FD" stroke-width="1.5"/>
          <circle cx="279" cy="33" r="9" fill="#FCD34D"/>
          <rect x="8" y="18" width="48" height="58" rx="4" fill="#BFDBFE" stroke="#93C5FD" stroke-width="1.5"/>
          <circle cx="46" cy="108" r="13" fill="#FBBF24"/>
          <circle cx="42" cy="105" r="2" fill="#374151"/><circle cx="50" cy="105" r="2" fill="#374151"/>
          <path d="M42 113 Q46 117 50 113" stroke="#374151" stroke-width="1.5" fill="none"/>
          <path d="M34 105 Q36 94 46 95 Q56 94 58 105" fill="#92400E"/>
          <rect x="36" y="121" width="20" height="28" rx="6" fill="#A78BFA"/>
          <line x1="56" y1="128" x2="70" y2="118" stroke="#FBBF24" stroke-width="4" stroke-linecap="round"/>
          <rect x="70" y="113" width="15" height="5" rx="2" fill="#EF4444"/>
          <rect x="72" y="110" width="11" height="4" rx="1" fill="#F9FAFB"/>
          <circle cx="22" cy="86" r="9" fill="#7C3AED"/>
          <text x="22" y="90" text-anchor="middle" fill="white" font-family="Nunito,sans-serif" font-size="11" font-weight="800">1</text>
          <rect x="95" y="174" width="76" height="12" rx="4" fill="#D97706"/>
          <rect x="105" y="186" width="8" height="30" rx="2" fill="#B45309"/>
          <rect x="155" y="186" width="8" height="30" rx="2" fill="#B45309"/>
          <ellipse cx="133" cy="175" rx="17" ry="7" fill="#FEF3C7" stroke="#FCD34D" stroke-width="1.5"/>
          <line x1="150" y1="167" x2="158" y2="177" stroke="#9CA3AF" stroke-width="2" stroke-linecap="round"/>
          <circle cx="133" cy="145" r="13" fill="#FDE68A"/>
          <circle cx="129" cy="142" r="2" fill="#374151"/><circle cx="137" cy="142" r="2" fill="#374151"/>
          <path d="M129 150 Q133 154 137 150" stroke="#374151" stroke-width="1.5" fill="none"/>
          <path d="M121 139 Q123 129 133 130 Q143 129 145 139" fill="#92400E"/>
          <rect x="123" y="158" width="20" height="24" rx="6" fill="#34D399"/>
          <circle cx="100" cy="160" r="9" fill="#7C3AED"/>
          <text x="100" y="164" text-anchor="middle" fill="white" font-family="Nunito,sans-serif" font-size="11" font-weight="800">2</text>
          <rect x="178" y="180" width="66" height="10" rx="3" fill="#D97706"/>
          <rect x="185" y="190" width="6" height="27" rx="2" fill="#B45309"/>
          <rect x="232" y="190" width="6" height="27" rx="2" fill="#B45309"/>
          <rect x="188" y="167" width="30" height="13" rx="2" fill="#DBEAFE" stroke="#93C5FD" stroke-width="1"/>
          <line x1="203" y1="167" x2="203" y2="180" stroke="#93C5FD" stroke-width="1"/>
          <rect x="222" y="166" width="5" height="14" rx="1" fill="#FCD34D"/>
          <polygon points="222,180 227,180 224.5,185" fill="#F97316"/>
          <circle cx="210" cy="145" r="13" fill="#FCA5A5"/>
          <circle cx="206" cy="142" r="2" fill="#374151"/><circle cx="214" cy="142" r="2" fill="#374151"/>
          <path d="M206 150 Q210 153 214 150" stroke="#374151" stroke-width="1.5" fill="none"/>
          <path d="M198 139 Q200 130 210 130 Q220 130 222 139" fill="#7C3AED"/>
          <rect x="200" y="158" width="20" height="24" rx="6" fill="#60A5FA"/>
          <line x1="210" y1="168" x2="210" y2="180" stroke="#FCA5A5" stroke-width="4" stroke-linecap="round"/>
          <circle cx="180" cy="160" r="9" fill="#7C3AED"/>
          <text x="180" y="164" text-anchor="middle" fill="white" font-family="Nunito,sans-serif" font-size="11" font-weight="800">3</text>
          <ellipse cx="285" cy="214" rx="17" ry="11" fill="#D97706"/>
          <circle cx="302" cy="207" r="8" fill="#D97706"/>
          <circle cx="308" cy="206" r="1.5" fill="#374151"/>
          <line x1="270" y1="220" x2="266" y2="234" stroke="#D97706" stroke-width="3" stroke-linecap="round"/>
          <line x1="278" y1="223" x2="276" y2="237" stroke="#D97706" stroke-width="3" stroke-linecap="round"/>
          <line x1="292" y1="223" x2="294" y2="236" stroke="#D97706" stroke-width="3" stroke-linecap="round"/>
          <line x1="300" y1="221" x2="304" y2="235" stroke="#D97706" stroke-width="3" stroke-linecap="round"/>
          <path d="M268 214 Q260 204 264 197" stroke="#D97706" stroke-width="3" fill="none" stroke-linecap="round"/>
          <path d="M302 207 Q308 200 296 188" stroke="#6B7280" stroke-width="1.5" fill="none"/>
          <circle cx="292" cy="162" r="13" fill="#FDE68A"/>
          <circle cx="288" cy="159" r="2" fill="#374151"/><circle cx="296" cy="159" r="2" fill="#374151"/>
          <path d="M288 167 Q292 171 296 167" stroke="#374151" stroke-width="1.5" fill="none"/>
          <path d="M280 157 Q282 148 292 149 Q302 148 304 157" fill="#D97706"/>
          <rect x="282" y="175" width="20" height="26" rx="6" fill="#F472B6"/>
          <line x1="302" y1="182" x2="304" y2="199" stroke="#FDE68A" stroke-width="4" stroke-linecap="round"/>
          <circle cx="265" cy="197" r="9" fill="#7C3AED"/>
          <text x="265" y="201" text-anchor="middle" fill="white" font-family="Nunito,sans-serif" font-size="11" font-weight="800">4</text>
          <rect x="8" y="194" width="68" height="38" rx="5" fill="#FCA5A5" stroke="#F87171" stroke-width="1.5"/>
          <rect x="8" y="194" width="68" height="14" rx="5" fill="#FEE2E2"/>
          <rect x="15" y="197" width="23" height="10" rx="4" fill="white" stroke="#FCA5A5" stroke-width="1"/>
          <line x1="8" y1="214" x2="76" y2="214" stroke="#F87171" stroke-width="1" stroke-dasharray="4,3"/>
          <circle cx="85" cy="190" r="10" fill="#FBB024"/>
          <circle cx="82" cy="188" r="1.5" fill="#374151"/><circle cx="88" cy="188" r="1.5" fill="#374151"/>
          <rect x="77" y="200" width="16" height="19" rx="5" fill="#A78BFA"/>
          <circle cx="14" cy="190" r="9" fill="#7C3AED"/>
          <text x="14" y="194" text-anchor="middle" fill="white" font-family="Nunito,sans-serif" font-size="11" font-weight="800">5</text>
          <rect x="138" y="68" width="58" height="38" rx="5" fill="#6B7280" stroke="#4B5563" stroke-width="1.5"/>
          <ellipse cx="167" cy="70" rx="21" ry="7" fill="#4B5563"/>
          <ellipse cx="167" cy="68" rx="19" ry="6" fill="#374151"/>
          <path d="M155 66 Q152 58 155 50" stroke="#D1D5DB" stroke-width="2" fill="none" stroke-linecap="round"/>
          <path d="M167 64 Q164 54 167 44" stroke="#D1D5DB" stroke-width="2" fill="none" stroke-linecap="round"/>
          <path d="M179 66 Q176 56 179 48" stroke="#D1D5DB" stroke-width="2" fill="none" stroke-linecap="round"/>
          <circle cx="167" cy="36" r="12" fill="#FDE68A"/>
          <circle cx="163" cy="33" r="2" fill="#374151"/><circle cx="171" cy="33" r="2" fill="#374151"/>
          <path d="M163 41 Q167 45 171 41" stroke="#374151" stroke-width="1.5" fill="none"/>
          <path d="M156 31 Q158 22 167 23 Q176 22 178 31" fill="#92400E"/>
          <rect x="160" y="18" width="14" height="8" rx="2" fill="white" stroke="#D1D5DB" stroke-width="1"/>
          <ellipse cx="167" cy="18" rx="10" ry="5" fill="white" stroke="#D1D5DB" stroke-width="1"/>
          <rect x="154" y="48" width="26" height="22" rx="6" fill="#FDE68A"/>
          <line x1="180" y1="56" x2="190" y2="68" stroke="#9CA3AF" stroke-width="2.5" stroke-linecap="round"/>
          <circle cx="191" cy="70" r="4" fill="#9CA3AF"/>
          <circle cx="144" cy="48" r="9" fill="#7C3AED"/>
          <text x="144" y="52" text-anchor="middle" fill="white" font-family="Nunito,sans-serif" font-size="11" font-weight="800">6</text>
          <rect x="0" y="219" width="320" height="3" fill="#A78BFA" opacity="0.4"/>
        </svg>
      </div>
      <div class="vocab-panel">
        <div class="vbank-label">📚 Word Bank</div>
        <div class="word-bank">
          <span class="word-pill">brush teeth</span>
          <span class="word-pill">eat breakfast</span>
          <span class="word-pill">do homework</span>
          <span class="word-pill">walk the dog</span>
          <span class="word-pill">make the bed</span>
          <span class="word-pill">cook dinner</span>
        </div>
        <div class="vbank-label">✍️ Choose the word</div>
        <div class="vocab-items" id="vocabItems">
          <div class="vi"><div class="vnum">1</div>
            <select id="v1" data-answer="brush teeth" onchange="updateProgress();markVocab(this)">
              <option value="">— choose —</option>
              <option>brush teeth</option><option>eat breakfast</option><option>do homework</option>
              <option>walk the dog</option><option>make the bed</option><option>cook dinner</option>
            </select>
          </div>
          <div class="vi"><div class="vnum">2</div>
            <select id="v2" data-answer="eat breakfast" onchange="updateProgress();markVocab(this)">
              <option value="">— choose —</option>
              <option>brush teeth</option><option>eat breakfast</option><option>do homework</option>
              <option>walk the dog</option><option>make the bed</option><option>cook dinner</option>
            </select>
          </div>
          <div class="vi"><div class="vnum">3</div>
            <select id="v3" data-answer="do homework" onchange="updateProgress();markVocab(this)">
              <option value="">— choose —</option>
              <option>brush teeth</option><option>eat breakfast</option><option>do homework</option>
              <option>walk the dog</option><option>make the bed</option><option>cook dinner</option>
            </select>
          </div>
          <div class="vi"><div class="vnum">4</div>
            <select id="v4" data-answer="walk the dog" onchange="updateProgress();markVocab(this)">
              <option value="">— choose —</option>
              <option>brush teeth</option><option>eat breakfast</option><option>do homework</option>
              <option>walk the dog</option><option>make the bed</option><option>cook dinner</option>
            </select>
          </div>
          <div class="vi"><div class="vnum">5</div>
            <select id="v5" data-answer="make the bed" onchange="updateProgress();markVocab(this)">
              <option value="">— choose —</option>
              <option>brush teeth</option><option>eat breakfast</option><option>do homework</option>
              <option>walk the dog</option><option>make the bed</option><option>cook dinner</option>
            </select>
          </div>
          <div class="vi"><div class="vnum">6</div>
            <select id="v6" data-answer="cook dinner" onchange="updateProgress();markVocab(this)">
              <option value="">— choose —</option>
              <option>brush teeth</option><option>eat breakfast</option><option>do homework</option>
              <option>walk the dog</option><option>make the bed</option><option>cook dinner</option>
            </select>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
 
<!-- SECTION 2 -->
<div class="section s2">
  <div class="sec-head">
    <div class="sec-num">2</div>
    <h2>Telling the Time</h2>
    <div class="hicon">🕐</div>
  </div>
  <div class="sec-body">
    <div class="instr">🕐 Look at the clocks and choose the correct answer.</div>
    <div class="clocks-grid" id="clocksGrid">
 
      <!-- Clock A: 3:00 -->
      <div class="clock-card" id="clockA">
        <div class="clk-lbl">A</div>
        <svg width="88" height="88" viewBox="0 0 88 88">
          <circle cx="44" cy="44" r="40" fill="white" stroke="#3B82F6" stroke-width="3"/>
          <circle cx="44" cy="44" r="3" fill="#1E40AF"/>
          <line x1="44" y1="8" x2="44" y2="14" stroke="#94A3B8" stroke-width="2"/>
          <line x1="80" y1="44" x2="74" y2="44" stroke="#94A3B8" stroke-width="2"/>
          <line x1="44" y1="80" x2="44" y2="74" stroke="#94A3B8" stroke-width="2"/>
          <line x1="8" y1="44" x2="14" y2="44" stroke="#94A3B8" stroke-width="2"/>
          <text x="44" y="18" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">12</text>
          <text x="76" y="48" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">3</text>
          <text x="44" y="78" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">6</text>
          <text x="12" y="48" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">9</text>
          <line x1="44" y1="44" x2="70" y2="44" stroke="#1E40AF" stroke-width="4" stroke-linecap="round"/>
          <line x1="44" y1="44" x2="44" y2="16" stroke="#3B82F6" stroke-width="2.5" stroke-linecap="round"/>
        </svg>
        <div class="opts">
          <button class="opt-btn" data-clock="A" data-val="a" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">a) half past three</span></button>
          <button class="opt-btn" data-clock="A" data-val="b" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">b) three o'clock</span></button>
          <button class="opt-btn" data-clock="A" data-val="c" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">c) quarter to three</span></button>
        </div>
      </div>
 
      <!-- Clock B: half past 7 -->
      <div class="clock-card" id="clockB">
        <div class="clk-lbl">B</div>
        <svg width="88" height="88" viewBox="0 0 88 88">
          <circle cx="44" cy="44" r="40" fill="white" stroke="#3B82F6" stroke-width="3"/>
          <circle cx="44" cy="44" r="3" fill="#1E40AF"/>
          <line x1="44" y1="8" x2="44" y2="14" stroke="#94A3B8" stroke-width="2"/>
          <line x1="80" y1="44" x2="74" y2="44" stroke="#94A3B8" stroke-width="2"/>
          <line x1="44" y1="80" x2="44" y2="74" stroke="#94A3B8" stroke-width="2"/>
          <line x1="8" y1="44" x2="14" y2="44" stroke="#94A3B8" stroke-width="2"/>
          <text x="44" y="18" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">12</text>
          <text x="76" y="48" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">3</text>
          <text x="44" y="78" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">6</text>
          <text x="12" y="48" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">9</text>
          <line x1="44" y1="44" x2="27" y2="63" stroke="#1E40AF" stroke-width="4" stroke-linecap="round"/>
          <line x1="44" y1="44" x2="44" y2="72" stroke="#3B82F6" stroke-width="2.5" stroke-linecap="round"/>
        </svg>
        <div class="opts">
          <button class="opt-btn" data-clock="B" data-val="a" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">a) seven o'clock</span></button>
          <button class="opt-btn" data-clock="B" data-val="b" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">b) quarter past seven</span></button>
          <button class="opt-btn" data-clock="B" data-val="c" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">c) half past seven</span></button>
        </div>
      </div>
 
      <!-- Clock C: quarter past 10 -->
      <div class="clock-card" id="clockC">
        <div class="clk-lbl">C</div>
        <svg width="88" height="88" viewBox="0 0 88 88">
          <circle cx="44" cy="44" r="40" fill="white" stroke="#3B82F6" stroke-width="3"/>
          <circle cx="44" cy="44" r="3" fill="#1E40AF"/>
          <line x1="44" y1="8" x2="44" y2="14" stroke="#94A3B8" stroke-width="2"/>
          <line x1="80" y1="44" x2="74" y2="44" stroke="#94A3B8" stroke-width="2"/>
          <line x1="44" y1="80" x2="44" y2="74" stroke="#94A3B8" stroke-width="2"/>
          <line x1="8" y1="44" x2="14" y2="44" stroke="#94A3B8" stroke-width="2"/>
          <text x="44" y="18" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">12</text>
          <text x="76" y="48" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">3</text>
          <text x="44" y="78" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">6</text>
          <text x="12" y="48" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">9</text>
          <line x1="44" y1="44" x2="22" y2="24" stroke="#1E40AF" stroke-width="4" stroke-linecap="round"/>
          <line x1="44" y1="44" x2="72" y2="44" stroke="#3B82F6" stroke-width="2.5" stroke-linecap="round"/>
        </svg>
        <div class="opts">
          <button class="opt-btn" data-clock="C" data-val="a" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">a) quarter to ten</span></button>
          <button class="opt-btn" data-clock="C" data-val="b" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">b) half past ten</span></button>
          <button class="opt-btn" data-clock="C" data-val="c" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">c) quarter past ten</span></button>
        </div>
      </div>
 
      <!-- Clock D: quarter to 6 -->
      <div class="clock-card" id="clockD">
        <div class="clk-lbl">D</div>
        <svg width="88" height="88" viewBox="0 0 88 88">
          <circle cx="44" cy="44" r="40" fill="white" stroke="#3B82F6" stroke-width="3"/>
          <circle cx="44" cy="44" r="3" fill="#1E40AF"/>
          <line x1="44" y1="8" x2="44" y2="14" stroke="#94A3B8" stroke-width="2"/>
          <line x1="80" y1="44" x2="74" y2="44" stroke="#94A3B8" stroke-width="2"/>
          <line x1="44" y1="80" x2="44" y2="74" stroke="#94A3B8" stroke-width="2"/>
          <line x1="8" y1="44" x2="14" y2="44" stroke="#94A3B8" stroke-width="2"/>
          <text x="44" y="18" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">12</text>
          <text x="76" y="48" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">3</text>
          <text x="44" y="78" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">6</text>
          <text x="12" y="48" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">9</text>
          <line x1="44" y1="44" x2="56" y2="69" stroke="#1E40AF" stroke-width="4" stroke-linecap="round"/>
          <line x1="44" y1="44" x2="16" y2="44" stroke="#3B82F6" stroke-width="2.5" stroke-linecap="round"/>
        </svg>
        <div class="opts">
          <button class="opt-btn" data-clock="D" data-val="a" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">a) half past five</span></button>
          <button class="opt-btn" data-clock="D" data-val="b" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">b) quarter to six</span></button>
          <button class="opt-btn" data-clock="D" data-val="c" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">c) six o'clock</span></button>
        </div>
      </div>
 
      <!-- Clock E: 9:00 -->
      <div class="clock-card" id="clockE">
        <div class="clk-lbl">E</div>
        <svg width="88" height="88" viewBox="0 0 88 88">
          <circle cx="44" cy="44" r="40" fill="white" stroke="#3B82F6" stroke-width="3"/>
          <circle cx="44" cy="44" r="3" fill="#1E40AF"/>
          <line x1="44" y1="8" x2="44" y2="14" stroke="#94A3B8" stroke-width="2"/>
          <line x1="80" y1="44" x2="74" y2="44" stroke="#94A3B8" stroke-width="2"/>
          <line x1="44" y1="80" x2="44" y2="74" stroke="#94A3B8" stroke-width="2"/>
          <line x1="8" y1="44" x2="14" y2="44" stroke="#94A3B8" stroke-width="2"/>
          <text x="44" y="18" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">12</text>
          <text x="76" y="48" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">3</text>
          <text x="44" y="78" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">6</text>
          <text x="12" y="48" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">9</text>
          <line x1="44" y1="44" x2="18" y2="44" stroke="#1E40AF" stroke-width="4" stroke-linecap="round"/>
          <line x1="44" y1="44" x2="44" y2="16" stroke="#3B82F6" stroke-width="2.5" stroke-linecap="round"/>
        </svg>
        <div class="opts">
          <button class="opt-btn" data-clock="E" data-val="a" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">a) quarter past nine</span></button>
          <button class="opt-btn" data-clock="E" data-val="b" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">b) half past nine</span></button>
          <button class="opt-btn" data-clock="E" data-val="c" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">c) nine o'clock</span></button>
        </div>
      </div>
 
      <!-- Clock F: half past 12 -->
      <div class="clock-card" id="clockF">
        <div class="clk-lbl">F</div>
        <svg width="88" height="88" viewBox="0 0 88 88">
          <circle cx="44" cy="44" r="40" fill="white" stroke="#3B82F6" stroke-width="3"/>
          <circle cx="44" cy="44" r="3" fill="#1E40AF"/>
          <line x1="44" y1="8" x2="44" y2="14" stroke="#94A3B8" stroke-width="2"/>
          <line x1="80" y1="44" x2="74" y2="44" stroke="#94A3B8" stroke-width="2"/>
          <line x1="44" y1="80" x2="44" y2="74" stroke="#94A3B8" stroke-width="2"/>
          <line x1="8" y1="44" x2="14" y2="44" stroke="#94A3B8" stroke-width="2"/>
          <text x="44" y="18" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">12</text>
          <text x="76" y="48" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">3</text>
          <text x="44" y="78" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">6</text>
          <text x="12" y="48" text-anchor="middle" fill="#1E40AF" font-family="Nunito,sans-serif" font-size="10" font-weight="700">9</text>
          <line x1="44" y1="44" x2="46" y2="18" stroke="#1E40AF" stroke-width="4" stroke-linecap="round"/>
          <line x1="44" y1="44" x2="44" y2="72" stroke="#3B82F6" stroke-width="2.5" stroke-linecap="round"/>
        </svg>
        <div class="opts">
          <button class="opt-btn" data-clock="F" data-val="a" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">a) twelve o'clock</span></button>
          <button class="opt-btn" data-clock="F" data-val="b" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">b) half past twelve</span></button>
          <button class="opt-btn" data-clock="F" data-val="c" onclick="selectClock(this)"><div class="opt-circ"></div><span class="opt-text">c) quarter to twelve</span></button>
        </div>
      </div>
 
    </div>
  </div>
</div>
 
<!-- SECTION 3 -->
<div class="section s3">
  <div class="sec-head">
    <div class="sec-num">3</div>
    <h2>Adverbs of Frequency</h2>
    <div class="hicon">📅</div>
  </div>
  <div class="sec-body">
    <div class="instr">✏️ Complete the sentences with <strong>always</strong>, <strong>usually</strong>, <strong>sometimes</strong> or <strong>never</strong>.</div>
    <div class="freq-chips">
      <span class="fchip fc1">always</span>
      <span class="fchip fc2">usually</span>
      <span class="fchip fc3">sometimes</span>
      <span class="fchip fc4">never</span>
    </div>
    <div class="sent-list">
      <div class="sent-row" id="sr1">
        <div class="snum">1</div>
        <div class="sent-text">I <select id="f1" data-answer="always" class="inline-sel" onchange="updateProgress();markFreq(this)"><option value="">—</option><option>always</option><option>usually</option><option>sometimes</option><option>never</option></select> brush my teeth before bed. It is very important!</div>
      </div>
      <div class="sent-row" id="sr2">
        <div class="snum">2</div>
        <div class="sent-text">My sister <select id="f2" data-answer="sometimes" class="inline-sel" onchange="updateProgress();markFreq(this)"><option value="">—</option><option>always</option><option>usually</option><option>sometimes</option><option>never</option></select> eats breakfast. She skips it on busy days.</div>
      </div>
      <div class="sent-row" id="sr3">
        <div class="snum">3</div>
        <div class="sent-text">We <select id="f3" data-answer="usually" class="inline-sel" onchange="updateProgress();markFreq(this)"><option value="">—</option><option>always</option><option>usually</option><option>sometimes</option><option>never</option></select> do our homework after school, but not every day.</div>
      </div>
      <div class="sent-row" id="sr4">
        <div class="snum">4</div>
        <div class="sent-text">Tom <select id="f4" data-answer="never" class="inline-sel" onchange="updateProgress();markFreq(this)"><option value="">—</option><option>always</option><option>usually</option><option>sometimes</option><option>never</option></select> walks to school — he always goes by bus.</div>
      </div>
      <div class="sent-row" id="sr5">
        <div class="snum">5</div>
        <div class="sent-text">My parents <select id="f5" data-answer="always" class="inline-sel" onchange="updateProgress();markFreq(this)"><option value="">—</option><option>always</option><option>usually</option><option>sometimes</option><option>never</option></select> cook dinner together every evening.</div>
      </div>
    </div>
  </div>
</div>
 
<div class="submit-wrap">
  <button class="submit-btn" id="submitBtn" onclick="submitAll()">Check my answers! 🎉</button>
</div>
 
<div id="resultBox" style="display:none"></div>
 
</div>
 
<script>
const clockAnswers = {A:'b',B:'c',C:'c',D:'b',E:'c',F:'b'};
const clockSelected = {};
 
function selectClock(btn) {
  const clock = btn.dataset.clock;
  document.querySelectorAll(`[data-clock="${clock}"]`).forEach(b => b.classList.remove('selected'));
  btn.classList.add('selected');
  clockSelected[clock] = btn.dataset.val;
  updateProgress();
}
 
function markVocab(sel) {
  sel.classList.remove('correct','wrong');
}
 
function markFreq(sel) {
  sel.classList.remove('correct','wrong');
  document.getElementById('sr'+sel.id.replace('f','')).classList.remove('correct-row','wrong-row');
}
 
function updateProgress() {
  let answered = 0;
  const total = 17;
  ['v1','v2','v3','v4','v5','v6'].forEach(id => { if(document.getElementById(id).value) answered++; });
  Object.keys(clockSelected).forEach(() => answered++);
  ['f1','f2','f3','f4','f5'].forEach(id => { if(document.getElementById(id).value) answered++; });
  document.getElementById('progressFill').style.width = Math.round((answered/total)*100)+'%';
  document.getElementById('progressLabel').textContent = answered+' of '+total+' answered';
}
 
function submitAll() {
  let score = 0;
  const total = 17;
 
  ['v1','v2','v3','v4','v5','v6'].forEach(id => {
    const el = document.getElementById(id);
    if(el.value === el.dataset.answer){ score++; el.classList.add('correct'); }
    else if(el.value){ el.classList.add('wrong'); }
  });
 
  Object.keys(clockAnswers).forEach(letter => {
    const correct = clockAnswers[letter];
    const sel = clockSelected[letter];
    document.querySelectorAll(`[data-clock="${letter}"]`).forEach(b => {
      if(b.dataset.val === correct) b.classList.add('correct');
      else if(b.classList.contains('selected') && b.dataset.val !== correct) b.classList.add('wrong');
      b.classList.remove('selected');
    });
    if(sel === correct) score++;
  });
 
  ['f1','f2','f3','f4','f5'].forEach((id,i) => {
    const el = document.getElementById(id);
    const row = document.getElementById('sr'+(i+1));
    if(el.value === el.dataset.answer){ score++; el.classList.add('correct'); row.classList.add('correct-row'); }
    else if(el.value){ el.classList.add('wrong'); row.classList.add('wrong-row'); }
  });
 
  document.getElementById('submitBtn').disabled = true;
 
  const pct = Math.round((score/total)*100);
  let cls, emoji, msg;
  if(pct >= 85){ cls='great'; emoji='🏆'; msg='Fantastic job! You are a Daily Routine star!'; }
  else if(pct >= 60){ cls='good'; emoji='👍'; msg='Good work! Keep practising and you will be perfect!'; }
  else{ cls='keep'; emoji='💪'; msg='Nice try! Review the exercises and try again!'; }
 
  const s1 = (['v1','v2','v3','v4','v5','v6'].filter(id=>document.getElementById(id).value===document.getElementById(id).dataset.answer).length);
  const s2 = Object.keys(clockAnswers).filter(l=>clockSelected[l]===clockAnswers[l]).length;
  const s3 = ['f1','f2','f3','f4','f5'].filter(id=>document.getElementById(id).value===document.getElementById(id).dataset.answer).length;
 
  const box = document.getElementById('resultBox');
  box.className = 'result-box '+cls;
  box.style.display = 'block';
  box.innerHTML = `
    <div class="result-emoji">${emoji}</div>
    <div class="result-score">${score} / ${total} &nbsp; (${pct}%)</div>
    <div class="result-msg">${msg}</div>
    <div class="breakdown">
      <div class="bd-item"><span>${s1}/6</span>Exercise 1</div>
      <div class="bd-item"><span>${s2}/6</span>Exercise 2</div>
      <div class="bd-item"><span>${s3}/5</span>Exercise 3</div>
    </div>
    <button class="retry-btn" onclick="resetAll()">Try again 🔄</button>
  `;
  box.scrollIntoView({behavior:'smooth',block:'center'});
}
 
function resetAll() {
  ['v1','v2','v3','v4','v5','v6'].forEach(id => {
    const el = document.getElementById(id);
    el.value=''; el.classList.remove('correct','wrong');
  });
  Object.keys(clockSelected).forEach(k => delete clockSelected[k]);
  document.querySelectorAll('.opt-btn').forEach(b => b.classList.remove('selected','correct','wrong'));
  ['f1','f2','f3','f4','f5'].forEach((id,i) => {
    const el = document.getElementById(id);
    el.value=''; el.classList.remove('correct','wrong');
    document.getElementById('sr'+(i+1)).classList.remove('correct-row','wrong-row');
  });
  document.getElementById('submitBtn').disabled = false;
  document.getElementById('resultBox').style.display = 'none';
  document.getElementById('progressFill').style.width = '0%';
  document.getElementById('progressLabel').textContent = '0 of 17 answered';
  window.scrollTo({top:0,behavior:'smooth'});
}
</script>
</body>
</html>
