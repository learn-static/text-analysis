---
title: Exploring Topics
layout: about
permalink: /exploring.html
---

{% for file in site.data.topics %}
{% assign filename = file[0] %}
{% assign topics = site.data.topics[filename] | map: 'topicname' %}
{% for t in topics %}
{% unless t == nil %}
{% capture filename %}{{ filename | remove: '_topics' }}{% endcapture %}
{% capture topic %}{{ t }}{% endcapture %}
{% include feature/line-chart.html data=filename topic=topic %}

**Include this chart**:

```
{% raw %}{% include feature/line-chart.html data="{% endraw %}{{ filename | remove: '_topics' }}{% raw %}" topic="{% endraw %}{{ t }}{% raw %}" %}{% endraw %}
```

---

{% endunless %}
{% endfor %}
{% endfor -%}