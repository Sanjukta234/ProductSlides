---
marp: true
math: true
paginate: true
theme: fintech-docs
author: "Technical Writer"
title: "Product Documentation — Platform X"
description: "Maintainable docs deck using Marp (version-controlled, multi-format)."
footer: "Page $\[page]/$\[total] • [22f1001636@ds.study.iitm.ac.in](mailto:22f1001636@ds.study.iitm.ac.in)"
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

<!-- _backgroundImage: url('https://images.unsplash.com/photo-1521790797524-b2497295b8a0') -->
<!-- _backgroundSize: cover -->
<!-- _class: white-text -->

# Vision & Strategy

Our platform empowers businesses with **real-time analytics** and **AI-driven insights**.  
We focus on scalability, security, and seamless integration.

---

## Algorithmic Complexity

We often analyze performance using Big-O notation:

$$
T(n) = O(n \log n)
$$

Example: Merge sort has complexity **O(n log n)** due to the divide-and-conquer approach.

---

## Code Example

```python
def compound_interest(principal, rate, time):
    return principal * (1 + rate) ** time

print(compound_interest(1000, 0.05, 10))
