{% extends "section.md" %}

{% block body %}
<table class="table table-hover">
{% for item in items %}
<tr>
  <td>
    {% if item.url %}
        <a href="{{ item.url }}">{{ item.name }}</a> <p></p>{{ item.details }}
    {% else %}
        {{ item.name }} {{item.details }}
    {% endif %}
  </td>
  <td class='col-md-1' style='text-align:right;'>{{ item.year }}</td>
</tr>
{% endfor %}
</table>
{% endblock body %}
