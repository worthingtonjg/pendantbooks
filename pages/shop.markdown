---
layout: default
title: Shop
permalink: /shop/
sort: 10
topmenu: true
---

{% assign sortedBooks = site.books | sort : 'bookSort' %}

{%- for post in sortedBooks -%}
    <div style="margin-bottom:50px">
        {% assign mod = forloop.index | modulo:2 %}
        {% if hideShop %}
        {% else %}
        {% if mod > 0 %}
            <div class="row">
                <div class="col" data-aos="fade-right">
                    <div class="bookTitle">{{post.title}}</div>
                    {{ post.content }}
                </div>
                <div class="col" data-aos="fade-left">
                    <img src="{{site.baseurl}}{{post.image}}" class="img-fluid">
                </div>
            </div>
        {% else %}
            <div class="row">
                <div class="col" data-aos="fade-right">
                    <img src="{{site.baseurl}}{{post.image}}" class="img-fluid">
                </div>
                <div class="col" data-aos="fade-left">
                    <div class="bookTitle">{{post.title}}</div>
                    {{ post.content }}
                </div>
            </div>        
        {% endif %}
        {% endif %}
    </div>
{%- endfor -%}
