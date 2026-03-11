<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Jobil Cherian — Full-Stack Marketer</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=DM+Sans:wght@300;400;500;700&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
<style>
:root {
  --black: #060606;
  --surface: #0f0f0f;
  --surface2: #161616;
  --surface3: #1e1e1e;
  --border: #242424;
  --accent: #e8ff00;
  --accent2: #ff4d00;
  --white: #f2efe8;
  --muted: #5a5a5a;
  --display: 'Bebas Neue', sans-serif;
  --body: 'DM Sans', sans-serif;
  --mono: 'Space Mono', monospace;
}
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body {
  background: var(--black); color: var(--white);
  font-family: var(--body); font-size: 16px; line-height: 1.6;
  overflow-x: hidden; cursor: none;
}
::-webkit-scrollbar { width: 2px; }
::-webkit-scrollbar-track { background: var(--black); }
::-webkit-scrollbar-thumb { background: var(--accent); }

/* CURSOR */
.cursor {
  width: 10px; height: 10px; background: var(--accent); border-radius: 50%;
  position: fixed; top: 0; left: 0; pointer-events: none; z-index: 99999;
  transform: translate(-50%,-50%); transition: transform 0.1s, width 0.2s, height 0.2s;
  mix-blend-mode: difference;
}
.cursor-ring {
  width: 32px; height: 32px; border: 1px solid rgba(232,255,0,0.35); border-radius: 50%;
  position: fixed; top: 0; left: 0; pointer-events: none; z-index: 99998;
  transform: translate(-50%,-50%); transition: all 0.14s ease;
}
.cursor.hovered { transform: translate(-50%,-50%) scale(3); }
.cursor-ring.hovered { transform: translate(-50%,-50%) scale(0); }

/* NAV */
nav {
  position: fixed; top: 0; left: 0; right: 0; z-index: 1000;
  padding: 20px 60px; display: flex; justify-content: space-between; align-items: center;
  transition: background 0.3s, padding 0.3s;
}
nav.scrolled {
  background: rgba(6,6,6,0.97); backdrop-filter: blur(20px);
  padding: 14px 60px; border-bottom: 1px solid var(--border);
}
.nav-logo {
  font-family: var(--display); font-size: 26px; letter-spacing: 4px;
  color: var(--white); text-decoration: none;
}
.nav-logo span { color: var(--accent); }
.nav-links { display: flex; gap: 32px; list-style: none; }
.nav-links a {
  font-family: var(--mono); font-size: 10px; letter-spacing: 2px; text-transform: uppercase;
  color: var(--muted); text-decoration: none; transition: color 0.2s; position: relative;
}
.nav-links a::after {
  content: ''; position: absolute; left: 0; bottom: -4px;
  width: 0; height: 1px; background: var(--accent); transition: width 0.3s;
}
.nav-links a:hover { color: var(--white); }
.nav-links a:hover::after { width: 100%; }
.nav-right { display: flex; align-items: center; gap: 16px; }
.nav-drive {
  font-family: var(--mono); font-size: 10px; letter-spacing: 1px; text-transform: uppercase;
  border: 1px solid rgba(232,255,0,0.4); color: var(--accent);
  padding: 8px 16px; text-decoration: none; transition: all 0.2s;
}
.nav-drive:hover { background: var(--accent); color: var(--black); }
.nav-cta {
  font-family: var(--mono); font-size: 10px; letter-spacing: 2px; text-transform: uppercase;
  background: var(--accent); color: var(--black);
  padding: 10px 22px; text-decoration: none; font-weight: 700; transition: all 0.2s;
}
.nav-cta:hover { background: var(--accent2); color: var(--white); }

/* HERO */
#hero {
  min-height: 100vh; display: flex; flex-direction: column; justify-content: flex-end;
  padding: 0 60px 80px; position: relative; overflow: hidden;
}
.hero-glow-1 {
  position: absolute; width: 600px; height: 600px;
  background: radial-gradient(circle, rgba(232,255,0,0.07) 0%, transparent 70%);
  top: -100px; right: -100px; pointer-events: none;
  animation: glowPulse 6s ease-in-out infinite;
}
.hero-glow-2 {
  position: absolute; width: 400px; height: 400px;
  background: radial-gradient(circle, rgba(255,77,0,0.05) 0%, transparent 70%);
  bottom: 0; left: 100px; pointer-events: none;
  animation: glowPulse 8s ease-in-out infinite reverse;
}
.hero-grid-bg {
  position: absolute; inset: 0;
  background-image:
    linear-gradient(rgba(255,255,255,0.018) 1px, transparent 1px),
    linear-gradient(90deg, rgba(255,255,255,0.018) 1px, transparent 1px);
  background-size: 70px 70px;
}
.hero-eyebrow {
  font-family: var(--mono); font-size: 11px; letter-spacing: 5px; text-transform: uppercase;
  color: var(--accent); margin-bottom: 24px;
  opacity: 0; animation: fadeUp 0.9s 0.3s forwards;
  display: flex; align-items: center; gap: 16px;
}
.hero-eyebrow::before { content: ''; width: 40px; height: 1px; background: var(--accent); }
.hero-name {
  font-family: var(--display); font-size: clamp(90px, 13vw, 200px);
  line-height: 0.85; letter-spacing: 6px; color: var(--white);
  opacity: 0; animation: fadeUp 0.9s 0.5s forwards;
}
.hero-name .outline { -webkit-text-stroke: 1.5px rgba(240,237,230,0.4); color: transparent; }
.hero-name .acc { color: var(--accent); }
.hero-bottom {
  margin-top: 40px; display: flex; align-items: flex-end; justify-content: space-between;
  opacity: 0; animation: fadeUp 0.9s 0.7s forwards;
}
.hero-tagline { font-size: 17px; font-weight: 300; color: var(--muted); max-width: 460px; line-height: 1.6; }
.hero-tagline strong { color: var(--white); font-weight: 500; }
.hero-tagline em { color: var(--accent); font-style: normal; }
.hero-stats { display: flex; }
.stat { padding: 20px 36px; border-left: 1px solid var(--border); text-align: center; }
.stat:last-child { border-right: 1px solid var(--border); }
.stat-num { font-family: var(--display); font-size: 48px; letter-spacing: 2px; color: var(--accent); line-height: 1; }
.stat-label { font-family: var(--mono); font-size: 9px; letter-spacing: 2px; text-transform: uppercase; color: var(--muted); margin-top: 6px; }
.hero-scroll {
  position: absolute; right: 60px; bottom: 90px;
  display: flex; flex-direction: column; align-items: center; gap: 10px;
  opacity: 0; animation: fadeUp 0.9s 1.2s forwards;
}
.hero-scroll-text { font-family: var(--mono); font-size: 9px; letter-spacing: 3px; text-transform: uppercase; color: var(--muted); writing-mode: vertical-rl; }
.hero-scroll-line { width: 1px; height: 50px; background: linear-gradient(to bottom, var(--accent), transparent); animation: scrollAnim 2s ease-in-out infinite; }

