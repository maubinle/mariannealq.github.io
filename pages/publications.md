---
layout: default
permalink: /publications/
---

## Peer-Reviewed Publications

{% assign peer = site.publications | where: "category", "peer-reviewed" | sort: "year" | reverse %}
{% for pub in peer %}
{% include publication-card.html pub=pub %}
{% endfor %}

## Workshops & Symposia

{% assign workshops = site.publications | where: "category", "workshop" | sort: "year" | reverse %}
{% for pub in workshops %}
{% include publication-card.html pub=pub %}
{% endfor %}

## Other Selected Conference Presentations

{% assign other = site.publications | where: "category", "other" | sort: "year" | reverse %}
{% for pub in other %}
{% include publication-card.html pub=pub %}
{% endfor %}

<p class="pub-note"><em>* indicates equal contribution</em></p>
