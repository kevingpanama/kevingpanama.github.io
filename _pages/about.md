---
permalink: /
title: "Kevin González Ortega"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

I am a **data scientist** and Systems and Computing Engineer working on **psychometrics, educational measurement, and machine learning and AI evaluation**. I am a **Fulbright Scholar** in the M.S.Ed. program in Qualitative and Quantitative Research Methodology at **Indiana University Bloomington**.

For ten years I have built data and learning systems at [Fundación Ayudinga](https://ayudinga.org), a nonprofit e-learning foundation in Panama, where I am Director of Technology and Educational Research. I direct an R&D portfolio of 10+ projects in machine learning, knowledge management and gamification for education, and I designed the foundation's data governance strategy and cloud infrastructure. My goal is to build and evaluate models and assessments that are **valid, reliable and fair**.

I am a member of the **American Educational Research Association (AERA)**, the **National Council on Measurement in Education (NCME)**, IEEE, ACM and PMI.

[Download CV (PDF)](/files/Kevin_Gonzalez_Ortega_CV.pdf){: .btn .btn--primary} [Google Scholar]({{ site.author.googlescholar }}){: .btn .btn--info} [ORCID]({{ site.author.orcid }}){: .btn .btn--info}

## Research interests

* **Data Science:** statistical and machine learning modeling, multivariate statistics, missing data, data governance, and learning analytics in education
* **Psychometrics:** educational and psychological measurement, assessment design, and evidence for reliability, validity and fairness
* **AI Evaluation:** applying measurement principles to evaluate machine learning models and large language models (LLMs) so their results are valid, reliable and fair

## Selected publications

{% assign pubs = site.publications | sort: "date" | reverse %}
{% for post in pubs limit: 3 %}
* [{{ post.title }}]({{ post.url }}) — *{{ post.venue }}*, {{ post.date | date: "%Y" }}{% if post.language %} · **In {{ post.language }}**{% endif %}{% if post.paperurl %} · [Link]({{ post.paperurl }}){% endif %}
{% endfor %}

[All publications →](/publications/)

## Featured projects

{% assign projects = site.portfolio | sort: "order" %}
{% for post in projects limit: 3 %}
* **[{{ post.title }}]({{ post.url }})** — {{ post.excerpt | split: "<br/>" | first | strip_html | strip }}
{% endfor %}

[All projects →](/projects/)

## News

* **Fall 2026:** Taking Educational Assessment and Psychological Measurement, Machine Learning Methods for Education and Social Science, and Applied Missing Data Analysis at IU Bloomington.
* **Nov 2025:** Paper on data governance for non-profit educational organizations published in the proceedings of [IEEE CONCAPAN XLIII](https://doi.org/10.1109/concapan66820.2025.11512483).
* **Oct 2025:** Joined IEEE as a member.
* **Aug 2025:** Started the M.S.Ed. at Indiana University Bloomington as a Fulbright Scholar.
* **Jan 2025:** Began the Fulbright Pre-Academic English Program at the University of North Texas.