/* MARQUEE */
.marquee-wrap { background: var(--accent); padding: 14px 0; overflow: hidden; }
.marquee-track { display: flex; width: max-content; animation: marquee 28s linear infinite; }
.marquee-item {
  font-family: var(--display); font-size: 15px; letter-spacing: 3px;
  color: var(--black); padding: 0 32px; white-space: nowrap;
  display: flex; align-items: center; gap: 32px;
}
.marquee-dot { width: 5px; height: 5px; background: rgba(0,0,0,0.25); border-radius: 50%; }

/* SECTION BASE */
section { padding: 120px 60px; }
.section-label {
  font-family: var(--mono); font-size: 10px; letter-spacing: 5px; text-transform: uppercase;
  color: var(--accent); margin-bottom: 20px; display: flex; align-items: center; gap: 14px;
}
.section-label::before { content: ''; width: 24px; height: 1px; background: var(--accent); }
.section-title {
  font-family: var(--display); font-size: clamp(52px, 6.5vw, 100px);
  line-height: 0.9; letter-spacing: 4px; color: var(--white); margin-bottom: 64px;
}

/* ABOUT */
#about { background: var(--surface); position: relative; overflow: hidden; }
#about::after {
  content: 'JOBIL'; font-family: var(--display); font-size: 300px;
  color: rgba(232,255,0,0.025); position: absolute; right: -40px; bottom: -60px;
  letter-spacing: 20px; pointer-events: none; line-height: 1;
}
.about-grid { display: grid; grid-template-columns: 1.1fr 0.9fr; gap: 80px; align-items: start; }
.about-text p { font-size: 17px; font-weight: 300; color: rgba(242,239,232,0.7); line-height: 1.85; margin-bottom: 22px; }
.about-text p strong { color: var(--white); font-weight: 500; }
.about-text p em { color: var(--accent); font-style: normal; border-bottom: 1px solid rgba(232,255,0,0.3); }
.about-tags { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 36px; }
.tag {
  font-family: var(--mono); font-size: 10px; letter-spacing: 1.5px; text-transform: uppercase;
  padding: 7px 14px; border: 1px solid var(--border); color: var(--muted); transition: all 0.25s;
}
.tag:hover { border-color: var(--accent); color: var(--accent); background: rgba(232,255,0,0.05); }
.about-cards { display: flex; flex-direction: column; gap: 2px; }
.about-card {
  padding: 24px 28px; border: 1px solid var(--border); background: var(--surface2);
  position: relative; overflow: hidden; transition: all 0.3s; display: flex; align-items: center; gap: 20px;
}
.about-card-bar {
  position: absolute; left: 0; top: 0; bottom: 0; width: 3px;
  background: var(--accent); transform: scaleY(0); transform-origin: bottom; transition: transform 0.4s ease;
}
.about-card:hover .about-card-bar { transform: scaleY(1); }
.about-card:hover { border-color: rgba(232,255,0,0.2); background: var(--surface3); }
.about-card-num { font-family: var(--display); font-size: 48px; color: var(--accent); line-height: 1; flex-shrink: 0; width: 110px; }
.about-card-text { font-size: 13px; color: var(--muted); line-height: 1.6; }
.about-card-text strong { color: var(--white); font-weight: 500; display: block; margin-bottom: 3px; }

/* EXPERIENCE */
#experience { background: var(--black); }
.exp-timeline { position: relative; padding-left: 2px; }
.exp-timeline::before {
  content: ''; position: absolute; left: 0; top: 0; bottom: 0;
  width: 1px; background: linear-gradient(to bottom, var(--accent), rgba(232,255,0,0.05), transparent);
}
.exp-item {
  display: grid; grid-template-columns: 220px 1fr; gap: 60px;
  padding: 52px 0 52px 48px; border-bottom: 1px solid rgba(255,255,255,0.04);
  position: relative; transition: background 0.3s;
}
.exp-dot {
  position: absolute; left: -5px; top: 60px; width: 11px; height: 11px;
  background: var(--black); border: 2px solid var(--accent); border-radius: 50%;
  box-shadow: 0 0 16px rgba(232,255,0,0.5); transition: background 0.3s;
}
.exp-item:hover { background: rgba(232,255,0,0.015); }
.exp-item:hover .exp-dot { background: var(--accent); }
.exp-year { font-family: var(--mono); font-size: 11px; letter-spacing: 2px; color: var(--accent); }
.exp-company { font-size: 13px; color: var(--muted); margin-top: 8px; }
.exp-role { font-family: var(--display); font-size: 30px; letter-spacing: 2px; color: var(--white); margin-bottom: 14px; line-height: 1.1; }
.exp-desc { font-size: 15px; font-weight: 300; color: rgba(242,239,232,0.55); line-height: 1.75; max-width: 580px; }
.exp-highlights { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 22px; }
.highlight {
  font-family: var(--mono); font-size: 9px; letter-spacing: 1.5px; text-transform: uppercase;
  padding: 5px 12px; background: rgba(232,255,0,0.07); border: 1px solid rgba(232,255,0,0.18); color: var(--accent);
}

/* CASE STUDIES */
#cases { background: var(--surface); }
.cases-top { display: flex; justify-content: space-between; align-items: flex-end; margin-bottom: 0; }
.cases-top .section-title { margin-bottom: 0; }
.cases-drive-btn {
  font-family: var(--mono); font-size: 11px; letter-spacing: 2px; text-transform: uppercase;
  color: var(--accent); border: 1px solid rgba(232,255,0,0.4); padding: 12px 24px;
  text-decoration: none; transition: all 0.2s; display: flex; align-items: center; gap: 10px; margin-bottom: 4px;
}
.cases-drive-btn:hover { background: var(--accent); color: var(--black); }
.cases-hint { font-family: var(--mono); font-size: 11px; letter-spacing: 2px; color: var(--muted); margin-bottom: 44px; margin-top: 14px; }
.cases-hint span { color: var(--accent); }
.cases-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 2px; }
.case-card {
  background: var(--surface2); padding: 36px 32px; border: 1px solid var(--border);
  position: relative; overflow: hidden; cursor: pointer; transition: all 0.35s;
}
.case-card-bg {
  position: absolute; inset: 0;
  background: linear-gradient(135deg, rgba(232,255,0,0.06) 0%, transparent 70%);
  opacity: 0; transition: opacity 0.35s;
}
.case-card:hover { transform: translateY(-6px); border-color: rgba(232,255,0,0.35); box-shadow: 0 20px 60px rgba(0,0,0,0.5); }
.case-card:hover .case-card-bg { opacity: 1; }
.case-num { font-family: var(--display); font-size: 80px; line-height: 1; color: rgba(232,255,0,0.08); margin-bottom: 20px; transition: color 0.3s; }
.case-card:hover .case-num { color: rgba(232,255,0,0.15); }
.case-category { font-family: var(--mono); font-size: 9px; letter-spacing: 3px; text-transform: uppercase; color: var(--accent2); margin-bottom: 10px; }
.case-title { font-family: var(--display); font-size: 22px; letter-spacing: 1px; color: var(--white); margin-bottom: 14px; line-height: 1.2; }
.case-desc { font-size: 13px; font-weight: 300; color: var(--muted); line-height: 1.65; }
.case-result { margin-top: 22px; padding-top: 18px; border-top: 1px solid var(--border); font-family: var(--mono); font-size: 11px; color: var(--accent); letter-spacing: 1px; }
.case-cta { margin-top: 14px; display: inline-flex; align-items: center; gap: 8px; font-family: var(--mono); font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: var(--muted); transition: color 0.2s; }
.case-card:hover .case-cta { color: var(--accent); }
.case-cta-arr { transition: transform 0.2s; }
.case-card:hover .case-cta-arr { transform: translateX(5px); }

