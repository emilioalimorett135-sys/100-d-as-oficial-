<!DOCTYPE html>

<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
  <meta name="apple-mobile-web-app-capable" content="yes" />
  <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent" />
  <meta name="apple-mobile-web-app-title" content="100 DÍAS" />
  <meta name="theme-color" content="#0a0a0f" />
  <title>OPERACIÓN 100 DÍAS</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Bebas+Neue&display=swap');

```
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --bg: #0a0a0f;
  --surface: #111118;
  --border: #1e1e2e;
  --purple: #7c6fff;
  --teal: #00d4aa;
  --orange: #ff6b35;
  --gold: #ffd700;
  --text: #e8e8f0;
  --muted: #555;
}

html, body {
  background: var(--bg);
  color: var(--text);
  font-family: 'Space Mono', monospace;
  min-height: 100vh;
  min-height: -webkit-fill-available;
  overflow-x: hidden;
}

/* BG GRID */
body::before {
  content: '';
  position: fixed; inset: 0; z-index: 0;
  background-image:
    linear-gradient(rgba(124,111,255,0.04) 1px, transparent 1px),
    linear-gradient(90deg, rgba(124,111,255,0.04) 1px, transparent 1px);
  background-size: 40px 40px;
  pointer-events: none;
}

/* GLOW ORBS */
body::after {
  content: '';
  position: fixed; top: -20%; left: -10%;
  width: 500px; height: 500px;
  background: radial-gradient(circle, rgba(124,111,255,0.07) 0%, transparent 70%);
  border-radius: 50%; pointer-events: none; z-index: 0;
}

#app {
  position: relative; z-index: 1;
  max-width: 600px;
  margin: 0 auto;
  padding: 24px 16px 48px;
}

/* HEADER */
.header { text-align: center; margin-bottom: 28px; }
.header .eyebrow {
  font-size: 10px; letter-spacing: 6px; color: var(--purple);
  text-transform: uppercase; margin-bottom: 8px;
}
.header h1 {
  font-family: 'Bebas Neue', sans-serif;
  font-size: clamp(52px, 15vw, 80px);
  letter-spacing: 4px; line-height: 1;
  background: linear-gradient(135deg, #fff 0%, var(--purple) 50%, var(--teal) 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
.rank-badge {
  margin-top: 10px;
  display: inline-flex; align-items: center; gap: 8px;
  background: var(--surface); border: 1px solid var(--border);
  border-radius: 20px; padding: 6px 16px;
}
.rank-badge span { font-size: 11px; letter-spacing: 3px; font-weight: 700; }

/* CARDS */
.card {
  background: var(--surface);
  border: 1px solid var(--border);
  border-radius: 16px;
  padding: 18px;
  margin-bottom: 14px;
}
.card-label {
  font-size: 10px; letter-spacing: 4px; color: var(--muted);
  margin-bottom: 14px; display: flex; align-items: center; gap: 8px;
}
.card-label::before { content: '▸'; color: var(--purple); }

/* PROGRESS */
.progress-header {
  display: flex; justify-content: space-between; align-items: center;
  margin-bottom: 14px;
}
.day-control {
  display: flex; align-items: center; gap: 8px;
}
.day-control span.label { font-size: 10px; color: var(--muted); letter-spacing: 2px; }
.day-control .num {
  font-size: 24px; font-weight: 700; color: var(--purple);
  min-width: 40px; text-align: center; font-family: 'Bebas Neue', sans-serif;
}
.btn-ctrl {
  background: #1a1a2e; border: 1px solid var(--border);
  color: #fff; width: 30px; height: 30px;
  border-radius: 8px; cursor: pointer; font-size: 16px;
  display: flex; align-items: center; justify-content: center;
  -webkit-tap-highlight-color: transparent;
  transition: background 0.15s;
}
.btn-ctrl:active { background: var(--purple); }

.progress-bar-wrap {
  height: 10px; background: #1a1a2e; border-radius: 5px; overflow: hidden;
}
.progress-bar-fill {
  height: 100%; border-radius: 5px;
  background: linear-gradient(90deg, var(--purple), var(--teal));
  box-shadow: 0 0 12px rgba(124,111,255,0.5);
  transition: width 0.6s ease;
}
.progress-labels {
  display: flex; justify-content: space-between;
  margin-top: 6px; font-size: 10px; color: var(--muted);
}
.progress-labels .mid { color: var(--purple); }

/* STATS */
.stats-grid {
  display: grid; grid-template-columns: repeat(4,1fr); gap: 10px;
  margin-bottom: 14px;
}
.stat-box {
  background: var(--surface); border: 1px solid var(--border);
  border-radius: 12px; padding: 12px 8px; text-align: center;
}
.stat-box .val { font-size: 20px; font-weight: 700; font-family: 'Bebas Neue', sans-serif; letter-spacing: 1px; }
.stat-box .lbl { font-size: 8px; color: var(--muted); letter-spacing: 2px; margin-top: 3px; }

/* MISSION STATS */
.mission-stats {
  display: flex; gap: 10px;
}
.mission-stat {
  flex: 1; text-align: center; padding: 10px 6px;
  background: var(--surface); border: 1px solid var(--border);
  border-radius: 12px;
}
.mission-stat .icon { font-size: 18px; }
.mission-stat .cnt { font-size: 18px; font-weight: 700; font-family: 'Bebas Neue', sans-serif; margin-top: 2px; }
.mission-stat .name { font-size: 8px; color: var(--muted); letter-spacing: 1px; margin-top: 2px; }

/* TODAY QUICK LOG */
.today-card {
  background: linear-gradient(135deg, #111118, #14141f);
  border: 1px solid rgba(124,111,255,0.3);
  border-radius: 16px; padding: 18px; margin-bottom: 14px;
  box-shadow: 0 0 30px rgba(124,111,255,0.06);
}
.missions-row { display: flex; gap: 10px; }
.mission-btn {
  flex: 1;
  background: #0d0d15; border: 2px solid var(--border);
  border-radius: 12px; padding: 14px 8px;
  cursor: pointer; transition: all 0.2s;
  text-align: center;
  -webkit-tap-highlight-color: transparent;
}
.mission-btn .m-icon { font-size: 22px; margin-bottom: 6px; }
.mission-btn .m-name { font-size: 9px; letter-spacing: 2px; font-weight: 700; color: var(--muted); }
.mission-btn .m-check { font-size: 18px; margin-top: 6px; color: var(--border); }
.mission-btn.done .m-name { }
.mission-btn.done .m-check { }

.completed-banner {
  text-align: center; margin-top: 12px;
  font-size: 11px; letter-spacing: 4px; font-weight: 700; color: var(--teal);
  animation: pulse 2s infinite;
}

.note-btn {
  margin-top: 10px; width: 100%;
  background: transparent; border: 1px dashed #2a2a3a;
  border-radius: 8px; padding: 10px;
  color: var(--muted); font-size: 10px; letter-spacing: 2px;
  cursor: pointer; font-family: 'Space Mono', monospace;
  -webkit-tap-highlight-color: transparent;
  transition: border-color 0.2s;
}
.note-btn:active { border-color: var(--purple); }

/* GRID */
.day-grid {
  display: grid; grid-template-columns: repeat(10, 1fr);
  gap: 5px;
}
.day-cell {
  aspect-ratio: 1;
  background: #0d0d15; border: 1px solid #1a1a2e;
  border-radius: 5px; cursor: pointer;
  display: flex; flex-direction: column;
  align-items: center; justify-content: center; gap: 2px;
  transition: transform 0.1s;
  -webkit-tap-highlight-color: transparent;
  position: relative;
}
.day-cell:active { transform: scale(0.9); }
.day-cell .d-num { font-size: 8px; font-weight: 700; }
.day-cell .d-dots { display: flex; gap: 1px; }
.day-cell .d-dot { width: 3px; height: 3px; border-radius: 50%; background: transparent; }
.day-cell .d-current-dot {
  position: absolute; top: 2px; right: 2px;
  width: 4px; height: 4px; background: var(--purple);
  border-radius: 50%;
}

.grid-legend {
  display: flex; flex-wrap: wrap; gap: 12px; margin-top: 14px;
}
.legend-item {
  display: flex; align-items: center; gap: 5px;
  font-size: 9px; color: var(--muted);
}
.legend-dot { width: 10px; height: 10px; border-radius: 2px; }

/* MODAL */
.modal-overlay {
  position: fixed; inset: 0; z-index: 100;
  background: rgba(0,0,0,0.88);
  display: flex; align-items: flex-end; justify-content: center;
  padding: 16px;
  opacity: 0; pointer-events: none;
  transition: opacity 0.2s;
}
.modal-overlay.open {
  opacity: 1; pointer-events: all;
}
.modal-box {
  background: #111118;
  border: 1px solid rgba(124,111,255,0.3);
  border-radius: 20px; padding: 24px;
  width: 100%; max-width: 480px;
  transform: translateY(30px);
  transition: transform 0.3s ease;
  box-shadow: 0 0 60px rgba(124,111,255,0.12);
}
.modal-overlay.open .modal-box { transform: translateY(0); }
.modal-title { font-size: 10px; color: var(--purple); letter-spacing: 4px; margin-bottom: 18px; }

.modal-missions { display: flex; flex-direction: column; gap: 10px; margin-bottom: 18px; }
.modal-mission {
  display: flex; align-items: center; gap: 14px;
  background: #0d0d15; border: 1.5px solid var(--border);
  border-radius: 10px; padding: 14px 16px;
  cursor: pointer; transition: all 0.2s;
  -webkit-tap-highlight-color: transparent;
}
.modal-mission .mm-icon { font-size: 22px; }
.modal-mission .mm-name { flex: 1; font-size: 11px; letter-spacing: 2px; font-weight: 700; color: #888; }
.modal-mission .mm-check { font-size: 18px; color: var(--border); }
.modal-mission.done .mm-name { }
.modal-mission.done .mm-check { }

.modal-textarea {
  width: 100%; background: #0d0d15;
  border: 1px solid var(--border); border-radius: 10px;
  padding: 12px; color: var(--text);
  font-size: 13px; font-family: 'Space Mono', monospace;
  resize: vertical; min-height: 80px; outline: none;
}
.modal-textarea:focus { border-color: var(--purple); }

.modal-actions { display: flex; gap: 10px; margin-top: 14px; }
.btn-save {
  flex: 1; background: linear-gradient(135deg, var(--purple), var(--teal));
  border: none; border-radius: 10px; padding: 14px;
  color: #fff; font-weight: 700; font-size: 11px;
  letter-spacing: 3px; cursor: pointer;
  font-family: 'Space Mono', monospace;
  -webkit-tap-highlight-color: transparent;
}
.btn-cancel {
  background: #0d0d15; border: 1px solid var(--border);
  border-radius: 10px; padding: 14px 18px;
  color: var(--muted); cursor: pointer; font-size: 14px;
  -webkit-tap-highlight-color: transparent;
}

@keyframes pulse {
  0%, 100% { opacity: 1; } 50% { opacity: 0.4; }
}
```

  </style>
