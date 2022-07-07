{% extends "section.md" %}

{% block body %}
<table class="table table-hover">
{% for r in items %}
<tr>
  <td class='col-md-3'>{{ r.dates }}</td>
  <td>
    <strong>{{ r.place }}</strong>, {{ r.advisor }} 
    {% if r.details %}
    {% for detail in r.details %}
      <br> {{ detail }}
    {% endfor %}
    {% endif %}
  </td>

</tr>
{% endfor %}
</table>

{% endblock body %}
