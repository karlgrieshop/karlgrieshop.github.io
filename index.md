---
title: Grieshop Lab
nav:
  order: 1
  tooltip: Home
---

We study the evolutionary causes and consequences of genetic variation underlying fitness trade-offs between sexes, traits, tissues, life-stages, and environments.

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
  aspect-ratio: 4/3;
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
.news-scroll {
  display: flex;
  overflow-x: auto;
  gap: 1.5rem;
  padding: 1rem 0;
  margin: 2rem 0;
  scroll-snap-type: x mandatory;
}
.news-scroll > div {
  flex: 0 0 320px;
  min-width: 0;
  scroll-snap-align: start;
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

<!-- News scroll section -->
<div>
  <h2 style="margin-bottom:0.5em;">News</h2>
  <div class="news-scroll">
    {% for post in site.posts limit:6 %}
      <div>
        {% include post-excerpt.html post=post %}
      </div>
    {% endfor %}
  </div>
</div>

## Research

<img src="../images/wordle+16.png" alt="wordle+16" class="center-image" />

My lab aims to understand the evolutionary causes and consequences of genetic variation underlying fitness trade-offs between sexes, traits, tissues, life-stages and environments. This includes topics such as sexual conflict, antagonistic pleiotropy, fluctuating selection, phenotypic plasticity and local adaptation, which have implications for wildlife conservation, pest management, and genetic disease. We take an interdisciplinary approach, blending lab experiments, statistics, quantitative genetics, bioinformatics, molecular genetics and mathematical modelling to understand these genetic trade-offs in the fruit fly *Drosophila melanogaster*. Similar questions are tackled in other organisms (birds, plants, other arthropods) through various collaborations. [Read more...]({{ '/research/' | relative_url }})
