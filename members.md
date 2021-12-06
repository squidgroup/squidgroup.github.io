---
layout: page
title: Members
permalink: /members/
---

{% for member in site.members %}
  <h2>
    <a href="{{ staff_member.url }}">
      {{ member.name }}
    </a>
  </h2>
  <p>{{ member.content | markdownify }}</p>
{% endfor %}