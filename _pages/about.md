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

Welcome, my name is Michael and I am currently a Ph.D. student (supervised by [Klaus H. Maier-Hein](https://scholar.google.com/citations?user=oCrBpVMAAAAJ&hl=de)) in the Medical Image Computing Group (MIC) at the German Cancer Research Center (DKFZ) in Heidelberg, Germany. My current work is focussed around object detection ([nnDetection](https://github.com/MIC-DKFZ/nnDetection)), instance segmentation and panoptic segmentation in radiological images but I'm always looking for new projects to experiment with and learn from them. During my I had the honor to work with [Fabian Isensee](https://scholar.google.com/citations?user=PjerEe4AAAAJ&hl=en), [Paul F. Jaeger](https://pfjaeger.github.io/), [Christoph Haarburger](https://www.linkedin.com/in/chaarburger/?originalSubdomain=de) and many more inspirational people. I have participated in several challenges and hackathons in the past and enjoy contributing to open source projects ([MONAI](https://github.com/Project-MONAI/MONAI) as Co-Chair of the Research Working Group, [Rising](https://github.com/PhoenixDL/rising), [Delira](https://github.com/delira-dev/delira)).

<br>

# Selected Highlights

<p>

{% include base_path %}

{% assign ordered_pages = site.highlights | sort:"prio" %}

{% for post in ordered_pages %}
  {% include archive-single.html type="grid" %}
{% endfor %}
</p>