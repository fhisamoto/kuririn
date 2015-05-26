---
layout: page
title: Resume
---

### {{ site.data.cv.personal_data.name }}

### Education
{% for ed in site.data.cv.education %}
  - {{ ed }}
{% endfor %}

### Experience

{% for ex in site.data.cv.experience %}

#### [{{ ex.company }}]({{ ex.url }})
- position: {{ ex.position }}
- _time period: from {{ ex.time_period }}_

{{ ex.description }}
{% endfor %}