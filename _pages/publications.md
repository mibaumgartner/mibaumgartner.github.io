---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
  <p> 
  You can find the full list of my articles on 
  <a href="{{ site.author.googlescholar }}" style="text-decoration:none"> my Google Scholar profile <i class="fab fa-fw fa-google zoom" aria-hidden="true"></i> </a>
  </p>
{% endif %}

{% include base_path %}

{% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %}
