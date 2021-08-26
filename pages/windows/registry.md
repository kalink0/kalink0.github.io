---
title: The Windows Registry
---

# The Windows Registry



| Type | TTP | OS | Key |
| ---- | --- | --- | --- |
{% for hive in site.data.registry.hives %}
| {{hive.type}} | {{hive.ttp}} | {{hive.os}} | {{hive.key}} |

{% endfor %}