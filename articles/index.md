---
layout: default
title: "Article Index"
---

<section class="articles-index">
  <h2>Articles</h2>
  <p class="articles-intro">
    The five essays in this zine each focus on some aspect of the evolving police response to political protests from 1968 to the present day.
  </p>

  <ul class="articles-list">
    {% assign article_pages = site.pages
       | where: "dir", "/articles/"
       | where_exp: "p", "p.name != 'index.md'"
       | sort: "title" %}

    {% for page in article_pages %}
      <li class="articles-list-item">
        <a href="{{ page.url | relative_url }}" class="article-title">{{ page.title }}</a>

        {% if page.poster == "happiness" %}
          <span class="article-poster-tag tag-happiness">Happiness Club</span>
        {% elsif page.poster == "quotes" %}
          <span class="article-poster-tag tag-quotes">Quotes Poster</span>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>
