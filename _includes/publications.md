<h2 id="publications" style="margin: 2px 0px -15px;">Courses</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    {% if link.image %} 
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% if link.conference_short %} 
    <abbr class="badge">{{ link.conference_short }}</abbr>
    {% endif %}
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
     <div class="publication-links">
  {% if link.Syllabus %}
    <a href="{{ link.Syllabus }}">Syllabus</a>
  {% endif %}

  {% if link.LectureNotes %}
    <a href="{{ link.LectureNotes }}">Lecture Notes</a>
  {% endif %}

  {% if link.Codes %}
    <a href="{{ link.Codes }}">Codes</a>
  {% endif %}

  {% if link.notes %}
    <em>{{ link.notes }}</em>
  {% endif %}
</div>

      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>
<br>

{% endfor %}

</ol>
</div>
