---
marp: true
math: true
paginate: true
theme: fintech-docs
author: "Technical Writer"
title: "Product Documentation — Platform X"
description: "Maintainable docs deck using Marp (version-controlled, multi-format)."
footer: "Page [$page]/[$total] • [22f1001636@ds.study.iitm.ac.in](mailto:22f1001636@ds.study.iitm.ac.in)"
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

section.white-text { color: white; text-shadow: 0 2px 6px rgba(0,0,0,.35); }
section.narrow ul { max-width: 80%; }
</style>

<!-- _class: lead -->
# Platform X — Product Documentation

Modern, maintainable docs deck powered by **Marp**.

**Contact:** [22f1001636@ds.study.iitm.ac.in](mailto:22f1001636@ds.study.iitm.ac.in)

---

## Table of Contents

1. Introduction  
2. Key Features  
3. Algorithmic Complexity  
4. Visual Design  
5. Code Example

---

## Introduction

Platform X is designed to streamline enterprise workflows.  

**Goals:**  
- Reduce operational costs  
- Increase productivity  
- Enhance decision-making with analytics

---

## Key Features

- **Scalable architecture**
- **Real-time analytics**
- **Secure integrations**
- **User-friendly dashboards**

---

## Algorithmic Complexity

Mathematical example for algorithm cost:

$$
T(n) = 5n^2 + 3n + 2
$$

**Big-O:** \( O(n^2) \)

---

<!-- _backgroundImage: url(https://images.unsplash.com/photo-1508780709619-79562169bc64?auto=format&fit=crop&w=1600&q=80) -->
<!-- _class: white-text -->
# Visual Design

This slide has a background image to emphasize branding and aesthetics.

---

## Code Example

```python
def compound_interest(principal, rate, times, years):
    # Calculate compound interest
    return principal * (1 + rate / times) ** (times * years)

amount = compound_interest(1000, 0.05, 4, 5)
print(f"Final amount: {amount:.2f}")
