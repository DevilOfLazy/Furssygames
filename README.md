[Furssy Games _ Play Beyond.html](https://github.com/user-attachments/files/35305385/Furssy.Games._.Play.Beyond.html)
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover" />
  <title>Furssy Games | Play Beyond</title>
  <meta name="description" content="사소한 상상이 멈추지 않는 플레이가 될 때까지. 독립 게임 스튜디오 Furssy Games의 공식 웹사이트입니다. 오리지널 IP AFW, 채굴 게임, 마인크래프트 서버 루미너스 에테르를 만들고 있습니다." />
  <meta name="theme-color" content="#0b0e13" />
  <meta name="color-scheme" content="dark" />

  <meta property="og:type" content="website" />
  <meta property="og:site_name" content="Furssy Games" />
  <meta property="og:title" content="Furssy Games | Play Beyond" />
  <meta property="og:description" content="조금 엉뚱하고, 그래서 더 재미있는 게임을 만드는 독립 게임 스튜디오." />
  <meta property="og:locale" content="ko_KR" />
  <meta name="twitter:card" content="summary" />
  <meta name="twitter:title" content="Furssy Games | Play Beyond" />
  <meta name="twitter:description" content="조금 엉뚱하고, 그래서 더 재미있는 게임을 만드는 독립 게임 스튜디오." />

  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Black+Han+Sans&family=Noto+Sans+KR:wght@400;500;700&family=JetBrains+Mono:wght@500;700&family=Unbounded:wght@500;700;900&display=swap" />
  <style>
:root {
  --bg: #0b0e13;
  --bg-2: #0e131a;
  --surface: #121821;
  --surface-2: #19222d;
  --text: #f3f6fa;
  --muted: #9ba8b8;
  --dim: #6b7787;
  --line: rgba(255,255,255,.10);
  --line-2: rgba(255,255,255,.18);
  --accent: #a8f06a;
  --accent-ink: #10150d;
  --accent-2: #63d9c4;
  --gold: #f5c66b;
  --max: 1200px;
  --radius: 14px;
  --ease: cubic-bezier(.2,.8,.2,1);
  --f-display: "Unbounded", "Black Han Sans", "Pretendard Variable", sans-serif;
  --f-kr-display: "Black Han Sans", "Pretendard Variable", sans-serif;
  --f-body: "Pretendard Variable", Pretendard, "Noto Sans KR", system-ui, sans-serif;
  --f-mono: "JetBrains Mono", ui-monospace, monospace;
}

* { box-sizing: border-box; }
html { scroll-behavior: smooth; scroll-padding-top: 84px; }
body {
  margin: 0;
  background: var(--bg);
  color: var(--text);
  font-family: var(--f-body);
  line-height: 1.6;
  -webkit-font-smoothing: antialiased;
  overflow-x: hidden;
}
a { color: inherit; text-decoration: none; }
button { font: inherit; cursor: pointer; color: inherit; }
img, svg, canvas { display: block; }
mark { background: none; color: var(--accent); }
::selection { background: var(--accent); color: var(--accent-ink); }
:focus-visible { outline: 2px solid var(--accent); outline-offset: 3px; border-radius: 4px; }
.sr-only { position: absolute; width: 1px; height: 1px; overflow: hidden; clip: rect(0 0 0 0); white-space: nowrap; }
.wrap { width: min(var(--max), calc(100% - 48px)); margin: 0 auto; }

.skip-link {
  position: fixed; left: 16px; top: -60px; z-index: 100; padding: 10px 16px;
  background: var(--accent); color: var(--accent-ink); font-weight: 800; border-radius: 8px;
  transition: top .2s;
}
.skip-link:focus { top: 16px; }

.grain {
  position: fixed; inset: 0; z-index: 90; pointer-events: none; opacity: .06;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='160' height='160'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='2' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
}
.scroll-progress { position: fixed; inset: 0 0 auto; height: 2px; z-index: 60; }
.scroll-progress span { display: block; height: 100%; width: 100%; background: linear-gradient(90deg, var(--accent), var(--accent-2)); transform-origin: 0 50%; transform: scaleX(0); }

/* ---------- NAV ---------- */
.topbar {
  position: fixed; inset: 0 0 auto; z-index: 50;
  border-bottom: 1px solid transparent;
  transition: background .3s, border-color .3s, transform .35s var(--ease);
}
.topbar.scrolled { background: rgba(11,14,19,.78); backdrop-filter: blur(16px); -webkit-backdrop-filter: blur(16px); border-color: var(--line); }
.topbar.hide { transform: translateY(-100%); }
.nav { height: 76px; display: flex; align-items: center; justify-content: space-between; gap: 20px; }
.brand { display: inline-flex; align-items: center; gap: 11px; }
.brand-mark {
  width: 34px; height: 34px; display: grid; place-items: center; border-radius: 10px;
  background: var(--accent); transition: transform .4s var(--ease);
}
.brand-mark svg { width: 26px; height: 26px; fill: var(--accent-ink); }
.brand:hover .brand-mark { transform: rotate(-12deg) scale(1.06); }
.brand-name { font-family: var(--f-display); font-weight: 900; font-size: 14px; letter-spacing: .02em; }
.brand-name em { font-style: normal; font-weight: 500; color: var(--muted); margin-left: 5px; }
.nav-links { display: flex; align-items: center; gap: 6px; font-family: var(--f-mono); font-size: 12px; font-weight: 700; color: var(--muted); }
.nav-links a { position: relative; padding: 8px 12px; border-radius: 6px; transition: color .2s, background .2s; }
.nav-links a i { font-style: normal; font-size: 9px; color: var(--dim); margin-right: 6px; vertical-align: 2px; }
.nav-links a:hover { color: var(--text); background: rgba(255,255,255,.04); }
.nav-links a.active { color: var(--accent); }
.nav-links a.active i { color: var(--accent); }
.nav-cta, .button {
  display: inline-flex; align-items: center; justify-content: center; gap: 9px;
  min-height: 48px; padding: 0 22px; border-radius: 8px;
  color: var(--accent-ink); background: var(--accent); font-size: 14px; font-weight: 800;
  border: 1px solid var(--accent);
  box-shadow: 0 4px 0 #6fa83f;
  transition: transform .15s var(--ease), box-shadow .15s var(--ease), background .2s;
}
.nav-cta:hover, .button:hover { transform: translateY(-2px); box-shadow: 0 6px 0 #6fa83f; background: #bcff80; }
.nav-cta:active, .button:active { transform: translateY(3px); box-shadow: 0 1px 0 #6fa83f; }
.nav-cta { min-height: 42px; font-size: 13px; padding: 0 18px; }
.nav-cta .dot { width: 8px; height: 8px; border-radius: 50%; background: var(--accent-ink); animation: pulse 1.6s infinite; }
.button.ghost { color: var(--text); background: rgba(255,255,255,.02); border-color: var(--line-2); box-shadow: 0 4px 0 rgba(255,255,255,.08); }
.button.ghost:hover { background: var(--surface-2); box-shadow: 0 6px 0 rgba(255,255,255,.08); }
.button .key { display: grid; place-items: center; width: 22px; height: 22px; border-radius: 5px; background: var(--accent); color: var(--accent-ink); font-size: 9px; }
.menu-toggle { display: none; position: relative; border: 1px solid var(--line); background: var(--surface); border-radius: 10px; width: 44px; height: 44px; }
.menu-toggle span { position: absolute; left: 12px; right: 12px; height: 2px; background: var(--text); border-radius: 2px; transition: transform .3s var(--ease), top .3s; }
.menu-toggle span:first-child { top: 16px; }
.menu-toggle span:last-child { top: 25px; }
.menu-toggle[aria-expanded="true"] span:first-child { top: 20px; transform: rotate(45deg); }
.menu-toggle[aria-expanded="true"] span:last-child { top: 20px; transform: rotate(-45deg); }

@keyframes pulse { 0%,100% { opacity: 1; transform: scale(1);} 50% { opacity: .35; transform: scale(.7);} }

/* ---------- HERO ---------- */
.hero {
  min-height: 100vh; min-height: 100svh; padding: 140px 0 40px; position: relative; overflow: hidden;
  display: flex; flex-direction: column; justify-content: center;
  background:
    radial-gradient(ellipse at 76% 42%, rgba(89,163,127,.18), transparent 38%),
    radial-gradient(ellipse at 12% 90%, rgba(87,109,175,.14), transparent 38%);
}
.hero::after {
  content: ""; position: absolute; inset: 0; pointer-events: none;
  background-image: linear-gradient(var(--line) 1px, transparent 1px), linear-gradient(90deg, var(--line) 1px, transparent 1px);
  background-size: 64px 64px; opacity: .25;
  mask-image: radial-gradient(ellipse at 60% 40%, #000 10%, transparent 65%);
  -webkit-mask-image: radial-gradient(ellipse at 60% 40%, #000 10%, transparent 65%);
}
.hero-canvas { position: absolute; inset: 0; width: 100%; height: 100%; z-index: 0; }
.hero-grid { display: grid; grid-template-columns: 1.15fr .85fr; align-items: center; gap: 40px; position: relative; z-index: 1; }
.eyebrow { font-family: var(--f-mono); color: var(--accent); font-size: 11px; font-weight: 700; letter-spacing: .16em; }
.blink { animation: blink 1s steps(1) infinite; }
@keyframes blink { 50% { opacity: 0; } }
.hero-title {
  margin: 22px 0 26px; font-family: var(--f-kr-display); font-weight: 400;
  font-size: clamp(44px, 7vw, 96px); line-height: 1.04; letter-spacing: -.02em; word-break: keep-all;
}
.hero-title .line { display: block; }
.hero-title mark { position: relative; display: inline-block; color: var(--accent-ink); padding: 0 .12em; }
.hero-title mark::before { content: ""; position: absolute; inset: .1em -.02em .02em; background: var(--accent); z-index: -1; transform: skewX(-8deg) scaleX(0); transform-origin: left; animation: swipe .7s .9s var(--ease) forwards; }
@keyframes swipe { to { transform: skewX(-8deg) scaleX(1); } }
.hero-title .caret { color: var(--accent); animation: blink 1s steps(1) infinite; }
.hero-copy { max-width: 520px; color: var(--muted); font-size: 17px; line-height: 1.85; word-break: keep-all; }
.hero-copy strong { color: var(--text); }
.hero-actions { display: flex; gap: 14px; flex-wrap: wrap; margin-top: 36px; }

.reveal-load { opacity: 0; transform: translateY(26px); animation: rise .9s var(--ease) forwards; animation-delay: calc(var(--d) * 110ms + 100ms); }
@keyframes rise { to { opacity: 1; transform: none; } }

.hero-art { position: relative; aspect-ratio: 1; max-width: 460px; width: 100%; justify-self: center; }
.art-frame { position: absolute; inset: 0; display: grid; place-items: center; transition: transform .2s linear; transform-style: preserve-3d; }
.art-orbit { position: absolute; border-radius: 50%; border: 1px solid rgba(255,255,255,.14); }
.art-orbit.o1 { inset: 4%; animation: spin 40s linear infinite; border-style: dashed; border-color: rgba(255,255,255,.16); }
.art-orbit.o2 { inset: 16%; border-color: rgba(168,240,106,.28); animation: spin 26s linear infinite reverse; }
.art-orbit.o2::after { content: ""; position: absolute; top: -5px; left: 50%; width: 10px; height: 10px; background: var(--accent); border-radius: 2px; }
.art-orbit.o3 { inset: 28%; border-color: rgba(99,217,196,.3); animation: spin 18s linear infinite; }
.art-orbit.o3::after { content: ""; position: absolute; bottom: 8%; right: 8%; width: 8px; height: 8px; background: var(--accent-2); border-radius: 50%; }
@keyframes spin { to { transform: rotate(360deg); } }
.art-core {
  width: 40%; aspect-ratio: 1;
  background: linear-gradient(145deg, #d8ff9e, #63d9c4 55%, #5861a5);
  box-shadow: 0 30px 90px rgba(99,217,196,.28), inset -14px -18px 40px rgba(20,30,60,.35);
  animation: morph 9s ease-in-out infinite;
}
@keyframes morph {
  0%,100% { border-radius: 27% 73% 58% 42% / 45% 39% 61% 55%; transform: rotate(25deg); }
  33% { border-radius: 58% 42% 33% 67% / 60% 52% 48% 40%; transform: rotate(60deg) scale(1.04); }
  66% { border-radius: 40% 60% 70% 30% / 35% 65% 35% 65%; transform: rotate(-5deg) scale(.97); }
}
.art-pixel { position: absolute; width: 12px; height: 12px; background: var(--accent); animation: bob 4s ease-in-out infinite; }
.art-pixel.p1 { top: 14%; left: 18%; }
.art-pixel.p2 { top: 70%; left: 8%; width: 8px; height: 8px; background: var(--accent-2); animation-delay: -1s; }
.art-pixel.p3 { top: 22%; right: 10%; width: 6px; height: 6px; background: var(--gold); animation-delay: -2s; }
.art-pixel.p4 { bottom: 10%; left: 46%; width: 9px; height: 9px; background: #8c84d6; animation-delay: -3s; }
@keyframes bob { 0%,100% { transform: translateY(0);} 50% { transform: translateY(-14px);} }
.art-hud { position: absolute; padding: 11px 14px; border: 1px solid var(--line); border-radius: 10px; background: rgba(18,24,33,.82); backdrop-filter: blur(8px); -webkit-backdrop-filter: blur(8px); color: var(--muted); font-family: var(--f-mono); font-size: 10px; letter-spacing: .1em; }
.art-hud strong { display: block; color: var(--text); font-family: var(--f-body); font-size: 14px; letter-spacing: 0; }
.art-hud b { color: var(--accent); margin-right: 8px; }
.hud-br { right: -2%; bottom: 10%; }
.hud-tl { left: 0; top: 8%; }
.hud-tr { right: 4%; top: 2%; }
.hp { display: flex; gap: 3px; }
.hp i { width: 10px; height: 10px; background: var(--accent); }
.hp i.off { background: rgba(255,255,255,.15); }

.hero-stats {
  position: relative; z-index: 1; margin-top: 64px; padding-top: 26px; border-top: 1px solid var(--line);
  display: grid; grid-template-columns: repeat(3, 1fr) auto; gap: 28px; color: var(--muted); font-size: 12px;
}
.hero-stats span { font-family: var(--f-mono); color: var(--dim); font-size: 10px; }
.hero-stats strong { display: block; margin: 2px 0; color: var(--text); font-family: var(--f-display); font-size: 18px; font-weight: 700; letter-spacing: .01em; }
.scroll-hint { display: flex; align-items: center; gap: 10px; font-family: var(--f-mono); font-size: 10px; letter-spacing: .2em; color: var(--muted); }
.scroll-hint span { width: 22px; height: 34px; border: 1px solid var(--line-2); border-radius: 12px; position: relative; }
.scroll-hint span::after { content: ""; position: absolute; left: 50%; top: 7px; width: 3px; height: 7px; margin-left: -1.5px; border-radius: 2px; background: var(--accent); animation: wheel 1.8s infinite; }
@keyframes wheel { 0% { opacity: 1; transform: translateY(0);} 100% { opacity: 0; transform: translateY(12px);} }

/* ---------- MARQUEE ---------- */
.marquee { overflow: hidden; border-block: 1px solid var(--line); background: var(--accent); color: var(--accent-ink); transform: rotate(-1.2deg) scale(1.02); margin: 10px 0 -10px; position: relative; z-index: 2; }
.marquee-track { display: flex; width: max-content; gap: 28px; padding: 14px 0; animation: marquee 36s linear infinite; font-family: var(--f-display); font-weight: 900; font-size: 18px; white-space: nowrap; align-items: center; }
.marquee-track b { font-size: 14px; }
@keyframes marquee { to { transform: translateX(-50%); } }

/* ---------- SECTIONS ---------- */
section { padding: 120px 0; position: relative; }
.section-head { display: flex; justify-content: space-between; align-items: end; gap: 24px; margin-bottom: 44px; }
.section-kicker { font-family: var(--f-mono); color: var(--accent); font-size: 11px; font-weight: 700; letter-spacing: .16em; }
h2 { margin: 12px 0 0; font-family: var(--f-kr-display); font-weight: 400; font-size: clamp(34px, 4.6vw, 56px); line-height: 1.12; letter-spacing: -.01em; word-break: keep-all; }
.section-desc { max-width: 420px; color: var(--muted); font-size: 14px; line-height: 1.8; word-break: keep-all; }
.section-desc b { color: var(--text); }

.reveal { opacity: 0; transform: translateY(40px); transition: opacity .9s var(--ease), transform .9s var(--ease); transition-delay: var(--rd, 0ms); }
.reveal.in { opacity: 1; transform: none; }

/* ---------- PROJECTS ---------- */
.games { background: var(--bg-2); border-bottom: 1px solid var(--line); padding-top: 140px; }
.bento { display: grid; grid-template-columns: repeat(12, 1fr); grid-auto-rows: minmax(0, auto); gap: 18px; }
.game-card {
  grid-column: span 6; position: relative; overflow: hidden; border: 1px solid var(--line); border-radius: var(--radius);
  background: var(--surface); display: flex; flex-direction: column; cursor: pointer;
  transition: border-color .3s, box-shadow .3s, transform .6s var(--ease), opacity .9s var(--ease);
  transform-style: preserve-3d;
}
.game-card.featured { grid-column: span 7; grid-row: span 2; }
.game-card:not(.featured):not(.teaser) { grid-column: span 5; }
.game-card.teaser { grid-column: span 12; }
.game-card:hover, .game-card:focus-visible { border-color: rgba(168,240,106,.5); box-shadow: 0 24px 60px rgba(0,0,0,.35); }
.game-card::after {
  content: ""; position: absolute; inset: 0; pointer-events: none; opacity: 0; transition: opacity .3s;
  background: radial-gradient(400px circle at var(--mx, 50%) var(--my, 50%), rgba(168,240,106,.10), transparent 45%);
}
.game-card:hover::after { opacity: 1; }
.game-cover { min-height: 220px; flex: 1; display: grid; place-items: center; position: relative; overflow: hidden; }
.featured .game-cover { min-height: 380px; }
.cover-afw { background: radial-gradient(circle at 50% 48%, #678c72, #273b39 56%, #151d28); color: rgba(216,255,158,.75); }
.cover-mining { background: radial-gradient(circle at 50% 45%, #b1874e, #51402d 55%, #1d2026); }
.cover-aether { background: radial-gradient(circle at 48% 45%, #7c6bb0, #38335c 55%, #161929); color: rgba(220,210,255,.8); }
.cover-glyph { width: 52%; max-width: 240px; transition: transform .8s var(--ease); }
.cover-glyph svg { width: 100%; height: auto; }
.cover-glyph.pixels { width: 34%; max-width: 140px; image-rendering: pixelated; filter: drop-shadow(0 14px 30px rgba(0,0,0,.45)); }
.cover-glyph.pixels svg { border-radius: 6px; }
.game-card:hover .cover-glyph { transform: scale(1.08) rotate(8deg); }
.featured:hover .cover-glyph { transform: scale(1.06) rotate(-22deg); }
.cover-tag {
  position: absolute; top: 16px; left: 16px; z-index: 2; padding: 5px 10px; border-radius: 6px;
  color: #f3f6fa; background: rgba(11,14,19,.58); border: 1px solid rgba(255,255,255,.16);
  backdrop-filter: blur(6px); font-size: 11px; font-weight: 800;
}
.cover-tag::before { content: ""; display: inline-block; width: 6px; height: 6px; border-radius: 50%; background: var(--gold); margin-right: 7px; vertical-align: 1px; animation: pulse 1.6s infinite; }
.cover-tag.original { color: var(--accent-ink); background: var(--accent); border-color: var(--accent); }
.cover-tag.original::before { background: var(--accent-ink); }
.cover-index { position: absolute; right: 16px; bottom: 14px; font-family: var(--f-mono); font-size: 11px; color: rgba(255,255,255,.55); letter-spacing: .1em; }
.game-info { padding: 22px 24px 24px; display: flex; flex-direction: column; }
.game-meta { font-family: var(--f-mono); color: var(--accent); font-size: 10px; font-weight: 700; letter-spacing: .14em; }
.game-info h3 { margin: 9px 0 8px; font-family: var(--f-display); font-size: 22px; font-weight: 700; letter-spacing: -.01em; }
.featured .game-info h3 { font-size: 40px; font-weight: 900; }
.game-info h3 small { font-family: var(--f-body); font-size: 13px; color: var(--muted); font-weight: 600; }
.game-info p { margin: 0; color: var(--muted); font-size: 14px; line-height: 1.7; word-break: keep-all; }
.stage { display: flex; gap: 4px; margin-top: 18px; }
.stage span { flex: 1; padding: 6px 0 0; border-top: 3px solid rgba(255,255,255,.1); font-size: 10px; font-weight: 700; color: var(--dim); }
.stage span.done { border-color: rgba(168,240,106,.45); color: var(--muted); }
.stage span.on { border-color: var(--accent); color: var(--accent); }
.game-link { margin-top: 18px; color: var(--text); font-size: 13px; font-weight: 800; display: inline-flex; gap: 6px; }
.game-link span { color: var(--accent); transition: transform .3s var(--ease); }
.game-card:hover .game-link span { transform: translate(3px,-3px); }
.teaser {
  flex-direction: row; align-items: center; gap: 22px; padding: 26px 28px; background: transparent;
  border-style: dashed; border-color: var(--line-2);
}
.teaser-plus { display: grid; place-items: center; width: 52px; height: 52px; border-radius: 12px; border: 1px dashed var(--accent); color: var(--accent); font-size: 28px; transition: transform .4s var(--ease); flex: none; }
.teaser:hover .teaser-plus { transform: rotate(90deg); }
.teaser strong { font-family: var(--f-kr-display); font-weight: 400; font-size: 24px; }
.teaser > span:last-child { margin-left: auto; color: var(--muted); font-size: 13px; }

/* ---------- DIALOG ---------- */
.project-dialog {
  width: min(720px, calc(100% - 32px)); max-height: calc(100% - 48px); padding: 0; border: 1px solid var(--line-2); border-radius: 18px;
  background: var(--surface); color: var(--text); overflow: auto;
}
.project-dialog::backdrop { background: rgba(5,7,10,.72); backdrop-filter: blur(6px); -webkit-backdrop-filter: blur(6px); }
.project-dialog[open] { animation: pop .4s var(--ease); }
@keyframes pop { from { opacity: 0; transform: translateY(24px) scale(.97); } }
.dlg-cover { height: 200px; display: grid; place-items: center; }
.dlg-cover .cover-glyph { width: 130px; }
.dlg-body { position: relative; padding: 28px 32px 32px; }
.dlg-close { position: absolute; top: 16px; right: 16px; z-index: 2; width: 40px; height: 40px; border-radius: 10px; border: 1px solid rgba(255,255,255,.2); background: rgba(11,14,19,.6); }
.dlg-close:hover { background: var(--surface-2); }
.dlg-body h3 { margin: 10px 0 10px; font-family: var(--f-display); font-size: 32px; font-weight: 900; }
.dlg-body > p { color: var(--muted); margin: 0 0 20px; word-break: keep-all; }
.dlg-points { list-style: none; margin: 0 0 26px; padding: 0; display: grid; gap: 10px; }
.dlg-points li { display: flex; gap: 12px; padding: 14px 16px; border: 1px solid var(--line); border-radius: 10px; background: var(--bg-2); font-size: 14px; word-break: keep-all; }
.dlg-points li::before { content: "▸"; color: var(--accent); }
.dlg-actions { display: flex; gap: 12px; flex-wrap: wrap; }

/* ---------- PLAY ---------- */
.play { overflow: hidden; }
.play::before { content: ""; position: absolute; width: 700px; height: 700px; right: -200px; top: 50%; transform: translateY(-50%); background: radial-gradient(circle, rgba(245,198,107,.10), transparent 60%); pointer-events: none; }
.play-grid { display: grid; grid-template-columns: 1fr 420px; gap: 72px; align-items: center; }
.play-intro .section-desc { max-width: 480px; margin-top: 18px; }
.legend { list-style: none; padding: 0; margin: 28px 0 0; display: grid; grid-template-columns: repeat(2, minmax(0, 1fr)); gap: 10px 18px; max-width: 460px; font-size: 13px; color: var(--muted); }
.legend li { display: flex; align-items: center; gap: 10px; }
.legend i { width: 18px; height: 18px; border-radius: 3px; flex: none; box-shadow: inset 0 -3px 0 rgba(0,0,0,.25); }
.t-dirt { background: #6b4f33; } .t-stone { background: #5b6370; }
.t-copper { background: #d3814a; } .t-silver { background: #c9d3dd; }
.t-gold { background: var(--gold); } .t-gem { background: #9b8cff; }
.t-energy { background: var(--accent); } .t-rock { background: #23272f; border: 1px solid #3a404c; }
.controls { margin-top: 26px; display: flex; flex-direction: column; gap: 8px; color: var(--dim); font-size: 12px; }
kbd { display: inline-grid; place-items: center; min-width: 24px; height: 24px; padding: 0 6px; margin: 0 2px; border: 1px solid var(--line-2); border-bottom-width: 3px; border-radius: 5px; font-family: var(--f-mono); font-size: 11px; color: var(--text); background: var(--surface); }

.arcade {
  position: relative; padding: 16px; border-radius: 22px;
  background: linear-gradient(180deg, #1b2430, #121821);
  border: 1px solid var(--line-2);
  box-shadow: 0 40px 80px rgba(0,0,0,.45), inset 0 1px 0 rgba(255,255,255,.08);
}
.arcade-hud { display: grid; grid-template-columns: repeat(3, auto) 1fr; gap: 14px; align-items: end; padding: 4px 6px 12px; font-family: var(--f-mono); }
.arcade-hud small { display: block; font-size: 9px; color: var(--dim); letter-spacing: .14em; }
.arcade-hud b { font-size: 16px; color: var(--text); }
.arcade-hud #hudBest { color: var(--gold); }
.stamina .bar { display: block; height: 10px; border-radius: 3px; background: rgba(255,255,255,.08); overflow: hidden; margin-top: 5px; }
.stamina .bar i { display: block; height: 100%; width: 100%; background: linear-gradient(90deg, var(--accent-2), var(--accent)); transform-origin: left; transition: transform .2s; }
.stamina.low .bar i { background: #ff7a6b; animation: blink .5s steps(1) infinite; }
.arcade-screen { position: relative; border-radius: 12px; overflow: hidden; background: #0a0d12; border: 1px solid #000; }
.arcade-screen.shake { animation: shake .25s; }
@keyframes shake { 25% { transform: translate(-3px, 2px);} 50% { transform: translate(3px,-2px);} 75% { transform: translate(-2px,-1px);} }
#digCanvas { width: 100%; height: auto; image-rendering: pixelated; touch-action: manipulation; cursor: pointer; }
.arcade-overlay { position: absolute; inset: 0; display: grid; place-items: center; background: rgba(8,11,16,.78); backdrop-filter: blur(3px); -webkit-backdrop-filter: blur(3px); transition: opacity .3s; text-align: center; padding: 20px; }
.arcade-overlay.hidden { opacity: 0; pointer-events: none; }
.overlay-kicker { font-family: var(--f-mono); font-size: 10px; letter-spacing: .2em; color: var(--accent); }
.overlay-title { font-family: var(--f-display); font-weight: 900; font-size: 40px; margin: 8px 0 10px; color: var(--text); text-shadow: 0 4px 0 #6fa83f; }
.overlay-box p { color: var(--muted); font-size: 13px; margin: 0 0 22px; word-break: keep-all; }
.overlay-box p strong { color: var(--gold); }
.float-layer { position: absolute; inset: 0; pointer-events: none; }
.float-pop { position: absolute; font-family: var(--f-mono); font-weight: 700; font-size: 14px; transform: translate(-50%, -50%); animation: floatUp .9s var(--ease) forwards; text-shadow: 0 2px 0 rgba(0,0,0,.6); }
@keyframes floatUp { to { opacity: 0; transform: translate(-50%, -160%); } }
.arcade-pad { display: none; gap: 10px; justify-content: center; margin-top: 14px; }
.arcade-pad button { width: 64px; height: 52px; border-radius: 12px; border: 1px solid var(--line-2); background: var(--surface-2); font-size: 18px; box-shadow: 0 4px 0 rgba(0,0,0,.4); }
.arcade-pad button:active { transform: translateY(3px); box-shadow: 0 1px 0 rgba(0,0,0,.4); background: var(--accent); color: var(--accent-ink); }

/* ---------- ABOUT ---------- */
.about { background: var(--bg-2); border-block: 1px solid var(--line); }
.about-grid { display: grid; grid-template-columns: .9fr 1.1fr; gap: 90px; align-items: start; }
.about-head { position: sticky; top: 120px; }
.about-sticker { position: relative; width: 130px; height: 130px; margin-top: 40px; color: var(--accent); }
.about-sticker svg { width: 100%; height: 100%; animation: spin 18s linear infinite; }
.about-sticker text { font-family: var(--f-mono); font-size: 10.5px; font-weight: 700; letter-spacing: .12em; fill: currentColor; }
.about-sticker span { position: absolute; inset: 0; display: grid; place-items: center; font-family: var(--f-display); font-weight: 900; font-size: 34px; }
.about-copy { color: var(--muted); font-size: 16px; line-height: 1.95; word-break: keep-all; }
.about-copy p { margin: 0 0 20px; }
.about-copy .lead { color: var(--text); font-size: 22px; line-height: 1.6; font-weight: 600; letter-spacing: -.01em; }
.about-copy q { color: var(--accent); quotes: "‘" "’"; }
.values { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; margin-top: 36px; }
.value { position: relative; padding: 22px; border: 1px solid var(--line); border-radius: 12px; background: var(--surface); overflow: hidden; transition: border-color .3s, transform .3s var(--ease); }
.value:hover { border-color: rgba(168,240,106,.4); transform: translateY(-4px); }
.value b { position: absolute; right: 14px; top: 8px; font-family: var(--f-display); font-size: 44px; font-weight: 900; color: rgba(255,255,255,.04); transition: color .3s; }
.value:hover b { color: rgba(168,240,106,.14); }
.value strong { display: block; font-family: var(--f-mono); color: var(--accent); font-size: 11px; letter-spacing: .12em; }
.value span { display: block; margin-top: 8px; color: var(--text); font-size: 15px; font-weight: 700; }
.process { margin-top: 90px; display: grid; grid-template-columns: repeat(4, 1fr); border: 1px solid var(--line); border-radius: var(--radius); overflow: hidden; }
.process-step { padding: 28px 24px; border-right: 1px solid var(--line); position: relative; transition: background .3s; }
.process-step:last-child { border-right: 0; }
.process-step:hover { background: rgba(168,240,106,.04); }
.process-step span { font-family: var(--f-mono); font-size: 10px; color: var(--accent); letter-spacing: .14em; }
.process-step strong { display: block; margin: 10px 0 6px; font-size: 18px; }
.process-step p { margin: 0; color: var(--muted); font-size: 13px; word-break: keep-all; }
.process-step:not(:last-child)::after { content: "→"; position: absolute; right: -11px; top: 50%; transform: translateY(-50%); width: 22px; height: 22px; display: grid; place-items: center; background: var(--bg-2); color: var(--accent); font-size: 12px; z-index: 1; border-radius: 50%; border: 1px solid var(--line); }

/* ---------- NEWS ---------- */
.filters { display: flex; gap: 6px; flex-wrap: wrap; }
.filters button { padding: 8px 14px; border-radius: 999px; border: 1px solid var(--line-2); background: transparent; font-family: var(--f-mono); font-size: 11px; font-weight: 700; color: var(--muted); transition: all .2s; }
.filters button:hover { color: var(--text); border-color: var(--text); }
.filters button.active { background: var(--accent); color: var(--accent-ink); border-color: var(--accent); }
.news-list { border-top: 1px solid var(--line); }
.news-item { display: grid; grid-template-columns: 140px 1fr 40px; gap: 22px; align-items: center; padding: 28px 8px; border-bottom: 1px solid var(--line); position: relative; overflow: hidden; }
.news-item::before { content: ""; position: absolute; inset: 0; background: var(--accent); transform: scaleY(0); transform-origin: bottom; transition: transform .45s var(--ease); z-index: -1; }
.news-item { z-index: 0; transition: color .3s, padding .4s var(--ease); }
.news-item:hover { color: var(--accent-ink); padding-left: 22px; }
.news-item:hover::before { transform: scaleY(1); }
.news-item:hover time, .news-item:hover .news-type, .news-item:hover .news-arrow { color: var(--accent-ink); }
.news-item time { font-family: var(--f-mono); color: var(--muted); font-size: 12px; }
.news-type { display: block; margin-bottom: 4px; font-family: var(--f-mono); color: var(--accent); font-size: 10px; font-weight: 700; letter-spacing: .14em; }
.news-title { font-size: 18px; font-weight: 700; word-break: keep-all; }
.news-arrow { color: var(--muted); font-size: 22px; justify-self: end; transition: transform .3s var(--ease); }
.news-item:hover .news-arrow { transform: rotate(45deg); }
.news-item.out { display: none; }
.news-empty { padding: 40px 8px; color: var(--muted); text-align: center; }

/* ---------- CONTACT ---------- */
.contact { background: radial-gradient(ellipse at 20% 100%, rgba(168,240,106,.08), transparent 50%); }
.contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 64px; align-items: start; }
.contact-info > p { color: var(--muted); font-size: 15px; max-width: 440px; margin: 22px 0 0; word-break: keep-all; }
.contact-channels { margin-top: 34px; display: grid; gap: 12px; max-width: 440px; }
.channel { display: flex; align-items: center; gap: 16px; padding: 16px 18px; border: 1px solid var(--line); border-radius: 12px; background: var(--surface); text-align: left; transition: border-color .25s, transform .25s var(--ease); width: 100%; }
.channel:hover { border-color: var(--accent); transform: translateX(6px); }
.channel-icon { width: 42px; height: 42px; display: grid; place-items: center; border-radius: 10px; background: var(--surface-2); color: var(--accent); flex: none; }
.channel-icon svg { width: 22px; height: 22px; }
.channel small { display: block; font-family: var(--f-mono); font-size: 10px; color: var(--dim); letter-spacing: .14em; }
.channel > span:nth-child(2) { font-weight: 700; font-size: 15px; }
.channel-arrow { margin-left: auto; color: var(--muted); }
.copy-label { font-family: var(--f-mono); font-size: 11px; padding: 4px 8px; border: 1px solid var(--line-2); border-radius: 6px; }
.channel.copied .copy-label { background: var(--accent); color: var(--accent-ink); border-color: var(--accent); }

.contact-form { padding: 32px; border: 1px solid rgba(168,240,106,.24); border-radius: 18px; background: radial-gradient(ellipse at 50% 0%, rgba(168,240,106,.08), transparent 60%), var(--surface); }
.hp-field { position: absolute; left: -9999px; }
.topic { border: 0; padding: 0; margin: 0 0 22px; display: flex; flex-wrap: wrap; gap: 8px; }
.topic legend { font-size: 13px; font-weight: 700; margin-bottom: 10px; padding: 0; }
.topic label { cursor: pointer; }
.topic input { position: absolute; opacity: 0; pointer-events: none; }
.topic span { display: inline-block; padding: 8px 14px; border-radius: 999px; border: 1px solid var(--line-2); font-size: 13px; color: var(--muted); transition: all .2s; }
.topic label:hover span { color: var(--text); border-color: var(--text); }
.topic input:checked + span { background: var(--accent); color: var(--accent-ink); border-color: var(--accent); font-weight: 700; }
.topic input:focus-visible + span { outline: 2px solid var(--accent); outline-offset: 2px; }
.field { position: relative; margin-bottom: 18px; }
.field label { display: block; font-size: 13px; font-weight: 700; margin-bottom: 8px; }
.field input, .field textarea {
  width: 100%; padding: 14px 16px; border-radius: 10px; border: 1px solid var(--line-2); background: var(--bg);
  color: var(--text); font: inherit; font-size: 15px; transition: border-color .2s, box-shadow .2s; resize: vertical;
}
.field input::placeholder, .field textarea::placeholder { color: var(--dim); }
.field input:focus, .field textarea:focus { outline: none; border-color: var(--accent); box-shadow: 0 0 0 4px rgba(168,240,106,.12); }
.field.invalid input, .field.invalid textarea { border-color: #ff7a6b; }
.field .error { display: block; min-height: 0; color: #ff9a8e; font-size: 12px; margin-top: 6px; }
.field .error:empty { display: none; }
.counter { position: absolute; right: 12px; top: 2px; font-family: var(--f-mono); font-size: 10px; color: var(--dim); }
.submit { width: 100%; margin-top: 6px; }
.submit[disabled] { opacity: .65; cursor: progress; }
.submit.loading .label::after { content: ""; display: inline-block; width: 12px; height: 12px; margin-left: 10px; border: 2px solid currentColor; border-right-color: transparent; border-radius: 50%; animation: spin .7s linear infinite; vertical-align: -1px; }
.form-status { margin: 14px 0 0; font-size: 14px; text-align: center; min-height: 1.6em; }
.form-status.ok { color: var(--accent); }
.form-status.err { color: #ff9a8e; }
.contact-form.sent .field, .contact-form.sent .topic, .contact-form.sent .submit { opacity: .4; pointer-events: none; }

/* ---------- FOOTER ---------- */
footer { border-top: 1px solid var(--line); padding: 30px 0 34px; color: var(--muted); font-size: 12px; overflow: hidden; }
.footer-big { font-family: var(--f-display); font-weight: 900; font-size: clamp(48px, 12.5vw, 170px); line-height: .9; letter-spacing: -.03em; color: transparent; -webkit-text-stroke: 1px rgba(255,255,255,.12); white-space: nowrap; margin-bottom: 34px; user-select: none; }
.footer-inner { display: flex; justify-content: space-between; align-items: center; gap: 20px; }
.footer-links { display: flex; gap: 20px; flex-wrap: wrap; }
.footer-links a:hover { color: var(--accent); }

/* ---------- TOAST ---------- */
.toast { position: fixed; left: 50%; bottom: 28px; z-index: 80; transform: translate(-50%, 140%); padding: 12px 18px; border-radius: 10px; background: var(--accent); color: var(--accent-ink); font-weight: 800; font-size: 14px; box-shadow: 0 16px 40px rgba(0,0,0,.4); transition: transform .4s var(--ease); pointer-events: none; }
.toast.show { transform: translate(-50%, 0); }

/* ---------- RESPONSIVE ---------- */
@media (max-width: 1020px) {
  .play-grid { grid-template-columns: 1fr; gap: 44px; }
  .arcade { max-width: 440px; width: 100%; justify-self: center; }
  .contact-grid { grid-template-columns: 1fr; gap: 44px; }
  .nav-links a i { display: none; }
}
@media (max-width: 860px) {
  .wrap { width: min(100% - 36px, var(--max)); }
  .nav { height: 66px; }
  .menu-toggle { display: block; }
  .nav-links { position: fixed; top: 66px; left: 0; right: 0; padding: 18px; background: rgba(16,21,29,.98); border-bottom: 1px solid var(--line); flex-direction: column; align-items: stretch; gap: 4px; font-size: 15px; transform: translateY(-12px); opacity: 0; visibility: hidden; transition: all .3s var(--ease); }
  .nav-links a { padding: 14px 12px; }
  .nav-links a i { display: inline; }
  .nav-links.open { transform: none; opacity: 1; visibility: visible; }
  .topbar:has(.nav-links.open) { background: rgba(11,14,19,.96); border-color: var(--line); }
  .nav-cta { display: none; }
  .hero { min-height: auto; padding: 120px 0 40px; }
  .hero-grid { grid-template-columns: 1fr; gap: 10px; }
  .hero-art { max-width: 320px; order: -1; margin-bottom: -10px; }
  .hero-stats { grid-template-columns: 1fr 1fr 1fr; gap: 16px; margin-top: 44px; }
  .hero-stats strong { font-size: 14px; }
  .scroll-hint { display: none; }
  section { padding: 84px 0; }
  .games { padding-top: 100px; }
  .section-head { display: block; }
  .section-desc { margin-top: 15px; }
  .filters { margin-top: 20px; }
  .bento { grid-template-columns: 1fr; }
  .game-card, .game-card.featured, .game-card:not(.featured):not(.teaser), .game-card.teaser { grid-column: auto; grid-row: auto; }
  .featured .game-cover { min-height: 260px; }
  .featured .game-info h3 { font-size: 30px; }
  .teaser { flex-direction: column; align-items: flex-start; }
  .teaser > span:last-child { margin-left: 0; }
  .about-grid { grid-template-columns: 1fr; gap: 28px; }
  .about-head { position: static; }
  .about-sticker { display: none; }
  .process { grid-template-columns: 1fr 1fr; margin-top: 56px; }
  .process-step:nth-child(2) { border-right: 0; }
  .process-step:nth-child(-n+2) { border-bottom: 1px solid var(--line); }
  .process-step::after { display: none; }
  .news-item { grid-template-columns: 1fr 24px; gap: 6px 12px; padding: 22px 4px; }
  .news-item time { grid-column: 1 / -1; }
  .news-title { font-size: 16px; }
  .contact-form { padding: 22px; }
  .footer-inner { align-items: flex-start; flex-direction: column; }
  .dlg-body { padding: 22px; }
}
@media (hover: none), (max-width: 860px) {
  .arcade-pad { display: flex; }
}
@media (max-width: 480px) {
  .hero-stats { grid-template-columns: 1fr; }
  .process { grid-template-columns: 1fr; }
  .process-step { border-right: 0; border-bottom: 1px solid var(--line); }
  .process-step:last-child { border-bottom: 0; }
  .legend { grid-template-columns: 1fr 1fr; font-size: 12px; }
  .arcade { padding: 12px; }
  .arcade-hud { gap: 10px; }
}

@media (prefers-reduced-motion: reduce) {
  html { scroll-behavior: auto; }
  *, *::before, *::after { animation-duration: .01ms !important; animation-iteration-count: 1 !important; transition-duration: .01ms !important; }
  .reveal, .reveal-load { opacity: 1; transform: none; }
  .marquee-track { animation: none; }
}

:root{box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
html{background:#0b0e13}
</style>
</head>
<body>
  <a class="skip-link" href="#main">본문으로 건너뛰기</a>
  <div class="scroll-progress" aria-hidden="true"><span id="scrollBar"></span></div>
  <div class="grain" aria-hidden="true"></div>

  <header class="topbar" id="topbar">
    <div class="wrap nav">
      <a class="brand" href="#home" aria-label="Furssy Games 홈">
        <span class="brand-mark" aria-hidden="true"><svg viewBox="0 0 64 64"><path d="M20 14h26v9H30v7h13v9H30v11H20z"/><rect x="42" y="42" width="8" height="8"/></svg></span>
        <span class="brand-name">FURSSY<em>GAMES</em></span>
      </a>
      <button class="menu-toggle" id="menuToggle" aria-label="메뉴 열기" aria-expanded="false" aria-controls="navLinks">
        <span></span><span></span>
      </button>
      <nav class="nav-links" id="navLinks" aria-label="주요 메뉴">
        <a href="#games" data-nav="games"><i>01</i>PROJECTS</a>
        
        <a href="#about" data-nav="about"><i>03</i>ABOUT</a>
        <a href="#news" data-nav="news"><i>04</i>NEWS</a>
        <a href="#contact" data-nav="contact"><i>05</i>CONTACT</a>
      </nav>
      <a class="nav-cta" href="#contact"><span class="dot" aria-hidden="true"></span>문의하기</a>
    </div>
  </header>

  <main id="main">
    <!-- HERO -->
    <section class="hero" id="home">
      <canvas class="hero-canvas" id="heroCanvas" aria-hidden="true"></canvas>
      <div class="wrap hero-grid">
        <div class="hero-text">
          <div class="eyebrow reveal-load" style="--d:0"><span class="blink" aria-hidden="true">▮</span> INDEPENDENT GAME STUDIO</div>
          <h1 class="hero-title">
            <span class="line reveal-load" style="--d:1">사소한 상상이</span>
            <span class="line reveal-load" style="--d:2">멈추지 않는 <mark>플레이</mark>가</span>
            <span class="line reveal-load" style="--d:3">될 때까지<span class="caret" aria-hidden="true">.</span></span>
          </h1>
          <p class="hero-copy reveal-load" style="--d:4">조금 엉뚱하고, 그래서 더 재미있는 게임을 만드는 스튜디오 <strong>Furssy Games</strong>입니다. 머릿속에 떠오른 재미있는 장면을 직접 경험할 수 있는 세계로 옮깁니다.</p>
          <div class="hero-actions reveal-load" style="--d:5">
            <a class="button" href="#games">프로젝트 둘러보기 <span aria-hidden="true">↘</span></a>
            <a class="button ghost" href="#about">스튜디오 소개</a>
          </div>
        </div>

        <div class="hero-art reveal-load" style="--d:3" id="heroArt">
          <div class="art-frame">
            <div class="art-orbit o1"></div>
            <div class="art-orbit o2"></div>
            <div class="art-orbit o3"></div>
            <div class="art-core"></div>
            <span class="art-pixel p1"></span><span class="art-pixel p2"></span><span class="art-pixel p3"></span><span class="art-pixel p4"></span>
          </div>
          <div class="art-hud hud-tl"><b>LV.01</b>STUDIO</div>
          <div class="art-hud hud-br">FURSSY GAMES<strong>Play Beyond Limits</strong></div>
          <div class="art-hud hud-tr" aria-hidden="true"><span class="hp"><i></i><i></i><i></i><i></i><i class="off"></i></span></div>
        </div>
      </div>

      <div class="wrap hero-stats reveal-load" style="--d:6">
        <div><span>01</span><strong>IMAGINE</strong>엉뚱하고 즐거운 발상</div>
        <div><span>02</span><strong>CREATE</strong>직접 부딪히며 만드는 재미</div>
        <div><span>03</span><strong>PLAY</strong>다시 켜고 싶어지는 순간</div>
        <a class="scroll-hint" href="#games" aria-label="아래로 스크롤"><span></span>SCROLL</a>
      </div>
    </section>

    <div class="marquee" aria-hidden="true">
      <div class="marquee-track">
        <span>IMAGINE</span><b>✦</b><span>사소한 상상</span><b>✦</b><span>CREATE</span><b>✦</b><span>끝까지 다듬기</span><b>✦</b><span>PLAY</span><b>✦</b><span>다시 켜고 싶은 순간</span><b>✦</b>
        <span>IMAGINE</span><b>✦</b><span>사소한 상상</span><b>✦</b><span>CREATE</span><b>✦</b><span>끝까지 다듬기</span><b>✦</b><span>PLAY</span><b>✦</b><span>다시 켜고 싶은 순간</span><b>✦</b>
      </div>
    </div>

    <!-- PROJECTS -->
    <section class="games" id="games">
      <div class="wrap">
        <div class="section-head reveal">
          <div>
            <div class="section-kicker">01 / OUR PROJECTS</div>
            <h2>우리가 만들고 있는 세계</h2>
          </div>
          <p class="section-desc">원작 세계관부터 신작 채굴 게임, 마인크래프트 서버까지. 카드를 눌러 각 프로젝트의 자세한 이야기를 확인해 보세요.</p>
        </div>

        <div class="bento">
          <article class="game-card featured reveal" data-project="afw" tabindex="0" role="button" aria-haspopup="dialog" aria-label="AFW 프로젝트 자세히 보기">
            <div class="game-cover cover-afw">
              <div class="cover-glyph" aria-hidden="true">
                <svg viewBox="0 0 200 200"><g fill="none" stroke="currentColor" stroke-width="1.2"><circle cx="100" cy="100" r="70"/><circle cx="100" cy="100" r="46" stroke-dasharray="4 6"/><path d="M100 18v164M18 100h164M42 42l116 116M158 42 42 158"/></g><rect x="88" y="88" width="24" height="24" fill="currentColor" transform="rotate(45 100 100)"/></svg>
              </div>
              <span class="cover-tag original">원작 제작중</span>
              <span class="cover-index">P—01</span>
            </div>
            <div class="game-info">
              <div class="game-meta">ORIGINAL IP · WORLDVIEW</div>
              <h3>AFW</h3>
              <p>Furssy Games만의 개성과 이야기를 담아 처음부터 새롭게 빚어내고 있는 오리지널 원작 프로젝트입니다.</p>
              <div class="stage" aria-label="진행 단계: 세계관 구축">
                <span class="on">세계관</span><span>기획</span><span>개발</span><span>공개</span>
              </div>
              <span class="game-link">자세히 보기 <span aria-hidden="true">↗</span></span>
            </div>
          </article>

          <article class="game-card reveal" data-project="mining" tabindex="0" role="button" aria-haspopup="dialog" aria-label="Mining Game 프로젝트 자세히 보기">
            <div class="game-cover cover-mining">
              <div class="cover-glyph pixels" aria-hidden="true">
                <svg viewBox="0 0 8 8" shape-rendering="crispEdges"><path fill="#3a2d20" d="M0 0h8v8H0z"/><path fill="#5a4530" d="M0 0h8v2H0z"/><path fill="#7a5c3a" d="M1 3h2v1H1zM5 4h2v1H5zM2 6h1v1H2z"/><path fill="#f5c66b" d="M3 4h2v2H3z"/><path fill="#fff1c2" d="M3 4h1v1H3z"/><path fill="#63d9c4" d="M6 6h1v1H6z"/></svg>
              </div>
              <span class="cover-tag">개발중</span>
              <span class="cover-index">P—02</span>
            </div>
            <div class="game-info">
              <div class="game-meta">MINING · ADVENTURE</div>
              <h3>Mining Game <small>(가제)</small></h3>
              <p>깊은 땅속을 파고들며 미지의 자원을 발견하고 성장해 나가는 손맛 가득한 채굴 게임 프로젝트입니다.</p>
              <div class="stage" aria-label="진행 단계: 개발">
                <span class="done">기획</span><span class="on">개발</span><span>테스트</span><span>출시</span>
              </div>
              <span class="game-link">자세히 보기 <span aria-hidden="true">↗</span></span>
            </div>
          </article>

          <article class="game-card reveal" data-project="aether" tabindex="0" role="button" aria-haspopup="dialog" aria-label="루미너스 에테르 프로젝트 자세히 보기">
            <div class="game-cover cover-aether">
              <div class="cover-glyph" aria-hidden="true">
                <svg viewBox="0 0 200 200"><g fill="none" stroke="currentColor" stroke-width="1.2"><path d="M100 22 168 61v78l-68 39-68-39V61z"/><path d="M100 22v78l68 39M100 100 32 139" stroke-dasharray="3 5"/></g><path d="M100 70l9 21 21 9-21 9-9 21-9-21-21-9 21-9z" fill="currentColor"/></svg>
              </div>
              <span class="cover-tag">개발중</span>
              <span class="cover-index">P—03</span>
            </div>
            <div class="game-info">
              <div class="game-meta">MINECRAFT SERVER</div>
              <h3>루미너스 에테르</h3>
              <p>새로운 모험과 함께 어울리는 즐거움을 경험할 수 있도록 구축 중인 Furssy Games의 마인크래프트 서버입니다.</p>
              <div class="stage" aria-label="진행 단계: 구축">
                <span class="done">기획</span><span class="on">구축</span><span>베타</span><span>오픈</span>
              </div>
              <span class="game-link">자세히 보기 <span aria-hidden="true">↗</span></span>
            </div>
          </article>

          <a class="game-card teaser reveal" href="#contact">
            <span class="teaser-plus" aria-hidden="true">+</span>
            <strong>다음 상상은 무엇일까요?</strong>
            <span>아이디어나 협업 제안이 있다면 들려주세요 ↗</span>
          </a>
        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section class="about" id="about">
      <div class="wrap about-grid">
        <div class="about-head reveal">
          <div class="section-kicker">03 / ABOUT US</div>
          <h2>조금 엉뚱하지만,<br />그래서 더 <mark>재미있게.</mark></h2>
          <div class="about-sticker" aria-hidden="true">
            <svg viewBox="0 0 120 120"><defs><path id="circ" d="M60 60m-46 0a46 46 0 1 1 92 0a46 46 0 1 1-92 0"/></defs><text><textPath href="#circ">FUN FIRST · PLAY BEYOND · FUN FIRST · PLAY BEYOND ·</textPath></text></svg>
            <span>F</span>
          </div>
        </div>
        <div class="about-copy reveal">
          <p class="lead">Furssy Games는 머릿속에 떠오른 재미있는 장면을 직접 플레이할 수 있는 세계로 옮기는 독립 게임 스튜디오입니다.</p>
          <p>정해진 공식에 갇히기보다 <q>이거 해보면 진짜 재미있겠다</q>라는 순수한 호기심에서 출발합니다. 우리는 플레이어와 가까이 호흡하며 피드백을 나누고, 어제보다 오늘 더 나은 재미를 더해가며 다시 켜고 싶어지는 게임을 꾸준히 선보입니다.</p>
          <div class="values">
            <div class="value"><b>01</b><strong>IMAGINATION</strong><span>사소한 상상을 현실로</span></div>
            <div class="value"><b>02</b><strong>FUN FIRST</strong><span>직관적이고 즐거운 플레이</span></div>
            <div class="value"><b>03</b><strong>TOGETHER</strong><span>플레이어와 가까이 호흡</span></div>
            <div class="value"><b>04</b><strong>PERSISTENCE</strong><span>끝까지 다듬는 집요함</span></div>
          </div>
        </div>
      </div>

      <div class="wrap process reveal">
        <div class="process-step"><span>STEP 01</span><strong>떠올리기</strong><p>"이러면 재밌겠다" 하는 장면 하나에서 시작합니다.</p></div>
        <div class="process-step"><span>STEP 02</span><strong>만들어보기</strong><p>빠르게 프로토타입을 만들고 직접 부딪혀 봅니다.</p></div>
        <div class="process-step"><span>STEP 03</span><strong>함께 다듬기</strong><p>플레이어의 피드백으로 재미를 한 겹씩 더합니다.</p></div>
        <div class="process-step"><span>STEP 04</span><strong>다시 켜게 만들기</strong><p>한 판 더 하고 싶어질 때까지 집요하게 손봅니다.</p></div>
      </div>
    </section>

    <!-- NEWS -->
    <section class="news" id="news">
      <div class="wrap">
        <div class="section-head reveal">
          <div><div class="section-kicker">04 / LATEST NEWS</div><h2>스튜디오 소식</h2></div>
          <div class="filters" role="tablist" aria-label="소식 분류">
            <button type="button" role="tab" class="active" aria-selected="true" data-filter="all">ALL</button>
            <button type="button" role="tab" aria-selected="false" data-filter="studio">STUDIO</button>
            <button type="button" role="tab" aria-selected="false" data-filter="project">PROJECT</button>
            <button type="button" role="tab" aria-selected="false" data-filter="minecraft">MINECRAFT</button>
          </div>
        </div>
        <div class="news-list reveal" id="newsList">
          <a class="news-item" href="#home" data-type="studio">
            <time datetime="2026-11-23">2026. 11. 23</time>
            <div><span class="news-type">STUDIO</span><div class="news-title">Furssy Games 공식 웹사이트 오픈</div></div>
            <span class="news-arrow" aria-hidden="true">↗</span>
          </a>
          <a class="news-item" href="#games" data-type="project">
            <time datetime="2026-11-15">2026. 11. 15</time>
            <div><span class="news-type">PROJECT</span><div class="news-title">AFW 원작 제작 및 신규 Mining Game 개발 진행 안내</div></div>
            <span class="news-arrow" aria-hidden="true">↗</span>
          </a>
          <a class="news-item" href="#games" data-type="minecraft">
            <time datetime="2026-11-02">2026. 11. 02</time>
            <div><span class="news-type">MINECRAFT</span><div class="news-title">마인크래프트 서버 '루미너스 에테르' 개발 소식</div></div>
            <span class="news-arrow" aria-hidden="true">↗</span>
          </a>
          <p class="news-empty" hidden>이 분류의 소식은 아직 준비 중이에요. 곧 찾아올게요!</p>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section class="contact" id="contact">
      <div class="wrap contact-grid">
        <div class="contact-info reveal">
          <div class="section-kicker">05 / GET IN TOUCH</div>
          <h2>함께 이야기하고<br />싶다면 언제든 <mark>편하게!</mark></h2>
          <p>게임 피드백, 협업 제안, 서버 문의 등 어떤 이야기든 환영합니다. 폼으로 남겨주시거나 이메일·디스코드로 편하게 연락해 주세요.</p>
          <div class="contact-channels">
            <a class="channel" href="mailto:furssy0630@gmail.com">
              <span class="channel-icon" aria-hidden="true"><svg viewBox="0 0 24 24"><path d="M3 6h18v12H3z M3 6l9 7 9-7" fill="none" stroke="currentColor" stroke-width="1.6"/></svg></span>
              <span><small>EMAIL</small>furssy0630@gmail.com</span>
              <span class="channel-arrow" aria-hidden="true">↗</span>
            </a>
            <button type="button" class="channel" id="copyDiscordBtn" aria-label="디스코드 아이디 furssy 복사">
              <span class="channel-icon" aria-hidden="true"><svg viewBox="0 0 24 24"><path d="M7 7.5c3.3-1.3 6.7-1.3 10 0l1.6 7.3c-1.6 1.3-3.2 2-4.8 2.2l-.8-1.5M7 7.5 5.4 14.8c1.6 1.3 3.2 2 4.8 2.2l.8-1.5" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linejoin="round"/><circle cx="9.6" cy="12" r="1.2" fill="currentColor"/><circle cx="14.4" cy="12" r="1.2" fill="currentColor"/></svg></span>
              <span><small>DISCORD</small><span id="discordText">furssy</span></span>
              <span class="channel-arrow copy-label" id="discordHint">ID 복사</span>
            </button>
          </div>
        </div>

        <form class="contact-form reveal" name="contact" id="contactForm" novalidate>
          <input type="hidden" name="form-name" value="contact" />
          <input type="hidden" name="subject" value="[Furssy Games] 새 문의가 도착했어요" />
          <p class="hp-field"><label>이 칸은 비워두세요 <input name="bot-field" tabindex="-1" autocomplete="off" /></label></p>

          <fieldset class="topic">
            <legend>어떤 이야기인가요?</legend>
            <label><input type="radio" name="topic" value="게임 피드백" checked /><span>게임 피드백</span></label>
            <label><input type="radio" name="topic" value="협업 제안" /><span>협업 제안</span></label>
            <label><input type="radio" name="topic" value="서버 문의" /><span>서버 문의</span></label>
            <label><input type="radio" name="topic" value="기타" /><span>기타</span></label>
          </fieldset>

          <div class="field">
            <label for="f-name">이름 / 닉네임</label>
            <input id="f-name" type="text" name="name" autocomplete="name" required maxlength="60" placeholder="예) 땅굴탐험가" />
            <span class="error" aria-live="polite"></span>
          </div>
          <div class="field">
            <label for="f-email">답장 받을 이메일</label>
            <input id="f-email" type="email" name="email" autocomplete="email" required placeholder="you@example.com" />
            <span class="error" aria-live="polite"></span>
          </div>
          <div class="field">
            <label for="f-message">메시지</label>
            <textarea id="f-message" name="message" rows="5" required minlength="10" maxlength="3000" placeholder="하고 싶은 이야기를 자유롭게 적어주세요."></textarea>
            <span class="error" aria-live="polite"></span>
            <span class="counter"><span id="msgCount">0</span> / 3000</span>
          </div>
          <button class="button submit" type="submit" id="submitBtn"><span class="label">메시지 보내기</span> <span aria-hidden="true">↗</span></button>
          <p class="form-status" id="formStatus" role="status" aria-live="polite"></p>
        </form>
      </div>
    </section>
  </main>

  <footer>
    <div class="wrap footer-big" aria-hidden="true">PLAY BEYOND</div>
    <div class="wrap footer-inner">
      <a class="brand" href="#home" aria-label="맨 위로">
        <span class="brand-mark" aria-hidden="true"><svg viewBox="0 0 64 64"><path d="M20 14h26v9H30v7h13v9H30v11H20z"/><rect x="42" y="42" width="8" height="8"/></svg></span>
        <span class="brand-name">FURSSY<em>GAMES</em></span>
      </a>
      <div>© 2026 Furssy Games. All rights reserved.</div>
      <div class="footer-links">
        <a href="mailto:furssy0630@gmail.com">furssy0630@gmail.com</a>
        <a href="#contact">Discord: furssy</a>
        <a href="#home">TOP ↑</a>
      </div>
    </div>
  </footer>

  <!-- PROJECT DIALOG -->
  <dialog class="project-dialog" id="projectDialog" aria-labelledby="dlgTitle">
    <button class="dlg-close" type="button" id="dlgClose" aria-label="닫기">✕</button>
    <div class="dlg-cover" id="dlgCover"></div>
    <div class="dlg-body">
      <div class="game-meta" id="dlgMeta"></div>
      <h3 id="dlgTitle"></h3>
      <p id="dlgDesc"></p>
      <ul class="dlg-points" id="dlgPoints"></ul>
      <div class="dlg-actions" id="dlgActions"></div>
    </div>
  </dialog>

  <div class="toast" id="toast" role="status" aria-live="polite"></div>

  <script>
(() => {
  const $ = (s, r = document) => r.querySelector(s);
  const toast = (m) => { const t = $('#toast'); t.textContent = m; t.classList.add('show'); setTimeout(() => t.classList.remove('show'), 2200); };

  // Reveal on scroll
  const io = 'IntersectionObserver' in window ? new IntersectionObserver((es) => es.forEach(e => { if (e.isIntersecting) { e.target.classList.add('in'); io.unobserve(e.target); } }), { threshold: .12 }) : null;
  document.querySelectorAll('.reveal').forEach(el => io ? io.observe(el) : el.classList.add('in'));

  // Nav state + progress
  const top = $('#topbar'), bar = $('#scrollBar');
  const onScroll = () => {
    const y = scrollY, h = document.documentElement.scrollHeight - innerHeight;
    top.classList.toggle('scrolled', y > 20);
    bar.style.transform = `scaleX(${h > 0 ? y / h : 0})`;
  };
  addEventListener('scroll', onScroll, { passive: true }); onScroll();

  // Mobile menu
  const tog = $('#menuToggle'), links = $('#navLinks');
  const setMenu = (o) => { links.classList.toggle('open', o); tog.setAttribute('aria-expanded', String(o)); tog.setAttribute('aria-label', o ? '메뉴 닫기' : '메뉴 열기'); };
  tog.addEventListener('click', () => setMenu(!links.classList.contains('open')));
  links.querySelectorAll('a').forEach(a => a.addEventListener('click', () => setMenu(false)));

  // Project dialog
  const P = {
    afw: { meta: 'ORIGINAL IP · WORLDVIEW', title: 'AFW', desc: 'Furssy Games만의 개성과 이야기를 담아 처음부터 새롭게 빚어내고 있는 오리지널 원작 프로젝트입니다.', points: ['현재 세계관과 캐릭터를 구축하는 단계입니다.', '세부 내용은 준비되는 대로 소식란에서 공개됩니다.'] },
    mining: { meta: 'MINING · ADVENTURE', title: 'Mining Game (가제)', desc: '깊은 땅속을 파고들며 미지의 자원을 발견하고 성장해 나가는 손맛 가득한 채굴 게임 프로젝트입니다.', points: ['파고, 발견하고, 성장하는 손맛이 핵심입니다.', '현재 개발이 진행 중입니다.'] },
    aether: { meta: 'MINECRAFT SERVER', title: '루미너스 에테르', desc: '새로운 모험과 함께 어울리는 즐거움을 경험할 수 있도록 구축 중인 Furssy Games의 마인크래프트 서버입니다.', points: ['함께 어울리는 모험을 위한 서버를 구축 중입니다.', '오픈 일정은 소식란과 디스코드로 안내됩니다.'] }
  };
  const dlg = $('#projectDialog');
  const open = (card) => {
    const d = P[card.dataset.project]; if (!d || !dlg.showModal) return;
    const cover = card.querySelector('.game-cover');
    $('#dlgCover').className = 'dlg-cover ' + [...cover.classList].filter(c => c.startsWith('cover-')).join(' ');
    $('#dlgCover').innerHTML = cover.querySelector('.cover-glyph').outerHTML;
    $('#dlgMeta').textContent = d.meta; $('#dlgTitle').textContent = d.title; $('#dlgDesc').textContent = d.desc;
    $('#dlgPoints').innerHTML = d.points.map(p => `<li>${p}</li>`).join('');
    $('#dlgActions').innerHTML = '<a class="button" href="#contact">관련 문의하기 ↗</a>';
    dlg.showModal();
  };
  document.querySelectorAll('.game-card[data-project]').forEach(c => {
    c.addEventListener('click', () => open(c));
    c.addEventListener('keydown', e => { if (e.key === 'Enter' || e.key === ' ') { e.preventDefault(); open(c); } });
    c.addEventListener('pointermove', e => { const r = c.getBoundingClientRect(); c.style.setProperty('--mx', `${e.clientX - r.left}px`); c.style.setProperty('--my', `${e.clientY - r.top}px`); });
  });
  $('#dlgClose').addEventListener('click', () => dlg.close());
  dlg.addEventListener('click', e => { if (e.target === dlg || e.target.closest('#dlgActions a')) dlg.close(); });

  // News filter
  const items = document.querySelectorAll('.news-item'), empty = $('.news-empty');
  document.querySelectorAll('.filters button').forEach(b => b.addEventListener('click', () => {
    document.querySelectorAll('.filters button').forEach(x => { x.classList.toggle('active', x === b); x.setAttribute('aria-selected', String(x === b)); });
    let n = 0; items.forEach(i => { const show = b.dataset.filter === 'all' || i.dataset.type === b.dataset.filter; i.classList.toggle('out', !show); n += show; });
    empty.hidden = n > 0;
  }));

  // Discord copy
  const dBtn = $('#copyDiscordBtn'), hint = $('#discordHint');
  dBtn.addEventListener('click', async () => {
    try { await navigator.clipboard.writeText('furssy'); } catch { const t = document.createElement('input'); t.value = 'furssy'; document.body.appendChild(t); t.select(); document.execCommand('copy'); t.remove(); }
    dBtn.classList.add('copied'); hint.textContent = '복사됨'; toast('디스코드 ID "furssy"를 복사했어요');
    setTimeout(() => { dBtn.classList.remove('copied'); hint.textContent = 'ID 복사'; }, 2200);
  });

  // Contact form
  const form = $('#contactForm'), status = $('#formStatus'), btn = $('#submitBtn'), msg = $('#f-message');
  msg.addEventListener('input', () => { $('#msgCount').textContent = msg.value.length; });
  const check = (el) => {
    const f = el.closest('.field'), err = f.querySelector('.error'); let m = '';
    if (el.validity.valueMissing) m = '이 항목을 입력해 주세요.';
    else if (el.validity.typeMismatch) m = '올바른 이메일 주소를 입력해 주세요.';
    else if (el.validity.tooShort) m = `${el.minLength}자 이상 적어주세요.`;
    f.classList.toggle('invalid', !!m); err.textContent = m; return !m;
  };
  form.querySelectorAll('.field input, .field textarea').forEach(el => el.addEventListener('blur', () => check(el)));
  form.addEventListener('submit', async (e) => {
    e.preventDefault();
    const fields = [...form.querySelectorAll('.field input, .field textarea')];
    const ok = fields.map(check).every(Boolean);
    if (!ok) { fields.find(f => !f.checkValidity())?.focus(); return; }
    btn.disabled = true; btn.classList.add('loading'); status.className = 'form-status'; status.textContent = '';
    try {
      const fd = new FormData(form);
      if (fd.get('bot-field')) throw new Error('bot');
      const body = '이름: ' + fd.get('name') + '\n답장 이메일: ' + fd.get('email') + '\n\n' + fd.get('message');
      location.href = 'mailto:furssy0630@gmail.com?subject=' + encodeURIComponent('[Furssy Games] ' + fd.get('topic')) + '&body=' + encodeURIComponent(body);
      form.classList.add('sent'); status.classList.add('ok'); status.textContent = '메일 앱이 열렸어요. 전송 버튼을 눌러 보내주세요!'; form.reset(); $('#msgCount').textContent = '0';
    } catch {
      status.classList.add('err'); status.textContent = '전송에 실패했어요. 잠시 후 다시 시도하거나 이메일로 보내주세요.';
    } finally { btn.disabled = false; btn.classList.remove('loading'); }
  });
})();

</script>
</body>
</html>
