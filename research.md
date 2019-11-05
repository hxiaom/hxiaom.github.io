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

      <!-- <a name="{{ category_name | slugize }}"></a>
      {% for post in site.categories[category_name] %}
        
        {% assign post_title = post.title %}
        {% unless post_title contains '2018.' or post_title contains '2019.' %}
          <article class="archive-item">
            <a href="{{ site.baseurl }}{{ post.url }}" target="_blank">{{post.title}}</a>
          </article>
        {% endunless %}
      {% endfor %} -->

    {% endif %}
  </div>
{% endfor %}
</div>

Research Skill
- [Writing](http://hxiaom.github.io/mobility/2019/06/12/writing.html)
- [Pipeline]()

[Research Topics](http://hxiaom.github.io/mobility/2019/04/12/research-framework.html)

HAI
- [TOP10 AI Paper](http://hxiaom.github.io/mobility/2019/10/09/ai-paper.html)
- [HAI Material](http://hxiaom.github.io/mobility/2019/10/14/xai-material.html)

Mobility
- [TOP10 Mobility Paper](http://hxiaom.github.io/mobility/2019/10/09/mobility-paper.html)
- [Mobility Material](http://hxiaom.github.io/mobility/2019/03/12/AV-in-academic.html)
- [Mobility Data](http://hxiaom.github.io/mobility/2018/10/23/Mobility-Data.html)

- [自动驾驶](http://hxiaom.github.io/mobility/2018/09/04/Automobile.html)
- [电动汽车](http://hxiaom.github.io/mobility/2018/09/04/Electricmobile.html)
- [高精地图](http://hxiaom.github.io/mobility/2018/09/17/Map.html)
- [自动驾驶安全](http://hxiaom.github.io/mobility/2019/02/24/Safety.html)
- [自动驾驶芯片](http://hxiaom.github.io/mobility/2019/02/26/av-chip.html)
- [自动驾驶人才](http://hxiaom.github.io/mobility/2018/09/18/automobile-job.html)
- [共享出行](http://hxiaom.github.io/mobility/2018/10/11/Ride-Sharing.html)
- [出行保险](http://hxiaom.github.io/mobility/2018/10/24/Insurance.html)
- [移动商业](http://hxiaom.github.io/mobility/2018/11/05/mobility-commerce.html)
- [智慧城市](http://hxiaom.github.io/mobility/2018/08/30/Smart-City.html)
- [AV Companies](http://hxiaom.github.io/mobility/2019/03/25/AV-Companies.html)
- [【Book】美国大城市的死与生](http://hxiaom.github.io/mind/mobility/2019/01/16/the-death-and-life-of-great-american-cities.html)
- [【Book】能源和交通的清洁革命](http://hxiaom.github.io/mobility/2018/10/21/Clean-Disruption.html)
- [【Book】滴滴：分享经济改变中国](http://hxiaom.github.io/mobility/2018/10/05/DiDi-book.html)
- [【Book】智能化未来：无人驾驶如何改变我们的生活](http://hxiaom.github.io/mobility/2018/09/19/intellegence-future.html)
- [【Book】无人驾驶：十万亿美元的大饼怎么分？](http://hxiaom.github.io/mobility/2018/09/18/economist-automobile.html)
- [【Book】寻找无人驾驶的缰绳——2018年全球自动驾驶法律政策研究报告](http://hxiaom.github.io/mobility/2018/09/16/Tencent-automobile.html)
- [【Book】无人驾驶](http://hxiaom.github.io/mobility/2018/09/16/Automobile.html)
- [【Book】Uber中国1000天：开拓、增长与竞争](http://hxiaom.github.io/mobility/2018/09/07/Uber-China-1000.html)
- [【Book】USDOT - Automated Vehicles 3.0 - Preparing for the Future of Transportation](http://hxiaom.github.io/mobility/2018/10/08/Automated-Vehicles-3.0.html)
- [【Talk】Past, Present, and Future of Motion Planning in a Complex World By Sertac Karaman](http://hxiaom.github.io/mobility/2018/11/12/Sertac-Karaman-Talk.html)
- [【Talk】The rise of ML in self-driving cars Sacha Arnoud](http://hxiaom.github.io/mobility/2018/11/12/Sacha-Arnoud-Talk.html)
- [【Talk】Technology, Policy and Vehicle Safety in the Age of AI J. Christian Gerdes](http://hxiaom.github.io/mobility/2018/11/12/Chris-Gerdes-Talk.html)
- [【Talk】Disruption of Transportation - & Implications for Society By Tony Seba](http://hxiaom.github.io/mobility/2018/11/11/Tony-Seba-Talk.html)
- [【Talk】折叠的空间，掏空的人—如何用数据治城市病 茅明睿](http://hxiaom.github.io/mobility/2018/11/11/Mingrui-Mao-Talk3.html)
- [【Talk】智能出行—从技术试验到社会试验 茅明睿](http://hxiaom.github.io/mobility/2018/11/11/Mingrui-Mao-Talk2.html)
- [【Talk】数据与城市正义 茅明睿](http://hxiaom.github.io/mobility/2018/11/11/Mingrui-Mao-Talk.html)
- [【Talk】无人驾驶就是你对美好生活的向往 吴甘沙](http://hxiaom.github.io/mobility/2018/11/11/Gansha-Wu-Talk.html)
- [【Talk】Sterling Anderson, Co-Founder, Aurora](http://hxiaom.github.io/mobility/2018/11/08/Sterling-Anderson-Talk.html)
- [【Talk】智能驾驶-未来汽车的新赛道战争 吴甘沙](http://hxiaom.github.io/mobility/2018/11/08/Gansha-Wu-Talk.html)
- [【Talk】nuTonomy's Vision for Autonomous Driving - Emilio Frazzoli, CTO, nuTonomy](http://hxiaom.github.io/mobility/2018/11/08/Emilio-Frazzoli-talk.html)
- [MIT 6.S094 Deep Learning for Self-Driving Cars](http://hxiaom.github.io/mobility/2018/11/07/MIT-course.html)
- [Baidu Apollo & Udacity Course](http://hxiaom.github.io/mobility/2018/11/07/Baidu-Apollo.html)

- ["车和家"还是"共享汽车"?](http://hxiaom.github.io/mobility/2018/09/13/mobility-question.html)
- [Waymo分析](http://hxiaom.github.io/mobility/2018/09/04/Waymo.html)
- [Uber分析](http://hxiaom.github.io/mobility/2018/09/04/Uber.html)
- [神州优车分析](http://hxiaom.github.io/mobility/2018/08/31/shenzhou-youche.html)
- [滴滴出行分析](http://hxiaom.github.io/mobility/2018/08/30/didi-Chuxing-Corporate-Citizenship-Report.html)
- [GeoTIFF文件操作](http://hxiaom.github.io/mobility/2018/08/29/GeoTiff.html)
- [City Nighttime Lights](http://hxiaom.github.io/mobility/2018/08/29/City-Nighttime-Light.html)