</head>
<body>
<div id="app">
  <!-- HEADER -->
  <div class="header">
    <div class="eyebrow">OPERACIÓN</div>
    <h1>100 DÍAS</h1>
    <div class="rank-badge">
      <span id="rank-icon">🌱</span>
      <span id="rank-title" style="color:#aaa">INICIADO</span>
    </div>
  </div>

  <!-- PROGRESS -->

  <div class="card">
    <div class="progress-header">
      <div class="card-label" style="margin:0">PROGRESO</div>
      <div class="day-control">
        <span class="label">DÍA</span>
        <button class="btn-ctrl" id="day-minus">−</button>
        <span class="num" id="current-day-display">30</span>
        <button class="btn-ctrl" id="day-plus">+</button>
      </div>
    </div>
    <div class="progress-bar-wrap">
      <div class="progress-bar-fill" id="progress-fill" style="width:30%"></div>
    </div>
    <div class="progress-labels">
      <span>DÍA 1</span>
      <span class="mid" id="progress-pct">30%</span>
      <span>DÍA 100</span>
    </div>
  </div>

  <!-- STATS -->

  <div class="stats-grid">
    <div class="stat-box">
      <div class="val" id="stat-completed" style="color:var(--teal)">0</div>
      <div class="lbl">DÍAS ✓</div>
    </div>
    <div class="stat-box">
      <div class="val" id="stat-streak" style="color:var(--orange)">0🔥</div>
      <div class="lbl">RACHA</div>
    </div>
    <div class="stat-box">
      <div class="val" id="stat-maxstreak" style="color:var(--purple)">0</div>
      <div class="lbl">MAX</div>
    </div>
    <div class="stat-box">
      <div class="val" id="stat-left" style="color:var(--gold)">70</div>
      <div class="lbl">QUEDAN</div>
    </div>
  </div>

  <!-- MISSION STATS -->

  <div class="card" style="padding:14px">
    <div class="mission-stats">
      <div class="mission-stat">
        <div class="icon">⚔️</div>
        <div class="cnt" id="ms-trabajar" style="color:var(--orange)">0</div>
        <div class="name">TRABAJAR</div>
      </div>
      <div class="mission-stat">
        <div class="icon">🔥</div>
        <div class="cnt" id="ms-entrenar" style="color:var(--teal)">0</div>
        <div class="name">ENTRENAR</div>
      </div>
      <div class="mission-stat">
        <div class="icon">📖</div>
        <div class="cnt" id="ms-estudiar" style="color:var(--purple)">0</div>
        <div class="name">ESTUDIAR</div>
      </div>
    </div>
  </div>

  <!-- TODAY QUICK LOG -->

  <div class="today-card">
    <div class="card-label" style="color:var(--purple);margin-bottom:14px">
      ▸ DÍA <span id="today-label">30</span> — REGISTRO RÁPIDO
    </div>
    <div class="missions-row">
      <button class="mission-btn" id="mb-trabajar" data-mission="Trabajar" onclick="toggleTodayMission('Trabajar')">
        <div class="m-icon">⚔️</div>
        <div class="m-name">TRABAJAR</div>
        <div class="m-check" id="mc-trabajar">○</div>
      </button>
      <button class="mission-btn" id="mb-entrenar" data-mission="Entrenar" onclick="toggleTodayMission('Entrenar')">
        <div class="m-icon">🔥</div>
        <div class="m-name">ENTRENAR</div>
        <div class="m-check" id="mc-entrenar">○</div>
      </button>
      <button class="mission-btn" id="mb-estudiar" data-mission="Estudiar" onclick="toggleTodayMission('Estudiar')">
        <div class="m-icon">📖</div>
        <div class="m-name">ESTUDIAR</div>
        <div class="m-check" id="mc-estudiar">○</div>
      </button>
    </div>
    <div class="completed-banner" id="completed-banner" style="display:none">✦ DÍA COMPLETADO ✦</div>
    <button class="note-btn" id="note-btn" onclick="openModal(currentDay)">+ AÑADIR NOTA DEL DÍA</button>
  </div>

  <!-- GRID -->

  <div class="card">
    <div class="card-label">MAPA DE BATALLA — 100 DÍAS</div>
    <div class="day-grid" id="day-grid"></div>
    <div class="grid-legend">
      <div class="legend-item"><div class="legend-dot" style="background:var(--teal)"></div>Completo</div>
      <div class="legend-item"><div class="legend-dot" style="background:var(--orange)"></div>Parcial</div>
      <div class="legend-item"><div class="legend-dot" style="background:var(--purple)"></div>Hoy</div>
      <div class="legend-item"><div class="legend-dot" style="background:#222"></div>Futuro</div>
    </div>
  </div>
