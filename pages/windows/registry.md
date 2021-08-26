---
title: The Windows Registry
---

# The Windows Registry



| Type | TTP | OS | Key | Date |
| ---- | --- | --- | --- | ---- |
{% for hive in site.data.registry.hives %}
| {{hive.type}} | {{hive.ttp}} | {{hive.os}} | {{hive.key}} |

{% endfor %}