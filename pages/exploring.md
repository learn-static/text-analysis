---
title: Exploring the Data
layout: about
permalink: /exploring.html
---

<p>Data: <input id="data"></p>
<p>Chart type: <input id="type"></p>
<p>Topic: <input id="topic"></p>

<button type="button" class="btn btn-primary" id="generate">Generate Include</button>

<div id="output"></div>

<script>
var allTopics = {
    {%- for t in site.data.topic-data -%}{% capture topicfile %}{{ t.filename-topics }}{% endcapture %}
    {{ t.name | jsonify }} : { {% for item in site.data.topics[topicfile] %}{% if item.TopicName %} "topicname": {{ item.TopicName | escape | jsonify }} {% endif %}{% endfor %}}{% unless forloop.last %},{% endunless %}
    {%- endfor -%}
};

function generateInclude() {
    var include_type = document.getElementById('type').value;
    var include_data = document.getElementById('data').value;
    var include_topic = document.getElementById('topic').value;

    var include = '{% raw %}{% include feature/' + include_type + '.html data="' + include_data + '" topic="' + include_topic + '" %}{% endraw %}';

    document.getElementById('output').innerHTML = include;
};

document.getElementById('generate').addEventListener('click', generateInclude);

</script>