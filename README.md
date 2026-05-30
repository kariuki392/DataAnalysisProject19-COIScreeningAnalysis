# ⚖️ Conflict of Interest Screening & Risk Assessment
## Professional Services Engagements — Independence & Ethics Compliance (Aug–Dec 2025)

![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python) ![Pandas](https://img.shields.io/badge/Pandas-2.0-150458?logo=pandas) ![IESBA](https://img.shields.io/badge/Framework-IESBA_Code_of_Ethics-darkblue) ![PCAOB](https://img.shields.io/badge/Framework-PCAOB_Rule_3520-navy) ![Domain](https://img.shields.io/badge/Domain-Risk_%26_Compliance-critical)

---

> *Conflict of interest screening is the cornerstone of independence compliance in professional services. Every audit, consulting, and advisory engagement must be screened against the firm's existing relationships before work begins — and the analyst conducting that screening is the first line of defence against regulatory breach. This project demonstrates the complete COI screening workflow applied to 36 simulated engagements under the IESBA, IFAC, and PCAOB independence frameworks.*

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Regulatory Framework](#-regulatory-framework)
- [Dataset](#-dataset)
- [Project Structure](#-project-structure)
- [Analysis Sections](#-analysis-sections)
- [Key Risk Findings](#-key-risk-findings)
- [Portfolio Summary](#-portfolio-summary)
- [Tools & Libraries](#-tools--libraries)
- [How to Run](#-how-to-run)

---

## 🎯 Overview

In professional services — audit, consulting, tax advisory, and assurance — independence is not optional. It is a regulatory and ethical obligation that protects the integrity of financial markets, public trust in audited information, and the professional reputation of the firm. Every new client engagement must be screened for conflicts of interest before work begins, and any identified threats must be assessed, documented, and either mitigated through safeguards or escalated for partner-level decision.

This project replicates the **conflict-of-interest screening workflow** used by Big 4 and mid-tier professional services firms in their Risk & Independence functions. For each of 36 simulated client engagements — spanning audit, consulting, and tax advisory across diverse industries — the analysis:

1. **Identifies independence threats** across all five IESBA threat categories
2. **Scores each threat** using a weighted risk engine calibrated to regulatory guidance
3. **Assigns a composite risk rating** (Low / Medium / High / Critical) with documented rationale
4. **Recommends a course of action** — proceed, apply safeguards, senior review, or escalate to Ethics Partner
5. **Tracks operational performance** — days open, SLA compliance, analyst workload, and escalation rates

The output is a **management-ready risk register** and **dashboard suite** that mirrors the deliverables a junior risk analyst would produce for weekly review by the Risk & Independence team.

> ⚠️ *All client names, financial figures, and engagement details are entirely synthetic and created for portfolio demonstration purposes only. No real client information has been used.*

---

## 📐 Regulatory Framework

### IESBA Code of Ethics — Five Threat Categories

| Threat | Section | Description | Scoring Trigger |
|--------|---------|-------------|-----------------|
| **Self-Interest** | S.120 | Financial interest in client outcome | Common ownership; fee dependency > $3M |
| **Self-Review** | S.121 | Evaluating own prior work | Prior non-audit services on current audit client |
| **Advocacy** | S.123 | Promoting client position | Related entity dependency; referral relationship |
| **Familiarity** | S.124 | Too sympathetic due to close relationship | Common director; long association |
| **Intimidation** | S.125 | Deterred from acting objectively | Active litigation with client |

### Additional Standards Applied
- **IFAC Independence Standards** — Cross-border and network firm considerations
- **PCAOB Rule 3520** — Auditor independence for SEC-registered public company audits; fee dependency and mandatory partner rotation requirements

---

## 📊 Dataset

All engagement data is **synthetically generated** to simulate a realistic professional services screening portfolio:

| Attribute | Details |
|-----------|---------|
| **Engagements** | 36 simulated client engagements |
| **Engagement Types** | Audit (17) · Consulting (12) · Tax Advisory (7) |
| **Industries** | 20 sectors including Financial Services, Healthcare, Technology, Energy, Real Estate |
| **Revenue Range** | $150,000 – $7,200,000 per engagement |
| **Total Portfolio Revenue** | ~$79M under review |
| **Threat Flags** | 5 binary flags per engagement (IESBA categories) |
| **Screening Period** | August – December 2025 |
| **Target SLA** | 2–5 business days per screening |

---

## 🗂️ Project Structure

```
conflict-of-interest-screening/
│
├── conflict_of_interest_screening.ipynb   # Fully executed analysis notebook
│
├── charts/
│   ├── portfolio_dashboard.png            # Portfolio risk overview
│   ├── threat_analysis.png               # IESBA threat breakdown
│   └── tracking_dashboard.png           # Operational tracking & KPIs
│
└── README.md
```

---

## 🔍 Analysis Sections

### 1️⃣ Engagement Register Generation
Synthetic generation of 36 client engagements with full attributes — client name, industry, engagement type, revenue, five IESBA threat flags, screening date, days open, status, and assigned analyst. Mirrors the intake register maintained in a real Risk & Independence function.

### 2️⃣ IESBA Risk Scoring Engine
A Python-implemented risk scoring engine that applies weighted scores across all five IESBA threat categories. Each threat is scored 0–100 based on flag presence and aggravating factors (revenue thresholds, engagement type, days open). A weighted composite score determines the overall risk rating.

**Scoring weights:**
- Self-Interest: 25% | Self-Review: 25% | Familiarity: 20% | Intimidation: 20% | Advocacy: 10%

### 3️⃣ Portfolio Risk Dashboard
Risk rating distribution across the full portfolio, screening status breakdown, risk by engagement type, total revenue at risk by rating tier, SLA compliance performance, and average risk score by industry sector.

### 4️⃣ Independence Threat Analysis
Average threat score by IESBA category, a threat score heatmap for the top 15 highest-risk engagements, threat flag prevalence across the portfolio, composite risk score distribution with threshold markers, risk rating by threat flag count, and analyst workload by risk rating.

### 5️⃣ Master Screening Register
A formatted, tiered risk register listing all 36 engagements sorted by risk rating — Critical through Low — with engagement ID, client name, industry, composite score, screening status, and recommended action for each engagement.

### 6️⃣ Operational Tracking Dashboard
Days-open distribution by screening status (with SLA threshold), escalation rate by industry, top 10 clients by engagement revenue (colour-coded by risk), cumulative screening volume timeline, analyst performance KPIs (total/cleared/escalated/avg days), and a risk score vs revenue scatter plot.

---

## 💡 Key Risk Findings

### 🚨 Financial Services Concentrates the Highest Portfolio Risk
The Financial Services sector accounts for the majority of Critical and High risk engagements — driven by complex ownership structures, related-entity webs, and fee dependency risk from large audit mandates. The three highest-risk engagements (Goldfield Asset Management, Imperium Banking Corp, Harbourview Capital) are all Financial Services audit clients with revenues above $5M and four or more simultaneous threat flags.

### 🏢 Common Ownership is the Most Prevalent Independence Threat
Common ownership flags appear in **42% of all engagements** — the highest prevalence of any single threat. Under IESBA S.120, any direct financial interest in a client creates a Self-Interest threat that requires documented safeguards or, in serious cases, refusal of the engagement. This prevalence rate signals a need for enhanced ownership research protocols at the intake stage.

### 🔄 Prior Non-Audit Services Trigger the Most Serious Self-Review Risk
Eight audit engagements involve clients where the firm previously provided non-audit services on the subject matter — the most serious Self-Review threat under IESBA S.121. All eight were escalated to Ethics Partner level. This finding reinforces the importance of tracking service history across engagement types in the firm's client relationship management system.

### 💰 59% of Portfolio Revenue is in Critical or High Risk Engagements
Approximately **$47M of the $79M portfolio** sits in Critical or High risk engagements. This concentration creates significant fee dependency risk at the portfolio level — a pattern that would require disclosure and review under IESBA's fee dependency provisions for audit clients.

### ⏱️ SLA Compliance Requires Structural Improvement
Approximately **28% of engagements breached the 5-day SLA target** — predominantly complex cases requiring escalation. The data shows a clear correlation between threat count and days open, confirming that multi-flag engagements need a dedicated fast-track escalation protocol rather than the standard screening workflow.

### 📊 Litigation Flags Trigger the Highest Individual Threat Scores
Active litigation (IESBA S.125 — Intimidation threat) generates the highest single-category threat score (70 points) in the scoring model — reflecting that an adversarial legal relationship with a client fundamentally undermines the objectivity required for professional services work. All five litigation-flagged engagements were escalated.

---

## 📋 Portfolio Summary

| Metric | Value |
|--------|-------|
| Total Engagements Screened | 36 |
| 🔴 Critical Risk | 6 (16.7%) |
| 🟠 High Risk | 8 (22.2%) |
| 🟡 Medium Risk | 9 (25.0%) |
| 🟢 Low Risk | 13 (36.1%) |
| Escalated to Ethics Partner | 12 (33.3%) |
| Cleared Without Conditions | 17 (47.2%) |
| Closed – Declined | 1 (2.8%) |
| SLA Compliance (≤5 days) | ~72% |
| Total Revenue Under Review | ~$79M |
| Revenue in Critical/High Risk | ~$47M (59%) |

---

## 🛠️ Tools & Libraries

| Library | Application |
|---------|------------|
| **Pandas** | Engagement register creation, threat flag processing, risk aggregation |
| **NumPy** | Weighted composite score calculation, synthetic data generation |
| **Matplotlib / Seaborn** | 18+ visualisations across 3 dashboards — bar charts, heatmaps, boxplots, scatter plots, pie charts |
| **Python (native)** | IESBA risk scoring engine, risk rating logic, recommended action engine |

---

## ▶️ How to Run

1. Clone the repository and navigate to the project folder
2. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn
```
3. Open and run the notebook — no external data file required (all data is generated internally):
```bash
jupyter notebook conflict_of_interest_screening.ipynb
```

> ✅ All cells are pre-executed with embedded outputs. The full register, dashboards, and risk summaries are visible without re-running.

---

## 📌 About This Project

This project was developed to demonstrate applied knowledge of professional services independence compliance — the workflow, the regulatory framework, and the analytical tools that a junior risk analyst would use in a Big 4 or mid-tier firm's Risk & Independence function. It bridges data analytics with professional ethics and compliance — a combination that is rare and highly valued in firms where independence breaches carry regulatory, reputational, and financial consequences.

Skills demonstrated:
- Applied knowledge of IESBA, IFAC, and PCAOB independence standards
- Structured risk scoring and rating methodology
- Professional documentation and risk register management
- SLA tracking and operational performance monitoring
- Management-ready dashboard design

---

*Part of a 20-project data analytics portfolio spanning HR analytics, financial forecasting, NLP, e-commerce, supply chain intelligence, public health, real estate prediction, credit risk modelling, aviation operations, media analytics, cybersecurity, clinical healthcare, urban analytics, and professional services risk & compliance.*
