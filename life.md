---
layout: page
permalink: /life/
title: Life
---


<div id="archives">

{% for category in site.categories %}
  <div class="archive-group">
    {% capture category_name %}{{ category | first }}{% endcapture %}
    {% if category_name != 'Mobility' and category_name != 'Analytics' %}
    <div id="#{{ category_name | slugize }}"></div>
    <p></p>
    
    <h3 class="category-head">{{ category_name }}</h3>
    <a name="{{ category_name | slugize }}"></a>
    {% for post in site.categories[category_name] %}
    <article class="archive-item">
      <!-- <h4><a href="{{ site.baseurl }}{{ post.url }}" target="_blank">{{post.title}}</a></h4> -->
      <a href="{{ site.baseurl }}{{ post.url }}" target="_blank">{{post.title}}</a>
    </article>
    {% endfor %}
    {% endif%}
  </div>
{% endfor %}
</div>