---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

## Contact
- **Name:** Dr Rahmat Ullah
- **Email:** [rahmat.ullah@essex.ac.uk](mailto:rahmat.ullah@essex.ac.uk)
- **Location:** Colchester, United Kingdom
- **Current role:** Lecturer in Computer Science, University of Essex

## Research Summary
I am a Lecturer in Computer Science at the University of Essex and a Fellow of the Higher Education Academy (FHEA). My research focuses on artificial intelligence and computational imaging for digital health, with particular emphasis on non-invasive monitoring of neurodegenerative diseases such as Alzheimer’s disease using microwave sensing technologies.

I completed my PhD at the University of Edinburgh in collaboration with clinical neuroscientists, where I developed data-driven imaging pipelines for translational healthcare applications. My work integrates machine learning, biomedical signal processing, and sensing technologies to advance early diagnosis and monitoring of neurological conditions.

## Research Interests
- Machine learning for healthcare
- Biomedical signal and image processing
- Microwave and radar sensing for medical applications
- Computational imaging
- Digital health technologies
- Human activity recognition and assistive technologies

## Professional Recognition
- Fellow of the Higher Education Academy (FHEA)
- Associate Fellow of the Higher Education Academy (AFHEA)
- UK Global Talent Visa Endorsement (Royal Academy of Engineering)

## Positions
- **2023–Present:** Lecturer in Computer Science, University of Essex, United Kingdom

## Teaching
<ul>{% for post in site.teaching reversed %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>

## Selected Publications
<ul>{% for post in site.publications reversed limit:15 %}
  {% include archive-single-cv.html %}
{% endfor %}</ul>

## Talks
<ul>{% for post in site.talks reversed %}
  {% include archive-single-talk-cv.html %}
{% endfor %}</ul>