</div>

<!-- MODAL -->

<div class="modal-overlay" id="modal-overlay" onclick="closeModal(event)">
  <div class="modal-box">
    <div class="modal-title">▸ DÍA <span id="modal-day-num">1</span></div>
    <div class="modal-missions" id="modal-missions"></div>
    <textarea class="modal-textarea" id="modal-note" placeholder="Notas del día..."></textarea>
    <div class="modal-actions">
      <button class="btn-save" onclick="saveModal()">GUARDAR</button>
      <button class="btn-cancel" onclick="closeModal()">✕</button>
    </div>
  </div>
</div>

<script>
  const TOTAL = 100;
  const MISSIONS = ['Trabajar', 'Entrenar', 'Estudiar'];
  const ICONS = { Trabajar: '⚔️', Entrenar: '🔥', Estudiar: '📖' };
  const COLORS = { Trabajar: '#ff6b35', Entrenar: '#00d4aa', Estudiar: '#7c6fff' };
  const KEY = 'op100days_v2';

  let state = loadState();
  let currentDay = state.currentDay || 30;
  let modalDay = null;

  function loadState() {
    try { return JSON.parse(localStorage.getItem(KEY)) || { days: {}, currentDay: 30 }; }
    catch { return { days: {}, currentDay: 30 }; }
  }
  function saveState() {
    state.currentDay = currentDay;
    localStorage.setItem(KEY, JSON.stringify(state));
  }
  function getDay(d) {
    return state.days[d] || { missions: {}, note: '', completed: false };
  }
  function setDay(d, data) {
    state.days[d] = data;
    saveState();
  }

  function toggleMission(day, mission) {
    const dd = getDay(day);
    dd.missions[mission] = !dd.missions[mission];
    dd.completed = MISSIONS.every(m => dd.missions[m]);
    setDay(day, dd);
  }

  function toggleTodayMission(mission) {
    toggleMission(currentDay, mission);
    renderAll();
  }

  function getStats() {
    let completed = 0, streak = 0, maxStreak = 0, cur = 0;
    const mc = { Trabajar: 0, Entrenar: 0, Estudiar: 0 };
    for (let d = 1; d <= TOTAL; d++) {
      const dd = getDay(d);
      if (dd.completed) { completed++; cur++; maxStreak = Math.max(maxStreak, cur); }
      else cur = 0;
      MISSIONS.forEach(m => { if (dd.missions[m]) mc[m]++; });
    }
    for (let d = currentDay; d >= 1; d--) {
      if (getDay(d).completed) streak++;
      else break;
    }
    return { completed, streak, maxStreak, mc };
  }

  function getRank(n) {
    if (n >= 90) return { title: 'LEYENDA', color: '#ffd700', icon: '👑' };
    if (n >= 70) return { title: 'ÉLITE', color: '#ff6b35', icon: '🏆' };
    if (n >= 50) return { title: 'GUERRERO', color: '#00d4aa', icon: '⚔️' };
    if (n >= 30) return { title: 'ASPIRANTE', color: '#7c6fff', icon: '🔮' };
    return { title: 'INICIADO', color: '#aaa', icon: '🌱' };
  }

  function renderAll() {
    const stats = getStats();
    const rank = getRank(stats.completed);
    const pct = Math.round((currentDay / TOTAL) * 100);

    // Header
    document.getElementById('rank-icon').textContent = rank.icon;
    const rt = document.getElementById('rank-title');
    rt.textContent = rank.title; rt.style.color = rank.color;

    // Progress
    document.getElementById('current-day-display').textContent = currentDay;
    document.getElementById('progress-fill').style.width = pct + '%';
    document.getElementById('progress-pct').textContent = pct + '%';
    document.getElementById('today-label').textContent = currentDay;

    // Stats
    document.getElementById('stat-completed').textContent = stats.completed;
    document.getElementById('stat-streak').textContent = stats.streak + '🔥';
    document.getElementById('stat-maxstreak').textContent = stats.maxStreak;
    document.getElementById('stat-left').textContent = TOTAL - currentDay;

    // Mission counts
    document.getElementById('ms-trabajar').textContent = stats.mc.Trabajar;
    document.getElementById('ms-entrenar').textContent = stats.mc.Entrenar;
    document.getElementById('ms-estudiar').textContent = stats.mc.Estudiar;

    // Today buttons
    const dd = getDay(currentDay);
    ['Trabajar','Entrenar','Estudiar'].forEach(m => {
      const btn = document.getElementById('mb-' + m.toLowerCase());
      const chk = document.getElementById('mc-' + m.toLowerCase());
      const done = !!dd.missions[m];
      if (done) {
        btn.style.background = COLORS[m] + '20';
        btn.style.borderColor = COLORS[m];
        btn.style.boxShadow = `0 0 18px ${COLORS[m]}55`;
        chk.textContent = '✓';
        chk.style.color = COLORS[m];
      } else {
        btn.style.background = '#0d0d15';
        btn.style.borderColor = 'var(--border)';
        btn.style.boxShadow = 'none';
        chk.textContent = '○';
        chk.style.color = 'var(--border)';
      }
    });

    // Completed banner
    const banner = document.getElementById('completed-banner');
    banner.style.display = dd.completed ? 'block' : 'none';

    // Note button
    const nb = document.getElementById('note-btn');
    nb.textContent = dd.note ? '✎ ' + dd.note.substring(0, 35) + (dd.note.length > 35 ? '...' : '') : '+ AÑADIR NOTA DEL DÍA';

    // Grid
    renderGrid();
  }

  function renderGrid() {
    const grid = document.getElementById('day-grid');
    grid.innerHTML = '';
    for (let d = 1; d <= TOTAL; d++) {
      const dd = getDay(d);
      const isCurrent = d === currentDay;
      const missCount = MISSIONS.filter(m => dd.missions[m]).length;

      const cell = document.createElement('div');
      cell.className = 'day-cell';
      cell.onclick = () => openModal(d);

      if (dd.completed) {
        cell.style.background = 'linear-gradient(135deg,rgba(0,212,170,0.15),rgba(124,111,255,0.15))';
        cell.style.borderColor = '#00d4aa';
        cell.style.color = '#00d4aa';
        cell.style.boxShadow = '0 0 8px rgba(0,212,170,0.18)';
      } else if (missCount > 0) {
        cell.style.background = 'rgba(255,107,53,0.08)';
        cell.style.borderColor = 'rgba(255,107,53,0.5)';
        cell.style.color = '#ff6b35';
      } else if (isCurrent) {
        cell.style.background = 'rgba(124,111,255,0.1)';
        cell.style.borderColor = '#7c6fff';
        cell.style.color = '#7c6fff';
        cell.style.boxShadow = '0 0 12px rgba(124,111,255,0.35)';
        cell.style.transform = 'scale(1.08)';
      } else if (d < currentDay) {
        cell.style.background = '#120808';
        cell.style.borderColor = '#1f0f0f';
        cell.style.color = '#2a1111';
      } else {
        cell.style.color = '#333';
      }

      const num = document.createElement('div');
      num.className = 'd-num'; num.textContent = d;
      cell.appendChild(num);

      if (missCount > 0) {
        const dots = document.createElement('div');
        dots.className = 'd-dots';
        MISSIONS.forEach(m => {
          const dot = document.createElement('div');
          dot.className = 'd-dot';
          if (dd.missions[m]) dot.style.background = COLORS[m];
          dots.appendChild(dot);
        });
        cell.appendChild(dots);
      }

      if (isCurrent) {
        const cd = document.createElement('div');
        cd.className = 'd-current-dot';
        cell.appendChild(cd);
      }

      grid.appendChild(cell);
    }
  }

  // MODAL
  function openModal(day) {
    modalDay = day;
    document.getElementById('modal-day-num').textContent = day;
    const dd = getDay(day);

    const mm = document.getElementById('modal-missions');
    mm.innerHTML = '';
    MISSIONS.forEach(m => {
      const done = !!dd.missions[m];
      const btn = document.createElement('div');
      btn.className = 'modal-mission' + (done ? ' done' : '');
      btn.innerHTML = `
        <span class="mm-icon">${ICONS[m]}</span>
        <span class="mm-name" style="color:${done ? COLORS[m] : '#888'}">${m.toUpperCase()}</span>
        <span class="mm-check" style="color:${done ? COLORS[m] : 'var(--border)'}">${done ? '✓' : '○'}</span>
      `;
      if (done) {
        btn.style.background = COLORS[m] + '15';
        btn.style.borderColor = COLORS[m];
      }
      btn.onclick = () => {
        toggleMission(day, m);
        openModal(day); // re-render modal
        renderAll();
      };
      mm.appendChild(btn);
    });

    document.getElementById('modal-note').value = dd.note || '';
    document.getElementById('modal-overlay').classList.add('open');
  }

  function closeModal(e) {
    if (!e || e.target === document.getElementById('modal-overlay') || !e.target) {
      document.getElementById('modal-overlay').classList.remove('open');
    }
  }

  function saveModal() {
    if (modalDay === null) return;
    const dd = getDay(modalDay);
    dd.note = document.getElementById('modal-note').value;
    setDay(modalDay, dd);
    document.getElementById('modal-overlay').classList.remove('open');
    renderAll();
  }

  // Day controls
  document.getElementById('day-minus').onclick = () => {
    if (currentDay > 1) { currentDay--; saveState(); renderAll(); }
  };
  document.getElementById('day-plus').onclick = () => {
    if (currentDay < TOTAL) { currentDay++; saveState(); renderAll(); }
  };

  // INIT
  renderAll();
</script>

</body>
</html>