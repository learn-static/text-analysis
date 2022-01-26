---
title: Exploring the Data
layout: about
permalink: /exploring.html
---

Data: <input id="data">
Chart type: <input id="type">
Topic: <input id="topic">

<button type="button" id="generate">Generate Include</button>

<div id="output"></div>

<script>
function generateInclude() {
    var include_type = document.getElementById('type').value;
    var include_data = document.getElementById('data').value;
    var include_topic = document.getElementById('topic').value;

    var include = '{% raw %}{% include feature/' + include_type + '.html data="' + include_data + '" topic="' + include_topic + '" %}{% endraw %}';

    document.getElementById('output').innerHTML = include;
};

document.getElementById('generate').addEventListener('click', generateInclude);

</script>