<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Field Log — Daily Task Ledger</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Special+Elite&family=IBM+Plex+Mono:wght@400;500;600&family=Source+Serif+4:opsz,wght@8..60,400;8..60,600&display=swap');

  :root{
    --paper: #E8E2D0;
    --paper-dark: #DDD5BE;
    --ink: #2B2E26;
    --ink-soft: #5A5A4E;
    --rule: #B8AE94;
    --stamp-red: #A8322D;
    --field-green: #4B5D3A;
  }

  *{ box-sizing: border-box; }

  html, body{
    margin:0; padding:0; min-height:100%;
    background: var(--paper-dark);
    background-image:
      radial-gradient(circle at 15% 20%, rgba(0,0,0,0.02) 0, transparent 40%),
      radial-gradient(circle at 85% 80%, rgba(0,0,0,0.025) 0, transparent 45%);
    font-family: 'Source Serif 4', serif;
    color: var(--ink);
    display:flex;
    justify-content:center;
    padding: 48px 16px;
  }

  .sheet{
    width: 100%;
    max-width: 620px;
    background: var(--paper);
    box-shadow:
      0 1px 0 rgba(255,255,255,0.4) inset,
      0 30px 60px -20px rgba(0,0,0,0.35),
      0 2px 6px rgba(0,0,0,0.15);
    padding: 40px 44px 32px;
    position: relative;
  }

  .sheet::before{
    content:"";
    position:absolute; inset:10px;
    border: 1px solid rgba(43,46,38,0.15);
    pointer-events:none;
  }

  header{
    text-align:center;
    padding-bottom: 18px;
    border-bottom: 2px solid var(--ink);
    margin-bottom: 6px;
  }

  .kicker{
    font-family:'IBM Plex Mono', monospace;
    font-size: 11px;
    letter-spacing: 3px;
    color: var(--stamp-red);
    text-transform: uppercase;
    margin-bottom: 6px;
  }

  h1{
    font-family: 'Special Elite', monospace;
    font-size: 30px;
    letter-spacing: 2px;
    margin: 0 0 6px;
    text-transform: uppercase;
  }

  .meta{
    font-family:'IBM Plex Mono', monospace;
    font-size: 12px;
    color: var(--ink-soft);
    display:flex;
    justify-content:space-between;
    max-width: 380px;
    margin: 8px auto 0;
  }

  .entry-form{
    display:flex;
    align-items:flex-end;
    gap: 10px;
    margin: 26px 0 8px;
  }

  .entry-form .field{
    flex:1;
    position:relative;
  }

  .entry-form label{
    font-family:'IBM Plex Mono', monospace;
    font-size: 10px;
    letter-spacing: 1.5px;
    color: var(--ink-soft);
    text-transform: uppercase;
  }

  .entry-form input[type=text]{
    width:100%;
    border:none;
    background: transparent;
    border-bottom: 1.5px dashed var(--rule);
    font-family:'Source Serif 4', serif;
    font-size: 16px;
    padding: 6px 2px;
    color: var(--ink);
  }

  .entry-form input[type=text]:focus{
    outline:none;
    border-bottom-color: var(--ink);
  }

  .entry-form button{
    font-family:'IBM Plex Mono', monospace;
    font-size: 12px;
    letter-spacing: 1px;
    background: var(--ink);
    color: var(--paper);
    border:none;
    padding: 10px 16px;
    cursor:pointer;
    text-transform: uppercase;
  }
  .entry-form button:hover{ background: var(--stamp-red); }
  .entry-form button:active{ transform: translateY(1px); }

  .ledger{
    list-style:none;
    margin: 18px 0 0;
    padding: 0;
    border-top: 1px solid var(--ink);
  }

  .row{
    display:flex;
    align-items:center;
    gap: 14px;
    padding: 13px 0;
    border-bottom: 1px dashed var(--rule);
    position:relative;
  }

  .row .num{
    font-family:'IBM Plex Mono', monospace;
    font-size: 12px;
    color: var(--stamp-red);
    width: 32px;
    flex-shrink:0;
  }

  .row .text{
    flex:1;
    font-size: 16px;
    line-height:1.4;
    word-break: break-word;
  }

  .row.done .text{
    color: var(--field-green);
    text-decoration: line-through;
    text-decoration-thickness: 1.5px;
    opacity: 0.75;
  }

  .stamp-box{
    width: 26px; height: 26px;
    border: 2px solid var(--ink);
    border-radius: 50%;
    flex-shrink:0;
    cursor:pointer;
    position:relative;
    background: transparent;
    transition: transform 0.08s ease;
  }
  .stamp-box:active{ transform: scale(0.9); }

  .row.done .stamp-box{
    border-color: var(--field-green);
    background: var(--field-green);
  }
  .row.done .stamp-box::after{
    content:"✓";
    position:absolute; inset:0;
    display:flex; align-items:center; justify-content:center;
    color: var(--paper);
    font-size: 14px;
    font-weight:600;
  }

  .stamp-mark{
    position:absolute;
    right: 40px;
    font-family:'Special Elite', monospace;
    font-size: 18px;
    color: var(--stamp-red);
    border: 2.5px solid var(--stamp-red);
    padding: 1px 8px;
    border-radius: 4px;
    transform: rotate(-9deg) scale(0);
    opacity:0;
    text-transform: uppercase;
    letter-spacing: 2px;
    pointer-events:none;
    mix-blend-mode: multiply;
  }
  .row.done .stamp-mark{
    animation: stampdown 0.32s cubic-bezier(.2,1.6,.4,1) forwards;
  }
  @keyframes stampdown{
    0%{ transform: rotate(-9deg) scale(2.4); opacity:0; }
    60%{ opacity:1; }
    100%{ transform: rotate(-9deg) scale(1); opacity:1; }
  }

  .remove{
    font-family:'IBM Plex Mono', monospace;
    font-size: 14px;
    color: var(--ink-soft);
    background:none; border:none;
    cursor:pointer;
    opacity:0;
    transition: opacity 0.15s ease;
    flex-shrink:0;
    padding: 4px;
  }
  .row:hover .remove{ opacity: 0.6; }
  .remove:hover{ color: var(--stamp-red) !important; opacity:1 !important; }

  .empty{
    text-align:center;
    padding: 40px 10px;
    color: var(--ink-soft);
    font-family:'IBM Plex Mono', monospace;
    font-size: 13px;
    letter-spacing: 0.5px;
  }

  footer{
    margin-top: 22px;
    padding-top: 14px;
    border-top: 2px solid var(--ink);
    display:flex;
    justify-content:space-between;
    font-family:'IBM Plex Mono', monospace;
    font-size: 11px;
    letter-spacing: 1px;
    color: var(--ink-soft);
    text-transform: uppercase;
  }

  @media (max-width: 480px){
    .sheet{ padding: 28px 20px 24px; }
    h1{ font-size: 24px; }
    .meta{ flex-direction:column; gap:4px; align-items:center; }
  }

  @media (prefers-reduced-motion: reduce){
    .stamp-box, .stamp-mark, .remove{ transition:none; animation:none; }
  }
