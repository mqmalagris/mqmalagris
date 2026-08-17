# Matheus Malagris

**Software Engineer** — based in Brazil.
Building production software — SaaS platforms, e-commerce storefronts, serverless data pipelines, and ERP integrations.

I started in Electrical Engineering and ended up deep in software, drawn by the same thing: building systems that work precisely and reliably. I like the parts of the job most people avoid — distributed state, third-party API complexity, schema design that has to survive real-world load.

---

## Selected projects

### [agent-skills](https://github.com/mqmalagris/agent-skills) — Dual-format agent skills collection
Curated collection of 23 agent skills shipped in two formats from the same `SKILL.md` files — a Claude Code plugin marketplace (`/plugin marketplace add mqmalagris/agent-skills`) or `bunx skills add mqmalagris/agent-skills`, which installs into any of 75+ agents. Headline is a nine-skill feature-delivery pipeline — `dev-flow → grill-me → to-prd → compass → heist → maestro → pr-craft → babysit-prs` — taking a feature from vague idea to merged PR, each stage consuming the prior stage's artifact and refusing to proceed on thin context; `babysit-prs` then drives the PR through bot and human review on its own loop until it merges. Also ships **code-craft** (language/framework idioms across 7 languages and 12 frameworks, with a PostToolUse hook that flips reviewer rules on automatically), a deterministic LLM-first **seo** audit suite, and OWASP WSTG security testing. Every skill is versioned independently with CI-validated manifests, and all use progressive disclosure: a `SKILL.md` router plus workflows, topics, and reference tables loaded on demand.

### [yield-curves](https://crates.io/crates/yield-curves) — Rust yield curve library
Pure-Rust fixed-income library: piecewise linear, natural cubic spline (C² via Thomas tridiagonal solver), PCHIP monotone Hermite, Nelson-Siegel (1987), Svensson (1994) — plus bond pricing (duration, convexity, par yield), compounding and implied-forward-rate conversion, and a zero-dependency date toolkit (ISDA 2006 day counts, business-day calendars incl. Brazil BUS/252, coupon schedules). No third-party numerical crates — bundles its own Nelder-Mead simplex optimizer. `unsafe_code = "forbid"`, post-fit sanity checks with deterministic spline fallback, SLSA Level 3 provenance on every crates.io release.

### [protoglot](https://crates.io/crates/protoglot) — Multiprotocol API client
Local-first, git-friendly API client spanning REST, GraphQL, SOAP, WebSocket, and gRPC in a single TOML collection format — a Postman/Bruno alternative. Dynamic gRPC via `.proto` reflection with no `protoc` dependency; JS pre/post-request hooks via `boa_engine`. CLI-first (`pglot`) test runner with JUnit/TAP output and CI-correct exit codes, data-driven testing (CSV/JSON), JSON Schema assertions, and snapshot testing — the same engine powers a native egui desktop app that self-updates from GitHub Releases. OpenAPI specs import straight into a TOML collection with spec tree search for picking endpoints. Tagged releases auto-publish to npm and crates.io via Trusted Publishing, with SLSA build provenance.

### [SynthChord](https://synthchord.com/) — Chord-pad music synthesizer
Flutter chord-pad synthesizer built on the Nashville Number System — tap diatonic pads or twist a joystick to morph chord quality (maj7, sus4, dim, aug). Three instrument engines (SF2 soundfont, subtractive synth, chromatic WAV sampler), a reorderable effects chain (Freeverb reverb, delay, low-pass filter), looper, arpeggiator, and a low-latency 512-frame PCM audio path with a FluidSynth fallback on desktop and web. The whole audio engine was since ported from Dart to a Rust crate behind `flutter_rust_bridge` + cargokit, shipped in three parts — FX chain, then the synth and sampler, then SF2 playback onto `rustysynth` — each landing dormant behind a render boundary and cut over only after byte-exact parity with the Dart implementation. EN/ES/FR/pt-BR i18n, RevenueCat freemium gate, v1.2.0 on Google Play via GitHub Actions signed-release CD with R8 gated in CI.

### [mic-router](https://github.com/mqmalagris/mic-router) — Multi-microphone recorder
Records two or more USB microphones on one computer in sync. Each USB mic runs on its own crystal clock, so over a long take they drift apart and desync — the standard reason multi-mic setups on a single machine fall apart. The first mic listed becomes the master clock and every other mic is linear-resampled to its exact sample count over the take, correcting nominal sample-rate mismatch and drift in one step, so all tracks come out equal-length. Rust with cpal capture, lock-free `rtrb` ring buffers to the writer, and one WAV per mic plus a mix via `hound`. Zero-config CLI: bare invocation lists numbered devices, `record 0,1` captures until Enter, with optional fixed duration, `--normalize`, and per-mic `--gain`. Shipped as a prebuilt Windows zip on GitHub Releases.

