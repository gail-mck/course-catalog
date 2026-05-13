---
title: Arts Department
---

{% assign courses = site.data.art %}

<div class="course-grid">
{% for course in courses %}
  <div class="course-card" data-id="{{ course.id }}">
    <strong>{{ course.name }}</strong>
    <p>{{ course.blocks }} Blocks</p>
    <p>Prerequisite courses: {{ course.prereqs }} Blocks</p>
  </div>
{% endfor %}
</div>