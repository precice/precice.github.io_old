---
layout: default
title: About
permalink: /about/
---

# About

preCICE is developed at the [Chair of Scientific Computing](http://www5.in.tum.de/wiki/index.php/Home) at the Technical University of Munich and at the [Institute for Parallel and Distributed Systems](http://www.ipvs.uni-stuttgart.de/) at the University of Stuttgart.

Scientific project leaders:

<ul class="devlist">
  {% for p in site.data.developer.leads %}
  <li{% if forloop.first %} class="devlist-first"{% endif %}>
    <div class="devlist-img">
      {% if p.img %}
      <img src="{{site.static_files | where: "basename", p.img | map: "path"}}" alt="Portait">
      {% endif %}
    </div>
    <div class="devlist-left">
      {{ p.name }}<br/>
      <i>{{ p.institution }}</i>
    </div>
    <ul class="devlist-right">
      {% if p.url %}<li><a href="{{ p.url }}" alt="See the institutional website"><i class="fas fa-university"></i></a></li>{% endif %}
      {% if p.github %}<li><a href="https://github.com/{{ p.github }}" alt="See the Github profile"><i class="fab fa-github"></i></a></li>{% endif %}
    </ul>
  </li>
  {% endfor %}
</ul>

Main contributors (in alphabetical order):

<ul class="devlist">
  {% for p in site.data.developer.main %}
  <li{% if forloop.first %} class="devlist-first"{% endif %}>
    <div class="devlist-img">
      {% if p.img %}
      <img src="{{site.static_files | where: "basename", p.img | map: "path"}}" alt="Portait">
      {% endif %}
    </div>
    <div class="devlist-left">
      {{ p.name }}<br/>
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

<ul class="devlist">
  {% for p in site.data.developer.main-inactive %}
  <li{% if forloop.first %} class="devlist-first"{% endif %}>
    <div class="devlist-left">
      {{ p.name }}<br/>
      <i>{{ p.institution }}</i>
    </div>
    <ul class="devlist-right">
      {% if p.url %}<li><a href="{{ p.url }}" alt="See the institutional website"><i class="fas fa-university"></i></a></li>{% endif %}
      {% if p.github %}<li><a href="https://github.com/{{ p.github }}" alt="See the Github profile"><i class="fab fa-github"></i></a></li>{% endif %}
    </ul>
  </li>
  {% endfor %}
</ul>

Further contributors include (in alphabetical order):

<ul class="devlist">
  {% for p in site.data.developer.contributors %}
  <li{% if forloop.first %} class="devlist-first"{% endif %}>
    <div class="devlist-left">
      {{ p.name }}<br/>
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
