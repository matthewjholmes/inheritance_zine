---
layout: default
title: "Contributors"
---

<section class="contributors-index">
  <h2>Contributors</h2>
  <p class="contributors-intro">
    The essays in this zine were written by students in Africana Studies,
    reflecting on protest, policing, and inheritance through two protest posters.
  </p>

  <ul class="contributors-list">
    {% assign people = site.pages
       | where: "dir", "/contributors/"
       | where_exp: "p", "p.name != 'index.md'"
       | sort: "title" %}

    {% for person in people %}
      <li class="contributors-list-item">
        <a href="{{ person.url | relative_url }}">{{ person.title }}</a>
        {% if person.role %}
          <span class="contributor-role-inline">{{ person.role }}</span>
        {% endif %}
      </li>
    {% endfor %}
  </ul>
</section>