### [Economapy](https://api.economapy.com/docs/) — Brazilian economic indicators API
Public freemium REST + GraphQL API (Indicadores-BR) aggregating Brazilian and international economic data — BCB, IBGE SIDRA, Tesouro Nacional, FRED, ECB — into normalized endpoints with complete history and aggressive caching. Rust + Axum with compile-time-checked sqlx queries, apalis ingestion workers with retry and circuit breakers, real-time PTAX over WebSocket, HMAC-signed webhooks and alerts, and financial calculators (SAC/Price amortization, monetary correction, CDB/LCI/LCA comparison). Yield-curve endpoints are backed by my own yield-curves crate. Single binary on Fly.io; OpenAPI docs and Swagger UI at api.economapy.com/docs.

---

## Stack

**Languages**

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" width="48" alt="TypeScript" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" width="48" alt="JavaScript" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/rust/rust-original.svg" width="48" alt="Rust" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/go/go-original.svg" width="48" alt="Go" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/dart/dart-original.svg" width="48" alt="Dart" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg" width="48" alt="HTML5" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg" width="48" alt="CSS3" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/bash/bash-original.svg" width="48" alt="Bash" />

**Frontend**

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg" width="48" alt="React" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/svelte/svelte-original.svg" width="48" alt="Svelte" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/astro/astro-original.svg" width="48" alt="Astro" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nextjs/nextjs-original.svg" width="48" alt="Next.js" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/remix/remix-original.svg" width="48" alt="Remix" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vuejs/vuejs-original.svg" width="48" alt="Vue.js" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/angular/angular-original.svg" width="48" alt="Angular" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/tailwindcss/tailwindcss-original.svg" width="48" alt="Tailwind CSS" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/sass/sass-original.svg" width="48" alt="Sass" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/redux/redux-original.svg" width="48" alt="Redux" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/apollographql/apollographql-original.svg" width="48" alt="Apollo GraphQL" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/graphql/graphql-plain.svg" width="48" alt="GraphQL" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vitejs/vitejs-original.svg" width="48" alt="Vite" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/webpack/webpack-original.svg" width="48" alt="Webpack" />

**Mobile**

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/flutter/flutter-original.svg" width="48" alt="Flutter" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/reactnative/reactnative-original.svg" width="48" alt="React Native" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/expo/expo-original.svg" width="48" alt="Expo" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/ionic/ionic-original.svg" width="48" alt="Ionic" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/capacitor/capacitor-original.svg" width="48" alt="Capacitor" />

**Backend**

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original.svg" width="48" alt="Node.js" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original.svg" width="48" alt="Express" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/bun/bun-original.svg" width="48" alt="Bun" />

**Databases**

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original.svg" width="48" alt="PostgreSQL" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original.svg" width="48" alt="MongoDB" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original.svg" width="48" alt="MySQL" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/sqlite/sqlite-original.svg" width="48" alt="SQLite" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/dynamodb/dynamodb-original.svg" width="48" alt="DynamoDB" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/supabase/supabase-original.svg" width="48" alt="Supabase" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/firebase/firebase-original.svg" width="48" alt="Firebase" />

**Cloud & Infra**

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" width="48" alt="AWS" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cloudflare/cloudflare-original.svg" width="48" alt="Cloudflare" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cloudflareworkers/cloudflareworkers-original.svg" width="48" alt="Cloudflare Workers" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vercel/vercel-original.svg" width="48" alt="Vercel" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original.svg" width="48" alt="Docker" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/terraform/terraform-original.svg" width="48" alt="Terraform" />

**Tooling & Testing**

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/git/git-original.svg" width="48" alt="Git" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/github/github-original.svg" width="48" alt="GitHub" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/githubactions/githubactions-original.svg" width="48" alt="GitHub Actions" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vitest/vitest-original.svg" width="48" alt="Vitest" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/jest/jest-plain.svg" width="48" alt="Jest" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/storybook/storybook-original.svg" width="48" alt="Storybook" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/pnpm/pnpm-original.svg" width="48" alt="pnpm" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vscode/vscode-original.svg" width="48" alt="VS Code" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postman/postman-original.svg" width="48" alt="Postman" />

---

## Background

B.Eng. Electrical Engineering — CEFET-RJ, Brazil. The engineering mindset stuck: understand the system, find the constraint, fix it properly.

---

## Contact

- **Email** — matheus@malagris.dev
