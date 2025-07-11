---
title: People
nav:
  order: 3
  tooltip: Meet the team
---

# People

<div style="display: flex; flex-wrap: wrap; gap: 2rem; align-items: flex-start; margin-bottom: 2rem;">
  <div style="flex: 1 1 300px;">
    <h2 style="margin-top:0;">Meet the team!</h2>
    <ul style="margin-bottom: 1.5em;">
      {% assign members = site.members | sort: "order" %}
      {% for member in members %}
        <li>
          <a href="#{{ member.name | slugify }}" style="color: inherit; text-decoration: underline;">
            <strong>{{ member.name }}</strong>
          </a>
        </li>
      {% endfor %}
    </ul>
  </div>
</div>

---

{% assign members = site.members | sort: "order" %}
{% for member in members %}
<div id="{{ member.name | slugify }}" style="display: flex; flex-wrap: wrap; gap: 2rem; align-items: flex-start; margin-bottom: 2rem;">
  <img src="{{ member.image }}" alt="{{ member.name }}" style="max-width: 250px; border-radius: 8px; box-shadow: 0 2px 8px #0002;">
  <div style="flex: 1 1 300px;">
    <h3 style="margin-top:0;">{{ member.name }}</h3>
    <p>{{ member.bio | markdownify }}</p>
  </div>
</div>
---
{% endfor %}
