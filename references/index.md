---
layout: default
title: "References"
---

<section class="references-index">
  <h2>References</h2>

  <p class="references-intro">
    Works cited pages for each article in <em>The Inheritance</em>.
  </p>

  <ul class="references-index-list">
    {%- assign ref_pages = site.pages
         | where: "layout", "reference"
         | sort: "title" -%}

    {%- for ref in ref_pages -%}
      {%- unless ref.url == page.url -%}
        {%- assign related_article = nil -%}
        {%- if ref.for_article_url -%}
          {%- assign candidates = site.pages | where: "url", ref.for_article_url -%}
          {%- assign related_article = candidates | first -%}
        {%- endif -%}

        <li class="references-index-item">
          <a href="{{ ref.url | relative_url }}">
            {{ ref.title }}
          </a>

          {%- if related_article -%}
            <span class="references-index-meta">
              for
              <a href="{{ related_article.url | relative_url }}">
                {{ related_article.title }}
              </a>
            </span>
          {%- endif -%}
        </li>
      {%- endunless -%}
    {%- endfor -%}
  </ul>
</section>
