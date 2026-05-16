---
title: Art Courses
---
<!-- Above tells Jekyll I am starting a page and titles it -->

<!-- Makes a variable called courses that contains all the course data for art -->
{% assign courses = site.data.art %}

<!-- Define a container that is a grid for the art courses -->
<div class="course-grid">

  <!-- Iterate through all the courses to make them into container classes with their own data attributes -->
{% for course in courses %}
  <div class="course-card"
    data-id="{{ course.id }}"
    data-name="{{ course.name }}"
    data-blocks="{{ course.blocks }}"
    data-prereqs="{{ course.prereqs }}"
    data-coreqs="{{ course.coreqs }}"
    data-notes="{{ course.notes }}"
    data-description="{{ course.description | escape }}">
    <!-- Escape in the last line tells Jekyll the course description is plain text, not html. -->
    <strong>{{ course.name }}</strong>
    <p>{{ course.blocks }} block(s)</p>
    <p style="font-size:0.75rem; color: #999">Prereq: {{ course.prereqs }}</p>
  </div>
{% endfor %}
</div>
