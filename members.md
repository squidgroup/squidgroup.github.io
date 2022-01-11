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
      
        {%- if member.googlescholar -%}
          <a href="{{ member.googlescholar }}" target="_blank">
            <i class="ai ai-google-scholar"></i>
          </a>
        {%- endif -%}
        
        {%- if member.researchgate -%}
          <a href="{{ member.researchgate }}" target="_blank">
            <i class="ai ai-researchgate"></i>
          </a>
        {%- endif -%}
      
        {%- if member.github -%}
          <a href="{{ member.github }}" target="_blank">
            <i class="fab fa-github"></i> 
          </a>
        {%- endif -%}
        
        {%- if member.twitter -%}
          <a href="{{ member.twitter }}" target="_blank">
            <i class="fab fa-twitter"></i>
          </a>
        {%- endif -%}
        
        
      </div>
      
    </div> 
  </div>
  {% endfor %}
</div>