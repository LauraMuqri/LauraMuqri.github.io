{% for course in site.data.courses.main %}
<div class="publication">

  {% if course.image %}
  <div class="publication-image">
    <img src="{{ course.image }}" alt="{{ course.title }}">

    {% if course.code %}
    <span class="conference-short">
      {{ course.code }}
    </span>
    {% endif %}
  </div>
  {% endif %}

  <div class="publication-text">
    <span class="publication-title">
      {{ course.title }}
    </span>

    <div class="publication-authors">
      {{ course.program }}
    </div>

    <div class="publication-links">
      <a href="{{ course.page }}">🧠 Course page</a>
      {% if course.notes %}
        · <em>{{ course.notes }}</em>
      {% endif %}
    </div>
  </div>

</div>
{% endfor %}
