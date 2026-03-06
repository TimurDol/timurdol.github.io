<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Hellenic Naval Combat — D&D 2024</title>
<link href="https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@400;700&family=Cinzel:wght@400;600;700&family=EB+Garamond:ital,wght@0,400;0,500;1,400&display=swap" rel="stylesheet">
<style>
  :root {
    --gold: #C9A84C;
    --gold-light: #E8CC7A;
    --gold-dark: #8B6914;
    --ink: #1A1208;
    --parchment: #F5EDD8;
    --parchment-dark: #E8DCC0;
    --red: #8B1A1A;
    --navy: #1A2744;
    --bronze: #7A4E2D;
    --wave: #2C5F7A;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background-color: var(--navy);
    background-image:
      radial-gradient(ellipse at 20% 50%, rgba(44,95,122,0.4) 0%, transparent 60%),
      radial-gradient(ellipse at 80% 20%, rgba(26,39,68,0.8) 0%, transparent 50%),
      url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%23ffffff' fill-opacity='0.02'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
    font-family: 'EB Garamond', serif;
    color: var(--ink);
    padding: 40px 20px;
    min-height: 100vh;
  }

  /* ── Language Toggle ── */
  .lang-toggle-wrap {
    display: flex;
    justify-content: center;
    margin-bottom: 22px;
  }
  .lang-toggle {
    display: flex;
    background: rgba(26,39,68,0.85);
    border: 1px solid var(--gold-dark);
    border-radius: 4px;
    overflow: hidden;
    box-shadow: 0 2px 12px rgba(0,0,0,0.4);
  }
  .lang-btn {
    padding: 9px 28px;
    font-family: 'Cinzel', serif;
    font-size: 13px;
    letter-spacing: 2px;
    color: var(--gold-light);
    background: transparent;
    border: none;
    cursor: pointer;
    transition: background 0.2s, color 0.2s, opacity 0.2s;
    text-transform: uppercase;
    opacity: 0.55;
  }
  .lang-btn.active { background: var(--gold-dark); color: var(--parchment); opacity: 1; }
  .lang-btn:hover:not(.active) { opacity: 0.85; }
  .lang-sep { width: 1px; background: var(--gold-dark); opacity: 0.5; }

  /* Language visibility */
  .ru { display: none; }
  body.lang-ru .en { display: none; }
  body.lang-ru .ru { display: revert; }

  .page-wrap { max-width: 900px; margin: 0 auto; position: relative; }

  .scroll-container {
    background: var(--parchment);
    background-image:
      url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='400' height='400'%3E%3Cfilter id='noise'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3CfeColorMatrix type='saturate' values='0'/%3E%3C/filter%3E%3Crect width='400' height='400' filter='url(%23noise)' opacity='0.04'/%3E%3C/svg%3E"),
      linear-gradient(180deg, var(--parchment-dark) 0%, var(--parchment) 5%, var(--parchment) 95%, var(--parchment-dark) 100%);
    border: 3px solid var(--gold-dark);
    box-shadow: 0 0 0 1px var(--gold), 0 0 40px rgba(0,0,0,0.6), inset 0 0 60px rgba(139,105,20,0.08);
    position: relative;
    overflow: hidden;
  }

  .corner { position: absolute; width: 80px; height: 80px; z-index: 10; }
  .corner svg { width: 100%; height: 100%; }
  .corner.tl { top: 8px; left: 8px; }
  .corner.tr { top: 8px; right: 8px; transform: scaleX(-1); }
  .corner.bl { bottom: 8px; left: 8px; transform: scaleY(-1); }
  .corner.br { bottom: 8px; right: 8px; transform: scale(-1); }

  .wave-band {
    height: 28px;
    background: var(--wave);
    background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 120 28' preserveAspectRatio='none'%3E%3Cpath d='M0 14 Q15 4 30 14 Q45 24 60 14 Q75 4 90 14 Q105 24 120 14 L120 0 L0 0 Z' fill='%231A2744'/%3E%3Cpath d='M0 20 Q15 10 30 20 Q45 30 60 20 Q75 10 90 20 Q105 30 120 20 L120 0 L0 0 Z' fill='%23C9A84C' opacity='0.3'/%3E%3C/svg%3E");
    background-size: 120px 28px;
    background-repeat: repeat-x;
  }
  .wave-band.bottom { transform: scaleY(-1); }

  .content-inner { padding: 50px 70px 60px; }

  .title-block { text-align: center; margin-bottom: 40px; }
  .subtitle-pre { font-family: 'Cinzel', serif; font-size: 11px; letter-spacing: 6px; color: var(--gold-dark); text-transform: uppercase; margin-bottom: 16px; }
  h1 { font-family: 'Cinzel Decorative', serif; font-size: clamp(24px, 4vw, 40px); color: var(--red); text-shadow: 2px 2px 0 rgba(139,105,20,0.2); line-height: 1.2; margin-bottom: 10px; }
  .title-sub { font-family: 'Cinzel', serif; font-size: 14px; color: var(--gold-dark); letter-spacing: 2px; margin-bottom: 20px; }
  .title-divider { display: flex; align-items: center; gap: 16px; margin: 20px auto; max-width: 500px; }
  .title-divider .line { flex: 1; height: 1px; background: linear-gradient(90deg, transparent, var(--gold-dark), transparent); }
  .title-divider .ornament { color: var(--gold); font-size: 18px; }
  .intro-text { font-style: italic; font-size: 16px; line-height: 1.7; color: #3a2a10; text-align: center; max-width: 680px; margin: 0 auto 40px; }

  .section { margin-bottom: 36px; }

  h2 { font-family: 'Cinzel', serif; font-size: 18px; color: var(--red); border-bottom: 2px solid var(--gold); padding-bottom: 8px; margin-bottom: 18px; display: flex; align-items: center; gap: 12px; }
  h2 .num { font-family: 'Cinzel Decorative', serif; font-size: 22px; color: var(--gold); line-height: 1; }
  h3 { font-family: 'Cinzel', serif; font-size: 12.5px; color: var(--bronze); text-transform: uppercase; letter-spacing: 2px; margin: 18px 0 8px; }
  p { font-size: 15px; line-height: 1.75; color: #2a1e0a; margin-bottom: 10px; }

  .rules-table { width: 100%; border-collapse: collapse; margin: 14px 0 20px; font-size: 14px; }
  .rules-table thead tr { background: var(--navy); color: var(--gold-light); }
  .rules-table thead th { font-family: 'Cinzel', serif; font-size: 11px; letter-spacing: 1.5px; padding: 9px 12px; text-align: left; text-transform: uppercase; }
  .rules-table tbody tr { border-bottom: 1px solid rgba(139,105,20,0.25); }
  .rules-table tbody tr:nth-child(even) { background: rgba(139,105,20,0.06); }
  .rules-table tbody td { padding: 8px 12px; vertical-align: top; line-height: 1.6; }
  .rules-table td:first-child { font-family: 'Cinzel', serif; font-size: 12px; color: var(--navy); font-weight: 600; }

  .callout { border-left: 4px solid var(--gold); background: rgba(201,168,76,0.10); padding: 14px 18px; margin: 16px 0; border-radius: 0 4px 4px 0; }
  .callout.red-callout { border-left-color: var(--red); background: rgba(139,26,26,0.07); }
  .callout strong { font-family: 'Cinzel', serif; font-size: 12px; color: var(--red); text-transform: uppercase; letter-spacing: 1px; display: block; margin-bottom: 6px; }

  ul, ol { padding-left: 22px; margin: 8px 0 12px; }
  li { font-size: 14.5px; line-height: 1.7; color: #2a1e0a; margin-bottom: 4px; }
  li::marker { color: var(--gold-dark); }
  ul li::marker { content: "⚓ "; font-size: 10px; }

  .phase-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(185px, 1fr)); gap: 14px; margin: 20px 0; }
  .phase-card { background: var(--navy); color: var(--parchment); padding: 16px 14px; border: 1px solid var(--gold-dark); border-top: 3px solid var(--gold); text-align: center; }
  .phase-card .phase-num { font-family: 'Cinzel Decorative', serif; font-size: 26px; color: var(--gold); display: block; line-height: 1; margin-bottom: 5px; }
  .phase-card .phase-name { font-family: 'Cinzel', serif; font-size: 11.5px; letter-spacing: 1.5px; color: var(--gold-light); text-transform: uppercase; display: block; margin-bottom: 7px; }
  .phase-card p { color: rgba(245,237,216,0.8); font-size: 12.5px; line-height: 1.5; margin: 0; }

  .ship-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin: 18px 0; }
  .ship-block { border: 1px solid var(--gold-dark); overflow: hidden; }
  .ship-block .ship-header { background: var(--navy); padding: 9px 14px; font-family: 'Cinzel', serif; color: var(--gold-light); font-size: 13px; letter-spacing: 0.8px; }
  .ship-block .ship-stats { padding: 10px 14px; display: grid; grid-template-columns: auto 1fr; gap: 3px 12px; }
  .ship-block .stat-label { font-family: 'Cinzel', serif; font-size: 10.5px; color: var(--bronze); text-transform: uppercase; letter-spacing: 0.8px; align-self: center; }
  .ship-block .stat-val { font-size: 13px; font-weight: 500; color: var(--ink); border-bottom: 1px dotted rgba(139,105,20,0.3); padding: 2px 0; }

  .ornament-divider { text-align: center; color: var(--gold); font-size: 20px; letter-spacing: 12px; margin: 28px 0; opacity: 0.7; }

  .footer { text-align: center; padding: 18px 0 10px; font-family: 'Cinzel', serif; font-size: 10px; color: var(--gold-dark); letter-spacing: 2px; text-transform: uppercase; border-top: 1px solid rgba(139,105,20,0.3); margin-top: 18px; }

  @media (max-width: 640px) {
    .content-inner { padding: 28px 18px 36px; }
    .ship-grid { grid-template-columns: 1fr; }
    h1 { font-size: 21px; }
    .rules-table { font-size: 12.5px; }
  }
