---
layout: default
title: Category
permalink: /category/
---

<link rel="stylesheet" href="/css/category.css">

{% capture cache %}
{% for category in site.categories %}{{ category | first }} {% endfor %}
{% endcapture %}
{% assign categories = cache | split: ' ' | sort %}

<div id="category-list">{%
for a in categories                 %}{%
  for category in site.categories   %}{%
    assign b = category | first     %}{%
    if a == b                       %}
  <a href="#{{ a | replace: '/', '-' }}">{{ a }}<span>{{ category | last | size }}</span></a>{%
    endif                           %}{%
  endfor                            %}{%
endfor                              %}
</div>

<div id="category-links">{%
for c in categories                 %}{%
  for category in site.categories   %}{%
    assign d = category | first     %}{%
    if c == d                       %}{%
      assign posts = category | last %}
  <hr>
  <div>
    <span class="category" id="{{ d | replace: '/', '-' }}">{{ d | downcase }}</span>
    <ul>{%
      for post in posts             %}{%
        if post.categories contains d %}
      <li><a class="link" href="{{ post.url }}">{{ post.title }}</a> <span class="date">{{ post.date | date: "%Y-%m-%d" }}</span></li>{%
      endif                         %}{%
    endfor                          %}
    </ul>
  </div>{%
    endif                           %}{%
  endfor                            %}{%
endfor                              %}
</div>
