---
title: Grieshop Lab
nav:
  order: 1
  tooltip: Home
---

<div class="homepage-container">
  <div class="homepage-main">

We study the evolutionary causes and consequences of genetic variation underlying fitness trade-offs between sexes, traits, tissues, life-stages, and environments.

---

<style>
.image-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
  width: 100%;
  max-width: 1200px;
  margin: 2rem auto;
}
.image-grid .img-tile {
  aspect-ratio: 4/3; /* or 1/1 for square, or adjust as needed */
  width: 100%;
  overflow: hidden;
  border-radius: 8px;
  background: #eee;
  display: flex;
  align-items: center;
  justify-content: center;
}
.image-grid img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}
@media (max-width: 700px) {
  .image-grid {
    grid-template-columns: 1fr;
  }
}
</style>

<div class="image-grid">
  <div class="img-tile">
    <img src="/images/Tania+equations.jpg" alt="Tania quantitative genetics equations">
  </div>
  <div class="img-tile">
    <img src="/images/IMG_0793.jpeg" alt="Mating cage">
  </div>
  <div class="img-tile">
    <img src="/images/Pure+DsRed+Ex.jpg" alt="Large genetic cross">
  </div>
  <div class="img-tile">
    <img src="/images/IMG_0795.jpeg" alt="Mating cages">
  </div>
</div>

---

## Research

<img src="../images/wordle+16.png" alt="wordle+16" class="center-image" />

My lab aims to understand the evolutionary causes and consequences of genetic variation underlying fitness trade-offs between sexes, traits, tissues, life-stages and environments. This includes topics such as sexual conflict, antagonistic pleiotropy, fluctuating selection, phenotypic plasticity and local adaptation, which have implications for wildlife conservation, pest management, and genetic disease. We take an interdisciplinary approach, blending lab experiments, statistics, quantitative genetics, bioinformatics, molecular genetics and mathematical modelling to understand these genetic trade-offs in the fruit fly *Drosophila melanogaster*. Similar questions are tackled in other organisms (birds, plants, other arthropods) through various collaborations. [Read more...]({{ '/research/' | relative_url }})

  </div>
  <aside class="homepage-news-sidebar">
    <h2>Latest News</h2>
    {% for post in site.posts limit:3 %}
      {% include post-excerpt.html post=post %}
    {% endfor %}
  </aside>
</div>