/* MODAL */
.modal-overlay {
  position: fixed; inset: 0; z-index: 10000;
  background: rgba(0,0,0,0.92); backdrop-filter: blur(12px);
  display: flex; align-items: center; justify-content: center;
  opacity: 0; pointer-events: none; transition: opacity 0.3s; padding: 40px;
}
.modal-overlay.open { opacity: 1; pointer-events: all; }
.modal {
  background: var(--surface2); border: 1px solid var(--border);
  width: 100%; max-width: 900px; max-height: 88vh; overflow-y: auto;
  position: relative; transform: translateY(30px) scale(0.97); transition: transform 0.35s ease;
}
.modal-overlay.open .modal { transform: translateY(0) scale(1); }
.modal-header {
  padding: 32px 40px 24px; border-bottom: 1px solid var(--border);
  display: flex; justify-content: space-between; align-items: flex-start;
  position: sticky; top: 0; background: var(--surface2); z-index: 2;
}
.modal-cat { font-family: var(--mono); font-size: 9px; letter-spacing: 3px; text-transform: uppercase; color: var(--accent2); margin-bottom: 8px; }
.modal-title { font-family: var(--display); font-size: 34px; letter-spacing: 2px; color: var(--white); }
.modal-close {
  width: 42px; height: 42px; background: var(--surface3); border: 1px solid var(--border);
  color: var(--muted); font-size: 18px; cursor: pointer; flex-shrink: 0;
  display: flex; align-items: center; justify-content: center; transition: all 0.2s;
}
.modal-close:hover { background: var(--accent); color: var(--black); border-color: var(--accent); }
.modal-body { padding: 32px 40px; }
.modal-stats { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 28px; }
.modal-stat-box { background: var(--surface3); padding: 22px; border: 1px solid var(--border); text-align: center; }
.modal-stat-num { font-family: var(--display); font-size: 38px; color: var(--accent); line-height: 1; }
.modal-stat-label { font-family: var(--mono); font-size: 9px; letter-spacing: 2px; text-transform: uppercase; color: var(--muted); margin-top: 6px; }
.modal-desc { font-size: 15px; font-weight: 300; color: rgba(242,239,232,0.7); line-height: 1.8; margin-bottom: 28px; }
.modal-work-label { font-family: var(--mono); font-size: 10px; letter-spacing: 3px; text-transform: uppercase; color: var(--accent); margin-bottom: 14px; padding-bottom: 10px; border-bottom: 1px solid var(--border); }
.modal-link {
  display: flex; align-items: center; gap: 16px; background: var(--surface3);
  border: 1px solid var(--border); padding: 18px 22px; text-decoration: none;
  transition: all 0.25s; margin-bottom: 10px;
}
.modal-link:hover { border-color: var(--accent); background: rgba(232,255,0,0.04); }
.modal-link-icon { font-size: 22px; }
.modal-link-body { flex: 1; }
.modal-link-name { font-size: 14px; color: var(--white); font-weight: 500; }
.modal-link-sub { font-family: var(--mono); font-size: 10px; letter-spacing: 1px; color: var(--muted); margin-top: 3px; }
.modal-link-arr { font-family: var(--mono); font-size: 14px; color: var(--accent); }

/* SKILLS */
#skills { background: var(--black); }
.skills-layout { display: grid; grid-template-columns: 1fr 2fr; gap: 80px; }
.skills-intro p { font-size: 16px; font-weight: 300; color: var(--muted); line-height: 1.75; }
.skills-intro p + p { margin-top: 18px; }
.skills-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 44px; }
.skill-group-title { font-family: var(--mono); font-size: 10px; letter-spacing: 3px; text-transform: uppercase; color: var(--accent); margin-bottom: 20px; padding-bottom: 12px; border-bottom: 1px solid var(--border); }
.skill-item { display: flex; justify-content: space-between; align-items: center; padding: 11px 0; border-bottom: 1px solid rgba(255,255,255,0.04); }
.skill-name { font-size: 13px; color: rgba(242,239,232,0.75); }
.skill-bar { width: 72px; height: 2px; background: rgba(255,255,255,0.07); }
.skill-fill { height: 100%; background: linear-gradient(to right, var(--accent), var(--accent2)); }

/* ACHIEVEMENTS */
#achievements { background: var(--surface); }
.ach-grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 2px; }
.ach-item {
  background: var(--surface2); padding: 36px 40px; border: 1px solid var(--border);
  display: flex; gap: 24px; align-items: flex-start; transition: all 0.3s;
}
.ach-item:hover { border-color: rgba(232,255,0,0.2); background: var(--surface3); }
.ach-icon { font-size: 24px; width: 52px; height: 52px; background: rgba(232,255,0,0.07); border: 1px solid rgba(232,255,0,0.15); display: flex; align-items: center; justify-content: center; flex-shrink: 0; }
.ach-title { font-family: var(--display); font-size: 18px; letter-spacing: 1px; color: var(--white); margin-bottom: 8px; line-height: 1.2; }
.ach-desc { font-size: 13px; font-weight: 300; color: var(--muted); line-height: 1.65; }
.ach-year { font-family: var(--mono); font-size: 9px; letter-spacing: 2px; color: var(--accent); margin-top: 10px; }

