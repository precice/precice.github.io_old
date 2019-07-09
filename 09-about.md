---
layout: default
title: About
permalink: /about/
---

# About the preCICE project

## Development

preCICE is developed at the [Chair of Scientific Computing](http://www5.in.tum.de/wiki/index.php/Home) at the Technical University of Munich and at the [Institute for Parallel and Distributed Systems](http://www.ipvs.uni-stuttgart.de/) at the University of Stuttgart.

Scientific project leaders:

{% assign dev_leads = site.data.developer.leads | sort: "name" %}
<ul class="devlist">
  {% for p in dev_leads %}
  <li{% if forloop.first %} class="devlist-first"{% endif %}>
    <div class="devlist-img">
      {% if p.img %}
      <img src="{{site.static_files | where: "basename", p.img | map: "path"}}" alt="Portait">
      {% endif %}
    </div>
    <div class="devlist-left">
      {{ p.fullname }}<br/>
      <i>{{ p.institution }}</i>
    </div>
    <ul class="devlist-right">
      {% if p.url %}<li><a href="{{ p.url }}" alt="See the institutional website"><i class="fas fa-university"></i></a></li>{% endif %}
      {% if p.github %}<li><a href="https://github.com/{{ p.github }}" alt="See the Github profile"><i class="fab fa-github"></i></a></li>{% endif %}
    </ul>
  </li>
  {% endfor %}
</ul>

Main contributors:

{% assign dev_main = site.data.developer.main | sort: "name" %}
<ul class="devlist">
  {% for p in dev_main %}
  <li{% if forloop.first %} class="devlist-first"{% endif %}>
    <div class="devlist-img">
      {% if p.img %}
      <img src="{{site.static_files | where: "basename", p.img | map: "path"}}" alt="Portait">
      {% endif %}
    </div>
    <div class="devlist-left">
      {{ p.fullname }}<br/>
      <i>{{ p.institution }}</i>
    </div>
    <ul class="devlist-right">
      {% if p.url %}<li><a href="{{ p.url }}" alt="See the institutional website"><i class="fas fa-university"></i></a></li>{% endif %}
      {% if p.github %}<li><a href="https://github.com/{{ p.github }}" alt="See the Github profile"><i class="fab fa-github"></i></a></li>{% endif %}
    </ul>
  </li>
  {% endfor %}
</ul>

Previous main contributors:

{% assign dev_premain = site.data.developer.main-inactive | sort: "name" %}
<ul class="devlist">
  {% for p in dev_premain %}
  <li{% if forloop.first %} class="devlist-first"{% endif %}>
    <div class="devlist-left">
      {{ p.fullname }}<br/>
      <i>{{ p.institution }}</i>
    </div>
    <ul class="devlist-right">
      {% if p.url %}<li><a href="{{ p.url }}" alt="See the institutional website"><i class="fas fa-university"></i></a></li>{% endif %}
      {% if p.github %}<li><a href="https://github.com/{{ p.github }}" alt="See the Github profile"><i class="fab fa-github"></i></a></li>{% endif %}
    </ul>
  </li>
  {% endfor %}
</ul>

Further contributors include:

{% assign dev_contrib = site.data.developer.contributors | sort: "name" %}
<ul class="devlist">
  {% for p in dev_contrib %}
  <li{% if forloop.first %} class="devlist-first"{% endif %}>
    <div class="devlist-left">
      {{ p.fullname }}<br/>
      <i>{{ p.institution }}</i>
    </div>
    <ul class="devlist-right">
      {% if p.url %}<li><a href="{{ p.url }}" alt="See the institutional website"><i class="fas fa-university"></i></a></li>{% endif %}
      {% if p.github %}<li><a href="https://github.com/{{ p.github }}" alt="See the Github profile"><i class="fab fa-github"></i></a></li>{% endif %}
    </ul>
  </li>
  {% endfor %}
</ul>

The conceptual ideas of preCICE are not completely new, preCICE is an advancement of FSI*ce, which has been developed by Dr. Markus Brenk.


## Funding

<ul class="funding">
  <li><a target="_blank" href="http://www.sppexa.de/"><img src="../assets/funding/sppexa.jpg" alt="SPPEXA"></a></li>
  <li><a target="_blank" href="http://gepris.dfg.de/gepris/projekt/391150578"><img src="../assets/funding/dfg.jpg" alt="preDOM"></a></li>
  <li><a target="_blank" href=""><img src="../assets/funding/bmwi.png" alt="BMWi"></a></li>
  <li>
    <a target="_blank" href="http://postdoc.eurotech-universities.eu/"><img src="../assets/funding/eurotech.jpeg" alt="EuroTech"></a>
  </li>
  <li>
    <img src="../assets/funding/eu.png" alt="European Union">
    <p>This project has received funding from the European Union’s Horizon 2020 research and innovation programme under the Marie Skłodowska-Curie grant agreement No 754462</p>
  </li>
</ul>

## Impressum

This website is maintained by

<tt>
Florian Lindner  
Simulation großer Systeme  
Institut für parallele und verteilte Systeme, Universität Stuttgart  
Universitätsstraße 38 | 70569 Stuttgart | Germany  
Tel: +49 (0)711 685 88427
</tt>

<figure>
    <img src="../assets/doughnuts.JPG" alt="preCICE doughnuts" style="max-width:100%" >
    <figcaption>preCICE is tasty because it is made with love by its contributors</figcaption>
</figure>
