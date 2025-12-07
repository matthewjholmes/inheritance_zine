---
layout: default
title: "Home"
---

<section class="intro">
  <h3>About this zine</h3>
  <p>
    [This content AI generated filler text]:
    Each article in this zine takes one of these posters as its focal point,
    reading it alongside moments of protest and police response.
    Together they trace what we inherit from earlier struggles—
    and what has, and has not, changed.
  </p>
</section>

<section class="hero">
  <div class="poster-row">
    <div class="poster-text">
      <h3>“Happiness is a Warm Club”</h3>
      <p>
        [This content AI generated filler text]:
        A historic protest poster associated with student organizing at San
        Francisco State in the late 1960s. Articles in this zine read it
        alongside the long arc of campus protest and state violence.
      </p>
      <p class="poster-inline-link">
        <a href="{{ '/posters/happiness-club/' | relative_url }}">
          Learn more about this item
        </a>
      </p>
    </div>

    <figure class="hero-poster">
      <a href="{{ "/posters/happiness-club/" | relative_url }}">
        <img class="poster-large"
             src="{{ "/assets/images/posters/happiness-club.jpg" | relative_url }}"
             alt="'Happiness Club' protest poster">
      </a>
      <figcaption><i>Happiness is a Warm Club</i> Protest Poster</figcaption>
    </figure>
  </div>

  <div class="poster-row">
    <div class="poster-text">
      <h3><i>The Inheritance</i></h3>
      <p>
        [This content AI generated filler text]:
        A contemporary poster that reflects present-day student protest and
        debates about policing and campus safety, while echoing earlier
        struggles in form and language.
      </p>
      <p class="poster-inline-link">
        <a href="{{ '/posters/inheritance-poster/' | relative_url }}">
          Learn more about this item
        </a>
      </p>
    </div>

    <figure class="hero-poster">
      <a href="{{ "/posters/quotes/" | relative_url }}">
        <img class="poster-large"
             src="{{ "/assets/images/posters/inheritance-poster.jpg" | relative_url }} "
             alt="Contemporary protest poster (Inheritance)">
      </a>
      <figcaption><i>Inheritance</i> Protest Poster</figcaption>
    </figure>
  </div>
</section>

<section class="article-listing">
  <h3>Articles</h3>
  <ul class="article-list">
    {% assign article_pages = site.pages
       | where: "dir", "/articles/"
       | where_exp: "page", "page.url != '/articles/'"
       | sort: "title" %}

    {% for page in article_pages %}
      <li class="article-list-item">
        <a href="{{ page.url | relative_url }}">{{ page.title }}</a>

        {% if page.contributor %}
          <span class="article-tag">By {{ page.contributor }}</span>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>
