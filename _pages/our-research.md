---
title: "Our Research"
permalink: /our-research/
layout: collection
collection: posts
entries_layout: list
author_profile: true
---

## Filter by Category

<ul class="taxonomy-index">
  {% assign custom_order = "Introduction,Finance,Tech" | split: ',' %}
  {% for category_name in custom_order %}
    {% for category in site.categories %}
      {% if category[0] == category_name %}
        <li>
          <a href="{{ site.baseurl }}/categories/#{{ category[0] | slugify }}">
            <span class="archive-taxonomy-name"><strong>{{ category[0] }}</strong></span>
            &nbsp; <span class="taxonomy-count">{{ category[1].size }}</span>
          </a>
        </li>
      {% endif %}
    {% endfor %}
  {% endfor %}
</ul>