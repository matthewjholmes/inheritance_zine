---
layout: default
title: "Home"
---

<section class="hero">
  <div class="hero-text">
    <h2>The Inheritance</h2>
    <p>
      An online zine exploring the misuse of force by police against protesters
      from the 1960s to the 2020s, with a focus on San Francisco State.
    </p>
  </div>

  <div class="hero-posters">
    <figure class="hero-poster">
      <a href="/assets/images/posters/happiness-club.jpg" target="_blank">
        <img class="poster-large"
             src="/assets/images/posters/happiness-club.jpg"
             alt="'Happiness Club' protest poster">
      </a>
      <figcaption>“Happiness Club” protest poster</figcaption>
    </figure>

    <figure class="hero-poster">
      <a href="/assets/images/posters/quotes_0.jpg" target="_blank">
        <img class="poster-large"
             src="/assets/images/posters/quotes_0.jpg"
             alt="Modern protest poster (Quotes)">
      </a>
      <figcaption>Modern protest poster (Quotes)</figcaption>
    </figure>
  </div>
</section>

<section class="intro">
  <h3>About this zine</h3>
  <p>
    Each article in this zine takes one of these posters as its focal point,
    reading it alongside moments of protest and police response.
    Together they trace what we inherit from earlier struggles—
    and what has, and has not, changed.
  </p>
</section>

<section class="article-listing">
  <h3>Read</h3>
  <ul class="article-list">
    {% assign article_pages = site.pages
       | where: "dir", "/articles/"
       | sort: "title" %}

    {% for page in article_pages %}
      <li class="article-list-item">
        <a href="{{ page.url | relative_url }}">{{ page.title }}</a>

        {% if page.poster == "happiness" %}
          <span class="article-tag">Happiness Club</span>
        {% elsif page.poster == "quotes" %}
          <span class="article-tag">Quotes poster</span>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>