/* CONTACT */
#contact { background: var(--black); position: relative; overflow: hidden; }
#contact::before {
  content: 'LETS'; font-family: var(--display); font-size: 320px;
  color: rgba(232,255,0,0.018); position: absolute; bottom: -60px; right: -40px; pointer-events: none; line-height: 1;
}
.contact-layout { display: grid; grid-template-columns: 1fr 1fr; gap: 80px; }
.contact-cta { font-size: 17px; font-weight: 300; color: rgba(242,239,232,0.6); line-height: 1.8; margin-bottom: 24px; }
.contact-cta strong { color: var(--white); }
.drive-btn {
  display: inline-flex; align-items: center; gap: 12px;
  font-family: var(--mono); font-size: 11px; letter-spacing: 2px; text-transform: uppercase;
  color: var(--black); background: var(--accent); padding: 14px 28px; text-decoration: none;
  font-weight: 700; border: 2px solid var(--accent); transition: all 0.2s; margin-bottom: 36px;
}
.drive-btn:hover { background: transparent; color: var(--accent); }
.contact-links { display: flex; flex-direction: column; gap: 12px; }
.contact-link {
  display: flex; align-items: center; gap: 16px; font-family: var(--mono); font-size: 12px;
  letter-spacing: 1px; color: var(--muted); text-decoration: none; padding: 15px 20px;
  border: 1px solid var(--border); transition: all 0.25s;
}
.contact-link:hover { border-color: var(--accent); color: var(--accent); background: rgba(232,255,0,0.03); }
.cli { font-size: 16px; width: 20px; text-align: center; }
.contact-form { display: flex; flex-direction: column; gap: 18px; }
.form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }
.form-group { display: flex; flex-direction: column; gap: 8px; }
.form-label { font-family: var(--mono); font-size: 9px; letter-spacing: 2px; text-transform: uppercase; color: var(--muted); }
.form-input, .form-textarea {
  background: var(--surface2); border: 1px solid var(--border); color: var(--white);
  padding: 13px 16px; font-family: var(--body); font-size: 14px; outline: none; transition: border-color 0.2s; resize: none;
}
.form-input:focus, .form-textarea:focus { border-color: var(--accent); }
.form-textarea { min-height: 110px; }
.form-btn {
  background: var(--accent); color: var(--black); border: none; padding: 18px 40px;
  font-family: var(--display); font-size: 22px; letter-spacing: 4px; cursor: pointer; transition: all 0.2s; align-self: flex-start;
}
.form-btn:hover { background: var(--accent2); color: var(--white); }

/* FOOTER */
footer {
  background: var(--surface); border-top: 1px solid var(--border); padding: 36px 60px;
  display: flex; justify-content: space-between; align-items: center;
}
.footer-logo { font-family: var(--display); font-size: 22px; letter-spacing: 4px; color: var(--white); }
.footer-logo span { color: var(--accent); }
.footer-copy { font-family: var(--mono); font-size: 10px; letter-spacing: 2px; color: var(--muted); }

/* ANIMATIONS */
@keyframes fadeUp { from { opacity: 0; transform: translateY(28px); } to { opacity: 1; transform: translateY(0); } }
@keyframes scrollAnim { 0%,100% { opacity:1; } 50% { opacity:0.3; } }
@keyframes glowPulse { 0%,100% { transform:scale(1); opacity:1; } 50% { transform:scale(1.1); opacity:0.7; } }
@keyframes marquee { from { transform: translateX(0); } to { transform: translateX(-50%); } }
.reveal { opacity: 0; transform: translateY(36px); transition: opacity 0.75s ease, transform 0.75s ease; }
.reveal.visible { opacity: 1; transform: translateY(0); }

@media (max-width: 900px) {
  nav { padding: 18px 24px; }
  .nav-links, .nav-drive { display: none; }
  section { padding: 80px 24px; }
  #hero { padding: 0 24px 60px; }
  .hero-name { font-size: clamp(72px, 16vw, 120px); }
  .hero-bottom { flex-direction: column; align-items: flex-start; gap: 28px; }
  .about-grid, .skills-layout, .skills-grid, .ach-grid, .contact-layout { grid-template-columns: 1fr; }
  .cases-grid { grid-template-columns: 1fr; }
  .cases-top { flex-direction: column; align-items: flex-start; gap: 20px; }
  .exp-item { grid-template-columns: 1fr; gap: 12px; padding: 36px 0 36px 32px; }
  .modal-overlay { padding: 16px; }
  .modal-stats { grid-template-columns: 1fr 1fr; }
  footer { flex-direction: column; gap: 14px; text-align: center; }
}
</style>
</head>
<body>

<div class="cursor" id="cursor"></div>
<div class="cursor-ring" id="cring"></div>

<!-- NAV -->
<nav id="mainNav">
  <a href="#hero" class="nav-logo">JOBIL<span>.</span></a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#cases">Work</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#achievements">Awards</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <div class="nav-right">
    <a href="https://drive.google.com/drive/folders/YOUR_FOLDER_ID" target="_blank" class="nav-drive">📁 View My Work</a>
    <a href="#contact" class="nav-cta">Hire Me</a>
  </div>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-glow-1"></div>
  <div class="hero-glow-2"></div>
  <div class="hero-grid-bg"></div>
  <div class="hero-eyebrow">Full-Stack Marketer · Kerala, India</div>
  <h1 class="hero-name"><span class="outline">JO</span><span class="acc">B</span>IL<br><span class="outline">CHE</span>RIAN</h1>
  <div class="hero-bottom">
    <p class="hero-tagline">Building brands that <strong>convert minds</strong>, not just eyeballs — blending <em>neuromarketing strategy</em> with <strong>full-funnel execution</strong>.</p>
    <div class="hero-stats">
      <div class="stat"><div class="stat-num">4+</div><div class="stat-label">Yrs Experience</div></div>
      <div class="stat"><div class="stat-num">30K+</div><div class="stat-label">Followers Grown</div></div>
      <div class="stat"><div class="stat-num">1M+</div><div class="stat-label">Organic Views</div></div>
    </div>
  </div>
  <div class="hero-scroll">
    <div class="hero-scroll-line"></div>
    <span class="hero-scroll-text">Scroll</span>
  </div>
</section>

