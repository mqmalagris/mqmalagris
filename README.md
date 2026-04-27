# Matheus Malagris

**Senior Full-Stack Developer** — based in Brazil.
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

[![Languages](https://skillicons.dev/icons?i=ts,js,rust,go,dart,html,css,bash)](https://skillicons.dev)

**Frontend**

[![Frontend](https://skillicons.dev/icons?i=react,svelte,astro,nextjs,vue,angular,tailwind,sass,redux,apollo,graphql,vite,webpack)](https://skillicons.dev)

**Mobile**

[![Mobile](https://skillicons.dev/icons?i=flutter)](https://skillicons.dev)

**Backend**

[![Backend](https://skillicons.dev/icons?i=nodejs,express,bun)](https://skillicons.dev)

**Databases**

[![Databases](https://skillicons.dev/icons?i=postgres,mongodb,mysql,sqlite,dynamodb,supabase,firebase)](https://skillicons.dev)

**Cloud & Infra**

[![Cloud](https://skillicons.dev/icons?i=aws,cloudflare,workers,vercel,docker,terraform)](https://skillicons.dev)

**Tooling & Testing**

[![Tooling](https://skillicons.dev/icons?i=git,github,githubactions,vitest,jest,pnpm,vscode,postman)](https://skillicons.dev)

---

## Background

B.Eng. Electrical Engineering — CEFET-RJ, Brazil. The engineering mindset stuck: understand the system, find the constraint, fix it properly.

---

## Contact

- **Email** — malagrismatheus@gmail.com
