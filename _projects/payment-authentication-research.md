---
layout: page
title: "The 3DS Oracle: BIN Attack via the Network"
description: Architectural and empirical study showing how browser-mediated EMV 3DS continuation boundaries act as pre-authorization screening oracles (arXiv:2610.32206).
importance: 3
redirect: https://arxiv.org/abs/2610.32206
---

This research paper investigates EMV 3-D Secure (3DS) as a protocol, integration surface, and governance problem:

- **Venue**: [arXiv:2610.32206](https://arxiv.org/abs/2610.32206) (cs.CR).
- **Authors**: Wasif Faisal (Lead Author) and Suprava Saha Dibya.
- **Key Insight**: Client-visible continuation boundaries in browser-mediated 3DS flows can reflect routing and authentication state before financial authorization, functioning as a pre-authorization card-screening oracle.
- **Evaluation**: Empirical tests separated researcher-owned anchor cards from bounded comparison PANs across 6 of 7 tested ACS/card-range cohorts.
- **Remediation**: Recommends consortium-level reforms, including strict minimization of client-visible pre-authorization responses and stronger client authenticity and session binding.
