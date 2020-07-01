---
layout: page
permalink: /table
title: Table test
---

{% assign row = site.data.authors[0] %}
{{ row | inspect }}

{% for pair in row %}
  {{ pair | inspect }}
{% endfor %}


<table>
  {% for row in site.data.authors %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}
  {% endfor %}
</table>
