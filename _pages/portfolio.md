---
title: "Portfolio"
layout: splash
permalink: /portfolio/
date: 2021-10-05
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /assets/images/home_header1.jpg
  actions:
    - label: ""
      url: ""
sidebar:
  - title: "Minsuk Kim"
    image: /assets/images/MyImage.png
    image_alt: "Face"
    text: "dd"
  - title: "Role"
    text: "Software Engineer, Graphics Programmer"
graphicproject:
  - image_path: /assets/images/GraphicSoloProject.png
    title: "Graphic Solo project"
    excerpt: 'Solo 3D graphics engine with **OpenGL**.'
    url: "/posts/2021_SoloGraphics"
    btn_label: "Read More"
    btn_class: "btn--primary"
WFT:
  - image_path: /assets/images/WFTTitle.png
    title: "World Firepower Tournament"
    excerpt: 'Made by custom 2D engine by team of 3'
    url: "/posts/GAM200_WFT"
    btn_label: "Read More"
    btn_class: "btn--primary"
ColorLeon:
  - image_path: /assets/images/ColorLeonTitle.png
    title: "ColorLeon"
    excerpt: 'Made by supported 2D engine(box2d) by team of 4'
    url: "/posts/GAM150_ColorLeon"
    btn_label: "Read More"
    btn_class: "btn--primary"
---

## About
- Name : Minsuk Kim
- Role : Software Engineer, Graphics Programmer
[Read More](/about/){: .btn .btn--primary}


## Work

{% include feature_row id="graphicproject" type="left" %}

{% include feature_row id="WFT" type="right" %}

{% include feature_row id="ColorLeon" type="left" %}
