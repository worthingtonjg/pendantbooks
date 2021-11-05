---
layout: default
title: Shop
permalink: /shop/
sort: 10
topmenu: true
---

{% assign sortedBooks = site.books | sort : 'bookSort' %}

{% assign i = 1 %}
{%- for post in sortedBooks -%}
    <div style="margin-bottom:50px">
        {% if post.hideShop == true %}
        {% else %}
        {% assign i = i | plus:1 %}
        {% assign mod = i | modulo:2 %}
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
