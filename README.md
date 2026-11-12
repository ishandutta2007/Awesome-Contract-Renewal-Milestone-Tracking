# Awesome-Contract-Renewal-Milestone-Tracking

# Top Contract Renewal & Milestone Tracking Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Renewal Alerts, Expiration Tracking & Post-Signature Milestone Management*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Contract Renewal & Milestone Tracking**. These tools help teams stay ahead of critical dates—auto-renewals, notice deadlines, price-change windows, and payment milestones—so organizations avoid unwanted rollovers, miss exit windows, or incur penalties from forgotten obligations.

**Examples** include Icertis, ContractSafe, ContractWorks, Gatekeeper, Trackado, CobbleStone, Ironclad, Agiloft, Zylo, and Vendr (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted renewal tracking, open-source deadline extraction, and community-driven obligation monitoring—ideal for teams seeking transparent, vendor-neutral date tracking without per-user SaaS licensing.

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Icertis](https://www.icertis.com/)** | Enterprise CLM with expiration and renewal tracking. Users report being "kept aware of when agreements are reaching their term, and notifications can be sent for renewal so we remain continually covered" [citation:5]. Central repository with searchable contract data and reporting. | Quote-only (enterprise contract) | No free tier; demo via sales |
| **[ContractSafe](https://www.contractsafe.com/)** | Contract repository with AI extraction of parties, dates, and renewal terms. Unlimited reminders and renewal alerts. Three tiers: Organize ($450/mo), Finalize ($660/mo), Maximize ($815/mo) — all include unlimited users [citation:7]. | Organize: **$450/month**; Finalize: $660/month; Maximize: $815/month (final price depends on active contract count) [citation:7] | No free tier; demo via sales |
| **[ContractWorks](https://www.contractworks.com/)** | Contract tracking platform with milestone alerts sent to inbox for renewals and expirations. Custom reporting with scheduled sharing. SOC 2 Type 2 certified. All plans include unlimited users and unlimited training/support [citation:10]. | From **$600/month** (all plans include unlimited users) [citation:10] | **Free trial** available; no permanent free tier |
| **[Gatekeeper](https://www.gatekeeperhq.com/)** | AI-driven contract management with renewal management and workflow automation. Helps identify wasted spend and actively manage renewals. "Keeps customers on track" for realized savings . | From **$775/month**  | No free tier; demo via sales |
| **[Trackado](https://www.trackado.com/)** | Simple, user-friendly contract tracking with alert functions for timing and trigger events (extension, options). Users praise email reminders that "tell me exactly what I need to do to ensure contracts are kept up to date" [citation:6]. | Quote-only; users note it is "reasonably priced" and "doesn't break the bank" [citation:6] | No free tier listed; trial via sales |
| **[CobbleStone](https://www.cobblestonesoftware.com/)** | CLM with automated alerts for renewals, high-risk vendors, and compliance needs. Reporting on key dates and financials. | **$59/user/month** starting (Capterra listing) [citation:11] | No free tier; demo via sales |
| **[Ironclad](https://ironcladapp.com/)** | CLM with renewal tracking and a **Renewal Agent** that generates renewal briefs automatically. Covers creation through storage and renewal on one platform [citation:8]. | Quote-only; **no free trial, no self-serve plan** [citation:8] | No free tier; demo via sales |
| **[Agiloft](https://www.agiloft.com/)** | CLM with real-time dashboards and automation from request through renewal. AI-based contract extraction and e-signature support [citation:9]. | Quote-only (paid only) [citation:9] | No free tier; demo via sales |
| **[Zylo](https://zylo.com/)** | SaaS management platform with **Contract Center** for renewal tracking. Organizations average **211 SaaS renewals per year** (~one per business day). Recommends starting renewal prep 60–90 days in advance. Tracks total contract value, license counts, and utilization [citation:14]. | Quote-only (SaaS management subscription) | No free tier; demo via sales |
| **[Vendr](https://www.vendr.com/)** | SaaS buying platform with renewal pricing intelligence. Data shows annual price increases at renewal typically **3–7%** unless locked in upfront. Multi-year renewal commitments unlock **10–20% lower annual pricing** [citation:13]. | Quote-only (buying platform subscription) | No free tier; demo via sales |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[amagi-contract-deadlines](https://pypi.org/project/amagi-contract-deadlines/)** | — | **The most purpose-built open-source contract deadline tracker in this list.** Extracts dated events from PDF/DOCX/TXT contracts: notice deadlines, option exercise windows, price-change deadlines, and auto-renewal dates. Every computed date shows its arithmetic with source clause citation. Handles tricky clauses: "five years from March 1" (computes end date), "not more than twelve months and not less than nine months prior" (computes both window edges), and rolls forward auto-renewals past already-missed cancel-by dates. Outputs ICS calendar and CSV [citation:4]. |
| **[dsh-contract-renewal](https://github.com/PerryLink/dsh-contract-renewal)** | [![Stars](https://img.shields.io/github/stars/PerryLink/dsh-contract-renewal?style=social&color=white)](https://github.com/PerryLink/dsh-contract-renewal/stargazers) | Registry-based renewal tracker (TypeScript). Ingests contract rows (contract_no, counterparty, dates, renewal_window_days, owner, amount). Computes mutually exclusive groups: **expired**, **in_renewal_window** (0 ≤ days_left ≤ window), and **expiring_soon** (within N days, not yet in window). Date math uses UTC calendar days. Exports CSV with SHA256 verification. Explicitly scoped: does **not** parse contract PDFs or decide whether to renew [citation:3]. |
| **[Hearth](https://hub.docker.com/r/jaysbeekay/hearth)** | — | Self-hosted household contract tracker with **renewal and expiry tracking**. SQLite-backed, single long-lived container. Auto-extracts dates, amounts, and provider details from uploaded PDFs/photos (pdftotext + tesseract, optional Ollama fallback). Exposes read-only MCP server so local LLMs can answer "what's renewing this month?" via `upcoming_renewals` tool. Designed for households, but architecture is adaptable [citation:2]. |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Aakd](https://github.com/aaked-app/aakd)** | [![Stars](https://img.shields.io/github/stars/aaked-app/aakd?style=social&color=white)](https://github.com/aaked-app/aakd/stargazers) | Open-source contract operations workspace with **obligation and renewal views, owners, deadlines, and audit history**. Source-linked facts with page-level evidence. Not a dedicated deadline calculator, but structured obligation data can feed reminder workflows. AGPL-3.0, Docker Compose deployment. |

**Frameworks for building custom systems**: The open-source path is genuinely functional here. **amagi-contract-deadlines** does the hard part—parsing clause language and computing derived dates with citations. **dsh-contract-renewal** provides the registry and grouping logic for "what's expiring soon vs. what's in the renewal window." Combine them: run amagi on your contract PDFs to generate an ICS/CSV, then ingest the dates into dsh-contract-renewal for tracking. Hearth offers a reference architecture for self-hosted tracking with LLM query access.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Renewal tracking involves legally critical dates; a missed notice window can lock an organization into another year of unfavorable terms or trigger penalties. Validate computed dates against source contracts before relying on any tool.
- **Pricing is opaque for most enterprise platforms.** ContractSafe ($450/mo), ContractWorks ($600/mo), Gatekeeper ($775/mo), and CobbleStone ($59/user/mo) publish entry points. Icertis, Ironclad, Agiloft, Zylo, and Vendr are quote-only. Ironclad explicitly offers **no free trial and no self-serve plan** [citation:8]. Open-source tools like **amagi-contract-deadlines** and **dsh-contract-renewal** provide genuine deadline computation and tracking logic, but require technical setup and do not replace legal review of renewal decisions.

---

**Made for contract administrators, legal ops teams, procurement managers, and developers building obligation tracking infrastructure.**  
Let's make contract renewal tracking more open, precise, and deadline-safe.