<!-- MARQUEE -->
<div class="marquee-wrap">
  <div class="marquee-track">
    <div class="marquee-item">NEUROMARKETING <span class="marquee-dot"></span></div>
    <div class="marquee-item">META ADS <span class="marquee-dot"></span></div>
    <div class="marquee-item">CONTENT STRATEGY <span class="marquee-dot"></span></div>
    <div class="marquee-item">VIDEO PRODUCTION <span class="marquee-dot"></span></div>
    <div class="marquee-item">FMCG <span class="marquee-dot"></span></div>
    <div class="marquee-item">TEAM LEADERSHIP <span class="marquee-dot"></span></div>
    <div class="marquee-item">BRAND STRATEGY <span class="marquee-dot"></span></div>
    <div class="marquee-item">AI PROMPT ENGINEERING <span class="marquee-dot"></span></div>
    <div class="marquee-item">FILMMAKING <span class="marquee-dot"></span></div>
    <div class="marquee-item">CLIENT SERVICING <span class="marquee-dot"></span></div>
    <div class="marquee-item">NEUROMARKETING <span class="marquee-dot"></span></div>
    <div class="marquee-item">META ADS <span class="marquee-dot"></span></div>
    <div class="marquee-item">CONTENT STRATEGY <span class="marquee-dot"></span></div>
    <div class="marquee-item">VIDEO PRODUCTION <span class="marquee-dot"></span></div>
    <div class="marquee-item">FMCG <span class="marquee-dot"></span></div>
    <div class="marquee-item">TEAM LEADERSHIP <span class="marquee-dot"></span></div>
    <div class="marquee-item">BRAND STRATEGY <span class="marquee-dot"></span></div>
    <div class="marquee-item">AI PROMPT ENGINEERING <span class="marquee-dot"></span></div>
    <div class="marquee-item">FILMMAKING <span class="marquee-dot"></span></div>
    <div class="marquee-item">CLIENT SERVICING <span class="marquee-dot"></span></div>
  </div>
</div>

<!-- ABOUT -->
<section id="about">
  <div class="reveal">
    <div class="section-label">01 — About</div>
    <h2 class="section-title">THE FULL<br>PICTURE</h2>
  </div>
  <div class="about-grid">
    <div class="about-text reveal">
      <p>I'm a <strong>full-stack marketer</strong> based in Kerala with nearly 4 years of experience building brands across digital and offline — from social strategy and video production to client servicing and team leadership.</p>
      <p>My edge? I approach every campaign through the lens of <em>neuromarketing</em> — understanding how the brain actually makes decisions, and designing content and funnels that work at that level.</p>
      <p>I run <strong>Infoparkology</strong> as a freelance creative gig alongside my full-time role as Team Lead at Brandpackt. I've worked across <strong>FMCG, hospitality, F&B, education, real estate and healthcare</strong>.</p>
      <p>Before marketing, I handled international patient relations and celebrity events at <strong>Lourdes Hospital</strong> — where I learned high-stakes brand representation and the real art of client servicing.</p>
      <div class="about-tags">
        <span class="tag">Neuromarketing</span><span class="tag">Meta Ads</span>
        <span class="tag">Content Strategy</span><span class="tag">Video Production</span>
        <span class="tag">LinkedIn Growth</span><span class="tag">Team Leadership</span>
        <span class="tag">Prompt Engineering</span><span class="tag">Client Servicing</span>
        <span class="tag">FMCG</span><span class="tag">Filmmaking</span>
      </div>
    </div>
    <div class="about-cards reveal">
      <div class="about-card">
        <div class="about-card-bar"></div>
        <div class="about-card-num">₹30L</div>
        <div class="about-card-text"><strong>Campaign Budget Managed</strong>Golden Truth — pan-India, 20-member team, 3 months.</div>
      </div>
      <div class="about-card">
        <div class="about-card-bar"></div>
        <div class="about-card-num">30K+</div>
        <div class="about-card-text"><strong>Followers Grown</strong>Across FMCG, F&B, hospitality, education &amp; more.</div>
      </div>
      <div class="about-card">
        <div class="about-card-bar"></div>
        <div class="about-card-num">6</div>
        <div class="about-card-text"><strong>Roles at Brandpackt</strong>Social → Video → Client Servicing → Strategy → Sales → Team Lead.</div>
      </div>
      <div class="about-card">
        <div class="about-card-bar"></div>
        <div class="about-card-num">🎬</div>
        <div class="about-card-text"><strong>Filmmaker First</strong>1st Prize as Director, Interschool Short Film Competition 2014.</div>
      </div>
    </div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience">
  <div class="reveal">
    <div class="section-label">02 — Experience</div>
    <h2 class="section-title">CAREER<br>ARC</h2>
  </div>
  <div class="exp-timeline">
    <div class="exp-item reveal">
      <div class="exp-dot"></div>
      <div><div class="exp-year">2022 — NOW</div><div class="exp-company">Brandpackt · Ad Agency</div></div>
      <div>
        <div class="exp-role">TEAM LEAD</div>
        <p class="exp-desc">Leading a cross-functional team across strategy, content, and client servicing. Overseeing multi-client campaigns, mentoring juniors, and driving agency growth. Evolved through 6 progressive roles from Social Media Manager to Team Lead.</p>
        <div class="exp-highlights"><span class="highlight">Leadership</span><span class="highlight">Strategy</span><span class="highlight">Client Growth</span><span class="highlight">6 Roles</span></div>
      </div>
    </div>
    <div class="exp-item reveal">
      <div class="exp-dot"></div>
      <div><div class="exp-year">2022 — NOW</div><div class="exp-company">Infoparkology</div></div>
      <div>
        <div class="exp-role">FREELANCE CREATIVE STRATEGIST</div>
        <p class="exp-desc">Running Infoparkology as a freelance digital and creative gig — managing clients across salons, restaurants, schools, hotels, and medical equipment. Full strategy, content, and execution handled end-to-end.</p>
        <div class="exp-highlights"><span class="highlight">Freelance</span><span class="highlight">Multi-Industry</span><span class="highlight">Full-Service</span></div>
      </div>
    </div>
    <div class="exp-item reveal">
      <div class="exp-dot"></div>
      <div><div class="exp-year">2021 — 2022</div><div class="exp-company">Lourdes Hospital</div></div>
      <div>
        <div class="exp-role">BRAND & EVENTS MANAGER</div>
        <p class="exp-desc">Managed international patient relations, celebrity event management, social media, branding, and video production at one of Kerala's most prominent hospitals.</p>
        <div class="exp-highlights"><span class="highlight">Branding</span><span class="highlight">Event Management</span><span class="highlight">VIP Relations</span></div>
      </div>
    </div>
    <div class="exp-item reveal">
      <div class="exp-dot"></div>
      <div><div class="exp-year">Brandpackt · Client</div><div class="exp-company">FMCG</div></div>
      <div>
        <div class="exp-role">THE HEARTHY STORE</div>
        <p class="exp-desc">Grew the brand from 400 to 22K followers in 8 months. Produced 30+ videos, introduced a new content format that generated 1M+ organic views — zero paid boost.</p>
        <div class="exp-highlights"><span class="highlight">0→22K Followers</span><span class="highlight">1M+ Views</span><span class="highlight">30+ Videos</span></div>
      </div>
    </div>
  </div>
</section>

