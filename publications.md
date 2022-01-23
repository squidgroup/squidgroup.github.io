---
layout: page
title: Publications
permalink: /publications/
---

<div class="publications">


  {% assign sorted-publications = site.publications | sort: 'date' | reverse %}
  {% for publication in sorted-publications %}
  
    <div class="publication">
  
      {%- if publication.authors -%} {{ publication.authors }} {%- endif -%}
      {%- if publication.year -%} &nbsp;({{ publication.year }}) {%- endif -%}
      
      {%- if publication.title -%} 
        &nbsp; <a target="_blank" href="https://doi.org/{{ publication.doi }}">{{ publication.title }}</a>.
      {%- endif -%}

      {%- if publication.journal -%} &nbsp;<i>{{ publication.journal }} </i> {%- endif -%}

      {%- if publication.volume -%} , {{ publication.volume }} {%- endif -%}
      {%- if publication.issue -%} ({{ publication.issue }}) {%- endif -%}

      {%- if publication.pages -%} , {{ publication.pages }} {%- endif -%}
      
      .

    </div>
  {% endfor %}
  
</div>