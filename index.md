---
layout: page
title: Abe's Posts!
tagline: Rambler, developer and gamer
---
{% include JB/setup %}

[Github](http://github.com/abepetrillo)
[LinkedIn](http://ie.linkedin.com/in/abrahampetrillo)
[Facebook](http://facebook.com/abe.petrillo)
[Twitter](http://twitter.com/AbePetrillo)

<ul class="posts">
  {% for post in site.posts %}
    <li>
      <span>{{ post.date | date_to_string }}</span> 
      &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>


