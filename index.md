---
layout: home-infographic
title: Home
---

{% for files in site.data.topics %}
{{ files[0] }}
{% endfor -%}

{% comment %}
{% for files in site.data.topics %}
{% assign filecontent = files[1] %}
{% for f in filecontent %}
{% if f.TopicName %}
{{ files[0] }}
{% endif %}
{% endfor -%}
{% endfor -%}
{% endcomment %}

{% for files in site.data.topics %}
{% assign filecontent = files[1] %}
{% for f in filecontent %}
{{ f.TopicName }}
{% endfor %}
{% endfor -%}