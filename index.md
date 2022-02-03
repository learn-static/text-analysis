---
layout: home-infographic
title: Home
---

{% for file in site.data.topics %}
{% assign filename = file[0] %}
{% assign foo = site.data.topics[filename] | map: 'TopicName' %}
{% for f in foo %}
{% if f != nil %}
{{ filename }}: {{ f }}
{% endif %}
{% endfor %}
{% endfor -%}


{% comment %}
{% capture whole %}{{ filename }}#{{ foo }}{% endcapture %}
{% assign wholething = whole | split: '#' %}
{% for w in wholething %}
{{ w }}
{% endfor %}
{% endcomment %}

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

{% comment %}
{% for files in site.data.topics %}
{% assign filecontent = files[1] %}
{% for f in filecontent %}
{{ f.TopicName }}
{% endfor %}
{% endfor -%}
{% endcomment %}