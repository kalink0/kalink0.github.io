---
title: The Windows Registry
---

# The Windows Registry



| Type | TTP | OS | Key |
| ---- | --- | --- | --- |
| abc | def | ghi | jkl |


Content of Registry.json

type: {{site.data.registry.hives.type[0].type}}

<ul>
<li> type html:  {{site.data.registry.hives[0].type}} </li>
</ul>

<table class="responsive-table table">
  <thead>
    <tr>
      <th scope="col">Type</th>
      <th scope="col">TTP</th>
      <th scope="col">OS</th>
      <th scope="col">Key</th>
      <th scope="col">Description</th>
    </tr>
  </thead>
  <tbody>
  {% for hive in site.data.registry.hives %}
    <tr>
      <td> {{ hive.type }} </td>
      <td> {{ hive.ttp }} </td>
      <td> 
      <table>
      {% for os in hive.os %}
      <tr><td> {{ os }} </td></tr>
      {% endfor %}
      </table>
      </td>
      <td> {{ hive.key }} </td>
      <td> {{ hive.description }} </td> 
    </tr>
    {% endfor %}
    
  </tbody>
</table>
