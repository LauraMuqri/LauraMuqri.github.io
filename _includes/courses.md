---
layout: page
title: Courses
permalink: /courses/
---

{% for course in site.data.courses.main %}
<div class="course-card">
  <h3> {{ course.title }}</h3>
  <p><strong>{{ course.code }}</strong> — {{ course.program }}</p>

  {% if course.image %}
  <img src="{{ course.image }}" alt="{{ course.title }}" style="max-width:300px;">
  {% endif %}

  <p>
    <a href="{{ course.page }}"> Course page</a>
    {% if course.notes %}
      · <em>{{ course.notes }}</em>
    {% endif %}
  </p>
</div>
<hr>
{% endfor %}