<!-- CASE STUDIES -->
<section id="cases">
  <div class="reveal">
    <div class="section-label">03 — Case Studies</div>
    <div class="cases-top">
      <h2 class="section-title">SELECTED<br>WORK</h2>
      <a href="https://drive.google.com/drive/folders/YOUR_FOLDER_ID" target="_blank" class="cases-drive-btn">📁 &nbsp;View Full Work on Drive ↗</a>
    </div>
    <p class="cases-hint">Click any card to <span>view the work →</span></p>
  </div>
  <div class="cases-grid">
    <div class="case-card reveal" onclick="openModal('loft')">
      <div class="case-card-bg"></div>
      <div class="case-num">01</div>
      <div class="case-category">Sales Close · Hospitality</div>
      <div class="case-title">The Loft Business Hotel</div>
      <p class="case-desc">Pitched and closed a full-service digital marketing retainer. Website strategy, Meta & Google Ads, LinkedIn, SEO — cold prospect to long-term client.</p>
      <div class="case-result">₹50,000/month retainer · Full-funnel</div>
      <div class="case-cta">View Work <span class="case-cta-arr">→</span></div>
    </div>
    <div class="case-card reveal" onclick="openModal('golden')">
      <div class="case-card-bg"></div>
      <div class="case-num">02</div>
      <div class="case-category">Campaign Management · Jewellery</div>
      <div class="case-title">Golden Truth — Pan-India</div>
      <p class="case-desc">Led a ₹30 lakh national campaign — 20-member pan-India team, full creative production, delivered in 3 months.</p>
      <div class="case-result">₹30L budget · 20-person team · 3 months</div>
      <div class="case-cta">View Work <span class="case-cta-arr">→</span></div>
    </div>
    <div class="case-card reveal" onclick="openModal('trinity')">
      <div class="case-card-bg"></div>
      <div class="case-num">03</div>
      <div class="case-category">Sales Close · Real Estate</div>
      <div class="case-title">Trinity Builders</div>
      <p class="case-desc">Closed a premium real estate client on a full-service digital package — Meta/Google/LinkedIn ads, SEO, HNI-targeted content strategy.</p>
      <div class="case-result">₹2,00,000/month retainer · HNI Targeting</div>
      <div class="case-cta">View Work <span class="case-cta-arr">→</span></div>
    </div>
    <div class="case-card reveal" onclick="openModal('hap')">
      <div class="case-card-bg"></div>
      <div class="case-num">04</div>
      <div class="case-category">Market Entry · FMCG</div>
      <div class="case-title">HAP Toothpaste — Kerala Launch</div>
      <p class="case-desc">Neuromarketing-led Kerala entry for a premium hydroxyapatite toothpaste. Shelf psychology, offline channels, brand positioning with Mohanlal.</p>
      <div class="case-result">Neuromarketing · Shelf Strategy · FMCG</div>
      <div class="case-cta">View Work <span class="case-cta-arr">→</span></div>
    </div>
    <div class="case-card reveal" onclick="openModal('hearthy')">
      <div class="case-card-bg"></div>
      <div class="case-num">05</div>
      <div class="case-category">Social Media · FMCG</div>
      <div class="case-title">The Hearthy Store</div>
      <p class="case-desc">400 to 22K followers in 8 months. 30+ videos, new content format, 1M+ organic views. Zero paid boost. Pure strategy.</p>
      <div class="case-result">↑ 22K followers · 1M+ views · 30+ videos</div>
      <div class="case-cta">View Work <span class="case-cta-arr">→</span></div>
    </div>
    <div class="case-card reveal" onclick="openModal('reddys')">
      <div class="case-card-bg"></div>
      <div class="case-num">06</div>
      <div class="case-category">Hyperlocal Marketing · F&B</div>
      <div class="case-title">Reddy's Kitchen</div>
      <p class="case-desc">Hyperlocal neuromarketing strategy. Meta ads + Swiggy/Zomato integration, content calendar, trigger-based creative for repeat orders.</p>
      <div class="case-result">Meta Ads · Hyperlocal · F&B</div>
      <div class="case-cta">View Work <span class="case-cta-arr">→</span></div>
    </div>
  </div>
</section>

<!-- MODAL -->
<div class="modal-overlay" id="modalOverlay" onclick="closeOut(event)">
  <div class="modal" id="modalBox">
    <div class="modal-header">
      <div>
        <div class="modal-cat" id="mCat"></div>
        <div class="modal-title" id="mTitle"></div>
      </div>
      <button class="modal-close" onclick="closeModal()">✕</button>
    </div>
    <div class="modal-body">
      <div class="modal-stats" id="mStats"></div>
      <p class="modal-desc" id="mDesc"></p>
      <div class="modal-work-label">📎 WORK SAMPLES & DOCUMENTS</div>
      <div id="mLinks"></div>
    </div>
  </div>
</div>

<!-- SKILLS -->
<section id="skills">
  <div class="reveal">
    <div class="section-label">04 — Skills & Tools</div>
    <h2 class="section-title">THE<br>TOOLKIT</h2>
  </div>
  <div class="skills-layout">
    <div class="skills-intro reveal">
      <p>A full-stack marketer doesn't just specialize — they connect the dots across every layer of a brand's growth.</p>
      <p>From the brief to the creative, the ad account to analytics, the client call to the campaign report — I own the whole board.</p>
      <p>My differentiator is bringing <strong style="color:var(--white)">neuromarketing thinking</strong> into every layer of execution.</p>
    </div>
    <div class="skills-grid reveal">
      <div>
        <div class="skill-group-title">Strategy</div>
        <div class="skill-item"><span class="skill-name">Neuromarketing</span><div class="skill-bar"><div class="skill-fill" style="width:95%"></div></div></div>
        <div class="skill-item"><span class="skill-name">Content Strategy</span><div class="skill-bar"><div class="skill-fill" style="width:90%"></div></div></div>
        <div class="skill-item"><span class="skill-name">Brand Positioning</span><div class="skill-bar"><div class="skill-fill" style="width:88%"></div></div></div>
        <div class="skill-item"><span class="skill-name">Market Entry</span><div class="skill-bar"><div class="skill-fill" style="width:82%"></div></div></div>
      </div>
      <div>
        <div class="skill-group-title">Execution</div>
        <div class="skill-item"><span class="skill-name">Meta Ads</span><div class="skill-bar"><div class="skill-fill" style="width:92%"></div></div></div>
        <div class="skill-item"><span class="skill-name">Google Ads</span><div class="skill-bar"><div class="skill-fill" style="width:85%"></div></div></div>
        <div class="skill-item"><span class="skill-name">Marketing Planning</span><div class="skill-bar"><div class="skill-fill" style="width:90%"></div></div></div>
        <div class="skill-item"><span class="skill-name">Team Management</span><div class="skill-bar"><div class="skill-fill" style="width:88%"></div></div></div>
      </div>
      <div>
        <div class="skill-group-title">Creative</div>
        <div class="skill-item"><span class="skill-name">Video Production / Editing</span><div class="skill-bar"><div class="skill-fill" style="width:93%"></div></div></div>
        <div class="skill-item"><span class="skill-name">AI Video & Image Gen</span><div class="skill-bar"><div class="skill-fill" style="width:88%"></div></div></div>
        <div class="skill-item"><span class="skill-name">Video Storytelling</span><div class="skill-bar"><div class="skill-fill" style="width:91%"></div></div></div>
        <div class="skill-item"><span class="skill-name">Concept Development</span><div class="skill-bar"><div class="skill-fill" style="width:87%"></div></div></div>
      </div>
      <div>
        <div class="skill-group-title">Tools & AI</div>
        <div class="skill-item"><span class="skill-name">ChatGPT / Claude / Gemini</span><div class="skill-bar"><div class="skill-fill" style="width:95%"></div></div></div>
        <div class="skill-item"><span class="skill-name">Premiere / CapCut / InVideo</span><div class="skill-bar"><div class="skill-fill" style="width:90%"></div></div></div>
        <div class="skill-item"><span class="skill-name">AI Prompt Engineering</span><div class="skill-bar"><div class="skill-fill" style="width:93%"></div></div></div>
        <div class="skill-item"><span class="skill-name">Flow / Grok</span><div class="skill-bar"><div class="skill-fill" style="width:82%"></div></div></div>
      </div>
    </div>
  </div>
