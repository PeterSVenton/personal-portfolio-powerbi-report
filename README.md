# Website Analytics Semantic Model (BigQuery → Power BI) 
A showcase analytics model powering [**peterventon.co.uk**](https://www.peterventon.co.uk).

This repository contains the semantic model and Power BI report structure I use to analyse traffic to my portfolio site: **https://www.peterventon.co.uk**.  
It demonstrates my approach to data modelling, metric design, and BI delivery using modern Microsoft tooling.

I've written an article on the full project which you can find [here.](https://www.peterventon.co.uk/work/ga4-bi)

---

## Scope of This Repository

This repository includes:

- The **Power BI semantic model**  
- Reusable **DAX measures**  
- Model metadata, relationships, and conventions  
- The analytical structure behind the report (KPI definitions, tables, layouts)

This repository does **not** contain the upstream ingestion or transformation scripts (GA4 → BigQuery → cleaned event tables).  
Those pipelines run in my private cloud environment due to credential, security, and cost constraints, but the model in this repo is built directly on top of that architecture.

---

## What This Project Demonstrates

Although the ingestion code is not stored here, this repository still showcases the key parts of how I build analytical systems:

- **Star-schema modelling** for GA4-style data  
- **Clear semantic layer design** suitable for enterprise BI  
- **Consistent KPI logic** using well-structured DAX  
- **Governance practices** (naming conventions, calculated tables, metric layering)  
- **Power BI report engineering**, including:
  - Acquisition analysis  
  - Device metrics  
  - Page performance  
  - Engagement and bounce rate logic  
  - Users/sessions/event behaviour metrics

The focus is on solid engineering rather than decorative visuals.

---

## Architecture Overview

This is the pipeline the model is designed to sit on top of:

```text
Google Analytics 4 
      ↓ (export)
BigQuery (raw events)
      ↓ (cleaning & sessionisation)
Cleaned, analytics-ready event tables
      ↓
Microsoft Fabric / Power BI semantic model
      ↓
Reusable DAX measures and time intelligence
      ↓
Analytics report (Acquisition, Devices, Pages)
```

Only the **semantic model and report layer** are included in this repository.

---

## Tech Stack

**Data Source**  
- Google Analytics 4  
- BigQuery export  
- Cleaned session/page/event tables built privately

**Modelling and Transformation (included)**  
- Power BI Desktop  
- Microsoft Fabric semantic layer  
- DAX  

**Dashboard (included)**  
- KPI dashboards and page layouts  
- Standardised visual structure and formatting  
- Consistent design, naming, and metric logic

---

## Purpose of This Project

This project exists to demonstrate:

- How I design **clean, scalable BI models**  
- My approach to **semantic layers, DAX, and metric governance**  
- Practical experience integrating cloud data sources with Power BI  
- My ability to construct a complete analytical workflow from ingestion → model → insights  
- A real example of the engineering behind my portfolio site

This reflects the same methods I use professionally when building long-lasting analytics systems.

---

## Portfolio

The live site and additional context are available at:  
https://www.peterventon.co.uk

---

## Contact
**Peter Venton**  
BI Engineer & Analytics Developer  
peterstevenventon@gmail.com  
https://www.peterventon.co.uk

---

## License
MIT License
