---
layout: page
permalink: /repositories/
title: Repositories
nav: true
nav_order: 4
---

{% if site.data.repositories.github_users %}

## GitHub User Profile

<div>
  {% for user in site.data.repositories.github_users %}
    <a href="https://github.com/{{ user }}">{{ user }}</a><br>
  {% endfor %}
</div>

{% endif %}

---

{% if site.data.repositories.github_repos %}

## GitHub Repositories

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% for repo in site.data.repositories.github_repos %}
    {% include repository/repo.liquid repository=repo %}
  {% endfor %}
</div>

{% endif %}
