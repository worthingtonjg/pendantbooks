---
layout: default
title: Home
sort: 0
---

{%- for post in site.books -%}
    <div style="margin-bottom:25px">
        <div class="row">
            <div class="col" data-aos="fade-right">
                <h2>{{post.title}}</h2>
                {{ post.excerpt }}
                <a href="{{post.url}}">Shop</a>
            </div>
            <div class="col" data-aos="fade-left">
                <img src="{{post.image}}" class="img-fluid">
            </div>
        </div>
    </div>
{%- endfor -%}