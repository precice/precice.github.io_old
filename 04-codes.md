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

{% for a in official %}

### {{ a.name }}

{{ a.content }}

* **Adapter's repository:** {{ a.repository }} ({{ a.language }})
* **Status:** {{ a.status }}
* **{{ a.name }} versions:** {{ a.versions }}
* **Typical applications:** {{ a.application }}
* **Can write:** {{ a.can-write }}
* **Can read:** {{ a.can-read }}

{% endfor %}

## Third-party adapters

These adapters have been developed by the preCICE community. For more information
on these adapters, you may contact the respective developers.
If you have written any other adapter, please [let us know](../resources/#contact)!

{% for a in inofficial %}

### {{ a.name }}

{{ a.content }}

* **Typical applications:** {{ a.application }}

{% endfor %}

## Legacy adapters

These adapters and/or the respective solvers are not maintained and might not work anymore, but are
listed here as an example of what other projects have used preCICE in the past.

{% for a in legacy %}

### {{ a.name }}

{{ a.content }}

* **Typical applications:** {{ a.application }}

{% endfor %}
