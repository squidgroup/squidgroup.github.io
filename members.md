---
layout: page
title: Members
permalink: /members/
---

<div class="members">
  {% for member in site.members %}
  <div class="member">
    <div class="container">

      {% assign avatar = site.static_files | find_exp: "item", "item.path contains member.photo" %}

      {% if avatar %}
      
        <img src="{{ avatar.path }}">
        
      {% else %}

       <img alt="squid_logo" src="{{site.images_path}}squid_logo.png">
       
      {% endif %}
      
      <h3>
        <!-- <a href="{{ member.url | prepend: site.baseurl }}"> -->
          {{ member.name }}
        <!-- </a> -->
      </h3>
      <!-- <p>{{ member.content | markdownify }}</p> -->
      
      
      <div class="links">
        {%- if member.github -%}
          <a href="{{ member.github }}" target="_blank">
            <svg class="svg-icon"><use xlink:href="{{ '/assets/minima-social-icons.svg#github' | relative_url }}"></use></svg> 
          </a>
        {%- endif -%}
        
        {%- if member.twitter -%}
        <a href="{{ member.twitter }}" target="_blank">
          <svg class="svg-icon"><use xlink:href="{{ '/assets/minima-social-icons.svg#twitter' | relative_url }}"></use></svg>
        </a>
      {%- endif -%}
      </div>
    </div> 
  </div>
  {% endfor %}
</div>