<div align="center">

<br/>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:ffe6f2,50:ffb6c1,100:ff69b4&height=200&section=header&text=Birthday+Card+for+Mom&fontSize=48&fontColor=ffffff&fontAlignY=38&desc=A+heartfelt+interactive+birthday+card+with+butterflies+and+confetti&descAlignY=60&descSize=14&descColor=fff0f5" width="100%"/>

<br/>

[![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Google Fonts](https://img.shields.io/badge/Font-Great%20Vibes-d63384?style=flat-square)](https://fonts.google.com/specimen/Great+Vibes)
[![MIT License](https://img.shields.io/badge/License-MIT-22c55e?style=flat-square)](LICENSE)
[![Deployed](https://img.shields.io/badge/Deployed-GitHub%20Pages-0ea5e9?style=flat-square&logo=github)](https://safin313-stack.github.io/Birthday-card/)
[![Stars](https://img.shields.io/badge/Stars-⭐%201-f97316?style=flat-square)]()

<br/>

<a href="https://safin313-stack.github.io/Birthday-card/">
  <img src="https://img.shields.io/badge/-%F0%9F%92%8C%20%20LIVE%20DEMO%20%20%E2%86%92-d63384?style=for-the-badge&logoColor=white" alt="Live Demo" height="42"/>
</a>

<br/>
<sub>✦ No login &nbsp;·&nbsp; No install &nbsp;·&nbsp; Opens instantly in your browser ✦</sub>

<br/><br/>

</div>

---

<div align="center">

### 🌸 Features

| 💌 Hidden Letter | 🦋 Butterflies | 🎊 Confetti | ✨ Sparkles | 🖋️ Cursive Font | 💖 Personal Message |
|:---:|:---:|:---:|:---:|:---:|:---:|
| Birthday letter revealed on button click with fade-in animation | Butterflies fly up the screen when the letter opens | Canvas-based falling confetti in rainbow colors | Twinkling sparkle dots scattered across the background | Google Fonts Great Vibes cursive for elegant typography | Heartfelt personal message written for Mom |

</div>

---

## 🖥️ Card Preview

```
╔══════════════════════════════════════════════════════════╗
║  ✨  ·  ✨  ·  ✨  ·  ✨  ·  ✨  ·  ✨  (sparkles)       ║
║                                                          ║
║   🎊 confetti raining from the top of the screen 🎊     ║
║                                                          ║
║         ╔══════════════════════════════════╗             ║
║         ║                                  ║             ║
║         ║   Happy Birthday, Mom! 🎂        ║             ║
║         ║                                  ║             ║
║         ║  [ Open Your Birthday Letter 💌 ]║             ║
║         ║                                  ║             ║
║         ║   ← click to reveal the letter   ║             ║
║         ║                                  ║             ║
║         ╚══════════════════════════════════╝             ║
║                                                          ║
║   🦋      🦋        🦋       🦋      🦋  (fly up)       ║
╚══════════════════════════════════════════════════════════╝
```

> ✦ Click **"Open Your Birthday Letter"** — butterflies release and the letter fades in!

---

## 🎨 Technical Highlights

### Reveal Letter with Fade-in Animation

```css
#letter {
  display: none;
  animation: fadeIn 2s forwards;
}

@keyframes fadeIn {
  from { opacity: 0; }
  to   { opacity: 1; }
}
```

```js
function revealLetter() {
  document.getElementById('letter').style.display = 'block';
  // also releases butterflies!
}
```

### Butterfly Release on Click

```js
for (let i = 0; i < 12; i++) {
  const b = document.createElement('div');
  b.className = 'butterfly';
  b.style.left = Math.random() * window.innerWidth + 'px';
  b.style.top  = window.innerHeight + 'px';
  b.style.animationDuration = (6 + Math.random() * 5) + 's';
  document.body.appendChild(b);
  setTimeout(() => b.remove(), 10000);
}
```

### Canvas Confetti Engine

```js
const confetti = Array.from({ length: 150 }, () => ({
  x: Math.random() * canvas.width,
  y: Math.random() * canvas.height,
  r: Math.random() * 4 + 1,
  color: `hsl(${Math.random() * 360}, 100%, 70%)`
}));

function update() {
  confetti.forEach(c => {
    c.y += Math.cos(c.d) + 1 + c.r / 2;   // gravity
    c.x += Math.sin(0.01);                  // gentle drift
    if (c.y > canvas.height) {
      c.y = 0;
      c.x = Math.random() * canvas.width;   // reset to top
    }
  });
}
```

### Twinkling Sparkles

```js
for (let i = 0; i < 60; i++) {
  const s = document.createElement('div');
  s.className = 'sparkle';
  s.style.top  = Math.random() * 100 + 'vh';
  s.style.left = Math.random() * 100 + 'vw';
  s.style.animationDelay = Math.random() * 3 + 's';
  document.body.appendChild(s);
}
```

---

## 💌 The Letter Inside

> *"Dear Mom, on this special day, I just want to tell you how much you mean to me. Your love is the foundation that made me who I am..."*

A heartfelt message written from a son to his mother — personal, warm, and full of love. 💖

---

## 📁 Project Structure

```
Birthday-card/
│
├── 📄 index.html    ← Complete card: HTML + CSS + JS in one file
└── 📄 README.md     ← Project documentation
```

---

## 🚀 Run It Yourself

**Option 1 — Live (instant, no setup)**

> 🔗 **[https://safin313-stack.github.io/Birthday-card/](https://safin313-stack.github.io/Birthday-card/)**

**Option 2 — Clone and open locally**

```bash
git clone https://github.com/Safin313-stack/Birthday-card.git
open index.html
```

---

## 🛠️ Tech Stack

```
┌──────────────────────────────────────────────────────┐
│           Frontend · Single File · No Framework      │
├─────────────────┬────────────────────────────────────┤
│  HTML5          │  Card structure and letter layout  │
│  CSS3           │  Animations · sparkles · butterfly │
│  JavaScript     │  Confetti engine · letter reveal   │
│  Canvas API     │  Real-time falling confetti        │
│  Google Fonts   │  Great Vibes cursive typeface      │
└─────────────────┴────────────────────────────────────┘
```

---

## 📚 Key Concepts Used

```
Canvas API           → real-time confetti particle rendering
createElement()      → dynamically spawning butterflies and sparkles
@keyframes fadeIn    → smooth letter reveal animation
@keyframes twinkle   → pulsing sparkle dots across the background
@keyframes fly       → butterflies floating upward off screen
setTimeout()         → auto-removing butterflies after 10 seconds
Math.random()        → randomised positions · timing · colors
hsl() color          → rainbow confetti using random hue values
Great Vibes font     → elegant cursive typography for the card
```

---

## 💡 Credits & Inspiration

Special thanks to **TCW - AI & coding resources** (Telegram Community)
for ideas, guidance, and coding support throughout this project. 🙏

---

<div align="center">

## 👤 Developer

<br/>

**Saharia Hassan Safin**
Front-end Developer · Loving Son 💖

<br/>

[![GitHub](https://img.shields.io/badge/GitHub-Safin313--stack-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Safin313-stack)
&nbsp;
[![Live Project](https://img.shields.io/badge/Live%20Project-Visit%20Now-d63384?style=for-the-badge&logo=vercel&logoColor=white)](https://safin313-stack.github.io/Birthday-card/)

<br/>

*"Because some feelings are too big for a text message — so I wrote code instead"* 💖

<br/>

</div>

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:ff69b4,50:ffb6c1,100:ffe6f2&height=120&section=footer" width="100%"/>

<sub>MIT License · © 2025 Saharia Hassan Safin · ⭐ Star this repo if it touched your heart!</sub>

</div>
