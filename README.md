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

| | |
|---|---|
| **Frontend** | Next.js · React · Svelte · Astro · Vue · Angular · Flutter · React Native · TypeScript · Tailwind |
| **Backend** | Node (Hono · Express · LoopBack · Strapi) · Rust (Axum) · Go · Bun |
| **Data** | PostgreSQL · MongoDB · MySQL/MariaDB · DynamoDB · D1 · Supabase |
| **Cloud** | AWS (Lambda · SAM · DynamoDB · SQS · EventBridge · SES · S3) · Cloudflare Workers (D1 · R2 · KV) · Fly.io · Vercel |
| **E-commerce** | BigCommerce (Stencil) · Miva (MVT) · Shopify · ReCharge · Stripe · DocuSign |
| **Testing** | Vitest · Playwright · Jest · insta · proptest · testcontainers |
| **Tooling** | Terraform · Docker · Turborepo · EAS · Wrangler |

---

## Background

B.Eng. Electrical Engineering — CEFET-RJ, Brazil. The engineering mindset stuck: understand the system, find the constraint, fix it properly.

---

## Contact

- **Email** — matheus.malagris@arcticleaf.com
