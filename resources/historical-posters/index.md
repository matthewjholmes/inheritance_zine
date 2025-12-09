---
layout: default
title: "Historical Posters"
---

<section class="historical-posters-index">
  <h2>Historical Posters</h2>

  <p class="historical-posters-intro">
    Archival posters related to protest movements, student strikes, and political organizing
    from the 1960s and 1970s. These pieces provide additional context for
    <em>Happiness is a Warm Club</em> and the contemporary work in this zine.
  </p>

  <ul class="historical-posters-list">
    {% assign posters = site.pages
       | where: "dir", "/resources/historical-posters/"
       | where_exp: "p", "p.name != 'index.md'"
       | sort: "title" %}

    {% for poster in posters %}
      <li class="historical-posters-item">
        <a href="{{ poster.url | relative_url }}" class="poster-resource-title">
          <strong>{{ poster.title }}</strong>
        </a>

        {% if poster.subtitle %}
          <span class="poster-resource-subtitle">
            {{ poster.subtitle }}
          </span>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>
