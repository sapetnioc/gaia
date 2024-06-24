---
layout: page_select
title:
permalink: /people/
---

{% assign people_sorted = site.people | sort: 'joined' %}
{% assign people_array = "pi|postdoc|gradstudent|engineer|alumni" | split: "|" %}

{% for item in people_array %}

<div class="pos_header">
{% if item == 'postdoc' %}
    <h3>Postdoctoral Fellows</h3>
{% elsif item == 'pi' %}
    <h3>Principal Investigators</h3>
{% elsif item == 'gradstudent' %}
    <h3>Graduate Students</h3>
{% elsif item == 'engineer' %}
    <h3>Research Engineers</h3>
{% elsif item == 'visiting' %}
    <h3>Visiting Scholars</h3>
{% elsif item == 'alumni' %}
    <h3>Alumni</h3>
{% endif %}
</div>

<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains item %}
    <div class="list-item-people {{profile.cat|replace: ' ', '-'}} {{profile.subcat|replace: ' ', '-'}}">
      <p style="text-align: left; padding-left: 5em; margin: 0;">
          {% if profile.site %}
            <a class="name" href="{{profile.site}}" target="_blank">
          {% endif %}
          {{profile.name}}
          {% if profile.desc %}
          - {{profile.desc}}
          {% endif %}
          {% if profile.site %}
            </a>
          {% endif %}
      </p>
    </div>
    {% endif %}
  {% endfor %}
</div>
<hr>

{% endfor %}
