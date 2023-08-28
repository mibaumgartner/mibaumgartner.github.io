---
permalink: /highlights/
title: "About me"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /
  - /about/
  - /about.html
---

Welcome, I'm Michael and am currently a Ph.D. student in the Medical Image Computing Group (MIC) at the German Cancer Research Center (DKFZ) in Heidelberg, Germany. My current work is mostly focussed around object detection, instance segmentation and panoptic segmentation in radiological images but I'm always looking for new projects to experiment with and learn from them. I have worked on several challenges and hackathons in the past and enjoy contributing to open source projects ([MONAI](https://github.com/Project-MONAI/MONAI) as Co-Chair of the Research Working Group, [Rising](https://github.com/PhoenixDL/rising), [Delira](https://github.com/delira-dev/delira)).

<br>

# Selected Highlights

<p>

{% include base_path %}

{% assign ordered_pages = site.highlights | sort:"prio" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %}
</p>