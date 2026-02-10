{% for link in site.data.publications.main %}
<div class="publication">

  {% if link.image %}
  <div class="publication-image">
    <img src="{{ link.image }}" alt="{{ link.title }}">
    {% if link.conference_short %}
    <span class="conference-short">{{ link.conference_short }}</span>
    {% endif %}
  </div>
  {% endif %}

  <div class="publication-text">
    <span class="publication-title">{{ link.title }}</span>

    <div class="publication-authors">
      {{ link.authors }}
    </div>

    <div class="publication-venue">
      {{ link.conference }}
    </div>

    <div class="publication-links">
      {% if link.pdf %}<a href="{{ link.pdf }}">PDF</a>{% endif %}
      {% if link.code %}<a href="{{ link.code }}">Code</a>{% endif %}
      {% if link.page %}<a href="{{ link.page }}">Page</a>{% endif %}
      {% if link.bibtex %}<a href="{{ link.bibtex }}">BibTeX</a>{% endif %}
      {% if link.notes %}<em>{{ link.notes }}</em>{% endif %}
    </div>
  </div>

</div>
{% endfor %}