</style>
</head>
<body>

<div class="sheet">
  <header>
    <div class="kicker">Ledger No. 01 · Personal</div>
    <h1>Field Log</h1>
    <div class="meta">
      <span id="date-display">—</span>
      <span id="tally-display">0 open</span>
    </div>
  </header>

  <div class="entry-form">
    <div class="field">
      <label for="entry-input">New entry</label>
      <input type="text" id="entry-input" placeholder="What needs doing…" maxlength="140" autocomplete="off">
    </div>
    <button id="add-btn" type="button">Log it</button>
  </div>

  <ul class="ledger" id="ledger"></ul>

  <footer>
    <span id="open-count">0 open</span>
    <span id="closed-count">0 closed</span>
  </footer>
</div>

<script>
(function(){
  const STORAGE_KEY = 'field-log-entries';
  const ledgerEl = document.getElementById('ledger');
  const input = document.getElementById('entry-input');
  const addBtn = document.getElementById('add-btn');
  const openCountEl = document.getElementById('open-count');
  const closedCountEl = document.getElementById('closed-count');
  const dateDisplay = document.getElementById('date-display');

  let entries = [];
  let loaded = false;

  dateDisplay.textContent = new Date().toLocaleDateString(undefined, {
    weekday: 'long', month: 'long', day: 'numeric', year: 'numeric'
  });

  function uid(){
    return 'e' + Date.now().toString(36) + Math.random().toString(36).slice(2,7);
  }

  async function load(){
    try{
      const res = await window.storage.get(STORAGE_KEY, false);
      entries = res && res.value ? JSON.parse(res.value) : [];
    }catch(e){
      entries = [];
    }
    loaded = true;
    render();
  }

  async function persist(){
    try{
      await window.storage.set(STORAGE_KEY, JSON.stringify(entries), false);
    }catch(e){
      console.error('Could not save log', e);
    }
  }

  function render(){
    ledgerEl.innerHTML = '';
    if(entries.length === 0){
      const empty = document.createElement('div');
      empty.className = 'empty';
      empty.textContent = loaded ? 'The page is blank. Log the first entry above.' : 'Opening the ledger…';
      ledgerEl.appendChild(empty);
    } else {
      entries.forEach((entry, idx) => {
        const row = document.createElement('li');
        row.className = 'row' + (entry.done ? ' done' : '');

        const num = document.createElement('span');
        num.className = 'num';
        num.textContent = String(idx + 1).padStart(3, '0');

        const box = document.createElement('button');
        box.className = 'stamp-box';
        box.type = 'button';
        box.setAttribute('aria-label', entry.done ? 'Mark as open' : 'Mark as done');
        box.addEventListener('click', () => toggleDone(entry.id));

        const text = document.createElement('span');
        text.className = 'text';
        text.textContent = entry.text;

        const stamp = document.createElement('span');
        stamp.className = 'stamp-mark';
        stamp.textContent = 'Done';

        const remove = document.createElement('button');
        remove.className = 'remove';
        remove.type = 'button';
        remove.textContent = '✕';
        remove.setAttribute('aria-label', 'Remove entry');
        remove.addEventListener('click', () => removeEntry(entry.id));

        row.appendChild(num);
        row.appendChild(box);
        row.appendChild(text);
        row.appendChild(stamp);
        row.appendChild(remove);
        ledgerEl.appendChild(row);
      });
    }

    const openCount = entries.filter(e => !e.done).length;
    const closedCount = entries.length - openCount;
    openCountEl.textContent = openCount + ' open';
    closedCountEl.textContent = closedCount + ' closed';
  }

  function addEntry(){
    const value = input.value.trim();
    if(!value) return;
    entries.push({ id: uid(), text: value, done: false });
    input.value = '';
    render();
    persist();
    input.focus();
  }

  function toggleDone(id){
    const entry = entries.find(e => e.id === id);
    if(!entry) return;
    entry.done = !entry.done;
    render();
    persist();
  }

  function removeEntry(id){
    entries = entries.filter(e => e.id !== id);
    render();
    persist();
  }

  addBtn.addEventListener('click', addEntry);
  input.addEventListener('keydown', (e) => {
    if(e.key === 'Enter') addEntry();
  });

  load();
})();
</script>

</body>
</html>
