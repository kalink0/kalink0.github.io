---
title: The Windows Registry
---

# The Windows Registry

<table class="responsive-table table">
  <thead>
    <tr>
      <th scope="col">Tactic</th>
      <th scope="col">Technique</th>
      <th scope="col">OS</th>
      <th scope="col">Key</th>
      <th scope="col">Description</th>
    </tr>
  </thead>
  <tbody>
  {% for hive in site.data.registry.hives %}
    <tr>
      <td> {{ hive.tactic }} </td>
      <td> {{ hive.technique }} </td>
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
