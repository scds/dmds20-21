---
layout: home
title: Home
nav_order: 1
has_toc: false

has_children: false 
---

{%- assign workshops = site.pages 
    | where_exp: "item", "item.grand_parent == null"
    | where_exp: "item", "item.parent == null"
    | sort: "title" 
-%}

<img src="assets/img/titleSlide.png" alt="Workshop Title Slide" width="100%">

# Welcome to the 2020-2021 Do More with Digital Scholarship Webinars

What is digital scholarship, how can I do more with it, and how can it contribute to my research and teaching? Join us for our free workshop series that introduces McMaster students, faculty, and staff to the multifaceted domain of digital scholarship.

- Develop skills for professionalization.
- Learn to use software including Audacity, Gephi, Obsidian, OpenRefine, Python, Two Tone, and Voyant.
- Engage with faculty, staff, and students with all levels of technical expertise.
- Explore digital approaches to research and knowledge mobilization. 
- Discover opportunities for collaboration.

## 2020-21 DMDS Workshop Topics

<div markdown="1" style="border: 1px solid #7a003c; border-radius: 6px; margin-bottom: 1em; padding: 0.5em 1em 0; margin-top: 1em;" class="toc">
<summary style="cursor:default; display: block; border-bottom: 1px solid #302d36; margin-bottom: 0.5em">
  Workshops
</summary>
<ul>
{% for workshop in workshops %}
{% if workshop.title != null and workshop.title != "Home" and workshop.title != "Learn More" %}
<li><a href="{{workshop.url | absolute_url}}">{{workshop.title}}</a></li>
{% endif %}
{% endfor %}
</ul>
</div>

## Land Acknowledgement

<!-- Grabs the default SCDS land acknowledgment. If you want to use a custom one, replace this line with it. -->
{% include def/land_ack.md %}