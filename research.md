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
      
      <!-- <h3 class="category-head">News</h3> -->
      <a name="{{ category_name | slugize }}"></a>
      {% for post in site.categories[category_name] %}
        <!-- {% if str(post.title).startswith('20') %} -->
        <article class="archive-item">
          <a href="{{ site.baseurl }}{{ post.url }}" target="_blank">{{post.title}}</a>
        </article>
        <!-- {% endif %} -->
      {% endfor %}

      <!-- <h3 class="category-head">Others</h3>
      <a name="{{ category_name | slugize }}"></a>
      {% for post in site.categories[category_name] %}
        {% if !str(post.title).startswith('20') %}
        <article class="archive-item">
          <a href="{{ site.baseurl }}{{ post.url }}" target="_blank">{{post.title}}</a>
        </article>
        {% endif %} -->
      {% endfor %}

    {% endif %}
  </div>
{% endfor %}
</div>