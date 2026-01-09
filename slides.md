---
marp: true
math: true
paginate: true
theme: fintech-docs
author: "Technical Writer"
title: "Product Documentation — Platform X"
description: "Maintainable docs deck using Marp (version-controlled, multi-format)."
footer: 'Page $[page]/$[total] • 22f1001636@ds.study.iitm.ac.in'
---

<style>
/* @theme fintech-docs */
@import 'gaia';

:root {
  --accent: #4f46e5; /* indigo */
  --ink: #e5e7eb;    /* gray-200 */
  --bg: #0b1020;
}

section {
  font-family: Inter, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
  letter-spacing: 0.1px;
}

h1, h2, h3 { color: var(--ink); }
strong { color: var(--accent); }

section.lead {
  background: radial-gradient(1200px 600px at 80% 10%, #1f2937, #0b1020);
  color: var(--ink);
}

code, pre { font-size: 0.9em; }
pre code { line-height: 1.35; }

/* Utility classes for slide-level customization */
section.white-text { color: white; text-shadow: 0 2px 6px rgba(0,0,0,.35); }
section.narrow ul { max-width: 80%; }
</style>


<!-- _class: lead -->

# Platform X — Product Documentation

Modern, maintainable docs deck powered by **Marp**.

**Contact:** [22f1001636@ds.study.iitm.ac.in](mailto:22f1001636@ds.study.iitm.ac.in)

---

## Why Marp for Product Docs?

* Single source of truth (**Markdown**) in version control
* Export to **HTML / PDF / PPTX** via CLI or VS Code extension
* Theming with CSS, math (KaTeX), diagram-friendly
* CI-ready for docs publishing

**Command:**

```bash
# Install
npm install -D @marp-team/marp-cli

# Convert to HTML and PDF
npx marp slides.md -o docs.html
npx marp slides.md --pdf -o docs.pdf


---

## Architecture Overview

* Microservices: Auth, Ingestion, Compute, API Gateway
* Storage: S3-compatible object store, Postgres, Redis
* Observability: OpenTelemetry + Prometheus + Grafana

> Version everything: API schemas, migrations, and configs.

---

<!-- A slide with a background image -->

<!-- _class: white-text -->

![bg](https://images.unsplash.com/photo-1558494949-ef010cbdcc31?q=80\&w=1600\&auto=format\&fit=crop)

# Request Lifecycle

1. Client → API Gateway (JWT)
2. Router → Service (rate-limit, authz)
3. Service → DB + Cache (CQRS pattern)
4. Emit traces/metrics/logs

---

## API Contract (OpenAPI excerpt)

```yaml
openapi: 3.0.3
info:
  title: Platform X API
  version: 1.2.0
paths:
  /v1/jobs:
    post:
      summary: Submit job
      requestBody:
        required: true
        content:
          application/json:
            schema:
              $ref: '#/components/schemas/JobRequest'
      responses:
        '202': { description: Accepted }
```

---

## SDK Usage (TypeScript)

```ts
import { Client } from '@platform-x/sdk';

const client = new Client({ token: process.env.TOKEN! });
const job = await client.jobs.submit({ task: 'ingest', source: 's3://bucket/key' });
console.log('Job submitted:', job.id);
```

---

## Release Process (SemVer)

* `feat:` minor, `fix:` patch, `breaking:` major
* Automated changelog from conventional commits
* Release artifacts: Docker image, CLI, SDK

```bash
# Example release
pnpm changeset version && pnpm -r build && pnpm changeset publish
```

---

## Mathematical Notes (Complexity & Throughput)

We analyze ingestion with batch size \$b\$, items \$n\$, per-item cost \$c\$, and parallelism \$p\$.

* **Time complexity:** $T(n) = O\bigg(\frac{n}{p}\log n\bigg)$
* **Throughput:** $\text{QPS} = \frac{p\cdot b}{\text{latency}_{\text{batch}}}$
* **Backpressure threshold (inline):** $q_{max} = \lambda \cdot \Delta t$

---

## Operational Runbook (Excerpt)

* Health checks: `/live`, `/ready`
* SLOs: Availability 99.9%, P95 latency ≤ 250ms
* Rollbacks: Blue/Green with DB schema guards

> Tip: Tag incidents with `component:` and `severity:` labels.

---

## Styling with Directives

This deck uses:

* `theme: fintech-docs` (custom CSS via `@theme`)
* `paginate: true` with footer `Page $[page]/$[total]`
* Slide class directives: `<!-- _class: lead -->`, `white-text`
* Background image via `![bg](...)`
* `math: true` for formulas

---

## Appendix — CLI Cheatsheet

```bash
# Watch mode for local preview
npx marp slides.md --server

# Export to PPTX
npx marp slides.md --pptx -o slides.pptx

# Use custom theme from this file
npx marp slides.md --theme-set slides.md -o docs.html
```

---

# Thank You

Questions? **[22f1001636@ds.study.iitm.ac.in](mailto:22f1001636@ds.study.iitm.ac.in)**
