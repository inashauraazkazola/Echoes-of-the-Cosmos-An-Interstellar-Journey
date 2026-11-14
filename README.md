# Echoes of the Cosmos: An Interstellar Journey

> **An interactive, voice-narrated children's web storybook that brings humanity's historic hardware left behind on the Moon and Mars to life.**

Built by **Team Suki to Sukses** for the **2026 NASA Space Apps Challenge**.

---

## Overview

When astronauts and robotic explorers complete their missions across the solar system, their hardware remains behind as silent monuments of human curiosity. **Echoes of the Cosmos: An Interstellar Journey** transforms these historic space artifacts into relatable, heartwarming stories for young readers.

Following **Emi** (a curious little orange fox in a white space helmet) and **Otty** (a friendly plump brown sea otter in a pastel blue space scarf), readers embark on a 22-screen cosmic adventure to meet **Flik** (the Apollo 11 Lunar Flag Assembly) on the Moon and **Oppy** (NASA's Opportunity Mars Exploration Rover) on Mars.

---

## Challenge

- **Selected Challenge:** *Abandoned but not Forgotten* (2026 NASA Space Apps Challenge)
- **Objective:** Inspire younger audiences to appreciate space exploration heritage by connecting real NASA mission history with engaging, child-friendly storytelling, interactive audio narration, and hands-on learning checkpoints.

---

## How It Works

1. **Cover & Onboarding (Screen 1):** Readers are welcomed aboard with an illustrated cover, automatic audio unlock on interaction, and a clean cosmic interface.
2. **4 Story Chapters (Screens 2–20):** Each chapter opens with a themed emblem intro followed by 4:3 illustrated story panels (`public/img/*.jpg`) featuring:
   - Distinct character dialogue bubbles (**Narrator**, **Emi**, **Otty**, **Flik**, and **Oppy**) with custom **3px** cartoon vector avatars.
   - Automatic client-side narration with **word-by-word read-along highlighting**, adjustable reading speed (`0.85× / 1.0× / 1.15×`), and soft synthesized chimes.
   - **Expandable NASA Fact Boxes** across all four chapters (Microgravity, Apollo 11 Flag Assembly, Opportunity Rover at Meridiani Planum, and Historic Exploration Plaques).
   - **Interactive Scene Hotspots** on key panels: float zero-gravity items in Chapter 1, inspect Flik's horizontal crossbar in Chapter 2, and gently brush Martian dust off Oppy's solar panels in Chapter 3.
3. **Explorer Challenge Checkpoint (Screen 21):** Before completing the mission, readers review their **3 Discovered NASA Artifact Badges** (*Apollo 11 Flag*, *Opportunity Rover*, and *Dreamers Plaque*) and must correctly answer the **3-question Space Explorer Mini Quiz** to unlock the finale—earning a star-sparkle celebration.
4. **Mission Complete Outro (Screen 22):** Displays team credits (**Team Suki to Sukses**), direct links to official NASA mission archives, and **Read Again / Reset Progress** controls.

---

## Key Features

- **Multi-Character Voice Narration & Word Highlighting:** Uses the browser-native **Web Speech API** with distinct pitch/rate profiles per character, melodic phrase contour, adjustable reading speed (`0.85× / 1.0× / 1.15×`), and dual-mode (`onboundary` + adaptive timer) word-by-word highlighting.
- **Tap-to-Replay & Independent Audio Controls:** Every narrator box, character speech bubble, NASA Fact Box, and quiz question can be replayed individually on tap, alongside a per-page `↺ Replay` button, independent `🔔 SFX` toggle, and global `🔊 Auto-Voice` toggle.
- **Interactive Story Moments:** Hands-on scene interactions (zero-gravity floating stars/pencils, crossbar inspection, and 3-step Martian solar-panel dust brushing) keep young readers engaged.
- **Synthesized Storybook Soundscape:** Gentle **Web Audio API** character chimes and soft page-turn sound effects with zero external audio file dependencies.
- **Interactive NASA Fact Boxes & 3-Question Quiz Gate:** Encourages active comprehension by gating the **Mission Complete** screen behind the Space Explorer Mini Quiz with helpful chapter hints.
- **Zero-PII Local Progress:** Automatically saves reading progress in browser `localStorage` (with a one-tap **Reset Progress** option) with zero name inputs and zero personal data collected or sent to any server.
- **Effortless Navigation Anywhere:** Supports `Previous` / `Next` buttons, a compact header **Story Chapters** dropdown menu (responsive on desktop and mobile), keyboard arrow keys (`←` / `→` / `Escape`), and mobile horizontal touch-swipe gestures.
- **Zero-Backend Static Architecture:** Built completely in static HTML5, CSS3, and Vanilla JavaScript (`index.html`) for instant deployment on Netlify, Vercel, or GitHub Pages.

---

## Impact & Creativity

- **Benefits & Intended Impact:** Makes complex planetary science and space history approachable for early learners, families, and classrooms—even on low-spec devices or in regions without paid software subscriptions. Long-term, it nurtures early STEM curiosity and teaches children that retired spacecraft and lunar hardware are enduring milestones of teamwork and discovery.
- **Creative Approach:** Instead of a static encyclopedia or text-heavy timeline, the project personifies real NASA artifacts—giving **Flik** a lesson on why flags don't flutter in an airless vacuum and letting **Oppy** share the story of Martian hematite *"Blueberries"* at Meridiani Planum and 15 years of resilience—paired with synced read-along highlighting like a living picture book.

---

## Tech Stack & NASA Data

### Technologies & Software
- **Core Frontend:** HTML5, CSS3 (CSS custom properties, responsive Grid/Flexbox, keyframe animations), Vanilla JavaScript (ES6+), and `localStorage`
- **Browser APIs:** Web Speech API (`window.speechSynthesis`), Web Audio API (`AudioContext`)
- **Typography & Visual Assets:** Google Fonts (`Fredoka` & `Nunito`), custom inline SVG character avatars/emblems, and 16 illustrated JPG storybook scenes (`public/img/`)
- **Build & Dev Tooling:** Vite (`vite`) and Node.js / npm

### Official NASA Data Sources
- **NASA Solar System Exploration:** [solarsystem.nasa.gov](https://solarsystem.nasa.gov)
- **NASA Apollo 11 Mission Archive (Flag Assembly & Lunar Plaque):** [nasa.gov/mission/apollo-11](https://www.nasa.gov/mission/apollo-11) (July 20, 1969 Tranquility Base landing, telescoping crossbar Lunar Flag Assembly engineering, and Apollo 11 Lunar Plaque)
- **NASA Mars Exploration Rover Opportunity (MER-B) Archive:** [science.nasa.gov/mission/mer-opportunity](https://science.nasa.gov/mission/mer-opportunity) (January 25, 2004 Meridiani Planum landing, 90-sol design vs. 5,111 sols / ~15 years of operation, 45.16 km traversed, and hematite *"Blueberries"* discovery)

---

## Installation & How to Run

### Prerequisites
- [Node.js](https://nodejs.org/) (v18+ recommended) and `npm`

### Local Development
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/echoes-of-the-cosmos.git
   cd echoes-of-the-cosmos
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the local development server (runs on port `3000`):
   ```bash
   npm run dev
   ```
4. Open `http://localhost:3000` in a modern browser (Chrome, Edge, or Safari recommended for the best Web Speech API voices).

### Production Build (Static Hosting)
```bash
npm run build
```
The compiled static bundle will be output to `dist/`, ready to deploy to GitHub Pages, Vercel, or Netlify with no backend or environment variables required.

---

## Team — **Team Suki to Sukses**

- **Team Member 1 (I.A.R.)** – *Frontend Web Developer*  
  Responsible for UI/UX implementation, responsive frontend engineering (`index.html`), Web Speech API narration & word-highlighting logic, Web Audio sound synthesis, interactive scene hotspots, and official NASA mission data integration.
- **Team Member 2 (N.Z.F.)** – *Project Manager & Live Demo / Pitch Presenter*  
  Responsible for project management, character & story narrative direction, educational fact curation, presentation design, and live demonstration/pitching.

---

## Use of Super Intelligence (SI) / AI Tools

In accordance with NASA Space Apps Challenge guidelines, **Team Suki to Sukses** discloses the following use of Super Intelligence (SI) / AI tools during development:

- **Code & Engineering Assistance:** We used **Google AI Studio (Gemini)** to assist with frontend prototyping, CSS responsiveness, debugging JavaScript state and Web Speech API word-highlighting timing, and drafting technical documentation.
- **Visual Asset Creation:** Custom non-humanoid storybook character illustrations (`public/img/*.jpg`) were created with AI-assisted illustration workflows (Google Gemini image generation) for original fictional characters (**Emi** the fox and **Otty** the otter) and storybook environments.
- **Audio & Data:** All voice narration is synthesized locally in the user's browser via the standard **Web Speech API**, and all chimes/page-turn effects are synthesized via the **Web Audio API**. No AI-generated audio files or unverified AI facts were used; every historical and scientific statement was manually verified against official NASA mission archives (`solarsystem.nasa.gov`, `nasa.gov/mission/apollo-11`, and `science.nasa.gov/mission/mer-opportunity`).
- **NASA Branding & Privacy Compliance:** We explicitly confirm that **no official NASA logos, insignias, seals, agency flags, or NASA branding elements were generated or modified using SI/AI tools**. (The storybook character **Flik** is a fictional artistic illustration representing the historic Apollo 11 Lunar Flag Assembly artifact on the Moon, not an official NASA logo, seal, or agency branding element.) No personally identifiable information (PII) or recognizable likenesses/voices of individuals under age 18 are collected, stored, or included.

---

## Third-Party Materials & Citations

In accordance with the NASA Space Apps Challenge *Use of Third-Party Materials* policy, all non-NASA resources and open-source packages present in the repository are freely and publicly available under OSI-approved or open font licenses and are cited below:

- **Google Fonts (`Fredoka` and `Nunito`):** Used for storybook typography via Google Fonts ([fonts.google.com](https://fonts.google.com)) — licensed under the **SIL Open Font License 1.1 (OFL-1.1)**.
- **Standard Browser APIs:** **Web Speech API** (`window.speechSynthesis`), **Web Audio API** (`AudioContext`), and **Web Storage API** (`localStorage`) — standard W3C browser specifications with no external paid services or proprietary audio libraries.
- **Repository & Build Tooling (`package.json`):**
  - `vite` — **MIT License**
  - `typescript` — **Apache License 2.0**
  - `@types/node` — **MIT License** (DefinitelyTyped)
  *(Note: The live static storybook runs directly from `index.html` with zero runtime backend or external API calls.)*
- **Official NASA Mission Sources:**
  - NASA Solar System Exploration — [https://solarsystem.nasa.gov](https://solarsystem.nasa.gov)
  - NASA Apollo 11 Mission Archive — [https://www.nasa.gov/mission/apollo-11](https://www.nasa.gov/mission/apollo-11)
  - NASA Mars Exploration Rover Opportunity Archive — [https://science.nasa.gov/mission/mer-opportunity](https://science.nasa.gov/mission/mer-opportunity)

---

## License

Original project code and storybook content created by **Team Suki to Sukses** for the **2026 NASA Space Apps Challenge** are released under the **Apache License 2.0** (see [`LICENSE`](./LICENSE) and [opensource.org/licenses/Apache-2.0](https://www.opensource.org/licenses/Apache-2.0)).

