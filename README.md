<p align="center">
  <img src="icon.svg" width="160" alt="App studio — telemóvel com batimento cardíaco, uma lâmpada, um lápis e um estetoscópio">
</p>

<h1 align="center">App studio — Claude Skill</h1>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"></a>
  <img src="https://img.shields.io/badge/Claude-Skill-D97757" alt="Claude Skill">
  <img src="https://img.shields.io/badge/modos-Idear%20·%20Criar%20·%20Diagnosticar-8A63D2" alt="Modos">
</p>

<p align="center">
📚 Faz parte da <b><a href="https://github.com/mozuraa/claude-skills">biblioteca de skills de mozuraa</a></b> · Part of <b><a href="https://github.com/mozuraa/claude-skills">mozuraa's skills library</a></b>
</p>

<p align="center"><b>🇬🇧 English · <a href="README.pt.md">🇵🇹 Português</a></b></p>

---

A **complete app studio** for **Claude** (iOS, Android, Flutter, React Native/Expo, desktop), with three linked modes:

| Mode | What for | Example request |
|---|---|---|
| 💡 **Ideate** | Detailed ideas for **new apps and games** you can build and publish on your own | "What game should I make next?" |
| 🛠️ **Create** | **Builds an app with you from scratch**, from the idea to an MVP and publishing on the App Store and Google Play | "I want an app to track my plants" |
| 🩺 **Diagnose** | **Examines and fixes** everything that affects the app: 12 areas, 140+ checks, a health report with an opinion and a "store-ready?" verdict | "My app crashes" · "Apple rejected it" |

In every mode Claude **asks questions, shows evidence, gives its honest opinion and only goes ahead with your approval**. The idea you pick in Ideate becomes the brief for Create; Create ends with a Diagnose check-up before going to the store; a diagnosis can lead to ideas for the next version.

### 💡 Ideate

- Two or three **well-developed** ideas, each with: what it is, who it's for, the core loop, what makes it different, how it makes money, effort, first steps and risks.
- Original ideas only: never clones of existing apps or games.
- It has an [inspiration catalog](references/idear/inspiracao.md) with:
  - game genres and mechanics;
  - utilities;
  - system features that spark ideas (widgets, Live Activities, on-device AI);
  - how to validate an idea before building it;
  - a grid for comparing ideas;
  - ideas to avoid.

### 🛠️ Create

```
1. Brief ─► 2. Plan (MVP) ─► ✋ ─► 3. Design ─► 4. Core flow ─► ✋ ─► 5. Rest of the app ─► 6. Verification ─► ✋ ─► 7. Stores and handover
```

- **Brief** with the right questions for each kind of app: games, utilities, habits, health, kids, social, business, fun apps.
- **MVP plan**: the smallest version that already delivers value, with the technology, data and costs. ✋ You approve.
- **Native design**, following Apple's and Google's guidelines.
- **Core flow first**, running in the simulator, with screenshots. ✋ You approve.
- **Rest of the app**: data that's never lost across updates, permissions at the right moment, accessibility, app icon, purchases with restore, Privacy Manifest.
- **Verification** with the Diagnose mode. ✋ You approve.
- **Publishing**: TestFlight, store listing, privacy, review, and a `COMO-ATUALIZAR.md` guide for future updates.
- **Guides:**
  - [`briefing`](references/criar/briefing.md);
  - [`stack`](references/criar/stack.md): SwiftUI, Compose, Flutter, Expo, SpriteKit/Godot, where to store data, accounts, purchases, ads, crash reporting and costs;
  - [`design`](references/criar/design.md): platform conventions, design system, essential screens, icon and games;
  - [`lancamento`](references/criar/lancamento.md): accounts, signing, testing, store listing, privacy, review, rejections and life after launch.

### 🩺 Diagnose

**Consultation → examination with evidence → health report (🔴🟠🟡🟢) → my opinion → you decide → verified treatment → discharge.**

The examination covers 12 areas: stability · functionality and languages · layout on every screen size · icons and images · performance and battery · security · privacy (Privacy Manifest, labels, Data safety, ATT) · accessibility · App Store and Google Play rules · network and data · purchases · build and code.

Guides: [`checklist`](references/diagnostico/checklist.md) (140+ checks) and [`como-verificar`](references/diagnostico/como-verificar.md) (Xcode, `simctl`, Gradle, `adb`, Flutter, Expo).

### Safety and ethics

It only examines your own apps, and security checks are always passive. It never loses users' data and never makes clones. It also doesn't create accounts, make purchases or submit to the stores without you: it prepares everything and tells you exactly which button to press.

### Examples (in Portuguese)

- [Ideate: iPhone games you can build in a month](examples/idear.md)
- [Create: brief and plan for a plant-care app](examples/criar.md)
- [Diagnose: report on a recipe app before the App Store](examples/diagnosticar.md)

### Installation

**Claude Code**

```bash
git clone https://github.com/mozuraa/claude-skill-app-studio.git ~/.claude/skills/app-studio
```

Or tell Claude in a new chat: *"install the skill from this link: https://github.com/mozuraa/claude-skill-app-studio"*.

**Or with the whole library, as a plugin:**

```
/plugin marketplace add mozuraa/claude-skills
/plugin install estudios@mozuraa-skills
```

**Claude app / claude.ai:** click **Code → Download ZIP** and upload the ZIP under **Settings → Capabilities → Skills**.

Start a new session so the skill loads. To update: `cd ~/.claude/skills/app-studio && git pull`.

### Structure

```
claude-skill-app-studio/
├── SKILL.md                     # the 3 modes and shared rules
├── references/
│   ├── idear/inspiracao.md      # genres, utilities, validation, comparison
│   ├── criar/                   # briefing, stack, design, lancamento
│   └── diagnostico/             # checklist (12 areas) and como-verificar (commands)
├── examples/                    # idear.md, criar.md, diagnosticar.md
├── icon.svg · README.md · README.pt.md · CHANGELOG.md · LICENSE
```

The skill's instructions are written in Portuguese, but Claude replies in whatever language you write in.

### History

Version 2.0 merges two earlier skills, **ideias-apps** and **app-doctor** (their git histories are preserved in this repository), and adds the Create mode.

### License

[MIT](LICENSE)
