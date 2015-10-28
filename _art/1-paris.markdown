---
title: Paris
subtitle: Bonjour mon amour...
layout: default
modal-id: Paris
date: 2015-09-08
img: dachacara_poster.png
caption_color: dark
thumbnail: chacara-thumb.svg
alt: Paris
project-date: 2013
client: Da Chácara Santo Antônio
categories: [Desenvolvimento Web, Web Design, Redação para Website, Fotografia de Produtos, Artes Gráficas]
description: Plantas medicinais orgânicas e produtos terapêuticos.
client_url: http://dachacara.com.br
details: Website compatível com dispositivos móveis (celulares e tablets). Integrado ao Google Analytics, Google Maps, Google Business e Facebook.
resources: HTML5 e CSS3. SEO. Google CSE (Custom Search Engine). Responsive website. Accordions, Flex boxes.
---

<div id="carousel-art" class="carousel slide" data-ride="carousel">
  <!-- Indicators -->
  <ol class="carousel-indicators">
    <li data-target="#carousel-art" data-slide-to="0" class="active"></li>
    {% for image in site.data.paris %} 
    <li data-target="#carousel-art" data-slide-to="{{ image.number }}"></li>
    {% endfor %}
  </ol>

  <!-- Wrapper for slides -->
  <div class="carousel-inner" role="listbox">
    <div class="item active">
      <img src="{{ site.baseurl }}/media/{{ page.img }}" alt="{{ page.alt }}">
      <div class="carousel-caption {{ page.caption_color }}">
        {{ page.title }}
      </div>
    </div>
    {% for image in site.data.paris %} 
    <div class="item">
      <img src="{{ image.url }}" alt="{{ image.title }}">
      <div class="carousel-caption {{ image.caption_color }}">
        {% if image.title %} {{ image.title }} {% endif %}
      </div>
    </div>
    {% endfor %}
  </div>

  <!-- Controls -->
  <a class="left carousel-control" href="#carousel-art" role="button" data-slide="prev">
    <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
    <span class="sr-only">Previous</span>
  </a>
  <a class="right carousel-control" href="#carousel-art" role="button" data-slide="next">
    <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
    <span class="sr-only">Next</span>
  </a>
</div>

