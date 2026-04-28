<div align="center">

<img src="https://upload.wikimedia.org/wikipedia/commons/1/1c/Logo_of_UNICEF.svg" alt="UNICEF" width="220" />

# Mina &amp; Raju — Reimagined

### *A Story Retold in Light*

###### *A fan tribute to UNICEF's beloved 1993 animated series*

**A semi-realistic, cinematic retelling of Bangladesh's most beloved cartoon — where a girl, her brother, and a clever parrot still teach a village to listen.**

<br/>

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Responsive](https://img.shields.io/badge/Responsive-Design-1abc9c?style=for-the-badge)
![Accessibility](https://img.shields.io/badge/A11Y-Friendly-blueviolet?style=for-the-badge)

![Status](https://img.shields.io/badge/status-live-success?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-blue?style=flat-square)
![Made With](https://img.shields.io/badge/made%20with-%E2%9D%A4-c0532b?style=flat-square)

<br/>

![Hero Banner](Image/HERO%20SECTION.jpeg)

</div>

---

## ✨ About The Project

**Mina &amp; Raju Reimagined** is an animated single-page portfolio that pays tribute to UNICEF's beloved 1993 character, **Mina** — and her brother **Raju** and parrot **Mithu** — by re-rendering their world in a warm, semi-realistic, painterly style.

The site weaves a story across six chapters:

| # | Section | What it does |
|:-:|:--------|:-------------|
| 01 | **Hero** | A sunset village hero with staggered word-by-word title reveal and floating parallax artwork |
| 02 | **About Mina** | Vertical zigzag timeline tracing the journey from 1993 to today |
| 03 | **Characters** | Cards for Mina, Raju, Mithu, and the villagers — with hover lift &amp; glow |
| 04 | **Story &amp; Impact** | Themes of courage, education, and community on a deep indigo backdrop |
| 05 | **Gallery** | A four-up bento grid of cinematic stills |
| 06 | **Closing** | Final invitation, with footer and credits |

---

## 🎨 Design Language

> *Warm, painterly, cinematic — colors borrowed from a Bengali sunset.*

```
Terracotta   #c0532b     ──  primary, warmth
Saffron      #e8a548     ──  accent, light
Indigo       #2d2456     ──  secondary, depth
Forest       #557a3e     ──  tertiary, life
Cream        #f7efe1     ──  background, paper
Espresso     #2b1d12     ──  ink, grounding
```

**Typography**
- **Display** — *Fraunces* (warm, literary serif)
- **Body** — *Inter* (clean, modern sans)

**Motion vocabulary** — `cubic-bezier(0.22, 1, 0.36, 1)` — soft, decisive, never bouncy.

---

## 🛠 How This Website Was Built — Step by Step

This site was built using the **`/animated-website`** pipeline, a 9-step Claude Code skill that turns a single text brief into a complete animated single-page site. Here's the full journey:

### **Step 1 — The Brief**
Started with a single creative brief in `brief.txt` describing the goal: *"Reimagine Mina &amp; Raju as semi-realistic humans, preserving their stories of courage, education, and community."*

### **Step 2 — Brand Foundation** *(skill: `brand`)*
Established the voice, narrative tone, and emotional north star — warm, hopeful, rooted in South Asian cultural memory. Output captured in `docs/brand-guidelines.md`.

### **Step 3 — UX Strategy** *(skill: `ui-ux-pro-max`)*
Mapped the user journey across six chapters. Chose a **storytelling layout** over a typical SaaS grid — vertical timeline, bento gallery, full-bleed hero — so the page reads like a picture book.

### **Step 4 — Design System** *(skill: `design-system`)*
Built a three-layer token architecture (primitive → semantic → component). Spacing scale (4–128px), radii (8–32px), elevation (sm/md/lg), and motion durations (`micro` 150ms · `std` 300ms · `expr` 600ms · `hero` 900ms). Tokens live in `assets/design-tokens.css`.

### **Step 5 — Visual Direction** *(skill: `design`)*
Locked in the painterly palette, chose **Fraunces + Inter** as the type pair, and defined the radial-gradient sun motif used in the hero and closing sections.

### **Step 6 — Imagery**
Seven cinematic key-art images rendered for hero, character portraits (Mina, Raju, Mithu, parents), village school scene, and gallery — saved under `Image/`.

### **Step 7 — UI Implementation** *(skill: `ui-styling`)*
Hand-authored a single `index.html` containing:
- Semantic HTML5 (header, main, sections, aside, footer)
- Self-contained CSS with design tokens, no framework
- Mobile-first responsive layout (320px → 1280px)
- Full keyboard nav + skip link + ARIA roles
- `prefers-reduced-motion` respected throughout

### **Step 8 — Animation Layer**
Vanilla JS, zero dependencies:
- **Hero word-by-word reveal** (staggered 120ms)
- **IntersectionObserver scroll reveals** with cascading delay
- **Parallax** on hero artwork &amp; sun rays
- **Float** keyframes (9s &amp; 12s) on focal art
- **Hover micro-interactions** on cards (lift, rotate, glow)

### **Step 9 — Provenance &amp; Build Report**
Pipeline metadata captured in `build-report.json` and embedded as an HTML comment at the top of `index.html` — every skill that fired, every image tier, every fallback documented.

---

## 📁 Project Structure

```
unicef-cartoon animation/
├── index.html              ← single-page site (HTML + CSS + JS in one file)
├── favicon.svg             ← brand mark
├── og-image.svg            ← social share card
├── brief.txt               ← original creative brief
├── build-report.json       ← pipeline provenance
├── assets/
│   └── design-tokens.css   ← shared design tokens
├── docs/
│   └── brand-guidelines.md ← brand voice &amp; visual direction
└── Image/
    ├── HERO SECTION.jpeg
    ├── MINA.jpeg
    ├── RAJU.jpeg
    ├── MITHU.jpeg
    ├── PARENTS  VILLAGERS.jpeg
    ├── BACKGROUND SCENE.jpeg
    └── STORY SCENE.jpeg
```

---

## 🚀 Run It Locally

No build step. No dependencies. Just open and go.

```bash
git clone https://github.com/jawar001/unicef-cartoonanimation.git
cd unicef-cartoonanimation
```

Then either:
- **Double-click** `index.html` to open it directly, **or**
- Serve it for hot-reload-friendly dev:
  ```bash
  npx serve .
  # or
  python -m http.server 8000
  ```

Open `http://localhost:8000` and enjoy.

---

## ♿ Accessibility

- Semantic landmarks (`header`, `main`, `nav`, `aside`, `footer`)
- Skip-to-content link
- All interactive elements keyboard-reachable with visible focus rings
- Color contrast meets **WCAG AA** on all text
- `prefers-reduced-motion` disables animations entirely
- All images carry meaningful `alt` text
- ARIA labels on every nav and interactive control

---

## 🌐 Browser Support

| Chrome | Firefox | Safari | Edge |
|:------:|:-------:|:------:|:----:|
| ✅ Latest | ✅ Latest | ✅ Latest | ✅ Latest |

Mobile-tested on iOS Safari and Chrome Android.

---

## 🙏 Credits

<div align="center">

### **Built by Shahajada Jawar**
[![GitHub](https://img.shields.io/badge/GitHub-jawar001-181717?style=for-the-badge&logo=github)](https://github.com/jawar001)
[![Email](https://img.shields.io/badge/Email-shahajadajawar%40gmail.com-c0532b?style=for-the-badge&logo=gmail&logoColor=white)](mailto:shahajadajawar@gmail.com)

*Designed, written, and shipped with care.*

</div>

**Inspired by:**

<a href="https://www.unicef.org">
  <img src="https://upload.wikimedia.org/wikipedia/commons/1/1c/Logo_of_UNICEF.svg" alt="UNICEF" width="120" align="right" />
</a>

- **UNICEF's Mina** (1993) — created by Ram Mohan, Rachelle Romeo &amp; team. This is a fan tribute and creative reimagining; all character likenesses are interpretations made with respect for the original work.
- This project is **not affiliated with or endorsed by UNICEF**. The UNICEF logo is shown for attribution only.

<br clear="right"/>

**Built using:**
- [Claude Code](https://claude.com/claude-code) by Anthropic — `/animated-website` pipeline
- Skills: `brand`, `ui-ux-pro-max`, `design-system`, `design`, `ui-styling`
- Type: [Fraunces](https://fonts.google.com/specimen/Fraunces) &amp; [Inter](https://fonts.google.com/specimen/Inter) via Google Fonts

---

## 📜 License

Released under the **MIT License**. Character likenesses are fan tributes; please honor UNICEF's original creative work when forking.

---

<div align="center">

### *"Even one girl learning to read can light a whole village."*

**⭐ If this story moved you, leave a star.**

</div>
