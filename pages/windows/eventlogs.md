---
title: The Windows Event Logs
---

# The Windows Event Logs



<table class="responsive-table table">
  <thead>
    <tr>
      <th scope="col">Type</th>
      <th scope="col">TTP</th>
      <th scope="col">OS</th>
      <th scope="col">ID</th>
      <th scope="col">Log Name</th>
      <th scope="col">Query</th>
      <th scope="col">Description</th>
    </tr>
  </thead>
  <tbody>
  {% for event in site.data.eventlogs.events %}
    <tr>
      <td> {{ event.type }} </td>
      <td> {{ event.ttp }} </td>
      <td> 
      <table>
      {% for os in event.os %}
      <tr><td> {{ os }} </td></tr>
      {% endfor %}
      </table>
      </td>
      <td> {{ event.ID }} </td>
      <td> {{ event.log_name }} </td>
      <td> {{ event.query }} </td>
      <td> {{ event.description }} </td> 
    </tr>
    {% endfor %}
    
  </tbody>
</table>