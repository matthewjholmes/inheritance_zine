---
layout: default
title: "Posters"
---

<section class="posters-index">
  <h2>Posters</h2>
  <p class="posters-intro">
  [This content is AI-generated filler text]:
    These posters anchor the zine. Each one appears in multiple articles, as students
    read them alongside protests, policing, and inheritance across decades.
  </p>

  <ul class="posters-list">
    {% assign posters = site.pages
       | where: "dir", "/posters/"
       | where_exp: "p", "p.name != 'index.md'"
       | sort: "title" %}

    {% for poster in posters %}
      <li class="posters-list-item">
        <a class="poster-title" href="{{ poster.url | relative_url }}">
          {{ poster.title }}
        </a>
        {% if poster.subtitle %}
          <span class="poster-subtitle-inline">{{ poster.subtitle }}</span>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>
