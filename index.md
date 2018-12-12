---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: default
---

<div id="home">
  <h2><i class="fa fa-bookmark" style="color: #C00000;"></i> Blog Posts</h2>
  <ul id="blog-posts" class="posts">
    {% for post in site.posts %}
      <li><span>{{ post.date | date: "%Y-%m-%d" }} &raquo;</span> <a href="{{ post.url }}">{{ post.title }}</a></li>
    {%- endfor -%}
  </ul>
</div>
