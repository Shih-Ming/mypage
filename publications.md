---
layout: page
permalink: /publications/
title: Publications
class: pubs
---

{:.hidden}
# Publications

{% assign pubyears = site.publications | group_by:"year"  %}
{% assign sorted_pubyears = pubyears | reverse %}
{% for year in sorted_pubyears %}
## {{ year.name }}
{:#y{{ year.name }} .year}
{% for pub in year.items %}
  {% include publication.html pub=pub %}
{% endfor %}
{% endfor %}

<!-- <script src="https://cdn.jsdelivr.net/npm/itemsjs@1.0.40/dist/itemsjs.min.js"></script> -->
<script>
  {% include itemsjs.min.js %}
  {% include pubfilter.js %}
</script>
