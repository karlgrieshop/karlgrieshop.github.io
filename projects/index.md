---
title: Projects
nav:
  order: false
  tooltip: Software, datasets, and more
---

# {% include icon.html icon="fa-solid fa-wrench" %}Projects

<img src="../images/project1.png" alt="Project 1" class="center-image" />

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.

<img src="../images/project2.png" alt="Project 2" class="center-image" />

{% include tags.html tags="publication, resource, website" %}

<img src="../images/project3.png" alt="Project 3" class="center-image" />

{% include search-info.html %}

{% include section.html %}

<img src="../images/project4.png" alt="Project 4" class="center-image" />

## Featured

{% include list.html component="card" data="projects" filter="group == 'featured'" %}

{% include section.html %}

## More

{% include list.html component="card" data="projects" filter="!group" style="small" %}
