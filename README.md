# AI & Data Product Portfolio
### Rahul Reddy Puchakayala

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-3fb950?style=flat-square&logo=github)]((https://rahulreddyutd.github.io/capitalone-pm-portfolio/))
[![Claude API](https://img.shields.io/badge/Powered%20By-Claude%20API-orange?style=flat-square)](https://anthropic.com)

> Three end-to-end AI & data systems built for the Capital One MarTech role. Every algorithm runs live in the browser — K-Means++ clustering, cosine similarity NBA recommendations, Bayesian A/B testing, ETL pipelines, and real-time Z-test statistics. Powered by the Claude API for live AI analysis.

---

## 🔗 Live Demo

**[→ Open Portfolio](https://rahulreddyutd.github.io/capitalone-pm-portfolio/)**

---

## What's Inside

| Project | What It Does | Key Algorithms |
|---|---|---|
| **01 · AI Personalization Engine** | Clusters customers → recommends next-best-action → A/B tests the result | K-Means++, Cosine Similarity, Beta-Binomial, Z-Test |
| **02 · Customer 360 Data Platform** | ETL across 4 sources → identity resolution → unified profiles → correlation matrix | Pearson r, Probabilistic matching, LTV/Churn feature engineering |
| **03 · Experimentation Platform** | Sample size calculator → live experiment simulation → AI insight report | Cohen's h, Two-sided Z-Test, Normal CDF |

---

## Project 1 — AI Personalization Engine

Paste customer CSV data (spend, frequency, recency, digital score, savings affinity) and the engine:

1. **Clusters** customers using real K-Means++ — centroids seeded via weighted probability distribution, not random
2. **Calls Claude API** to profile each segment with behavioral reasoning based on the actual computed centroids
3. **Recommends** next-best-action per customer using cosine similarity against 6 Capital One product templates
4. **A/B tests** the recommendation with a live Bayesian posterior — drag sliders and watch the Beta distributions update in real time

**The math:**
```
K-Means++ init:   P(x) ∝ D(x)²   (weighted by distance from nearest centroid)
Cosine similarity: cos(A,B) = (A·B) / (‖A‖ · ‖B‖)
Z-test:            z = |p_A - p_B| / SE_pooled,   p = 2·(1 - Φ(z))
Beta posterior:    Beta(α = conversions+1, β = non-conversions+1)
```

---

## Project 2 — Customer 360 Data Platform

A live ETL pipeline with 4 configurable source systems (Transactions, Web Events, CRM, Mobile App):

1. **Ingests** records from each source with different schemas
2. **Resolves identities** probabilistically — models the match rate of a real email+device+phone hash matching system
3. **Engineers features** — LTV score, churn risk (0–1), preferred channel, lifecycle stage — all computed, not sourced
4. **Computes** a real Pearson correlation matrix across all generated profiles
5. **Calls Claude API** to write a live Data Strategy Report based on the actual computed stats

**The math:**
```
LTV = 0.38·spend + 4.8·sessions + 9.5·opens + 95·mobile_score
Churn risk = clamp(1 - (LTV/1500)·noise, 0.02, 0.98)
Pearson r(X,Y) = Σ((xi-x̄)(yi-ȳ)) / (σX · σY · n)
```

---

## Project 3 — Experimentation Platform

A self-serve A/B testing platform with real statistical machinery:

1. **Calculates required sample size** using Cohen's h and the standard power formula — the same formula every stats textbook uses
2. **Launches experiments** with configurable type, baseline rate, MDE, power, and significance level
3. **Simulates daily traffic** with binomial noise — the true effect includes a random multiplier (0.6x–1.4x) because real experiments never hit exactly the planned MDE
4. **Tracks significance** in real time — watch confidence accumulate on the chart day by day
5. **Auto-generates insight report** via Claude API when significance is crossed — definitive SHIP/NO-SHIP with reasoning

**The math:**
```
Cohen's h:    h = |2·arcsin(√p1) - 2·arcsin(√p2)|
Sample size:  n = ((z_α/2 + z_β) / h)²
              z_α/2 = 1.96 (α=0.05),  z_β = 0.842 (80% power)
```
---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla JS, HTML5 Canvas, Chart.js 4.4 |
| AI / LLM | Claude API (`claude-sonnet-4-20250514`) |
| ML Algorithms | K-Means++, Cosine Similarity, Beta PDF (Log-Gamma) |
| Statistics | Cohen's h, Normal CDF (erf / Horner method), Z-Test, Pearson r |
| Data Layer | Procedural customer generation with archetype-based behavioral noise |
| ETL | Multi-source merge, probabilistic identity resolution |
| Deployment | Single HTML file — GitHub Pages, no build step |


---

## Contact

**Rahul Reddy Puchakayala**
- LinkedIn: [linkedin.com/in/YOUR-LINKEDIN](https://www.linkedin.com/in/rahulreddypuchakayala/)
- Email: rahulreddypuch@gmail.com
- Portfolio: [YOUR-USERNAME.github.io/rahul-ai-portfolio](https://rahulreddyutd.github.io/capitalone-pm-portfolio/)
