---
title: Exploring the Data
layout: about
permalink: /exploring.html
---

<p>
    Include type: <select id="includetype">
        <option value="" selected="selected">Select include type</option>
        <option value="line-chart" id="line-chart">Line Chart</option>
        <option value="topic-table" id="topic-table">Topic Table</option>
        <option value="image" id="image">Image</option>
        <option value="pdf" id="pdf">PDF</option>
    </select>
    <input type="submit" value="Submit">
</p>
<p>
    Data: <select id="filename">
        <option value="" selected="selected">Select data file</option>
    </select>
</p>

<!--
<p>Data: <input id="data"></p>
<p>Chart type: <input id="type"></p>
<p>Topic: <input id="topic"></p>

<button type="button" class="btn btn-primary" id="generate">Generate Include</button>

<div id="output"></div>-->

<script>
var allTopics = [
    {%- for t in site.data.topic-data -%}
    {% capture filename %}{{ t.filename-topics }}{% endcapture %}
    {%- assign topicdata = site.data.topics[filename] | where_exp: "item", "item.TopicName" -%}
    {% capture topicnames %}[{% for f in topicdata %}{{ f.TopicName | jsonify }}{% unless forloop.last %}, {% endunless %}{% endfor %}]{% endcapture %}
    {% capture filename-topics %}{% for f in topicdata %}{% if forloop.first %}{{ filename }}:{{ topicnames }}*{% endif %}{% endfor %}{% endcapture %}
    {%- assign finaltopics = filename-topics | split: "*" -%}
    {%- for a in finaltopics -%}{ "filename":{{ a | split: ":" | first | jsonify }}, "topics":{{ a | split: ":" | last }} },{%- endfor -%}{% endfor %}
];

for (let i = 0; i < allTopics.length; i++) {
    function createDropItem(name) {
        var option = document.createElement('option');
        option.textContent = name;
        return option;
    };
    var filename_id = document.getElementById("filename");
    filename_id.appendChild(createDropItem(allTopics[i].filename));
};

/*
function generateInclude() {
    var include_type = document.getElementById('type').value;
    var include_data = document.getElementById('data').value;
    var include_topic = document.getElementById('topic').value;

    var include = '{% raw %}{% include feature/' + include_type + '.html data="' + include_data + '" topic="' + include_topic + '" %}{% endraw %}';

    document.getElementById('output').innerHTML = include;
};

document.getElementById('generate').addEventListener('click', generateInclude);
*/
</script>