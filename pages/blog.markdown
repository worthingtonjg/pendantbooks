---
layout: default
title: Blog
permalink: /blog/
sort: 4
---


## Blog

{%- for post in site.posts -%}

  {{post.title}}

  {{post.excerpt}}

  <a href="{{post.url}}">More</a>

{%- endfor -%}
