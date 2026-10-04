---
title: "Democratizing Data Analytics in Education: A Governance Strategy for Non-Profit Educational Organizations"
collection: publications
category: conferences
permalink: /publication/2025-11-26-democratizing-data-analytics-in-education
excerpt: 'Case study of a data engineering and governance framework for Fundación Ayudinga: a cloud-based Dremio Lakehouse plus a formal governance program (roles, semantic layers, six policies) that raised the organization''s TDWI data-literacy maturity from Basic (Stage 3) to Literate (Stage 4).'
date: 2025-11-26
venue: '2025 IEEE 43rd Central America and Panama Convention (CONCAPAN XLIII)'
paperurl: 'https://doi.org/10.1109/concapan66820.2025.11512483'
citation: 'Verbel, G., González, K., Muñoz, A. C., López, V., &amp; Sánchez-Galán, J. E. (2025). &quot;Democratizing Data Analytics in Education: A Governance Strategy for Non-Profit Educational Organizations.&quot; <i>2025 IEEE 43rd Central America and Panama Convention (CONCAPAN XLIII)</i>. https://doi.org/10.1109/concapan66820.2025.11512483'
---

**Authors:** Gabriel Verbel, **Kevin González**, Ana Cecilia Muñoz, Víctor López, Javier E. Sánchez-Galán<br/>
**Venue:** 2025 IEEE 43rd Central America and Panama Convention (CONCAPAN XLIII)<br/>
**DOI:** [10.1109/concapan66820.2025.11512483](https://doi.org/10.1109/concapan66820.2025.11512483) (IEEE Xplore)<br/>
**Keywords:** data governance, data literacy, data lakehouse, non-profit organizations, TDWI assessment

## Summary

Becoming a data-driven organization is hard for non-profits, which often have limited resources and gaps in technical expertise. This paper is a case study of how we built a data engineering and governance framework for **Fundación Ayudinga**, a nonprofit e-learning organization in Panama whose data was spread across many platforms and formats. That fragmentation made it hard to measure educational impact and to base decisions on evidence.

We measured the organization's data-literacy maturity with the **TDWI Data Literacy Maturity Assessment** before and after the work. Overall maturity rose from **Stage 3 (Basic)** to **Stage 4 (Literate)**.

## Methodology

The implementation ran in three phases:

1. **Initial maturity assessment.** We applied the TDWI assessment across five dimensions: culture and resources, data infrastructure, skills and talent, tools, and data governance and processes.
2. **Data architecture.** We designed and deployed a cloud **Lakehouse** with three tiers: data producers, warehouse and data consumers. Its requirements included a central repository, ETL/ELT pipelines, orchestration, data documentation, semantic layers and environments for exploring data.
3. **Formal governance strategy.** We wrote policies for data quality, privacy and security, defined roles and responsibilities, and set up processes for monitoring data quality on an ongoing basis.

### Technology stack

| Component | Technology |
|---|---|
| Lakehouse engine | Dremio |
| Orchestration | Kubernetes |
| Containerization | Docker |
| Infrastructure | Cloud-based deployment |
| Data sources | PostgreSQL |

Virtual datasets are organized into **five semantic layers**: Staging → Features → Master Tables → Results → Business Intelligence.

### Governance framework

* **Data structure** at three levels: *attribute* (column), *source* (table) and *domain* (business theme).
* **Four roles:** Head of Data Governance, Data Owner, Data Steward and Data Worker. Each role has its own create, read, update and delete permissions on each semantic layer.
* **Six initial policies:**
  * naming conventions
  * minimum documentation for each domain, source and attribute
  * management of the data glossary
  * access permissions
  * data-quality metrics (record counts, nulls per column, unique fields)
  * a 7-step process for adding new data sources, from request to production

## Results

| TDWI dimension | Initial stage | Final stage |
|---|:---:|:---:|
| Culture and Resources | 3 | 3 |
| Data Infrastructure | 2 | **4** |
| Skills and Talent | 4 | 4 |
| Tools | 2 | **4** |
| Data Governance | 2 | **4** |
| **Overall** | **3 (Basic)** | **4 (Literate)** |

The three dimensions the project targeted (infrastructure, tools and governance) each rose by two stages. *Culture and Resources* stayed at Basic, as expected. Changing culture takes long-term leadership and sustained investment, and a dedicated data role such as a Chief Data Officer, beyond any technical implementation. The paper's main lesson is that **technology enables a data culture, but building one is a separate effort that has to run in parallel.**

## Why it matters

The paper offers a framework that other non-profit educational organizations can adapt, and it shows that the TDWI model works both to diagnose a starting point and to evaluate the result. Next steps include bringing in unstructured data sources, strengthening the policies, and applying more TDWI assessments (data management, analytics and data strategy maturity).

**Related project:** [Data Governance and Learning Platform at Fundación Ayudinga](/projects/ayudinga-data-platform/)

## BibTeX

```bibtex
@inproceedings{verbel2025democratizing,
  title     = {Democratizing Data Analytics in Education: A Governance Strategy for Non-Profit Educational Organizations},
  author    = {Verbel, Gabriel and Gonz{\'a}lez, Kevin and Mu{\~n}oz, Ana Cecilia and L{\'o}pez, V{\'i}ctor and S{\'a}nchez-Gal{\'a}n, Javier E.},
  booktitle = {2025 IEEE 43rd Central America and Panama Convention (CONCAPAN XLIII)},
  year      = {2025},
  publisher = {IEEE},
  doi       = {10.1109/CONCAPAN66820.2025.11512483}
}
```
