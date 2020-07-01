---
layout: page
permalink: /table
title: Table test
---

{% assign row = site.data.ncbs-repository %}

<table>
  {% for row in site.data.ncbs-repository %}
    {% if forloop.first %}
    <thead>
      <tr>
        {% for pair in row %}
          <th>{{ pair[0] }}</th>
        {% endfor %}
      </tr>
    </thead>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}

  {% endfor %}
</table>
