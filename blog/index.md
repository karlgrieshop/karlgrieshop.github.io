---
title: News
nav:
  order: 2
  tooltip: News and announcements
---

# News

Welcome to the Grieshop Lab news feed! Here you'll find updates, announcements, and recent highlights.

---

{% for post in site.posts %}
- [{{ post.title }}]({{ post.url | relative_url }}) <span style="color: #888;">({{ post.date | date: "%Y-%m-%d" }})</span>
{% endfor %}
