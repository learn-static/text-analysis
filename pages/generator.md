---
title: Include Generator
layout: about
permalink: /generator.html
custom-foot: js/include-js.html
---

<div class="row justify-content-center">
  <div class="col-md-6">
    <p>Use the form below to generate "include" code for images and documents. For specific instructions see documentation at <a href="https://learn-static.github.io/writing-with-visualizations/content/essay/includes.html">https://learn-static.github.io/writing-with-visualizations/content/essay/includes.html</a>.</p>
    <div class="form-group pt-3">
    <select class="custom-select" id="include-type">
        <option value="">Select include type</option>
        <option value="image">Image</option>
        <option value="pdf">PDF</option>
    </select>
    </div>
    <div id="form-content"></div>
  </div>
  <div class="col-md-10">
    <div id="include-output" class="pt-4"></div>
  </div>
</div>