---
layout: default
title: Publications
description: "Selected and recent publications by Xuehai Huang in finite element methods and numerical analysis."
permalink: /publications/
---

<header class="page-header">
  <div class="container narrow">
    <p class="eyebrow">Publications</p>
    <h1>Selected and recent work</h1>
    <p class="page-lead">Formal publication data is checked against journal records and MathSciNet. For the most complete and continuously updated lists, use the academic-profile links below.</p>
    <div class="button-row">
      <a class="button button-primary" href="{{ site.social.mathscinet }}">MathSciNet</a>
      <a class="button" href="{{ site.social.scholar }}">Google Scholar</a>
      <a class="button" href="{{ site.social.researchgate }}">ResearchGate</a>
      <a class="button" href="{{ site.social.orcid }}">ORCID</a>
    </div>
  </div>
</header>

<section class="section">
  <div class="container">
    <div class="publication-list publication-list-full">
      {% assign current_year = "" %}
      {% for paper in site.data.publications %}
        {% if paper.year != current_year %}
          {% assign current_year = paper.year %}
          <h2 class="year-heading">{{ current_year }}</h2>
        {% endif %}
        {% include publication.html paper=paper %}
      {% endfor %}
    </div>
    <p class="source-note">This curated page emphasizes current and representative work. MathSciNet is the reference source for authoritative bibliographic details; Google Scholar and ResearchGate provide broader and more rapidly updated coverage.</p>
  </div>
</section>
