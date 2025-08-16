---
marp: true
math: true
paginate: true
theme: fintech-docs
author: "Technical Writer"
title: "Product Documentation — Platform X"
description: "Maintainable docs deck using Marp (version-controlled, multi-format)."
footer: 'Page $[page]/$[total] • [22f1001636@ds.study.iitm.ac.in](mailto:22f1001636@ds.study.iitm.ac.in)'
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

## Introduction

This presentation covers:

- Product overview
- Key features
- API integration
- Security best practices
- Performance benchmarks

---

<!-- _backgroundImage: "https://images.unsplash.com/photo-1554224154-22dec7ec8818" -->
<!-- _class: white-text -->
# Background Image Example

This slide has a full background image for visual impact.

---

## Algorithmic Complexity

Example of a **mathematical equation** in Marp (Big-O notation):

$$
T(n) = O(n \log n)
$$

---

## Sample Code

```python
# Author: Technical Writer
# Contact: 22f1001636@ds.study.iitm.ac.in

def compound_interest(principal, rate, time):
    """Calculate compound interest."""
    return principal * (1 + rate) ** time

print(compound_interest(1000, 0.05, 5))
