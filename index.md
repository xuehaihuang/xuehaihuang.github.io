---
layout: default
title: Home
description: "Xuehai Huang is Professor of Mathematics at Shanghai University of Finance and Economics, working on finite element methods and numerical PDEs."
permalink: /
---

<section class="hero">
  <div class="container hero-grid">
    <div class="hero-copy">
      <p class="eyebrow">Professor of Mathematics</p>
      <h1>Xuehai Huang <span>黄学海</span></h1>
      <p class="affiliation">School of Mathematics<br>Shanghai University of Finance and Economics</p>
      <p class="hero-summary">I work on finite element methods and numerical methods for partial differential equations, with particular interests in finite element complexes, tensor finite elements, mixed and nonconforming methods, and structure-preserving discretizations.</p>
      <div class="button-row">
        <a class="button button-primary" href="mailto:huang.xuehai@sufe.edu.cn">Email</a>
        <a class="button" href="{{ '/cv/' | relative_url }}">CV</a>
        <a class="button" href="{{ site.social.scholar }}">Google Scholar</a>
        <a class="button" href="{{ site.social.mathscinet }}">MathSciNet</a>
      </div>
    </div>
    <div class="hero-art" aria-hidden="true">
      <img src="{{ '/assets/images/complex.svg' | relative_url }}" alt="">
      <p>geometry · complexes · computation</p>
    </div>
  </div>
</section>

<section class="section">
  <div class="container">
    <div class="section-heading">
      <div><p class="eyebrow">Research</p><h2>Structure-aware finite element methods</h2></div>
      <a class="text-link" href="{{ '/research/' | relative_url }}">Explore research →</a>
    </div>
    <div class="interest-grid">
      <article><span>01</span><h3>Finite Element Complexes</h3><p>de Rham, elasticity, Hessian, div-div, Stokes, and conformal complexes.</p></article>
      <article><span>02</span><h3>Tensor Finite Elements</h3><p>Symmetric and traceless tensors, tangential-normal and normal-normal continuity.</p></article>
      <article><span>03</span><h3>Mixed & Nonconforming Methods</h3><p>Stable discretizations, virtual elements, hybridization, and staggered DG methods.</p></article>
      <article><span>04</span><h3>Numerical PDEs</h3><p>Elasticity, Stokes systems, singular perturbations, and higher-order equations.</p></article>
    </div>
  </div>
</section>

<section class="section section-tinted">
  <div class="container">
    <div class="section-heading">
      <div><p class="eyebrow">Selected work</p><h2>Publications</h2></div>
      <a class="text-link" href="{{ '/publications/' | relative_url }}">View publications →</a>
    </div>
    <div class="publication-list">
      {% assign selected = site.data.publications | where: 'selected', true %}
      {% for paper in selected limit: 7 %}{% include publication.html paper=paper compact=true %}{% endfor %}
    </div>
  </div>
</section>

<section class="section">
  <div class="container split-section">
    <div><p class="eyebrow">Updates</p><h2>Recent news</h2></div>
    <div class="news-list">
      {% for item in site.data.news %}
      <article><time>{{ item.date }}</time><p>{{ item.text }}</p></article>
      {% endfor %}
    </div>
  </div>
</section>

<section class="contact-band">
  <div class="container contact-grid">
    <div><p class="eyebrow">Contact</p><h2>Research conversations are welcome.</h2></div>
    <div><p>School of Mathematics, Shanghai University of Finance and Economics<br>Shanghai 200433, China</p><a href="mailto:huang.xuehai@sufe.edu.cn">huang.xuehai@sufe.edu.cn</a></div>
  </div>
</section>
