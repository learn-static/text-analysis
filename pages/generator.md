---
title: Include Generator
layout: about
permalink: /generator.html
custom-foot: js/data-js.html
---

<form>
  <div class="form-group">
    <select class="custom-select" id="include-type">
        <option selected>Select include type</option>
        <option value="image-upload">Uploaded Image</option>
        <option value="image-external">External Image</option>
        <option value="pdf">PDF</option>
    </select>
  </div>

  <div id="files"></div>

  <button type="submit" class="btn btn-primary">Submit</button>
</form>



<div id="topics"></div>

<div id="include-output">

<div id="button"></div>


<!--
<p>Data: <input id="data"></p>
<p>Chart type: <input id="type"></p>
<p>Topic: <input id="topic"></p>

<button type='button' class='btn btn-primary' id='generate'>Generate Include</button>

<div id="output"></div>-->