</section>

<!-- ACHIEVEMENTS -->
<section id="achievements">
  <div class="reveal">
    <div class="section-label">05 — Achievements</div>
    <h2 class="section-title">AWARDS &<br>MILESTONES</h2>
  </div>
  <div class="ach-grid">
    <div class="ach-item reveal"><div class="ach-icon">🏆</div><div><div class="ach-title">INTERSCHOOL SHORT FILM — 1ST PRIZE</div><p class="ach-desc">Won first prize as Director at the Interschool Short Film Competition. Storytelling has always been my core language.</p><div class="ach-year">2014</div></div></div>
    <div class="ach-item reveal"><div class="ach-icon">🎬</div><div><div class="ach-title">CEMCA COMMUNITY RADIO VIDEO CHALLENGE — 3RD PRIZE</div><p class="ach-desc">Placed 3rd at the 6th CEMCA Community Radio Video Challenge — a national-level competition in video production.</p><div class="ach-year">2019</div></div></div>
    <div class="ach-item reveal"><div class="ach-icon">💰</div><div><div class="ach-title">₹3 LAKHS — ONLINE CREATIVE CONTESTS</div><p class="ach-desc">Won nearly ₹3 lakhs across online creative competitions through strategic creative thinking.</p><div class="ach-year">Multiple Years</div></div></div>
    <div class="ach-item reveal"><div class="ach-icon">📈</div><div><div class="ach-title">30K+ FOLLOWERS — GROWN ACROSS CLIENTS</div><p class="ach-desc">Grown 30,000+ followers across multiple client accounts — including Hearthy Store: 400 to 22K in 8 months with 1M+ organic views.</p><div class="ach-year">Brandpackt · Multiple Clients</div></div></div>
    <div class="ach-item reveal"><div class="ach-icon">🚀</div><div><div class="ach-title">₹30L PAN-INDIA CAMPAIGN IN 3 MONTHS</div><p class="ach-desc">Led Golden Truth — 20-member national team, ₹30 lakh budget, strategy to full execution in 90 days.</p><div class="ach-year">Brandpackt · Malabar Gold</div></div></div>
    <div class="ach-item reveal"><div class="ach-icon">🏢</div><div><div class="ach-title">6 PROGRESSIVE ROLES — ONE STARTUP</div><p class="ach-desc">Social Media Manager → Video Editor → Client Servicing → Creative Strategist → Sales → Team Lead. All at Brandpackt.</p><div class="ach-year">2022 — Present</div></div></div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="reveal">
    <div class="section-label">06 — Contact</div>
    <h2 class="section-title">LET'S<br>TALK</h2>
  </div>
  <div class="contact-layout">
    <div class="reveal">
      <p class="contact-cta">Have a brand that needs <strong>sharper strategy</strong>, a campaign that needs <strong>real results</strong>, or a team that needs <strong>a full-stack thinker</strong>? Let's talk.</p>
      <a href="https://drive.google.com/drive/folders/YOUR_FOLDER_ID" target="_blank" class="drive-btn">📁 &nbsp;View My Work on Google Drive</a>
      <div class="contact-links">
        <a href="mailto:j4jobil.10@gmail.com" class="contact-link"><span class="cli">✉</span> j4jobil.10@gmail.com</a>
        <a href="https://www.linkedin.com/in/jobil-cherian-1a3438168/" target="_blank" class="contact-link"><span class="cli">in</span> linkedin.com/in/jobil-cherian-1a3438168</a>
        <a href="tel:+919567016220" class="contact-link"><span class="cli">☎</span> +91 95670 16220</a>
      </div>
    </div>
    <div class="contact-form reveal">
      <div class="form-row">
        <div class="form-group"><label class="form-label">Your Name</label><input type="text" class="form-input" placeholder="John Doe"></div>
        <div class="form-group"><label class="form-label">Email</label><input type="email" class="form-input" placeholder="hello@brand.com"></div>
      </div>
      <div class="form-group"><label class="form-label">What do you need?</label><input type="text" class="form-input" placeholder="Brand strategy, campaign, content..."></div>
      <div class="form-group"><label class="form-label">Tell me more</label><textarea class="form-textarea" placeholder="Brief details about your project..."></textarea></div>
      <button class="form-btn">SEND MESSAGE →</button>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">JOBIL<span>.</span></div>
  <div class="footer-copy">© 2025 Jobil Cherian · Full-Stack Marketer · Kerala, India</div>
</footer>

<script>
// Cursor
const cur = document.getElementById('cursor'), ring = document.getElementById('cring');
let mx=0,my=0,rx=0,ry=0;
document.addEventListener('mousemove',e=>{ mx=e.clientX; my=e.clientY; cur.style.left=mx+'px'; cur.style.top=my+'px'; });
(function loop(){ rx+=(mx-rx)*0.12; ry+=(my-ry)*0.12; ring.style.left=rx+'px'; ring.style.top=ry+'px'; requestAnimationFrame(loop); })();
document.querySelectorAll('a,button,.case-card').forEach(el=>{
  el.addEventListener('mouseenter',()=>{ cur.classList.add('hovered'); ring.classList.add('hovered'); });
  el.addEventListener('mouseleave',()=>{ cur.classList.remove('hovered'); ring.classList.remove('hovered'); });
});

// Nav
window.addEventListener('scroll',()=>{ document.getElementById('mainNav').classList.toggle('scrolled',scrollY>60); });

