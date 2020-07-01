---
layout: page
permalink: /table
title: Table test
---

{% assign row = site.data.ncbs-repository[0] %}

<table>
  {% for row in site.data.ncbs-repository %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>