</style>
</head>
<body>

<div class="lang-toggle-wrap">
  <div class="lang-toggle">
    <button class="lang-btn active" id="btn-en" onclick="setLang('en')">&#127468;&#127463; English</button>
    <div class="lang-sep"></div>
    <button class="lang-btn" id="btn-ru" onclick="setLang('ru')">&#127479;&#127482; Русский</button>
  </div>
</div>

<div class="page-wrap">
  <div class="scroll-container">

    <div class="corner tl"><svg viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M8 8 L8 72 M8 8 L72 8" stroke="#8B6914" stroke-width="2"/><path d="M16 16 L16 64 M16 16 L64 16" stroke="#C9A84C" stroke-width="1"/><path d="M8 8 C8 8 20 8 28 20 C36 32 32 48 44 56 C56 64 72 64 72 64" stroke="#C9A84C" stroke-width="1.5" fill="none"/><circle cx="8" cy="8" r="4" fill="#C9A84C"/></svg></div>
    <div class="corner tr"><svg viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M8 8 L8 72 M8 8 L72 8" stroke="#8B6914" stroke-width="2"/><path d="M16 16 L16 64 M16 16 L64 16" stroke="#C9A84C" stroke-width="1"/><path d="M8 8 C8 8 20 8 28 20 C36 32 32 48 44 56 C56 64 72 64 72 64" stroke="#C9A84C" stroke-width="1.5" fill="none"/><circle cx="8" cy="8" r="4" fill="#C9A84C"/></svg></div>
    <div class="corner bl"><svg viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M8 8 L8 72 M8 8 L72 8" stroke="#8B6914" stroke-width="2"/><path d="M16 16 L16 64 M16 16 L64 16" stroke="#C9A84C" stroke-width="1"/><path d="M8 8 C8 8 20 8 28 20 C36 32 32 48 44 56 C56 64 72 64 72 64" stroke="#C9A84C" stroke-width="1.5" fill="none"/><circle cx="8" cy="8" r="4" fill="#C9A84C"/></svg></div>
    <div class="corner br"><svg viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M8 8 L8 72 M8 8 L72 8" stroke="#8B6914" stroke-width="2"/><path d="M16 16 L16 64 M16 16 L64 16" stroke="#C9A84C" stroke-width="1"/><path d="M8 8 C8 8 20 8 28 20 C36 32 32 48 44 56 C56 64 72 64 72 64" stroke="#C9A84C" stroke-width="1.5" fill="none"/><circle cx="8" cy="8" r="4" fill="#C9A84C"/></svg></div>

    <div class="wave-band"></div>
    <div class="content-inner">

      <!-- TITLE -->
      <div class="title-block">
        <div class="subtitle-pre en">Supplement Rules for D&amp;D 2024</div>
        <div class="subtitle-pre ru">Дополнительные правила для D&amp;D 2024</div>
        <h1 class="en">Hellenic Naval Combat</h1>
        <h1 class="ru">Эллинский Морской Бой</h1>
        <div class="title-sub en">Rules for Ship-to-Ship Battles on the Wine-Dark Sea</div>
        <div class="title-sub ru">Правила корабельных сражений на тёмно-винном море</div>
        <div class="title-divider"><div class="line"></div><div class="ornament">&#9875;</div><div class="line"></div></div>
        <p class="intro-text en">"As when two warships clash upon the wine-dark sea, so too shall fate be decided not by a single blade, but by oar, ram, and the courage of every sailor." These rules bring the grandeur of Hellenic naval warfare to your table.</p>
        <p class="intro-text ru">«Как два боевых корабля сталкиваются на тёмно-винном море, так и судьба решается не одним клинком, но веслом, тараном и отвагой каждого моряка.» Эти правила переносят величие эллинских морских сражений за ваш игровой стол.</p>
      </div>

      <!-- I: OVERVIEW -->
      <div class="section">
        <h2><span class="num">I</span><span class="en">Overview &amp; Scale</span><span class="ru">Обзор и масштаб</span></h2>
        <p class="en">Naval combat uses <strong>Combat Rounds</strong> (6 seconds each), but ships act on a <strong>Ship Turn</strong> — once per round, after all crew have declared their actions. Each ship requires a crew filling key roles. A single creature may fill multiple roles on a small vessel.</p>
        <p class="ru">Морской бой использует <strong>раунды боя</strong> (по 6 секунд), но корабли действуют в <strong>корабельный ход</strong> — один раз за раунд, после объявления действий экипажа. Одно существо может занимать несколько ролей на малом судне.</p>
        <p class="en"><strong>Distance</strong> is measured in <strong>Ship Lengths (SL)</strong>. One SL ≈ 60 feet. Use a grid where 1 square = 1 SL, or describe distance narratively.</p>
        <p class="ru"><strong>Расстояние</strong> измеряется в <strong>Длинах корабля (ДК)</strong>. Одна ДК ≈ 18 м. Используйте сетку (1 клетка = 1 ДК) или описывайте расстояние словами.</p>
        <div class="callout en"><strong>The Golden Rule</strong>If a rule feels cumbersome in the moment, simplify it. These rules add drama, not slowdown. The DM always has final say.</div>
        <div class="callout ru"><strong>Золотое правило</strong>Если правило кажется громоздким — упростите его. Эти правила созданы для драмы, не для замедления. Мастер всегда имеет последнее слово.</div>
      </div>

      <!-- II: SHIPS -->
      <div class="section">
        <h2><span class="num">II</span><span class="en">Ship Statistics</span><span class="ru">Характеристики кораблей</span></h2>
        <p class="en">Each ship has the following statistics. The DM may adjust values to suit the campaign.</p>
        <p class="ru">Каждый корабль обладает следующими характеристиками. Мастер может корректировать значения под нужды кампании.</p>

        <div class="ship-grid">
          <div class="ship-block">
            <div class="ship-header en">&#9875; Trireme (Trières)</div>
            <div class="ship-header ru">&#9875; Триера (Trières)</div>
            <div class="ship-stats">
              <span class="stat-label en">Hull Points</span><span class="stat-label ru">Очки корпуса</span><span class="stat-val">200 HP</span>
              <span class="stat-label en">Armor Class</span><span class="stat-label ru">Класс брони</span><span class="stat-val">13</span>
              <span class="stat-label en">Speed</span><span class="stat-label ru">Скорость</span><span class="stat-val en">5 SL oars / 3 SL sail</span><span class="stat-val ru">5 ДК вёсла / 3 ДК парус</span>
              <span class="stat-label">Maneuver</span><span class="stat-val">+2</span>
              <span class="stat-label en">Ram Damage</span><span class="stat-label ru">Урон тараном</span><span class="stat-val">6d10</span>
              <span class="stat-label en">Min. Crew</span><span class="stat-label ru">Мин. экипаж</span><span class="stat-val en">30 (full: 170)</span><span class="stat-val ru">30 (полный: 170)</span>
              <span class="stat-label en">Capacity</span><span class="stat-label ru">Вместимость</span><span class="stat-val en">40 marines</span><span class="stat-val ru">40 воинов</span>
            </div>
          </div>
          <div class="ship-block">
            <div class="ship-header en">&#9875; Pentekonter (50-oar)</div>
            <div class="ship-header ru">&#9875; Пентеконтер</div>
            <div class="ship-stats">
              <span class="stat-label en">Hull Points</span><span class="stat-label ru">Очки корпуса</span><span class="stat-val">120 HP</span>
              <span class="stat-label en">Armor Class</span><span class="stat-label ru">Класс брони</span><span class="stat-val">12</span>
              <span class="stat-label en">Speed</span><span class="stat-label ru">Скорость</span><span class="stat-val en">4 SL oars / 3 SL sail</span><span class="stat-val ru">4 ДК вёсла / 3 ДК парус</span>
              <span class="stat-label">Maneuver</span><span class="stat-val">+3</span>
              <span class="stat-label en">Ram Damage</span><span class="stat-label ru">Урон тараном</span><span class="stat-val">4d10</span>
              <span class="stat-label en">Min. Crew</span><span class="stat-label ru">Мин. экипаж</span><span class="stat-val en">20 (full: 60)</span><span class="stat-val ru">20 (полный: 60)</span>
              <span class="stat-label en">Capacity</span><span class="stat-label ru">Вместимость</span><span class="stat-val en">20 marines</span><span class="stat-val ru">20 воинов</span>
            </div>
          </div>
          <div class="ship-block">
            <div class="ship-header en">&#9875; Merchant Vessel (Holkas)</div>
            <div class="ship-header ru">&#9875; Торговое судно (Holkas)</div>
            <div class="ship-stats">
              <span class="stat-label en">Hull Points</span><span class="stat-label ru">Очки корпуса</span><span class="stat-val">150 HP</span>
              <span class="stat-label en">Armor Class</span><span class="stat-label ru">Класс брони</span><span class="stat-val">11</span>
              <span class="stat-label en">Speed</span><span class="stat-label ru">Скорость</span><span class="stat-val en">2 SL oars / 4 SL sail</span><span class="stat-val ru">2 ДК вёсла / 4 ДК парус</span>
              <span class="stat-label">Maneuver</span><span class="stat-val">+0</span>
              <span class="stat-label en">Ram Damage</span><span class="stat-label ru">Урон тараном</span><span class="stat-val">2d10</span>
              <span class="stat-label en">Min. Crew</span><span class="stat-label ru">Мин. экипаж</span><span class="stat-val en">10 (full: 30)</span><span class="stat-val ru">10 (полный: 30)</span>
              <span class="stat-label en">Capacity</span><span class="stat-label ru">Вместимость</span><span class="stat-val en">Cargo + 10 fighters</span><span class="stat-val ru">Груз + 10 бойцов</span>
            </div>
          </div>
          <div class="ship-block">
            <div class="ship-header en">&#9875; Fishing Boat (Akatos)</div>
            <div class="ship-header ru">&#9875; Рыбацкая лодка (Akatos)</div>
            <div class="ship-stats">
              <span class="stat-label en">Hull Points</span><span class="stat-label ru">Очки корпуса</span><span class="stat-val">40 HP</span>
              <span class="stat-label en">Armor Class</span><span class="stat-label ru">Класс брони</span><span class="stat-val">10</span>
              <span class="stat-label en">Speed</span><span class="stat-label ru">Скорость</span><span class="stat-val en">3 SL oars / 3 SL sail</span><span class="stat-val ru">3 ДК вёсла / 3 ДК парус</span>
              <span class="stat-label">Maneuver</span><span class="stat-val">+4</span>
              <span class="stat-label en">Ram Damage</span><span class="stat-label ru">Урон тараном</span><span class="stat-val">1d10</span>
              <span class="stat-label en">Min. Crew</span><span class="stat-label ru">Мин. экипаж</span><span class="stat-val en">2 (full: 10)</span><span class="stat-val ru">2 (полный: 10)</span>
              <span class="stat-label en">Capacity</span><span class="stat-label ru">Вместимость</span><span class="stat-val en">4 fighters</span><span class="stat-val ru">4 бойца</span>
            </div>
          </div>
        </div>

        <h3 class="en">Hull Damage Thresholds</h3>
        <h3 class="ru">Пороги повреждений корпуса</h3>
        <p class="en">Ships track damage via <strong>Damage States</strong>, not per-attack HP.</p>
        <p class="ru">Корабли отслеживают урон через <strong>Состояния повреждения</strong>, а не поточечно.</p>
        <table class="rules-table">
          <thead><tr><th>HP %</th><th class="en">State</th><th class="ru">Состояние</th><th class="en">Effect</th><th class="ru">Эффект</th></tr></thead>
          <tbody>
            <tr><td>76–100%</td><td class="en">Intact</td><td class="ru">Цел</td><td class="en">No penalties.</td><td class="ru">Без штрафов.</td></tr>
            <tr><td>51–75%</td><td class="en">Strained</td><td class="ru">Повреждён</td><td class="en">Speed –1 SL.</td><td class="ru">Скорость –1 ДК.</td></tr>
            <tr><td>26–50%</td><td class="en">Damaged</td><td class="ru">Разбит</td><td class="en">Speed –2 SL; Maneuver –2.</td><td class="ru">Скорость –2 ДК; Манёвр –2.</td></tr>
            <tr><td>1–25%</td><td class="en">Crippled</td><td class="ru">Искалечен</td><td class="en">Speed –3 SL; Maneuver –4; taking on water.</td><td class="ru">Скорость –3 ДК; Манёвр –4; набирает воду.</td></tr>
            <tr><td>0</td><td class="en">Sinking</td><td class="ru">Тонет</td><td class="en">Sinks in 1d6 rounds. All aboard must swim or drown.</td><td class="ru">Тонет через 1d6 раундов. Все должны плыть.</td></tr>
          </tbody>
        </table>
      </div>

      <div class="ornament-divider">· · &#9876; · ·</div>

      <!-- III: CREW ROLES -->
      <div class="section">
        <h2><span class="num">III</span><span class="en">Crew Roles</span><span class="ru">Роли экипажа</span></h2>
        <p class="en">Each round, key positions must be filled. Unnamed crew work automatically but may be killed or panicked (see <em>Crew Morale</em>).</p>
        <p class="ru">Каждый раунд ключевые должности должны быть заняты. Безымянный экипаж действует автоматически, но может быть убит или впасть в панику (см. <em>Мораль экипажа</em>).</p>
        <table class="rules-table">
          <thead><tr><th class="en">Role</th><th class="ru">Роль</th><th class="en">Action</th><th class="ru">Действие</th><th class="en">Check</th><th class="ru">Проверка</th></tr></thead>
          <tbody>
            <tr><td class="en">Helmsman (Kybernetes)</td><td class="ru">Кормчий</td><td class="en">Steers ship; Maneuver rolls.</td><td class="ru">Управляет кораблём; броски манёвра.</td><td class="en">Dex (Athletics) or Wis (Survival)</td><td class="ru">Ловк (Атлетика) или Мудр (Выживание)</td></tr>
            <tr><td class="en">Oar-Master (Keleustes)</td><td class="ru">Нач. гребцов</td><td class="en">Controls ship Speed.</td><td class="ru">Контролирует скорость корабля.</td><td class="en">Cha (Persuasion) or Con</td><td class="ru">Хар (Убеждение) или Тел</td></tr>
            <tr><td class="en">Captain (Trierarchos)</td><td class="ru">Капитан</td><td class="en">Issues orders; grants Inspiration to one crew action.</td><td class="ru">Отдаёт приказы; даёт Вдохновение одному действию.</td><td class="en">Cha (Intimidation/Persuasion)</td><td class="ru">Хар (Запугивание/Убеждение)</td></tr>
            <tr><td class="en">Marines (Epibatai)</td><td class="ru">Морпехи</td><td class="en">Ranged attacks, repel boarders, lead boarding.</td><td class="ru">Дальние атаки, отражение абордажа.</td><td class="en">Attack rolls as normal</td><td class="ru">Броски атаки как обычно</td></tr>
            <tr><td class="en">Repair Crew</td><td class="ru">Ремонтники</td><td class="en">Patch hull damage.</td><td class="ru">Чинят повреждения корпуса.</td><td class="en">Int (tools) or Str</td><td class="ru">Инт (инструменты) или Сила</td></tr>
            <tr><td class="en">Lookout (Prorates)</td><td class="ru">Наблюдатель</td><td class="en">Spot enemies; warn of hazards.</td><td class="ru">Обнаруживает врагов; предупреждает об угрозах.</td><td class="en">Wis (Perception)</td><td class="ru">Мудрость (Восприятие)</td></tr>
          </tbody>
        </table>
        <div class="callout en"><strong>Playing as Crew</strong>PCs may take one Ship Action and one Personal Action per round. Ship Actions require occupying a crew role. Personal Actions are standard D&amp;D combat actions.</div>
        <div class="callout ru"><strong>Игра в роли экипажа</strong>ПИ совершают одно Действие корабля и одно Личное действие за раунд. Действия корабля требуют роли в экипаже. Личные действия — стандартные боевые действия D&amp;D.</div>
      </div>

      <!-- IV: ROUND STRUCTURE -->
      <div class="section">
        <h2><span class="num">IV</span><span class="en">Round Structure</span><span class="ru">Структура раунда</span></h2>
        <p class="en">Each round of naval combat follows these six phases in order.</p>
        <p class="ru">Каждый раунд морского боя следует шести фазам по порядку.</p>
        <div class="phase-grid">
          <div class="phase-card"><span class="phase-num">1</span><span class="phase-name en">Declaration</span><span class="phase-name ru">Объявление</span><p class="en">Each captain secretly declares their intended Ship Action.</p><p class="ru">Каждый капитан тайно объявляет планируемое Действие корабля.</p></div>
          <div class="phase-card"><span class="phase-num">2</span><span class="phase-name en">Initiative</span><span class="phase-name ru">Инициатива</span><p class="en">Both helmsmen roll Initiative (d20 + Dex). High roll resolves first.</p><p class="ru">Оба кормчих бросают инициативу (к20 + Ловк). Высший действует первым.</p></div>
          <div class="phase-card"><span class="phase-num">3</span><span class="phase-name en">Movement</span><span class="phase-name ru">Движение</span><p class="en">Ships move per their speed and helmsman's Maneuver roll.</p><p class="ru">Корабли движутся согласно скорости и броску манёвра кормчего.</p></div>
          <div class="phase-card"><span class="phase-num">4</span><span class="phase-name en">Ship Actions</span><span class="phase-name ru">Действия корабля</span><p class="en">Ramming, grappling, artillery, and ship-scale actions resolve.</p><p class="ru">Таран, абордаж, артиллерия и другие корабельные действия.</p></div>
          <div class="phase-card"><span class="phase-num">5</span><span class="phase-name en">Personal Actions</span><span class="phase-name ru">Личные действия</span><p class="en">Individual creatures (PCs, marines, monsters) take their turns.</p><p class="ru">Отдельные существа совершают личные ходы.</p></div>
          <div class="phase-card"><span class="phase-num">6</span><span class="phase-name en">End of Round</span><span class="phase-name ru">Конец раунда</span><p class="en">Check morale, apply fire/sinking, begin next round.</p><p class="ru">Проверьте мораль, применить огонь/затопление, начать следующий раунд.</p></div>
        </div>
      </div>

      <div class="ornament-divider">· · &#9876; · ·</div>

      <!-- V: MOVEMENT -->
      <div class="section">
        <h2><span class="num">V</span><span class="en">Movement &amp; Maneuvering</span><span class="ru">Движение и манёвры</span></h2>
        <p class="en">On its turn a ship moves up to its current Speed in Ship Lengths. Turning requires a <strong>Maneuver Roll</strong> from the helmsman.</p>
        <p class="ru">В свой ход корабль движется на величину своей Скорости в ДК. Для поворота кормчий делает <strong>бросок манёвра</strong>.</p>
        <table class="rules-table">
          <thead><tr><th class="en">Maneuver</th><th class="ru">Манёвр</th><th>DC/КС</th><th class="en">Notes</th><th class="ru">Примечание</th></tr></thead>
          <tbody>
            <tr><td class="en">Gentle turn (45°)</td><td class="ru">Плавный поворот (45°)</td><td>8</td><td class="en">Standard course correction.</td><td class="ru">Стандартная коррекция курса.</td></tr>
            <tr><td class="en">Sharp turn (90°)</td><td class="ru">Резкий поворот (90°)</td><td>13</td><td class="en">Requires half Speed remaining.</td><td class="ru">Требует половины оставшейся скорости.</td></tr>
            <tr><td class="en">Hard about (180°)</td><td class="ru">Полный разворот</td><td>18</td><td class="en">Costs all remaining Speed.</td><td class="ru">Расходует всю оставшуюся скорость.</td></tr>
            <tr><td class="en">Hold position</td><td class="ru">Удержание позиции</td><td>—</td><td class="en">No roll; ship holds station.</td><td class="ru">Без броска; корабль остаётся на месте.</td></tr>
            <tr><td class="en">Emergency evasion</td><td class="ru">Экстренное уклонение</td><td>15</td><td class="en">Disadvantage on one incoming ram/grapple this round.</td><td class="ru">Помеха на один входящий таран/абордаж.</td></tr>
          </tbody>
        </table>
        <h3 class="en">Wind &amp; Oar</h3><h3 class="ru">Ветер и вёсла</h3>
        <ul>
          <li class="en"><strong>Rowing:</strong> reliable speed but limited by Exhaustion. After 3 consecutive full-speed rounds, the Oar-Master rolls DC 12 or crew gains one Exhaustion level (Speed –1 SL).</li>
          <li class="ru"><strong>Гребля:</strong> надёжная скорость, ограниченная Истощением. После 3 раундов полного хода нач. гребцов проходит КС 12 или экипаж получает уровень Истощения (Скорость –1 ДК).</li>
          <li class="en"><strong>Sailing:</strong> free speed but needs favorable wind. Against the wind: –1 SL. With the wind: +1 SL.</li>
          <li class="ru"><strong>Паруса:</strong> бесплатная скорость при попутном ветре. Против ветра: –1 ДК. По ветру: +1 ДК.</li>
          <li class="en">Ships may combine oars and sail, taking the best Speed value.</li>
          <li class="ru">Корабли могут использовать и вёсла, и парус, беря лучшее значение скорости.</li>
        </ul>
      </div>

      <!-- VI: SHIP ACTIONS -->
      <div class="section">
        <h2><span class="num">VI</span><span class="en">Ship Actions</span><span class="ru">Действия корабля</span></h2>
        <p class="en">Each ship may take <strong>one Ship Action</strong> per round, declared in the Declaration phase.</p>
        <p class="ru">Каждый корабль совершает <strong>одно Действие корабля</strong> за раунд, объявляемое в фазе объявления.</p>

        <h3 class="en">The Ram (Embolos)</h3><h3 class="ru">Таран (Embolos)</h3>
        <p class="en">The ship must have at least 2 SL of movement remaining and the enemy must be in its front arc.</p>
        <p class="ru">Корабль должен иметь не менее 2 ДК движения, а враг — находиться в передней дуге.</p>
        <ol>
          <li class="en">Helmsman makes a Maneuver Roll vs DC 12 + target's Maneuver bonus.</li><li class="ru">Кормчий делает бросок манёвра против КС 12 + бонус манёвра цели.</li>
          <li class="en">Success: target takes Ram Damage; ramming ship takes <strong>half</strong>.</li><li class="ru">Успех: цель получает урон тараном; атакующий корабль — <strong>половину</strong>.</li>
          <li class="en">Failure by 5+ (<em>Glancing Blow</em>): both ships take one-quarter Ram Damage.</li><li class="ru">Провал на 5+ (<em>Скользящий удар</em>): оба корабля получают четверть урона.</li>
          <li class="en"><strong>Diekplous:</strong> Roll at Disadvantage. On success, shears enemy oars — target loses 2 SL Speed until repaired.</li><li class="ru"><strong>Диэкплус:</strong> Бросок с Помехой. Успех — срубает вёсла врага (–2 ДК скорости до починки).</li>
        </ol>

        <h3 class="en">Grapple &amp; Board (Katastrôma)</h3><h3 class="ru">Абордаж (Katastrôma)</h3>
        <p class="en">Ships must be adjacent (0 SL). The captain orders grappling hooks thrown.</p>
        <p class="ru">Корабли должны быть вплотную (0 ДК). Капитан приказывает бросить абордажные крюки.</p>
        <ol>
          <li class="en">Strength (Athletics) DC 12. Success: ships are <strong>Grappled</strong> (cutting lines requires a Ship Action, DC 15).</li><li class="ru">Сила (Атлетика) КС 12. Успех: корабли <strong>захвачены</strong> (перерубить тросы — Действие корабля, КС 15).</li>
          <li class="en">Once grappled, crew may cross to the enemy ship as part of movement (costs 10 ft).</li><li class="ru">После захвата экипаж может перейти на вражеский корабль как часть движения (3 м).</li>
          <li class="en">Boarding combat uses standard D&amp;D 2024 rules.</li><li class="ru">Абордажный бой использует стандартные правила D&amp;D 2024.</li>
        </ol>

        <h3 class="en">Artillery (Katapeltai)</h3><h3 class="ru">Артиллерия (Katapeltai)</h3>
        <table class="rules-table">
          <thead><tr><th class="en">Weapon</th><th class="ru">Оружие</th><th class="en">Range</th><th class="ru">Дальность</th><th class="en">Attack/Damage</th><th class="ru">Атака/Урон</th><th class="en">Special</th><th class="ru">Особое</th></tr></thead>
          <tbody>
            <tr><td class="en">Bolt-thrower (Oxybeles)</td><td class="ru">Стреломёт</td><td class="en">6/12 SL</td><td class="ru">6/12 ДК</td><td>+5 / 4d10 P</td><td class="en">Targets creatures or rigging</td><td class="ru">Существа или такелаж</td></tr>
            <tr><td class="en">Stone-thrower (Lithobolos)</td><td class="ru">Камнемёт</td><td class="en">4/8 SL</td><td class="ru">4/8 ДК</td><td>+3 / 6d10 B</td><td class="en">Deals hull damage</td><td class="ru">Наносит урон корпусу</td></tr>
            <tr><td class="en">Fire pot (Pyrophoros)</td><td class="ru">Огненный горшок</td><td class="en">2/4 SL</td><td class="ru">2/4 ДК</td><td>+4 / 3d8 Fire</td><td class="en">Ship catches fire on hit</td><td class="ru">Корабль загорается при попадании</td></tr>
          </tbody>
        </table>

        <h3 class="en">Full Sprint</h3><h3 class="ru">Полный ход</h3>
        <p class="en">Ship doubles oar Speed. Oar-Master rolls DC 14 Constitution or crew gains one Exhaustion level immediately.</p>
        <p class="ru">Корабль удваивает скорость вёсел. Нач. гребцов проходит КС 14 Телосложения или экипаж немедленно получает уровень Истощения.</p>

        <h3 class="en">Repair</h3><h3 class="ru">Ремонт</h3>
        <p class="en">One creature makes an Intelligence check with tools (DC 15). On a success, the ship recovers 2d10 + 5 Hull Points.</p>
        <p class="ru">Одно существо проходит проверку Интеллекта с инструментами (КС 15). Успех: корабль восстанавливает 2к10 + 5 очков корпуса.</p>

        <h3 class="en">Disengage</h3><h3 class="ru">Отход</h3>
        <p class="en">Helmsman Maneuver Roll (DC 15 if grappled; DC 10 otherwise). Success: moves full Speed away without provoking a free ram.</p>
        <p class="ru">Бросок манёвра кормчего (КС 15, если захвачены; КС 10 иначе). Успех: движется на полную скорость прочь без ответного тарана.</p>
      </div>

      <div class="ornament-divider">· · &#9876; · ·</div>

      <!-- VII: FIRE -->
      <div class="section">
        <h2><span class="num">VII</span><span class="en">Fire at Sea</span><span class="ru">Пожар на море</span></h2>
        <ul>
          <li class="en">When a ship <strong>catches fire</strong>, place a <em>Fire token</em> on it.</li><li class="ru">Когда корабль <strong>загорается</strong>, поместите на него жетон Огня.</li>
          <li class="en">End of each round: burning ship takes <strong>2d10 fire damage</strong> per Fire token.</li><li class="ru">В конце раунда: горящий корабль получает <strong>2к10 урона огнём</strong> за каждый жетон.</li>
          <li class="en">A crew member may douse fire (Personal Action): DC 14 Str or Dex check removes one token.</li><li class="ru">Член экипажа может тушить огонь (Личное действие): проверка Силы или Ловкости КС 14 убирает один жетон.</li>
          <li class="en">Each Fire token has a 1-in-6 chance per round of spawning another token on an adjacent area.</li><li class="ru">Каждый жетон Огня имеет шанс 1 из 6 в раунд создать ещё один жетон на соседнем участке.</li>
          <li class="en"><strong>Ablaze (3+ tokens):</strong> Crew must pass DC 12 Wisdom save each round or be Frightened.</li><li class="ru"><strong>Охвачен огнём (3+ жетона):</strong> Экипаж проходит спасбросок Мудрости КС 12 каждый раунд или получает Испуг.</li>
        </ul>
        <div class="callout red-callout en"><strong>Abandoning Ship</strong>Any creature may leap overboard as part of movement. Heavy armor wearers who fail DC 15 Athletics begin drowning (see D&amp;D 2024, Suffocation).</div>
        <div class="callout red-callout ru"><strong>Покинуть корабль</strong>Любое существо может прыгнуть за борт как часть движения. Существа в тяжёлой броне, провалившие Атлетику КС 15, начинают тонуть (D&amp;D 2024, Удушение).</div>
      </div>

      <!-- VIII: MORALE -->
      <div class="section">
        <h2><span class="num">VIII</span><span class="en">Crew Morale</span><span class="ru">Мораль экипажа</span></h2>
        <p class="en">At the following triggers, the captain makes a <strong>Morale Check</strong>: Charisma (Intimidation or Persuasion) DC 13.</p>
        <p class="ru">При следующих условиях капитан делает <strong>Проверку морали</strong>: Харизма (Запугивание или Убеждение) КС 13.</p>
        <ul>
          <li class="en">Ship drops below 50% Hull Points for the first time.</li><li class="ru">Корабль впервые опускается ниже 50% очков корпуса.</li>
          <li class="en">Ship catches fire.</li><li class="ru">Корабль загорается.</li>
          <li class="en">More than half the visible crew are slain in one round.</li><li class="ru">Более половины видимого экипажа убито за один раунд.</li>
          <li class="en">The captain is incapacitated or killed.</li><li class="ru">Капитан недееспособен или убит.</li>
        </ul>
        <table class="rules-table">
          <thead><tr><th class="en">Result</th><th class="ru">Результат</th><th class="en">Effect</th><th class="ru">Эффект</th></tr></thead>
          <tbody>
            <tr><td class="en">Success by 5+</td><td class="ru">Успех на 5+</td><td class="en">Inspired: +2 to all checks this round.</td><td class="ru">Вдохновлён: +2 ко всем проверкам в раунде.</td></tr>
            <tr><td class="en">Success</td><td class="ru">Успех</td><td class="en">Crew holds. No effect.</td><td class="ru">Экипаж держится. Без эффекта.</td></tr>
            <tr><td class="en">Failure</td><td class="ru">Провал</td><td class="en">Shaken: –2 to all Ship Actions next round.</td><td class="ru">Потрясён: –2 ко всем Действиям корабля в след. раунде.</td></tr>
            <tr><td class="en">Failure by 5+</td><td class="ru">Провал на 5+</td><td class="en">Routs: abandon stations; no Ship Actions until captain succeeds.</td><td class="ru">Бежит: покидают посты; нет Действий корабля до успеха капитана.</td></tr>
          </tbody>
        </table>
        <p class="en">A PC present on deck may substitute their own Charisma roll for the captain's Morale Check by spending their Personal Action.</p>
        <p class="ru">Персонаж игрока на палубе может заменить бросок капитана, потратив своё Личное действие.</p>
      </div>

      <!-- IX: PERSONAL COMBAT -->
      <div class="section">
        <h2><span class="num">IX</span><span class="en">Marines &amp; Personal Combat</span><span class="ru">Морпехи и личный бой</span></h2>
        <h3 class="en">Ranged Combat</h3><h3 class="ru">Дальний бой</h3>
        <ul>
          <li class="en">Within 4 SL (240 ft) of another ship: no penalty.</li><li class="ru">В пределах 4 ДК от другого корабля: без штрафа.</li>
          <li class="en">4–8 SL: Disadvantage on ranged attacks due to distance and movement.</li><li class="ru">4–8 ДК: Помеха на дальние атаки из-за расстояния и движения.</li>
          <li class="en">Small weapons deal no hull damage unless a critical hit is scored.</li><li class="ru">Маленькое оружие не наносит урона корпусу, если это не критическое попадание.</li>
        </ul>
        <h3 class="en">The Unstable Deck</h3><h3 class="ru">Неустойчивая палуба</h3>
        <ul>
          <li class="en">When rammed, all creatures on that ship make <strong>DC 13 Dexterity save</strong> or fall Prone.</li><li class="ru">При таране все существа на корабле делают <strong>спасбросок Ловкости КС 13</strong> или падают ничком.</li>
          <li class="en">Moving across a burning deck: DC 10 Acrobatics or take 1d6 fire damage.</li><li class="ru">Движение по горящей палубе: Акробатика КС 10 или 1к6 урона огнём.</li>
          <li class="en">Medium-armor creatures knocked overboard make Athletics checks at Disadvantage.</li><li class="ru">Существа в средней броне, сброшенные за борт, делают Атлетику с Помехой.</li>
        </ul>
        <h3 class="en">The Boarding Party</h3><h3 class="ru">Абордажный отряд</h3>
        <p class="en">Once grappled, boarding follows normal D&amp;D initiative. Defenders behind railings have <strong>three-quarters cover</strong> (+5 AC and Dex saves).</p>
        <p class="ru">После захвата бой идёт по нормальной инициативе D&amp;D. Защитники за бортовыми поручнями имеют <strong>укрытие на 3/4</strong> (+5 КБ и спасброски Ловкости).</p>
        <div class="callout en"><strong>NPC Soldier Swarms</strong>To speed play, unnamed marines can be grouped as <strong>Swarms of Soldiers</strong> (AC 13, 45 HP, Multiattack 4d4 + 2). Defeat the swarm and the deck is won.</div>
        <div class="callout ru"><strong>Стаи солдат НПС</strong>Для ускорения безымянных морпехов объединяйте в <strong>Стаи солдат</strong> (КБ 13, 45 ОЗ, Мультиатака 4к4 + 2). Победите стаю — палуба взята.</div>
      </div>

      <div class="ornament-divider">· · &#9876; · ·</div>

      <!-- X: VICTORY -->
      <div class="section">
        <h2><span class="num">X</span><span class="en">Victory &amp; Defeat</span><span class="ru">Победа и поражение</span></h2>
        <table class="rules-table">
          <thead><tr><th class="en">Condition</th><th class="ru">Условие</th><th class="en">Result</th><th class="ru">Результат</th></tr></thead>
          <tbody>
            <tr><td class="en">Ship reaches 0 HP</td><td class="ru">Корабль достигает 0 ОЗ</td><td class="en">Ship sinks in 1d6 rounds; crew swims or surrenders.</td><td class="ru">Тонет через 1к6 раундов; экипаж плывёт или сдаётся.</td></tr>
            <tr><td class="en">Ship escapes by 10+ SL</td><td class="ru">Отрыв на 10+ ДК</td><td class="en">Pursuit at DM's discretion; escaping ship survives.</td><td class="ru">Преследование — на усм. Мастера; ушедший корабль выживает.</td></tr>
            <tr><td class="en">Grappled; all defenders slain/surrendered</td><td class="ru">Захват; все защитники убиты/сдались</td><td class="en">Boarding party claims the ship as a prize.</td><td class="ru">Абордажный отряд захватывает корабль как приз.</td></tr>
            <tr><td class="en">Captain surrenders</td><td class="ru">Капитан сдаётся</td><td class="en">Honorable surrender; victors may ransom crew or claim cargo.</td><td class="ru">Почётная сдача; победители получают выкуп или груз.</td></tr>
          </tbody>
        </table>
        <h3 class="en">Prizes &amp; Plunder</h3><h3 class="ru">Призы и добыча</h3>
        <p class="en">A captured intact ship is worth 3,000–15,000 gp depending on type. Captured enemy marines may be ransomed for 50 gp each, or impressed into service (Charisma DC 15).</p>
        <p class="ru">Захваченный целый корабль стоит 3 000–15 000 зм. Пленники выкупаются по 50 зм или принуждаются к службе (Харизма КС 15).</p>
      </div>

      <!-- XI: OPTIONAL -->
      <div class="section">
        <h2><span class="num">XI</span><span class="en">Optional Rules</span><span class="ru">Необязательные правила</span></h2>
        <h3 class="en">Divine Favor</h3><h3 class="ru">Божественное покровительство</h3>
        <p class="en">A PC who prays to Poseidon, Athena, or Ares and passes DC 14 Religion may once per battle reroll any one ship die roll, taking the better result. Each god may be invoked once per battle.</p>
        <p class="ru">ПИ, молящийся Посейдону, Афине или Аресу и проходящий Религию КС 14, может один раз за бой перебросить любой корабельный бросок и взять лучший результат. Каждый бог — один раз за бой.</p>
        <h3 class="en">Weather &amp; Poseidon's Wrath</h3><h3 class="ru">Погода и гнев Посейдона</h3>
        <p class="en">Roll a d6 at the start of each round. On a 6, a sudden squall strikes: all ships suffer –2 to Maneuver rolls and –1 SL Speed for that round.</p>
        <p class="ru">Бросайте к6 в начале каждого раунда. На 6 — шторм: все корабли получают –2 к манёвру и –1 ДК скорости в этом раунде.</p>
        <h3 class="en">Heroic Deeds</h3><h3 class="ru">Героические деяния</h3>
        <p class="en">A PC who kills the enemy captain in single combat during boarding immediately triggers a Morale Check for the enemy crew at Disadvantage.</p>
        <p class="ru">ПИ, убивший вражеского капитана в единоборстве при абордаже, немедленно вызывает Проверку морали врага с Помехой.</p>
        <h3 class="en">Fog of War</h3><h3 class="ru">Туман войны</h3>
        <p class="en">Captains write their Ship Actions secretly and reveal simultaneously. Adds tension and strategic bluffing to fleet engagements.</p>
        <p class="ru">Капитаны записывают Действия корабля тайно и раскрывают одновременно. Добавляет напряжение и блефование во флотские сражения.</p>
      </div>

      <!-- QUICK REF -->
      <div class="section">
        <h2><span class="num">&#10022;</span><span class="en">Quick Reference Card</span><span class="ru">Таблица быстрых правил</span></h2>
        <table class="rules-table">
          <thead><tr><th class="en">Situation</th><th class="ru">Ситуация</th><th class="en">Roll</th><th class="ru">Бросок</th><th>DC/КС</th></tr></thead>
          <tbody>
            <tr><td class="en">Ram the enemy</td><td class="ru">Таранить врага</td><td class="en">Helmsman Dex/Wis</td><td class="ru">Ловк/Мудр кормчего</td><td>12 (+Man.)</td></tr>
            <tr><td class="en">Sharp turn (90°)</td><td class="ru">Резкий поворот</td><td class="en">Helmsman Dex/Wis</td><td class="ru">Ловк/Мудр кормчего</td><td>13</td></tr>
            <tr><td class="en">Hard about (180°)</td><td class="ru">Полный разворот</td><td class="en">Helmsman Dex/Wis</td><td class="ru">Ловк/Мудр кормчего</td><td>18</td></tr>
            <tr><td class="en">Grapple enemy ship</td><td class="ru">Абордажный захват</td><td class="en">Str (Athletics)</td><td class="ru">Сила (Атлетика)</td><td>12</td></tr>
            <tr><td class="en">Cut grapple lines</td><td class="ru">Перерубить тросы</td><td class="en">Helmsman Dex/Wis</td><td class="ru">Ловк/Мудр кормчего</td><td>15</td></tr>
            <tr><td class="en">Repair hull</td><td class="ru">Починить корпус</td><td class="en">Int (tools)</td><td class="ru">Инт (инструменты)</td><td>15</td></tr>
            <tr><td class="en">Douse fire</td><td class="ru">Потушить огонь</td><td class="en">Str or Dex</td><td class="ru">Сила или Ловкость</td><td>14</td></tr>
            <tr><td class="en">Crew morale check</td><td class="ru">Мораль экипажа</td><td class="en">Cha (Intimidation/Persuasion)</td><td class="ru">Хар (Запугивание/Убеждение)</td><td>13</td></tr>
            <tr><td class="en">Ram survival (on deck)</td><td class="ru">Выжить при таране</td><td class="en">Dex save</td><td class="ru">Спасбросок Ловкости</td><td>13</td></tr>
            <tr><td class="en">Sprint sustain</td><td class="ru">Выдержать полный ход</td><td class="en">Oar-Master Con</td><td class="ru">Телосл. нач. гребцов</td><td>14</td></tr>
            <tr><td class="en">Diekplous (oar-shear)</td><td class="ru">Диэкплус</td><td class="en">Helmsman (Disadv.)</td><td class="ru">Кормчий (с Помехой)</td><td>12</td></tr>
          </tbody>
        </table>
      </div>

      <div class="footer">
        <span class="en">Hellenic Naval Combat &middot; Supplement for D&amp;D 2024 &middot; Not official Wizards of the Coast material</span>
        <span class="ru">Эллинский морской бой &middot; Дополнение к D&amp;D 2024 &middot; Не является официальным материалом Wizards of the Coast</span>
      </div>

    </div>
    <div class="wave-band bottom"></div>
  </div>
</div>

<script>
  function setLang(lang) {
    document.body.classList.toggle('lang-ru', lang === 'ru');
    document.getElementById('btn-en').classList.toggle('active', lang === 'en');
    document.getElementById('btn-ru').classList.toggle('active', lang === 'ru');
    document.documentElement.lang = lang;
  }
</script>
</body>
</html>
