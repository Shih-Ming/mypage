---
layout: page
title: "Home"
class: home
---

# Hi, I'm Shih-Ming Huang

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I'm a master's student at the [Advanced Antenna Laboratory](https://shihyuansite.wordpress.com/) at [National Taiwan University](https://www.ntu.edu.tw/english/) and an intern at [Academia Sinica Institute of Astronomy and Astrophysics](https://www.asiaa.sinica.edu.tw/people/cv.php?i=smhuang). I am interested in developing novel applications of microwave engineering and specialized at system integration of microwave and baseband circuits.
</div>

<div class="me" markdown="1">
<picture>
  <img
    src= '/mypage/images/ShihMing.jpg'
    alt='Shih-Ming Huang'>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
</div>

</div>

## Featured Projects

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>
<a href="{{ "/projects/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show More Projects
</a>

## Awards
{% assign awards = site.data.awards %}
{% for award in awards %}
  <div class="awards">
    {% include awards.html award = award %} 
  </div>
{% endfor %}