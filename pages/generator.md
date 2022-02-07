---
title: Include Generator
layout: about
permalink: /generator.html
custom-foot: js/include-js.html
---

<div class="row justify-content-center">
  <div class="col-md-6">
    <p>Use the form below to generate "include" code for images and documents.</p>
    <div class="form-group">
      <select class="custom-select" id="include-type">
          <option selected>Select include type</option>
          <option value="image-upload">Uploaded Image</option>
          <option value="image-external">External Image</option>
          <option value="pdf">PDF</option>
      </select>
    </div>
    <div id="form-content"></div>
    <div id="include-output" class="pt-3"></div>
  </div>
</div>