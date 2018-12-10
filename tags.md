---
layout: default
title: Tags
permalink: /tags/
---

<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/solid.css" integrity="sha384-rdyFrfAIC05c5ph7BKz3l5NG5yEottvO/DQ0dCrwD8gzeQDjYBHNr1ucUpQuljos" crossorigin="anonymous">
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.5.0/css/fontawesome.css" integrity="sha384-u5J7JghGz0qUrmEsWzBQkfvc8nK3fUT7DCaQzNQ+q4oEXhGSx+P2OqjWsfIRB8QT" crossorigin="anonymous">
<link rel="stylesheet" href="/css/tags.css">

{% capture cache %}
{% for tag in site.tags %}{{ tag | first }} {% endfor %}
{% endcapture %}
{% assign tags = cache | split: ' ' | sort %}

<div id="tag-list">{%
for a in tags               %}{%
  for tag in site.tags      %}{%
    assign b = tag | first  %}{%
    if a == b               %}
  <a href="#{{ tag | first }}">{{ tag | first }}<span>{{ tag | last | size }}</span></a>{%
    endif                   %}{%
  endfor                    %}{%
endfor                      %}
</div>

<div id="tag-links">{%
for c in tags               %}{%
  for tag in site.tags      %}{%
    assign d = tag | first  %}{%
    if c == d               %}{%
      assign posts = tag | last %}
  <hr>
  <div>
    <span class="tag" id="{{ d }}">{{ d | downcase }}</span>
    <ul>{%
      for post in posts     %}{%
        if post.tags contains d %}
      <li><a class="link" href="{{ post.url }}">{{ post.title }}</a> <span class="date">{{ post.date | date: "%Y/%m/%d" }}</span></li>{%
        endif               %}{%
      endfor                %}
    </ul>
  </div>{%
    endif                   %}{%
  endfor                    %}{%
endfor                      %}
</div>
