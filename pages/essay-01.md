---
title: Essay 1
layout: about
permalink: /essay-01.html
---

Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
Curabitur maximus nisl magna, at blandit quam interdum sit amet. 
Proin consequat ultricies ante, volutpat porttitor dui luctus non.

# Topics

{% assign topics = site.data.keys_1900_2000 %}

<table class="table table-striped" style="max-width: 650px;margin-left: auto;margin-right: auto;">
    <thead>
       <tr>
          <th>Topic</th>
          <th>Word Count</th>
          <th>Words</th>
       </tr>
    </thead>
    <tbody>
    {% for t in topics %}
    <tr>
       <td class="topic">{{ t.Topic }}</td>
       <td class="wordcount center">{{ t.TokenCount }}</td>
       <td class="words">{{ t.Words }}</td>
    </tr>
    {% endfor %}
    </tbody>
</table>

---

# Military

{% include feature/topic-chart.html topic="war and economics" %}

Curabitur ullamcorper maximus mi quis dapibus. Nullam tempus urna id metus pulvinar, non pretium lectus volutpat. Sed mi est, maximus ac maximus at, accumsan et diam. Donec viverra sodales enim a tempus. In eu suscipit odio. Nam augue nulla, dignissim in tempus sed, commodo nec neque. Morbi felis lectus, eleifend non efficitur varius, semper in tortor. Suspendisse maximus massa ac velit posuere, ut congue leo auctor. Praesent non magna quis lorem fringilla mattis id iaculis magna. Donec nec nisi lectus. Pellentesque non volutpat nisl.

{% include feature/image.html objectid="demo_001" width="50" %}

# Supporting Evidence

{% include feature/pdf.html objectid="demo_002" width="50" %}
