---
layout: home-infographic
title: Home
---

{% comment %}
{% for files in site.data.topics %}
{{ files[0] }}
{% endfor %}
{% endcomment %}

{% comment %}
{% for file in site.data.topics %}
{% assign filename = file[0] %}
{% assign topics = site.data.topics[filename] | map: 'topicname' %}
{% for t in topics limit:2 %}
{% unless t == nil %}
{{ filename | replace: '_', ' ' | replace: 'sotu', 'State of the Union' | replace: 'party platforms', 'Party Platforms' | remove: ' all' }}
{% endunless %}
{% endfor %}
{% endfor -%}
{% endcomment %}

{% comment %}
{% for file in site.data.topics %}
{% assign filename = file[0] %}
{% assign foo = site.data.topics[filename] | map: 'topicname' %}
{% for f in foo %}
{% if f != nil %}
{{ filename }}: {{ f }}
{% endif %}
{% endfor %}
{% endfor -%}
{% endcomment %}


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
{% if f.topicname %}
{{ files[0] }}
{% endif %}
{% endfor -%}
{% endfor -%}
{% endcomment %}

{% comment %}
{% for files in site.data.topics %}
{% assign filecontent = files[1] %}
{% for f in filecontent %}
{{ f.topicname }}
{% endfor %}
{% endfor -%}
{% endcomment %}