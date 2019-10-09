---
layout: page
permalink: /research/
title: Research
---


<div id="archives">

{% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    
    {% if category_name == 'Mobility' %}
      <div id="#{{ category_name | slugize }}"></div>
      <p></p>
      
      <a name="{{ category_name | slugize }}"></a>
      {% for post in site.categories[category_name] %}
        
        {% assign post_title = post.title %}
        {% if post_title.startswith('20') %}
          <article class="archive-item">
            <a href="{{ site.baseurl }}{{ post.url }}" target="_blank">{{post.title}}</a>
          </article>
        {% endif %}
      {% endfor %}

    {% endif %}
  </div>
{% endfor %}
</div>