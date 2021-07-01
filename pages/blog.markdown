---
layout: default
title: Blog
permalink: /blog/
sort: 4
---


## Blog

<div>
{%- for post in site.posts -%}

  {{post.title}}

  {{post.excerpt}}

  <a href="{{site.baseurl}}{{post.url}}">More</a>

{%- endfor -%}
</div>
