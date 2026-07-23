---

layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

My research focuses on **non-invasive biomedical sensing, artificial intelligence for healthcare, and intelligent monitoring systems**, with applications in neurodegenerative disease assessment, computational imaging, and human activity analysis.

You can also view my publications on
[Google Scholar](https://scholar.google.com/citations?user=r3q7Re0AAAAJ&hl=en)

{% assign publication_total = site.publications | size %}
{% assign journal_count = 0 %}
{% assign conference_count = 0 %}
{% assign dataset_count = 0 %}
{% assign thesis_count = 0 %}

{% for publication in site.publications %}
  {% if publication.type == "conference" %}
    {% assign conference_count = conference_count | plus: 1 %}
  {% elsif publication.type == "thesis" %}
    {% assign thesis_count = thesis_count | plus: 1 %}
  {% elsif publication.type == "dataset" or publication.venue == "Data in Brief" or publication.venue == "Data in brief" %}
    {% assign dataset_count = dataset_count | plus: 1 %}
  {% else %}
    {% assign journal_count = journal_count | plus: 1 %}
  {% endif %}
{% endfor %}

{% assign publications_by_date = site.publications | sort: "date" %}
{% assign latest_publication = publications_by_date | last %}

<section class="publication-stats" aria-label="Publication statistics">
  <div class="publication-stat">
    <strong>{{ publication_total }}</strong>
    <span>Publications</span>
  </div>
  <div class="publication-stat">
    <strong>{{ journal_count }}</strong>
    <span>Journal articles</span>
  </div>
  <div class="publication-stat">
    <strong>{{ conference_count }}</strong>
    <span>Conference papers</span>
  </div>
  <div class="publication-stat">
    <strong>{{ dataset_count }}</strong>
    <span>Data articles</span>
  </div>
  <div class="publication-stat">
    <strong>{{ thesis_count }}</strong>
    <span>Theses</span>
  </div>
  <div class="publication-stat">
    <strong>{{ latest_publication.date | date: "%Y" }}</strong>
    <span>Latest year</span>
  </div>
</section>

---

## ⭐ Selected Publications

{% for post in site.publications reversed %}
{% if post.highlight == true %}
{% include archive-single.html %}
{% endif %}
{% endfor %}

---

## 🎓 Thesis

{% for post in site.publications reversed %}
{% if post.type == "thesis" %}
{% include archive-single.html %}
{% endif %}
{% endfor %}

---

## Journal Articles

{% for post in site.publications reversed %}
{% if post.type == "journal" or post.type == nil %}
{% unless post.type == "thesis" or post.type == "conference" %}
{% include archive-single.html %}
{% endunless %}
{% endif %}
{% endfor %}

---

## Conference Papers

{% for post in site.publications reversed %}
{% if post.type == "conference" %}
{% include archive-single.html %}
{% endif %}
{% endfor %}
