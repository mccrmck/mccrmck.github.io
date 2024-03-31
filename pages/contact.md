---
layout: page
title: Contact
permalink: /contact
images:
  - path: /assets/img/emailqr.png
    column: 1
    text: email
  - path: /assets/img/phoneqr.png
    column: 2
    text: phone
---

# Contact

<ul>
  {% for image in page.images %}
    <li class="col-{{ image.column }}" style="background-image: {{ image.path }}">
      <p>{{ image.text }}</p>
    </li>
  {% endfor %}
</ul>
