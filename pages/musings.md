---
layout: page
title: musings
permalink: /musings
---
# musings

<section>
  <div class="blog-container">
    {% for post in site.posts %}
      <div class="blog-unit">
        <h4><a href="{{ site.github.url }}{{ post.url }}">{{ post.title }}</a></h4>
        <span class="blog-date">
          {% assign d = post.date | date: "%-d"  %}
          {{ post.date | date: "%B" }}
          <!-- gotta use some weird formatting to avoid extra spaces -->
          {% case d %}{%
          when '1' or '21' or '31' %}{{ d }}st{%
          when '2' or '22' %}{{ d }}nd{%
          when '3' or '23' %}{{ d }}rd{%
          else %}{{ d }}th{% endcase %},
          {{ post.date | date: "%Y" }}
        </span>
      </div>
    {% endfor %}
  </div>
</section>
