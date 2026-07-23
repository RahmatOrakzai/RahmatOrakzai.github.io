---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

My research focuses on **non-invasive biomedical sensing, artificial intelligence for healthcare, and intelligent monitoring systems**, with applications in neurodegenerative disease assessment, computational imaging, and human activity analysis.

You can also view my publications on
[Google Scholar](https://scholar.google.com/citations?user=r3q7Re0AAAAJ&hl=en).

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
{% assign first_publication = publications_by_date | first %}
{% assign publications_by_year = site.publications | group_by_exp: "publication", "publication.date | date: '%Y'" | sort: "name" | reverse %}
{% assign max_year_count = 1 %}
{% for year in publications_by_year %}
  {% assign year_count = year.items | size %}
  {% if year_count > max_year_count %}
    {% assign max_year_count = year_count %}
  {% endif %}
{% endfor %}

<section class="publication-dashboard" aria-label="Publication overview">
  <div class="publication-dashboard__summary">
    <div class="publication-dashboard__total">
      <span class="publication-dashboard__eyebrow">Research output</span>
      <strong>{{ publication_total }}</strong>
      <span>publications since {{ first_publication.date | date: "%Y" }}</span>
    </div>
    <div class="publication-dashboard__latest">
      <span>Latest publication year</span>
      <strong>{{ latest_publication.date | date: "%Y" }}</strong>
    </div>
  </div>

  <div class="publication-dashboard__metrics">
    <div class="publication-metric">
      <strong>{{ journal_count }}</strong>
      <span>Journal articles</span>
    </div>
    <div class="publication-metric">
      <strong>{{ conference_count }}</strong>
      <span>Conference papers</span>
    </div>
    <div class="publication-metric">
      <strong>{{ dataset_count }}</strong>
      <span>Data articles</span>
    </div>
    <div class="publication-metric">
      <strong>{{ thesis_count }}</strong>
      <span>Theses</span>
    </div>
  </div>

  <div class="publication-dashboard__timeline">
    <h2>Publications by year</h2>
    <div class="publication-year-chart">
      {% for year in publications_by_year %}
        {% assign year_count = year.items | size %}
        {% assign bar_width = year_count | times: 100 | divided_by: max_year_count %}
        <div class="publication-year-row">
          <span class="publication-year-row__year">{{ year.name }}</span>
          <div class="publication-year-row__track" aria-hidden="true">
            <span class="publication-year-row__bar" style="width: {{ bar_width }}%"></span>
          </div>
          <strong class="publication-year-row__count">{{ year_count }}</strong>
        </div>
      {% endfor %}
    </div>
  </div>
</section>

---

## Selected Publications

{% for post in site.publications reversed %}
{% if post.highlight == true %}
{% include archive-single.html %}
{% endif %}
{% endfor %}

---

## Theses

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

---
