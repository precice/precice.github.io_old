---
layout: default
title: Coupled Codes
permalink: /codes/
---

{% assign official = site.codes | where: "category", "official" %}
{% assign inofficial = site.codes | where: "category", "inofficial" %}
{% assign legacy = site.codes | where: "category", "legacy" %}

# Coupled Codes

There are various codes - free and proprietary ones - currently coupled with preCICE. If you want to add your code here, please let us know.

**Official adapters:** {%- for a in official -%}
[{{ a.name }}](#{{ a.ID }}){% if forloop.last == false %}, {% endif %}
{% endfor %}

**Third-party adapters:** {%- for a in inofficial -%}
[{{ a.name }}](#{{ a.ID }}){% if forloop.last == false %}, {% endif %}
{% endfor %}

**Legacy adapters:** {%- for a in legacy -%}
[{{ a.name }}](#{{ a.ID }}){% if forloop.last == false %}, {% endif %}
{% endfor %}

## Official adapters

These adapters are hosted on [GitHub](https://github.com/precice/) and
are maintained by us. We try to keep these adapters up-to-date and we constantly
strive to improve their quality, compatibility, and feature coverage.
If you would like to contribute to these adapters, please [contact us](../resources/#contact)!

<ul class="codeslist">
{% for a in official %}
  <li>
    <h3 id="{{ a.ID }}">{{ a.name }}</h3>
    <div>
      {{ a.content }}
    </div>
    <dl>
      <dt>Adapter's repository:</dt>
      <dd><a href="{{ a.repository }}">Repository</a> written in {{ a.language }} <span class="label
      {%- case a.status -%}
      {% when 'up-to-date'%}
       success
       {% when 'needs-small-updates' %}
       warning
       {% when 'experimental' %}
       alert
       {% when 'out-of-date' %}
       alert
        {% else %}
      {%- endcase -%}
      ">{{ a.status }}</span></dd>
      <dt>Supported {{ a.name }} versions:</dt>
      <dd>{{ a.versions }}</dd>
      <dt>Typical applications:</dt>
      <dd>{{ a.application }}</dd>
      <dt>Can write:</dt>
      <dd>{{ a.can-write }}</dd>
      <dt>Can read:</dt>
      <dd>{{ a.can-read }}</dd>
    {% if a.notes %}
      <dt>Notes:</dt>
      <dd>{{ a.notes | markdownify }}</dd>
    {% endif %}
    </dl>
  </li>
{% endfor %}
</ul>

## Third-party adapters

These adapters have been developed by the preCICE community. For more information
on these adapters, you may contact the respective developers.
If you have written any other adapter, please [let us know](../resources/#contact)!

<ul class="codeslist">
{% for a in inofficial %}
  <li>
    <h3 id="{{ a.ID }}">{{ a.name }}</h3>
    <div>
      {{ a.content }}
    </div>
    <dl>
    {% if a.contact %}
      <dt>Contact:</dt>
      <dd>{{ a.contact | markdownify }}</dd>
    {% endif %}
      <dt>Typical applications:</dt>
      <dd>{{ a.application }}</dd>
    {% if a.notes %}
      <dt>Notes:</dt>
      <dd>{{ a.notes | markdownify }}</dd>
    {% endif %}
    </dl>
  </li>
{% endfor %}
</ul>

## Legacy adapters

These adapters and/or the respective solvers are not maintained and might not work anymore, but are
listed here as an example of what other projects have used preCICE in the past.

<ul class="codeslist">
{% for a in legacy %}
  <li>
    <h3 id="{{ a.ID }}">{{ a.name }}</h3>
    <div>
      {{ a.content }}
    </div>
    <dl>
    {% if a.contact %}
      <dt>Contact:</dt>
      <dd>{{ a.contact | markdownify }}</dd>
    {% endif %}
      <dt>Typical applications:</dt>
      <dd>{{ a.application }}</dd>
    {% if a.notes %}
      <dt>Notes:</dt>
      <dd>{{ a.notes | markdownify }}</dd>
    {% endif %}
    </dl>
  </li>
{% endfor %}
</ul>
