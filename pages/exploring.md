---
title: Exploring the Data
layout: about
permalink: /exploring.html
custom-foot: js/data-js.html
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
<p>
    <div id="topics"></div>
</p>



<!--
<p>Data: <input id="data"></p>
<p>Chart type: <input id="type"></p>
<p>Topic: <input id="topic"></p>

<button type="button" class="btn btn-primary" id="generate">Generate Include</button>

<div id="output"></div>-->