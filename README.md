<p align="center"><img src="assets/banner.svg" alt="Automation Capacity Atlas" width="100%"></p>

<p align="center">
<img src="https://img.shields.io/badge/stack-Apps_Script_·_Webhooks_·_Chrome_extension-14384E?style=flat-square">
<img src="https://img.shields.io/badge/data-fictional-89CDE7?style=flat-square">
<a href="https://sider.ai/agents/web-creator/share/695ea81100a621619985fdfb"><img src="https://img.shields.io/badge/Portfolio-Nae_Kitakado-1D4C93?style=flat-square"></a>
</p>

<p align="center"><a href="https://naekitakadoportfolio.github.io/automation-capacity-atlas/"><img src="https://img.shields.io/badge/%E2%96%B6%20Try%20the%20live%20demo-14384E?style=for-the-badge" alt="Live demo"></a></p>

# Automation Capacity Atlas

Forecasts monthly automation usage, finds the cheapest plan tier that fits, and ranks which rules to migrate off-platform. Change usage, the day of the month and the migration slider to model the renewal decision.

> **Portfolio rebuild.** This is a from-scratch recreation of a production system I designed and run, rebuilt with **fictional data** and no client names, code or branding. The live demo runs entirely in the browser.

## The problem
A large automation add-on (~$900/month) was up for renewal. The platform's usage report only showed month-to-date, support couldn't supply history, and there was no API for automation definitions, so nobody could tell whether a cheaper tier would fit.

## Impact in production
Built an independent usage history, inventoried 338 automation rules (476 actions per pass), and found that the top 14 rules drove ~58% of consumption. That turned a renewal guess into a data-backed downgrade and migration plan.

## What it demonstrates
| Capability | How |
|---|---|
| Usage projection | Month-to-date → full-month forecast |
| Tier fit analysis | Cheapest tier that covers projected volume, with annual savings |
| Scenario modeling | Slider shows the impact of migrating rules off-platform |
| Automation inventory | Rules ranked by consumption, flagged as port candidates |
| Data capture | Webhooks plus a Chrome extension where no API exists |

## Production architecture
Webhooks → Apps Script ingest → Sheets (ACTIVITY, INVENTORY) · Chrome extension scrapes activity log · lazy-loaded Atlas endpoint · HTML dashboard

## Try it
Open the **[live demo](https://naekitakadoportfolio.github.io/automation-capacity-atlas/)** or run `index.html` locally. No install needed.

---
<p align="center"><sub>Built by <b>Nae Kitakado</b>, AI Automation Consultant · <a href="https://www.linkedin.com/in/nae-k-203194265">LinkedIn</a> · <a href="https://sider.ai/agents/web-creator/share/695ea81100a621619985fdfb">Portfolio</a> · open to retainer &amp; part-time consulting</sub></p>
