---
title: Publications
layout: single
toc: true
header:
    
    overlay_image: /images/pub.jpg
    caption: "Photo by [Art Lasovsky](https://unsplash.com/@artlasovsky) on [Unsplash](https://unsplash.com/s/photos/pen?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText)"
---

{% assign cur = '2101' %}
{% for pub in site.pubs reversed %}
{% capture year %}{{pub.date | date:'%Y'}}{% endcapture %}
{% if year != cur %}## {{year}} {% endif %}
{% assign cur = year %}
{{pub.excerpt | replace: "#", pub.url }}
{% endfor %}
