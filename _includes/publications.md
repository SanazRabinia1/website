<h2 id="publications" style="margin: 2px 0px -15px;">Publications</h2>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>

<div class="pub-row">

  <!-- Publication Image -->
  <div class="col-sm-3 abbr"
       style="position: relative; padding-right: 15px; padding-left: 15px;">

    {% if link.image %}
    <img src="{{ link.image }}"
         class="teaser img-fluid z-depth-1"
         style="width: 100%; height: auto;">

      {% if link.conference_short %}
      <abbr class="badge">
        {{ link.conference_short }}
      </abbr>
      {% endif %}

    {% endif %}

  </div>


  <!-- Publication Information -->
  <div class="col-sm-9"
       style="position: relative; padding-right: 15px; padding-left: 20px;">

    <!-- Title -->
    <div class="title">

      {% if link.pdf %}
      <a href="{{ link.pdf }}" target="_blank">
        {{ link.title }}
      </a>

      {% else %}
      {{ link.title }}
      {% endif %}

    </div>


    <!-- Authors -->
    <div class="author">
      {{ link.authors }}
    </div>


    <!-- Journal / Conference -->
    <div class="periodical">
      <em>{{ link.conference }}</em>
    </div>


    <!-- PDF + Code + Accepted -->
    <div class="links"
         style="
           display: flex;
           align-items: center;
           flex-wrap: wrap;
           gap: 7px;
           margin-top: 5px;
         ">

      {% if link.pdf %}
      <a href="{{ link.pdf }}"
         class="btn btn-sm z-depth-0"
         role="button"
         target="_blank"
         style="font-size: 12px;">
        PDF
      </a>
      {% endif %}


      {% if link.code %}
      <a href="{{ link.code }}"
         class="btn btn-sm z-depth-0"
         role="button"
         target="_blank"
         style="font-size: 12px;">
        Code
      </a>
      {% endif %}


      {% if link.notes %}
      <strong style="margin-left: 6px;">
        <i style="color: #e74d3c;">
          {{ link.notes }}
        </i>
      </strong>
      {% endif %}

    </div>

  </div>

</div>

</li>

<br>

{% endfor %}

</ol>
</div>
