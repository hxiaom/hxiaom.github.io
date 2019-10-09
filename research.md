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
      
      <h3 class="category-head">News</h3>
      <a name="{{ category_name | slugize }}"></a>
      {% for post in site.categories[category_name] %}
        
        {% assign post_title = post.title %}
        {% if post_title contains '2018.' or post_title contains '2019.' %}
          <article class="archive-item">
            <a href="{{ site.baseurl }}{{ post.url }}" target="_blank">{{post.title}}</a>
          </article>
        {% endif %}
      {% endfor %}

      <p></p>
      <h3 class="category-head">Notes</h3>

      <a name="{{ category_name | slugize }}"></a>
      {% for post in site.categories[category_name] %}
        
        {% assign post_title = post.title %}
        {% unless post_title contains '2018.' or post_title contains '2019.' %}
          <article class="archive-item">
            <a href="{{ site.baseurl }}{{ post.url }}" target="_blank">{{post.title}}</a>
          </article>
        {% endunless %}
      {% endfor %}

    {% endif %}
  </div>
{% endfor %}
</div>

<!-- - 自动驾驶
  - [自动驾驶](http://localhost:4000/mobility/2018/09/04/Automobile.html)
  - [电动汽车](http://localhost:4000/mobility/2018/09/04/Electricmobile.html)
  - [高精地图](http://localhost:4000/mobility/2018/09/17/Map.html)
  - [自动驾驶安全](http://localhost:4000/mobility/2019/02/24/Safety.html)
  - [自动驾驶芯片](http://localhost:4000/mobility/2019/02/26/av-chip.html)
  - [自动驾驶人才](http://localhost:4000/mobility/2018/09/18/automobile-job.html)
  - [共享出行](http://localhost:4000/mobility/2018/10/11/Ride-Sharing.html)
  - [出行保险](http://localhost:4000/mobility/2018/10/24/Insurance.html)
  - [移动商业](http://localhost:4000/mobility/2018/11/05/mobility-commerce.html)
  - [智慧城市](http://localhost:4000/mobility/2018/08/30/Smart-City.html)
- Academic
- Industrial
  -  -->