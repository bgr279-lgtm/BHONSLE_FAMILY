---
title: Father
permalink: /people/
---

# Our family

{% assign people = site.people | sort: "generation" %}
<ul class="people-list">
{% for p in people %}
  <li>
    <a href="{{ p.url | relative_url }}"><strong>{{ p.title }}</strong></a>
    <small>{{ p.relation }}</small>
    <small>{% if p.born %}{{ p.born }}{% endif %}{% if p.died %} – {{ p.died }}{% endif %}</small>
  </li>
{% endfor %}
</ul>

*To add someone, copy a file in the `_people` folder, rename it, and fill in their story.*
