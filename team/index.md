---
title: People
nav:
  order: 3
  tooltip: Meet the team
---

# People

Meet the team!

{% assign members = site.members | sort: "order" %}
{% for member in members %}
## {{ member.name }}

![{{ member.name }}]({{ member.image }}){: style="max-width: 250px;" }

{{ member.bio }}

---
{% endfor %}
