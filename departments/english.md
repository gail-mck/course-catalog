---
title: English Courses
---

{% assign courses = site.data.english %}

<div class="course-grid">
{% for course in courses %}
  <div class="course-card"
    data-id="{{ course.id }}"
    data-name="{{ course.name }}"
    data-blocks="{{ course.blocks }}"
    data-prereqs="{{ course.prereqs }}"
    data-coreqs="{{ course.coreqs }}"
    data-notes="{{ course.notes }}"
    data-description="{{ course.description | escape }}">
    <strong>{{ course.name }}</strong>
    <p>{{ course.blocks }} block(s)</p>
    <p style="font-size:0.75rem; color: #999;">Prereq: {{ course.prereqs }}</p>
  </div>
{% endfor %}
</div>