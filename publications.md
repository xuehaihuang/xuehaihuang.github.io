---
layout: default
title: Publications
description: "Preprints and published papers by Xuehai Huang in finite element methods and numerical analysis."
permalink: /publications/
---

<header class="page-header">
  <div class="container narrow">
    <p class="eyebrow">Publications</p>
    <h1>Preprints and published papers</h1>
    <p class="page-lead">Preprints and formally published work are listed separately. Published entries are maintained from my bibliographic database; academic profiles provide complementary and continuously updated coverage.</p>
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
    {% assign preprints = site.data.publications | where: "status", "Preprint" %}
    {% assign published = site.data.publications | where: "status", "Published" %}

    <section class="publication-group" aria-labelledby="preprints-heading">
      <div class="publication-group-header">
        <div>
          <p class="eyebrow">Working papers</p>
          <h2 id="preprints-heading">Preprints</h2>
        </div>
        <p class="publication-count">{{ preprints.size }} papers</p>
      </div>
      <div class="publication-list publication-list-full">
        {% assign current_year = "" %}
        {% for paper in preprints %}
          {% if paper.year != current_year %}
            {% assign current_year = paper.year %}
            <h3 class="year-heading">{{ current_year }}</h3>
          {% endif %}
          {% include publication.html paper=paper %}
        {% endfor %}
      </div>
    </section>

    <section class="publication-group" aria-labelledby="published-heading">
      <div class="publication-group-header">
        <div>
          <p class="eyebrow">Journal articles and chapters</p>
          <h2 id="published-heading">Published Papers</h2>
        </div>
        <p class="publication-count">{{ published.size }} papers</p>
      </div>
      <div class="publication-list publication-list-full">
        {% assign current_year = "" %}
        {% for paper in published %}
          {% if paper.year != current_year %}
            {% assign current_year = paper.year %}
            <h3 class="year-heading">{{ current_year }}</h3>
          {% endif %}
          {% include publication.html paper=paper %}
        {% endfor %}
      </div>
    </section>

    <p class="source-note">Published entries follow the author-maintained BibTeX library. MathSciNet remains the reference for authoritative bibliographic details; Google Scholar and ResearchGate provide broader and more rapidly updated coverage.</p>
  </div>
</section>