// Reveal
const obs=new IntersectionObserver(entries=>entries.forEach((e,i)=>{ if(e.isIntersecting){ setTimeout(()=>e.target.classList.add('visible'),i*80); obs.unobserve(e.target); } }),{threshold:0.08});
document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));

// Modal data — replace YOUR_*_ID with actual Google Drive file/folder IDs
const data = {
  loft:{
    cat:'Sales Close · Hospitality', title:'The Loft Business Hotel',
    stats:[{n:'₹50K',l:'Monthly Retainer'},{n:'4+',l:'Services'}],
    desc:'Pitched and closed a full-service digital marketing retainer with The Loft Business Hotel. The proposal covered website revamp, Meta & Google Ads, LinkedIn marketing, and SEO. A cold prospect was converted into a long-term monthly client through a tailored pitch backed by competitor analysis and a clear ROI projection.',
    links:[
      {i:'📄',n:'Sales Pitch Deck',s:'Full proposal presented to client',url:'https://drive.google.com/file/d/YOUR_LOFT_PITCH_ID/view'},
      {i:'📊',n:'Campaign Strategy Document',s:'Meta & Google Ads plan',url:'https://drive.google.com/file/d/YOUR_LOFT_STRATEGY_ID/view'}
    ]
  },
  golden:{
    cat:'Campaign Management · Jewellery', title:'Golden Truth — Pan-India Campaign',
    stats:[{n:'₹30L',l:'Campaign Budget'},{n:'20',l:'Team Members'}],
    desc:"Led Malabar Gold's Golden Truth Season 2 — a ₹30 lakh pan-India campaign managed from brief to execution. Coordinated a 20-member team across multiple cities, overseeing creative production, logistics, and delivery. Completed in 3 months, on time and on budget.",
    links:[
      {i:'🎬',n:'Campaign Highlights Reel',s:'Final production video',url:'https://drive.google.com/file/d/YOUR_GOLDEN_VIDEO_ID/view'},
      {i:'📄',n:'Campaign Report',s:'Strategy, execution & results',url:'https://drive.google.com/file/d/YOUR_GOLDEN_REPORT_ID/view'}
    ]
  },
  trinity:{
    cat:'Sales Close · Real Estate', title:'Trinity Builders',
    stats:[{n:'₹2L',l:'Monthly Retainer'},{n:'HNI',l:'Target Audience'}],
    desc:'Closed Trinity Builders on a full-service digital marketing retainer. The package covers Meta & Google Ads, LinkedIn campaigns, SEO, and premium content targeting high-net-worth individuals looking for luxury real estate in Kerala.',
    links:[
      {i:'📄',n:'Pitch Presentation',s:'Full client proposal',url:'https://drive.google.com/file/d/YOUR_TRINITY_PITCH_ID/view'},
      {i:'📊',n:'Digital Strategy Plan',s:'HNI targeting approach',url:'https://drive.google.com/file/d/YOUR_TRINITY_STRATEGY_ID/view'}
    ]
  },
  hap:{
    cat:'Market Entry Strategy · FMCG', title:'HAP Toothpaste — Kerala Launch',
    stats:[{n:'FMCG',l:'Industry'},{n:'Neuro',l:'Strategy Core'}],
    desc:"Developed a full neuromarketing-led market entry strategy for Willy Whyte's HAP Toothpaste — a premium hydroxyapatite product with Mohanlal as brand ambassador. The Kerala-first plan covers shelf psychology, consumer trigger mapping, offline channel strategy, digital activation, and a phased launch playbook.",
    links:[
      {i:'📄',n:'Market Entry Strategy Document',s:'Full neuromarketing-led plan',url:'https://drive.google.com/file/d/YOUR_HAP_STRATEGY_ID/view'},
      {i:'📊',n:'Shelf Psychology & Packaging Brief',s:'POS & retail conversion notes',url:'https://drive.google.com/file/d/YOUR_HAP_SHELF_ID/view'}
    ]
  },
  hearthy:{
    cat:'Social Media Growth · FMCG', title:'The Hearthy Store',
    stats:[{n:'22K',l:'Followers (from 400)'},{n:'1M+',l:'Organic Views'}],
    desc:'Managed The Hearthy Store as a Brandpackt client — grew from 400 to 22K followers in just 8 months. Introduced a new short-video content format and built a consistent storytelling framework across 30+ videos. The result: 1M+ organic views with zero ad spend.',
    links:[
      {i:'📹',n:'Sample Content Videos',s:'Videos that drove 1M+ views',url:'https://drive.google.com/file/d/YOUR_HEARTHY_VIDEO_ID/view'},
      {i:'📄',n:'Content Strategy Document',s:'Full 8-month growth plan',url:'https://drive.google.com/file/d/YOUR_HEARTHY_STRATEGY_ID/view'}
    ]
  },
  reddys:{
    cat:'Hyperlocal Marketing · F&B', title:"Reddy's Kitchen",
    stats:[{n:'F&B',l:'Industry'},{n:'Hyper',l:'Local Strategy'}],
    desc:"Designed a hyperlocal neuromarketing strategy for Reddy's Kitchen. The plan integrates Meta ads with Swiggy/Zomato visibility, a monthly content calendar, and trigger-based creatives engineered to drive repeat orders and in-store footfall.",
    links:[
      {i:'📄',n:'Hyperlocal Marketing Plan',s:'Full F&B strategy document',url:'https://drive.google.com/file/d/YOUR_REDDYS_PLAN_ID/view'},
      {i:'📱',n:'Content Samples',s:'Social media creatives',url:'https://drive.google.com/file/d/YOUR_REDDYS_CONTENT_ID/view'}
    ]
  }
};

function openModal(id){
  const d=data[id];
  document.getElementById('mCat').textContent=d.cat;
  document.getElementById('mTitle').textContent=d.title;
  document.getElementById('mDesc').textContent=d.desc;
  document.getElementById('mStats').innerHTML=d.stats.map(s=>`<div class="modal-stat-box"><div class="modal-stat-num">${s.n}</div><div class="modal-stat-label">${s.l}</div></div>`).join('');
  document.getElementById('mLinks').innerHTML=d.links.map(l=>`<a href="${l.url}" target="_blank" class="modal-link"><div class="modal-link-icon">${l.i}</div><div class="modal-link-body"><div class="modal-link-name">${l.n}</div><div class="modal-link-sub">${l.s}</div></div><div class="modal-link-arr">↗</div></a>`).join('');
  document.getElementById('modalOverlay').classList.add('open');
  document.body.style.overflow='hidden';
}
function closeModal(){ document.getElementById('modalOverlay').classList.remove('open'); document.body.style.overflow=''; }
function closeOut(e){ if(e.target===document.getElementById('modalOverlay')) closeModal(); }
document.addEventListener('keydown',e=>{ if(e.key==='Escape') closeModal(); });
</script>
</body>
</html>
