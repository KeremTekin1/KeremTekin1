<div align="center">

# Kerem Tekin

### Computer Engineering student at Hacettepe University

I spend most of my time building things I would actually want to use: AI tools, backend systems, web products, and games.

[![Portfolio](https://img.shields.io/badge/Portfolio-keremtekin.dev-1F2937?style=flat-square&logo=vercel&logoColor=white)](https://keremtekin.dev)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Kerem_Tekin-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/keremtekin1/)
[![Email](https://img.shields.io/badge/Email-keremtkn44%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:keremtkn44@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-KeremTekin1-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/KeremTekin1)

<sub>Ankara, Türkiye | Open to internships and collaboration</sub>

</div>

---

## About me

I enjoy taking an idea beyond the demo stage and figuring out the less exciting but important parts too: data, permissions, error handling, tests, deployment, and maintenance.

Most of my recent work is around backend development and applied AI. I also keep building game and graphics projects because that is where I first became interested in software systems.

This profile also serves as my main portfolio, and the same projects are written up as case studies on [keremtekin.dev](https://keremtekin.dev) (English and Turkish). I own more than 25 repositories, most of them private. For those, I have included short case studies here without publishing the source code or sensitive data.

## Projects I want to highlight

### Taskflow `(private)`

A Jira-like work management platform built as a modular monolith.

- Java 21, Spring Boot, Spring Modulith, PostgreSQL, and Flyway
- React 19, TypeScript, Vite, and React Router
- Workspace and project permissions, scoped API tokens, OpenAPI, and Docker Compose
- An assistant for drafting descriptions, extracting tasks, searching work, summarizing projects, and spotting sprint or capacity risks

The assistant only makes suggestions. It cannot silently change project data.

`Java 21` `Spring Boot` `Spring Modulith` `PostgreSQL` `React` `Playwright`

### Yargıtay Emsal Karar Asistanı `(private)`

I built this for a real legal research use case. It is used by a practicing lawyer to search Turkish Supreme Court (Yargıtay) decisions and ask source-based questions.

- Started on 21,000 scraped decisions and now searches a live index of **about 9.8 million Yargıtay decisions** (open CC0 dataset, indexed with Tantivy)
- Each query takes top-100 candidates from the full archive, merges them with domain-scoped embeddings (Chroma) and BM25 through Reciprocal Rank Fusion, then reranks with a cross-encoder
- Answers follow a structured answer + citations contract; an unverifiable case number or a citation outside the retrieved sources blocks the answer
- A versioned evaluation set drives retrieval changes: on the original corpus, adding lexical search raised recall@10 from **21% to 60%**, and an "improvement" that dropped it to 31% was caught and reverted
- At full-archive scale, candidate recall is tracked separately (about 80% top-100 on a small 44-decision gold set) and is not presented as answer accuracy
- New PDF sources stay quarantined until hashed, scanned, and approved; Streamlit and FastAPI interfaces, rate limiting, query cost telemetry, and 700+ offline tests

`Python` `Tantivy` `Chroma` `SQLite FTS5` `FastAPI` `Streamlit` `Pytest`

### Reality Foundry `(private)`

A platform that turns ideas described in natural language into browsable 3D worlds, built around a validated world document.

- pnpm monorepo with three slices: a React-free Three.js player runtime, a React Three Fiber studio editor, and a Fastify API
- Every change is a validated command with revision history, undo/redo, restore, idempotency keys, and compare-and-set commits on PostgreSQL
- Email/password sessions, world ownership, and project-level authorization on every route
- Randomized invariant tests, a real-PostgreSQL concurrency suite in CI, Playwright end-to-end journeys, and architecture decisions recorded as ADRs
- Optional model-assisted editing and world generation sit behind explicit server flags and are off by default

`TypeScript` `Fastify` `PostgreSQL` `Three.js` `React Three Fiber` `Playwright`

### Lakehouse Agent, KKB Hackathon 2026 `(private)`

A domain-agnostic, metadata-driven analytics agent that will not state a number without evidence.

- Looks at a local lakehouse first, fetches missing series from official sources, then analyzes them with validated tools
- Immutable Bronze, Silver, and Gold layers with lineage; an evidence gate rejects numeric answers that no analysis tool call backs
- Trend, lagged correlation, Granger precedence, backtested forecasting, anomalies, change points, and charts
- Web, search, and OCR content is treated as untrusted data; SSRF-protected fetcher and a loopback-only demo UI
- 1,800+ automated tests, `mypy --strict`, ruff, and CI

`Python` `DuckDB` `Parquet` `Pydantic` `statsmodels` `Pytest`

### Sillage `(private)`

A mobile app that tells you which perfume to wear today based on the weather, the season, and your own shelf.

- No LLM: a 16-dimensional accord space, cosine similarity, and a weather formula make every suggestion free, instant, and explainable
- Local-first with an offline shelf; optional Supabase sync with row-level security checked by 167 automated checks
- Catalog harvested from official brand sites with robots.txt respected and a data-quality audit
- CI runs typecheck, lint, tests, a deterministic catalog build, Expo Doctor, and a web export on every push

`TypeScript` `Expo` `React Native` `Supabase` `GitHub Actions`

### RoomForge `(private)`

Turns a phone video of a room into a game-ready 3D scene: a measured floor plan, walls with doors cut out, furniture as separate objects, a navmesh, and baked textures, exported as a Blender scene and glTF.

- Reconstruction with MapAnything, plane fitting, wall-versus-wardrobe selection from where the camera actually walked, and optional metric scale from an ArUco marker
- Nothing falls back silently: every stage reports what it could not do, and the exported glTF is audited for UVs, material, and a real texture before a run counts as successful
- Python worker, FastAPI job service, React and three.js viewer, headless Blender scripts, and a GPU Docker profile
- About 360 worker tests

`Python` `Blender` `FastAPI` `three.js` `Docker`

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

## University and team game projects

| Project | Short description | Stack |
|---|---|---|
| **The Last Tenant** `(private)` | First-person mystery game built by a five-person team for a university Game Tech course. A ten-week vertical slice shown in three staged demos. Story and narrative are written by teammates; my part is the Unity implementation. | Unity 6 · C# · URP |
| **Marble Game Upgrade** `(private)` | BBM 423 Game Technologies Lab assignment: an assigned Unity base game upgraded with post-processing, audio, ghost runs, achievements, level select, and a time-attack mode, without changing its core mechanics. In progress. | Unity 6 · C# |

## Other private projects

| Project | Short description | Stack |
|---|---|---|
| **Unity + Python Hand Tracking** | Webcam hand tracking with OpenCV and MediaPipe, streamed over UDP to Unity for grabbing, throwing, two-handed scaling, and UI control. | Python · MediaPipe · Unity · C# |
| **ColoringApp** | Unity children's coloring app with BFS flood fill, coroutine frame budgeting, hover preview, undo, persistence, sequential unlocking, ScriptableObject configuration, and focused NUnit tests. | Unity · C# · DOTween · NUnit |
| **Scale Vault** | Data extraction and static catalog pipeline for Mini GT, Inno64, and Tarmac Works models; search, filters, favorites, comparisons, stock-aware data generation, QA, and single-file builds. | JavaScript · HTML · CSS · Node.js |
| **DiecastAlert** | Scheduled product/price monitoring with separate Telegram notification flows, persistent state, dry-run operation, Playwright fallback, and brand filtering. | Python · Playwright · Telegram Bot API |
| **AuraRoom** | Interior design MVP that turns a room brief, and optionally a photo, into palette, furniture, layout, and budget suggestions. | Next.js · TypeScript · OpenAI API |
| **QueuePass** | QR-first queue and appointment product prototype for barbers, salons, clinics, repair shops, and other small service businesses. | TypeScript · JavaScript · HTML · CSS |
| **Local Quiz App** | Small reusable browser quiz app with data-driven questions and explanations. Runs without a backend or dependencies. | JavaScript · HTML · CSS |
| **Portfolio** | Source of [keremtekin.dev](https://keremtekin.dev): a bilingual (English/Turkish) portfolio with light/dark themes, GitHub integration, and detailed case-study pages. | Next.js · TypeScript · Tailwind CSS |

## Public projects

| Project | Short description | Stack |
|---|---|---|
| [**MiniGameEngine**](https://github.com/KeremTekin1/MiniGameEngine) | A small WebGL2 engine with modular shaders, camera controls, procedural meshes, textures, skybox rendering, OBJ loading, and a debug panel. | WebGL2 · JavaScript · GLSL |
| [**Hide and Seek WebGL**](https://github.com/KeremTekin1/hide-and-seek-webgl) | University team project with 3D rendering, player and camera control, collisions, modular scenes, and state-based enemy AI. | WebGL · JavaScript · GLSL |
| [**SpaceInvader**](https://github.com/KeremTekin1/SpaceInvader) | JavaFX arcade shooter with dynamic spawning, rewards and penalties, power-ups, scoring, pause/restart, and complete menu-to-game-over flow. | Java · JavaFX |
| [**Tower Defense Unity**](https://github.com/KeremTekin1/tower-defense-unity) | Public Unity foundation/prototype associated with the more extensive private tower-defense systems project. | Unity · C# · ShaderLab |

## Technologies I use

<div align="center">

![Skills](https://skillicons.dev/icons?i=java,spring,python,fastapi,ts,js,react,nextjs,html,css,cs,unity,threejs,postgres,sqlite,supabase,prisma,docker,blender,git,github&perline=11)

</div>

- **Languages:** Java, Python, TypeScript, JavaScript, C#, C++, SQL
- **Backend and data:** Spring Boot, Spring Modulith, FastAPI, Fastify, ASP.NET Core, PostgreSQL, SQLite, DuckDB, SQLAlchemy, Prisma, Supabase
- **AI:** RAG, hybrid retrieval, embeddings, BM25/FTS5, Tantivy, RRF, cross-encoder reranking, tool use, evaluation pipelines, agent runtimes, local LLMs
- **Frontend and mobile:** React, Next.js, Vite, Tailwind CSS, React Native / Expo, Three.js, React Three Fiber
- **Games, graphics, and vision:** Unity, WebGL/WebGL2, GLSL/ShaderLab, JavaFX, Blender scripting, OpenCV, MediaPipe
- **Tools:** Git, Docker, Maven, pnpm, Pytest, NUnit, Playwright, GitHub Actions

<div align="center">

### Contact

I am currently open to internship opportunities, especially in backend development, applied AI, developer tools, game technology, and graphics.

[Portfolio](https://keremtekin.dev) · [LinkedIn](https://www.linkedin.com/in/keremtekin1/) · [Email](mailto:keremtkn44@gmail.com)

<sub>I can demonstrate or discuss private projects when appropriate.</sub>

</div>
