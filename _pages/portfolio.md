---
title: "Portfolio"
layout: splash
permalink: /portfolio/
date: 2021-10-05
author_profile: true
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/home_header1.jpg
  actions:
    - label: ""
      url: ""
  caption: ""
sidebar:
  - title: "Minsuk Kim"
    image: /assets/images/MyImage.png
    image_alt: "Face"
    text: ""
  - title: "Role"
    text: "Software Engineer, Graphics Programmer"
graphicproject:
  - image_path: /assets/images/GraphicSoloProject.png
    alt: "graphic_solo"
    title: "Graphic Solo project"
    excerpt: 'This is some sample content that goes here with **Markdown** formatting. Left aligned with `type="left"`'
    url: "https://github.com/minsuk0519/minsuk0519.github.io/actions/new"
    btn_label: "Read More"
    btn_class: "btn--primary"
feature_row3:
  - image_path: /assets/images/GraphicSoloProject.png
    alt: "placeholder image 2"
    title: "Placeholder Image Right Aligned"
    excerpt: 'This is some sample content that goes here with **Markdown** formatting. Right aligned with `type="right"`'
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
---

{% include feature_row %}

{% include feature_row id="graphicproject" type="left" %}

{% include feature_row id="feature_row3" type="right" %}
