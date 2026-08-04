<div align="center">

# Kerem Tekin

### Computer Engineering student at Hacettepe University

I spend most of my time building things I would actually want to use: AI tools, backend systems, web products, and games.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Kerem_Tekin-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/keremtekin1/)
[![Email](https://img.shields.io/badge/Email-keremtkn44%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:keremtkn44@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-KeremTekin1-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/KeremTekin1)

<sub>Ankara, Türkiye | Open to internships and collaboration</sub>

</div>

---

## About me

I enjoy taking an idea beyond the demo stage and figuring out the less exciting but important parts too: data, permissions, error handling, tests, deployment, and maintenance.

Most of my recent work is around backend development and applied AI. I also keep building game and graphics projects because that is where I first became interested in software systems.

This profile also serves as my main portfolio. I currently own **20 repositories: 14 private and 6 public**. For private projects, I have included short case studies without publishing the source code or sensitive data.

## Projects I want to highlight

### Taskflow `(private)`

My latest project is a Jira-like work management platform built as a modular monolith.

- Java 21, Spring Boot, Spring Modulith, PostgreSQL, and Flyway
- React 19, TypeScript, Vite, and React Router
- Workspace and project permissions, scoped API tokens, OpenAPI, and Docker Compose
- An assistant for drafting descriptions, extracting tasks, searching work, summarizing projects, and spotting sprint or capacity risks

The assistant only makes suggestions. It cannot silently change project data.

### Yargıtay Emsal Karar Asistanı `(private)`

I built this for a real legal research use case. It is currently used by a lawyer to search Turkish Supreme Court decisions and ask source-based questions.

- More than **21,000 decisions** across 10 legal areas
- Combines multilingual embeddings in Chroma with SQLite FTS5/BM25 through Reciprocal Rank Fusion
- Every case number in an answer is checked against the retrieved documents
- A versioned evaluation set measures recall@1/5/10 and MRR after retrieval changes
- Adding lexical search improved measured recall@10 from **21% to 60%**
- Streamlit interface, FastAPI service, rate limiting, query telemetry, and offline tests

`Python` `FastAPI` `Chroma` `SQLite FTS5` `Claude` `Streamlit` `Pytest`

### JARVIS `(private)`

This started as a personal assistant and gradually became a small local-first agent runtime.

- Typed tool registry with risk levels and confirmation rules
- Local memory, reminders, calendar, scheduled jobs, and conversation history in SQLite
- Redacted traces so tool activity can be inspected without logging secrets
- A Project Copilot that scans local repositories and keeps snapshots of what changed
- Terminal and desktop interfaces
- **389 offline tests** covering permissions, schemas, redaction, scheduling, snapshots, and tool selection

`Python` `Claude tool use` `SQLite` `pywebview` `Pytest`

### RASYO `(private)`

A personal Borsa İstanbul research and paper-trading tool. It collects market data, scores a watchlist, follows its own suggestions, and keeps a record of how they perform.

- Fundamental, technical, news, flow, and ML-based signals
- Scheduled scans, intraday alerts, morning reports, and a nine-section dashboard
- Sector-neutral scoring, liquidity checks, ATR-based stops, and correlation-aware position sizing
- Local Ollama model for news sentiment and HistGradientBoosting for ranking
- Backtests document transaction costs, survivorship bias, and sampling limitations instead of hiding them

`Python` `FastAPI` `SQLAlchemy` `scikit-learn` `Ollama` `SQLite`

> This is a research project, not investment advice.

### Tower Defense `(private)`

This is my largest Unity project. I used it to explore how a game with many connected systems can stay manageable without relying heavily on Inspector wiring.

- More than 50 runtime systems for towers, waves, UI, pooling, saves, VFX, audio, progression, achievements, and challenges
- Tower synergies, adaptive difficulty, abilities, wave modifiers, meta upgrades, skins, and a minimap
- Multiplayer and relay groundwork
- Separate ASP.NET Core 8 leaderboard API with Entity Framework and Docker support

`Unity 6` `C#` `URP / ShaderLab` `ASP.NET Core` `Docker`

### Spider-Man: NYC `(private)`

A browser gameplay experiment built on Google Photorealistic 3D Tiles. The city is streamed from real-world map data rather than modeled by hand.

- Two independent webs that attach to tile geometry with raycasts
- Pendulum-style swinging, pumping, release boosts, diving, and zip movement
- First and third-person cameras, enemies, collectibles, combos, and slow-motion spider-sense
- A procedural city fallback when map tiles are unavailable

`JavaScript` `Three.js` `Vite` `Google Photorealistic 3D Tiles`

### FORME `(private)`

A full-stack fashion website with both the visual brand experience and the operational parts behind it.

- Product collections, lookbook, campaign media, editorial sections, and an animated hero
- Appointment, enquiry, newsletter, and email flows
- Protected admin area and persistent product data
- Prisma with libSQL, Resend, React Three Fiber, and Playwright-based checks

`Next.js 16` `React 19` `TypeScript` `Prisma` `React Three Fiber` `Resend`

## Other private projects

| Project | Short description | Stack |
|---|---|---|
| **ColoringApp** | Unity children's coloring app with BFS flood fill, coroutine frame budgeting, hover preview, undo, persistence, sequential unlocking, ScriptableObject configuration, and focused NUnit tests. | Unity · C# · DOTween · NUnit |
| **Scale Vault** | Data extraction and static catalog pipeline for Mini GT, Inno64, and Tarmac Works models; search, filters, favorites, comparisons, stock-aware data generation, QA, and single-file builds. | JavaScript · HTML · CSS · Node.js |
| **DiecastAlert** | Scheduled product/price monitoring with separate Telegram notification flows, persistent state, dry-run operation, Playwright fallback, and brand filtering. | Python · Playwright · Telegram Bot API |
| **AuraRoom** | Interior design MVP that turns a room brief, and optionally a photo, into palette, furniture, layout, and budget suggestions. | Next.js · TypeScript · OpenAI API |
| **QueuePass** | QR-first queue and appointment product prototype for barbers, salons, clinics, repair shops, and other small service businesses. | TypeScript · JavaScript · HTML · CSS |
| **Local Quiz App** | Small reusable browser quiz app with data-driven questions and explanations. Runs without a backend or dependencies. | JavaScript · HTML · CSS |
| **Portfolio** | My previous bilingual portfolio site with light/dark themes, GitHub integration, animations, and detailed project pages. | Next.js · TypeScript · Tailwind CSS |

## Public projects

| Project | Short description | Stack |
|---|---|---|
| [**MiniGameEngine**](https://github.com/KeremTekin1/MiniGameEngine) | A small WebGL2 engine with modular shaders, camera controls, procedural meshes, textures, skybox rendering, OBJ loading, and a debug panel. | WebGL2 · JavaScript · GLSL |
| [**Hide and Seek WebGL**](https://github.com/KeremTekin1/hide-and-seek-webgl) | University team project with 3D rendering, player and camera control, collisions, modular scenes, and state-based enemy AI. | WebGL · JavaScript · GLSL |
| [**SpaceInvader**](https://github.com/KeremTekin1/SpaceInvader) | JavaFX arcade shooter with dynamic spawning, rewards and penalties, power-ups, scoring, pause/restart, and complete menu-to-game-over flow. | Java · JavaFX |
| [**Tower Defense Unity**](https://github.com/KeremTekin1/tower-defense-unity) | Public Unity foundation/prototype associated with the more extensive private tower-defense systems project. | Unity · C# · ShaderLab |

<details>
<summary>Older repositories</summary>

- [`KeremTekin`](https://github.com/KeremTekin1/KeremTekin) is my old profile README repository.
- [`horror-game`](https://github.com/KeremTekin1/horror-game) is an empty repository left from an early game idea.

</details>

## Technologies I use

<div align="center">

![Skills](https://skillicons.dev/icons?i=java,spring,python,fastapi,ts,js,react,nextjs,html,css,cs,unity,threejs,postgres,sqlite,prisma,docker,git,github&perline=10)

</div>

- **Languages:** Java, Python, TypeScript, JavaScript, C#, C++, SQL
- **Backend and data:** Spring Boot, Spring Modulith, FastAPI, ASP.NET Core, PostgreSQL, SQLite, SQLAlchemy, Prisma
- **AI:** RAG, hybrid retrieval, embeddings, BM25/FTS5, RRF, tool use, evaluation pipelines, local LLMs
- **Frontend:** React, Next.js, Vite, Tailwind CSS, Three.js, React Three Fiber
- **Games and graphics:** Unity, WebGL/WebGL2, GLSL/ShaderLab, JavaFX
- **Tools:** Git, Docker, Maven, Pytest, NUnit, Playwright, GitHub Actions

<div align="center">

### Contact

I am currently open to internship opportunities, especially in backend development, applied AI, developer tools, game technology, and graphics.

[LinkedIn](https://www.linkedin.com/in/keremtekin1/) · [Email](mailto:keremtkn44@gmail.com)

<sub>I can demonstrate or discuss private projects when appropriate.</sub>

</div>
