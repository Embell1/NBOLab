---
layout: page
permalink: /publications/
title: Publicaciones
description: Una lista de nuestras publicaciones de investigación organizadas por año
years: [2024, 2023, 2022, 2021, 2020, 2019, 2018, 2017, 2016, 2015, 2014, 2013, 2012, 2011, 2010, 2009, 2008, 2007, 2006]
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">
  <div class="accordion" id="accordionPublications">
    {% for year in page.years %}
      <div class="accordion-item">
        
        <h2 class="accordion-header" id="heading-{{ year }}">
          <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#collapse-{{ year }}" aria-expanded="false" aria-controls="collapse-{{ year }}">
            <strong>{{ year }}</strong>
          </button>
        </h2>
        
        <div id="collapse-{{ year }}" class="accordion-collapse collapse" aria-labelledby="heading-{{ year }}">
          <div class="accordion-body">
            {% bibliography --query @*[year={{ year }}] %}
          </div>
        </div>

      </div>
    {% endfor %}
  </div>
</div>