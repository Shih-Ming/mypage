---
layout: page
title: "Home"
class: home
---

# Hi, I'm Shih-Ming Huang

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I'm an M.S. student at [Advanced Antenna Laboratory](https://shihyuansite.wordpress.com/) at [National Taiwan University](https://www.ntu.edu.tw/english/) and a student research assistant at [Academia Sinica Institute of Astronomy and Astrophysics](https://www.asiaa.sinica.edu.tw/people/cv.php?i=smhuang). I am interested in developing novel applications of microwave engineering and specialized at system integration of microwave, baseband circuits, and embedded systems.

My current research topic is <b>Spatially Reconfigurable Phased Arrays</b>. The project is sponsored by  [Ministry of Science and Technology](https://www.most.gov.tw/?l=en) (MOST) in Taiwan, and led by my advisor, Prof. [Shih-Yuan Chen](https://www.ee.ntu.edu.tw/profile1.php?teacher_id=942017). In this project, I am responsible for system integration and proposal drafting to MOST.
</div>

<div class="me" markdown="1">
<picture>
  <a href="/mypage/images/ShihMing.jpg">
    <img
      src= '/mypage/images/ShihMing.jpg'
      alt='Shih-Ming Huang'>
  </a>
</picture>
  <br>
  <a href="{{ "/CV_ShihMing.pdf" | relative_url }}" class="button">
    <i class="fas fa-chevron-circle-right"></i>
    <b>Download CV</b>
  </a>

<!-- {:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a> -->
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