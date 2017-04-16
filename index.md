---
layout: page
title: Prashant Anantharaman's Blog
tagline: Trying to make the computer world more secure!
---




Here is a list of posts on this site.

<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>


