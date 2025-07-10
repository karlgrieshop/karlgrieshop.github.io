---
title: Grieshop Lab
nav:
  order: 1
  tooltip: Home
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
.carousel-container {
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 2rem 0;
  gap: 1rem;
}
.carousel-btn {
  background: #fff;
  border: 2px solid var(--primary, #0795d9);
  color: var(--primary, #0795d9);
  font-size: 1rem;
  padding: 0.25em 0.5em;
  border-radius: 50%;
  cursor: pointer;
  transition: background 0.2s, color 0.2s, border-color 0.2s, box-shadow 0.2s;
  user-select: none;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 2px 8px #0001;
  outline: none;
  width: 1.5em;
  height: 1.5em;
  line-height: 1;
}
.carousel-btn:hover:not(:disabled) {
  background: var(--primary, #0795d9);
  color: #fff;
  border-color: var(--primary, #0795d9);
  box-shadow: 0 4px 12px #0002;
}
.carousel-btn:disabled {
  background: #f5f5f5;
  color: #ccc;
  border-color: #eee;
  cursor: not-allowed;
  opacity: 0.5;
  box-shadow: none;
}
.carousel-scroll {
  display: flex;
  overflow: hidden;
  scroll-behavior: smooth;
  gap: 1.5rem;
  width: 100%;
  max-width: 1000px;
}
.carousel-scroll > div {
  flex: 0 0 320px;
  min-width: 0;
}
</style>

<script>
document.addEventListener("DOMContentLoaded", function() {
  const scrollContainer = document.querySelector('.carousel-scroll');
  const leftBtn = document.querySelector('.carousel-btn.left');
  const rightBtn = document.querySelector('.carousel-btn.right');
  const blogUrl = "{{ '/blog/' | relative_url }}";
  const cardWidth = 320 + 24; // 320px card + 1.5rem gap

  function updateButtons() {
    if (!scrollContainer) return;
    leftBtn.disabled = scrollContainer.scrollLeft <= 0;
    // If at (or past) the end, show link style for right button
    if (scrollContainer.scrollLeft + scrollContainer.offsetWidth >= scrollContainer.scrollWidth - 2) {
      rightBtn.setAttribute('data-end', 'true');
      rightBtn.title = "Go to News page";
    } else {
      rightBtn.removeAttribute('data-end');
      rightBtn.title = "Next";
    }
  }

  leftBtn.addEventListener('click', function() {
    scrollContainer.scrollBy({ left: -cardWidth, behavior: 'smooth' });
    setTimeout(updateButtons, 400);
  });

  rightBtn.addEventListener('click', function() {
    if (rightBtn.getAttribute('data-end') === 'true') {
      window.location.href = blogUrl;
    } else {
      scrollContainer.scrollBy({ left: cardWidth, behavior: 'smooth' });
      setTimeout(updateButtons, 400);
    }
  });

  scrollContainer.addEventListener('scroll', updateButtons);
  updateButtons();
});
</script>

<div class="main-content">
We study the evolutionary causes and consequences of genetic variation underlying fitness trade-offs between sexes, traits, tissues, life-stages, and environments.

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

<!-- Carousel News section -->
<div>
  <h2>
    <a href="{{ '/blog/' | relative_url }}" style="color: inherit; text-decoration: none;">News</a>
  </h2>
  <div class="carousel-container">
    <button class="carousel-btn left" aria-label="Previous news">&#8592;</button>
    <div class="carousel-scroll">
      {% for post in site.posts limit:6 %}
        <div>
          {% include post-excerpt.html post=post %}
        </div>
      {% endfor %}
    </div>
    <button class="carousel-btn right" aria-label="Next news">&#8594;</button>
  </div>
</div>

<h2>
  <a href="{{ '/research/' | relative_url }}" style="color: inherit; text-decoration: none;">Research</a>
</h2>

<img src="../images/Research1.png" alt="laptop logo" class="center-image" />

<p>
My lab aims to understand the evolutionary causes and consequences of genetic variation underlying fitness trade-offs between sexes, traits, tissues, life-stages and environments. This includes topics such as sexual conflict, antagonistic pleiotropy, fluctuating selection, phenotypic plasticity and local adaptation, which have implications for wildlife conservation, pest management, and genetic disease. We take an interdisciplinary approach, blending lab experiments, statistics, quantitative genetics, bioinformatics, molecular genetics and mathematical modelling to understand these genetic trade-offs in the fruit fly <em>Drosophila melanogaster</em>. Similar questions are tackled in other organisms (birds, plants, other arthropods) through various collaborations.
</p>
<p>
  <a href="{{ '/research/' | relative_url }}">Read more...</a>
</p>
</div>
