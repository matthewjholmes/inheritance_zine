---
layout: default
title: "Home"
---

<section class="intro">
  <h3>About this zine</h3>
  <p>
    The Inheritance is the result of a collaboration between nine students at San Francisco State University: five from AFRS 120 (Communicating Realness: Minding the Gap), and four from DES 525 (Graphic Design III: Advanced). The AFRS students crafted the articles and the DES students created the modern protest poster also entitled <em>The Inheritance</em>. Each was inspired by a poster made in 1968 by Dennis Beall called <em>Happiness is a Warm Club</em>, which was created during a period of massive student organizing for programs and policies to better address the needs of students of color at SF State, as well as nation-wide (indeed, world-wide) sense of revolution. These modern pieces comment on what has changed and what has stayed the same in police and government response to current movements for social justice.
  </p>
</section>

<section class="hero">
  <div class="poster-row">
    <div class="poster-text">
      <h3>Happiness is a Warm Club</h3>
      <p>
        This historic poster served as inspiration for this project.
      </p>
      <p class="poster-inline-link">
        <a href="{{ '/posters/happiness-club.html' | relative_url }}">
          Learn more about this item
        </a>
      </p>
    </div>

    <figure class="hero-poster">
      <a href="{{ "/posters/happiness-club.html" | relative_url }}">
        <img class="poster-large"
             src="{{ "/assets/images/posters/happiness-club.jpg" | relative_url }}"
             alt="Happiness Club protest poster">
      </a>
      <figcaption><i>Happiness is a Warm Club</i> Protest Poster</figcaption>
    </figure>
  </div>

  <div class="poster-row">
    <div class="poster-text">
      <h3>The Inheritance</h3>
      <p>
        This modern poster serves as an homage of design themes to <em>Happiness is a Warm Club</em>, while demonstrating the continuing phenomena of police misconduct.
      </p>
      <p class="poster-inline-link">
        <a href="{{ '/posters/inheritance-poster.html' | relative_url }}">
          Learn more about this item
        </a>
      </p>
    </div>

    <figure class="hero-poster">
      <a href="{{ '/posters/inheritance-poster.html' | relative_url }}">
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
