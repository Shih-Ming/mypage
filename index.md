---
layout: page
title: "Home"
class: home
---

# Hi, I'm Shih-Ming Huang

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I'm a PhD candidate at [Digital Microwave Lab](https://www.dmlab.ee.ucla.edu/) in University of California, Los Angeles (UCLA). I am interested in antnena design, phased array design, and radio-frequency systems.

My current research topic is <b>Ferromagnetic Resonance Enhanced Electrically Small Antenna</b>. The project uses the resonance of electron spin precession to create very small antennas with high radiation efficiency and frequency tunability.This project is sponsored by [Intelligence Advanced Research Projects Activity (IARPA)](https://www.iarpa.gov/research-programs/equal-p), and led by my advisor, Prof. [Yuanxun Ethan Wang](https://www.dmlab.ee.ucla.edu/people). In this project, I am responsible for the antenna design, measurement, and system integration.
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