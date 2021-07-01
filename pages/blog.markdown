---
layout: default
title: Blog
permalink: /blog/
sort: 4
---


## Blog

{%- for post in site.posts -%}
  <div>

  <h1>{{post.title}}</h1>

  {{post.excerpt}}

  <a href="{{site.baseurl}}{{post.url}}">More</a>
  </div>

{%- endfor -%}
