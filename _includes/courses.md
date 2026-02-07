{% for course in site.data.courses.main %}
<div class="publication">

  {% if course.image %}
  <div class="publication-image-wrapper">
    <img src="{{ course.image }}" class="publication-image">
    <span class="conference-short">{{ course.code }}</span>
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
      <a href="{{ course.page }}"> Course page</a>
      {% if course.notes %} · <em>{{ course.notes }}</em>{% endif %}
    </div>
  </div>

</div>
{% endfor %}

