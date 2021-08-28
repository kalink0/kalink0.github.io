---
title: The Windows Event Logs
datatable: true
---

# The Windows Event Logs

## Further Links
[[Microsoft Security Auditing Overview](https://docs.microsoft.com/en-us/windows/security/threat-protection/auditing/security-auditing-overview)]

## Overview Events
<table class="display">
  <thead>
    <tr>
      <th scope="col">Tactic</th>
      <th scope="col">Technique</th>
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
      <td> {{ event.tactic }} </td>
      <td> {{ event.technique }} </td>
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
