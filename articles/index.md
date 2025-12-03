---
layout: default
title: "Article Index"
---

<section class="articles-index">
  <h2>Articles</h2>
  <p class="articles-intro">
    [This content AI-generated filler text]
    The five essays in this zine each focus on a single protest poster—either the
    historical <em>Happiness Club</em> poster or the contemporary <em>Quotes</em> poster—and
    use them to reflect on the inheritance of protest, state power, and resistance.
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
