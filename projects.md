---
layout: default
title: Projects
permalink: "/projects/"
description: Companies, applications, and experiments by Tanaka Mawere.
---
<div class="projects-journal site-shell">
  <header class="projects-intro">
    <p class="eyebrow"><span class="hello-dot"></span> Ideas, turned into things</p>
    <h1>A little curiosity.<br>A lot of <em>building.</em><span class="sunburst" aria-hidden="true">✳</span></h1>
    <p>Companies, apps, and experiments. Some out in the world, some still taking shape. Here’s what I’ve been working on.</p>
    <span class="photo-scribble" aria-hidden="true">from “what if” to “it works” ↴</span>
  </header>

  {% assign company = site.projects | where: 'featured', true | first %}
  {% if company %}
  <section class="company-feature" aria-labelledby="company-title">
    <div class="company-story">
      <p class="eyebrow">The company behind the apps</p>
      <h2 id="company-title">{{ company.title }}<span>.</span></h2>
      <p>{{ company.description }}</p>
      <a class="journal-button" href="{{ company.address }}" target="_blank" rel="noopener noreferrer">Explore Alcanzar <span aria-hidden="true">↗</span><span class="visually-hidden"> (opens in a new tab)</span></a>
      <a class="journal-text-link" href="{{ company.url | relative_url }}">More about the company <span aria-hidden="true">→</span></a>
    </div>
    <div class="company-products"><p class="eyebrow">Four applications. One home.</p>
      <div class="company-product-grid">
        <div><span class="product-index">01 / COMMERCE</span><h3>Auctions</h3><p>Buying, selling, and the next bid.</p></div>
        <div><span class="product-index">02 / HEALTHCARE</span><h3>Clinic management</h3><p>Patient care meets everyday operations.</p></div>
        <div><span class="product-index">03 / E-COMMERCE</span><h3>Marketplace</h3><p>Connecting buyers and sellers.</p></div>
        <div><span class="product-index">04 / EDUCATION</span><h3>School management</h3><p>Bringing school life into one system.</p></div>
      </div>
    </div>
  </section>
  {% endif %}

  {% assign independent_projects = site.projects | where_exp: 'project', 'project.company == nil' | where_exp: 'project', 'project.featured != true' %}
  {% assign categories = independent_projects | map: 'category' | uniq | sort %}
  {% for category in categories %}
  <section class="project-group" aria-labelledby="group-{{ forloop.index }}">
    <div class="section-heading"><div><p class="eyebrow">{% if category == 'Work' %}Built with others{% else %}Following the curiosity{% endif %}</p><h2 id="group-{{ forloop.index }}">{% if category == 'Work' %}Work & <em>collaborations.</em>{% else %}Apps & <em>experiments.</em>{% endif %}</h2></div><span class="photo-scribble" aria-hidden="true">{% if category == 'Work' %}good things take a team{% else %}a few more tabs open{% endif %}</span></div>
    <div class="portfolio-grid">
      {% for project in independent_projects %}
        {% if project.category == category %}{% include projects-control.html %}{% endif %}
      {% endfor %}
    </div>
  </section>
  {% endfor %}
  <section class="projects-contact"><div><p class="eyebrow">The next idea could be yours</p><h2>Something worth <em>building?</em></h2></div><a class="journal-button" href="mailto:{{ site.author.email }}">Let’s talk <span aria-hidden="true">↗</span></a></section>
</div>
