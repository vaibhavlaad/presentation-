# HealthWise AI — Interactive Project Presentation

An immersive, single-page **web-based project presentation** for a final-year B.Tech Data Science project: **HealthWise AI** — an AI-powered personal health report analysis and lifestyle recommendation platform.

This is **not** a dashboard and **not** a traditional PowerPoint. It is a full-screen, slide-style presentation website that combines the feel of an Apple product launch, a modern startup landing page, and an interactive project demo.

## ✨ Features

- **11 full-screen sections** — each fills the viewport like a presentation slide
- **Multiple navigation methods**
  - ← / → and ↑ / ↓ arrow keys
  - Spacebar to advance
  - On-screen Prev / Next buttons
  - `Home` / `End` to jump to first / last slide
- **Slide progress indicator** — slide counter (`03 / 11`), progress ring, and vertical dot rail
- **Smooth animated transitions** between sections (Framer Motion `AnimatePresence`)
- **Apple-inspired premium design** — dark navy backgrounds, glassmorphism cards, cyan/teal healthcare accents, soft glowing effects, drifting data particles
- **Fully responsive** — works smoothly on desktop and mobile
- **Interactive elements** — hoverable step explorer, animated pipelines, live Recharts visualizations

## 🧱 Tech Stack

- **React 18 + Vite 5**
- **Tailwind CSS 3**
- **Framer Motion** for animations
- **Lucide React** for icons
- **Recharts** for charts

## 🚀 Getting Started

```bash
npm install
npm run dev
```

The app runs at `http://localhost:5173`.

To build for production:

```bash
npm run build
npm run preview
```

## 📂 Project Structure

```
healthwise-presentation/
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── Navigation.jsx          # Top logo, slide counter, progress ring, prev/next
│   │   ├── ProgressIndicator.jsx   # Vertical right-edge dot rail
│   │   ├── AnimatedBackground.jsx   # Per-slide ambient background + particles
│   │   ├── SlideLayout.jsx         # Full-screen section wrapper with entrance animation
│   │   └── ArchitectureFlow.jsx    # Reusable animated pipeline component
│   ├── slides/
│   │   ├── Hero.jsx                # 1  — Title / hero
│   │   ├── Problem.jsx             # 2  — The problem
│   │   ├── WhyItMatters.jsx        # 3  — Why it matters
│   │   ├── ExistingSolutions.jsx   # 4  — Existing solutions comparison
│   │   ├── ProposedSolution.jsx    # 5  — Proposed solution pipeline
│   │   ├── HowItWorks.jsx          # 6  — System architecture (interactive steps)
│   │   ├── Objectives.jsx          # 7  — Five objectives
│   │   ├── Technology.jsx          # 8  — Tech stack & methodology flow
│   │   ├── Outcomes.jsx            # 9  — Mock dashboard, metrics, charts, comparison
│   │   ├── Timeline.jsx            # 10 — Feasibility & 6-phase timeline
│   │   └── Conclusion.jsx         # 11 — Conclusion + disclaimer + restart
│   ├── App.jsx                     # Slide registry, keyboard nav, transitions
│   ├── main.jsx
│   └── index.css
├── index.html
├── package.json
├── vite.config.js
├── tailwind.config.js
├── postcss.config.js
└── README.md
```

## 🎮 Navigation Reference

| Action            | Key / Control           |
| ----------------- | ----------------------- |
| Next slide       | `→` `↓` `Space` or Next button |
| Previous slide   | `←` `↑` or Prev button         |
| First slide      | `Home`                        |
| Last slide       | `End`                         |
| Restart          | "Restart Presentation" button on the final slide |

## 📝 Project Context

**HealthWise AI** lets users upload laboratory health reports (PDF or image). The system uses OCR and document processing to extract health parameters, values, units, and available reference ranges. The extracted data is cleaned and analyzed using a rule-based reference-range engine. AI then explains the results in simple language and provides general lifestyle guidance.

> **Disclaimer:** HealthWise AI does not diagnose diseases, prescribe medicines, or replace doctors. It is an educational and wellness-support platform.

## ✏️ Customization

- **Team / guide / college details** are in `src/slides/Hero.jsx`.
- **Sample metrics, charts, and comparison data** are in `src/slides/Outcomes.jsx`.
- **Color theme** is in `tailwind.config.js` (`colors.navy`, `colors.teal`).
- **Add or reorder slides** in the `SLIDES` array in `src/App.jsx`.
