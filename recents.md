---
layout: default
title: Recents
permalink: /recents/
---

<link rel="stylesheet" href="/css/recents.css">

{% for post in site.posts          %}{%
  capture month  %}{{ post.date | date: '%m%Y'      }}{% endcapture %}{%
  capture nmonth %}{{ post.next.date | date: '%m%Y' }}{% endcapture %}{%
  if month != nmonth            %}{%
    if forloop.index != 1         %}
  </ul>{%
    endif                         %}
<h3>{{ post.date | date: '%Y년 %m월' }}</h3><ul>{%
  endif %}
  <li><a href="{{ post.url }}">{{ post.title }}</a> <span class="date">{{ post.date | date: "%Y-%m-%d" }}</span>
    <ul class="tags post-tags cf">{%
      for tag in post.tags %}
      <li><a href="/tags/#{{ tag }}">{{ tag | downcase }}</a></li>{%
      endfor %}
    </ul>
  </li>{%
endfor %}
