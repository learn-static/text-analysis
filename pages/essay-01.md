---
title: Essay 1
layout: about
permalink: /essay-01.html
---

{% include feature/pdf.html filename="demo_002.pdf" caption="demo" alt="Document representing demo" width="100" %}

Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
Curabitur maximus nisl magna, at blandit quam interdum sit amet. 
Proin consequat ultricies ante, volutpat porttitor dui luctus non.

{% include feature/topic-table.html data="party-platforms-20th-century-all" topics="families;governing;security and defense;freedom and prosperity" %}

---

{% include feature/line-chart.html data="sotu-20th-century" topic="America at war" %}

{% include feature/line-chart.html data="party-platforms-20th-century-all" topic="security and defense" %}

{% include feature/radar-chart.html data="party-platforms-20th-century-all" years="1964;1972" topics="governing;freedom and prosperity;security and defense" %}

{% include feature/radar-chart.html data="sotu-20th-century" years="1905;1945;1969;1990" topics="America at war;America as world power;labor in America;American economy" %}

Curabitur ullamcorper maximus mi quis dapibus. Nullam tempus urna id metus pulvinar, non pretium lectus volutpat. Sed mi est, maximus ac maximus at, accumsan et diam. Donec viverra sodales enim a tempus. In eu suscipit odio. Nam augue nulla, dignissim in tempus sed, commodo nec neque. Morbi felis lectus, eleifend non efficitur varius, semper in tortor. Suspendisse maximus massa ac velit posuere, ut congue leo auctor. Praesent non magna quis lorem fringilla mattis id iaculis magna. Donec nec nisi lectus. Pellentesque non volutpat nisl.

{% include feature/image.html objectid="demo_001" width="50" %}

# Supporting Evidence

{% include feature/pdf.html objectid="demo_002" width="50" %}
