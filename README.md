# Matheus Malagris

**Full-Stack Developer** — based in Brazil.
Building production software at [Arctic Leaf Inc.](https://arcticleaf.io) — SaaS platforms, e-commerce storefronts, serverless data pipelines, and ERP integrations.

I started in Electrical Engineering and ended up deep in software, drawn by the same thing: building systems that work precisely and reliably. I like the parts of the job most people avoid — distributed state, third-party API complexity, schema design that has to survive real-world load.

---

## Selected projects

### [yield-curves](https://crates.io/crates/yield-curves) — Rust yield curve library
Pure-Rust fixed-income interpolation and parametric fitting: piecewise linear, natural cubic spline (C² via Thomas tridiagonal solver), Nelson-Siegel (1987), Svensson (1994). Zero third-party numerical crates — bundles its own Nelder-Mead simplex optimizer. `unsafe_code = "forbid"` at the crate level, with a post-fit sanity check so callers can deterministically fall back to the spline when the optimizer lands on an implausible mode. Published to crates.io.

### [CalculeOnline](https://calculeonline.com) — PT-BR calculator platform
140+ static Astro pages with Svelte 5 islands — every calculator is a pre-rendered HTML page that hydrates one interactive component. Build-time sync of Selic/CDI/IPCA/IGP-M/INPC/TR from my own Indicadores-BR API. Full Brazilian tax & payroll suite (IRPF, FGTS, rescisão CLT, INSS, Simples Nacional, MEI, 13º), real-estate financing with composable extra-payment strategies (SAC vs Price), symbolic-calculus parser, 2D/3D function plotters. All math runs client-side.

### [Ephemask](https://ephemask.com/) — Disposable email service
Go Lambdas + Terraform-managed AWS (SES inbound, S3, DynamoDB with TTL auto-delete, API Gateway, Route53). Astro + Svelte 5 web, React Native + Expo mobile, shared TypeScript API client — all in a Turborepo monorepo.

---

## Stack

**Languages**

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" width="48" alt="TypeScript" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" width="48" alt="JavaScript" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/rust/rust-original.svg" width="48" alt="Rust" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/go/go-original.svg" width="48" alt="Go" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/dart/dart-original.svg" width="48" alt="Dart" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg" width="48" alt="HTML5" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg" width="48" alt="CSS3" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/bash/bash-original.svg" width="48" alt="Bash" />

**Frontend**

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg" width="48" alt="React" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/svelte/svelte-original.svg" width="48" alt="Svelte" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/astro/astro-original.svg" width="48" alt="Astro" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nextjs/nextjs-original.svg" width="48" alt="Next.js" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vuejs/vuejs-original.svg" width="48" alt="Vue.js" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/angular/angular-original.svg" width="48" alt="Angular" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/tailwindcss/tailwindcss-original.svg" width="48" alt="Tailwind CSS" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/sass/sass-original.svg" width="48" alt="Sass" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/redux/redux-original.svg" width="48" alt="Redux" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/apollographql/apollographql-original.svg" width="48" alt="Apollo GraphQL" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/graphql/graphql-plain.svg" width="48" alt="GraphQL" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vitejs/vitejs-original.svg" width="48" alt="Vite" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/webpack/webpack-original.svg" width="48" alt="Webpack" />

**Mobile**

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/flutter/flutter-original.svg" width="48" alt="Flutter" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/reactnative/reactnative-original.svg" width="48" alt="React Native" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/expo/expo-original.svg" width="48" alt="Expo" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/ionic/ionic-original.svg" width="48" alt="Ionic" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/capacitor/capacitor-original.svg" width="48" alt="Capacitor" />

**Backend**

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original.svg" width="48" alt="Node.js" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/express/express-original.svg" width="48" alt="Express" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/bun/bun-original.svg" width="48" alt="Bun" />

**Databases**

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original.svg" width="48" alt="PostgreSQL" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original.svg" width="48" alt="MongoDB" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original.svg" width="48" alt="MySQL" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/sqlite/sqlite-original.svg" width="48" alt="SQLite" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/dynamodb/dynamodb-original.svg" width="48" alt="DynamoDB" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/supabase/supabase-original.svg" width="48" alt="Supabase" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/firebase/firebase-original.svg" width="48" alt="Firebase" />

**Cloud & Infra**

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/amazonwebservices/amazonwebservices-original-wordmark.svg" width="48" alt="AWS" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cloudflare/cloudflare-original.svg" width="48" alt="Cloudflare" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cloudflareworkers/cloudflareworkers-original.svg" width="48" alt="Cloudflare Workers" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vercel/vercel-original.svg" width="48" alt="Vercel" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original.svg" width="48" alt="Docker" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/terraform/terraform-original.svg" width="48" alt="Terraform" />

**Tooling & Testing**

<img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/git/git-original.svg" width="48" alt="Git" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/github/github-original.svg" width="48" alt="GitHub" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/githubactions/githubactions-original.svg" width="48" alt="GitHub Actions" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vitest/vitest-original.svg" width="48" alt="Vitest" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/jest/jest-plain.svg" width="48" alt="Jest" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/pnpm/pnpm-original.svg" width="48" alt="pnpm" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/vscode/vscode-original.svg" width="48" alt="VS Code" /> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postman/postman-original.svg" width="48" alt="Postman" />

---

## Background

B.Eng. Electrical Engineering — CEFET-RJ, Brazil. The engineering mindset stuck: understand the system, find the constraint, fix it properly.

---

## Contact

- **Email** — malagrismatheus@gmail.com
