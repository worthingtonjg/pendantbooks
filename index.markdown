---
layout: default
title: Home
sort: 0
---
{% assign sortedBooks = site.books | sort : 'bookSort' %}

{%- for post in sortedBooks -%}
    <div style="margin-bottom:50px">
        {% if post.sectionBanner1 %}
        <div class="row">
            <div class="sectionBanner1">
                {{post.sectionBanner1}}
            </div>
        </div>
        {% endif %}   
        {% if post.sectionBanner2 %}
        <div class="row">
            <div class="sectionBanner2">
                {{post.sectionBanner2}}
            </div>
        </div>
        {% endif %}   
        {% if post.redBanner %}
        <div class="row">
            <div class="redBanner">
                {{post.redBanner}}
            </div>
        </div>
        {% endif %}        
        {% if post.blackBanner %}
        <div class="row">
            <div class="blackBanner">
                {{post.blackBanner}}
            </div>
        </div>
        {% endif %}        
        <div class="row">
            <div class="col" data-aos="fade-right">
                <div class="bookTitle">{{post.title}}</div>
                {{ post.excerpt }}
                {% if post.hideShop == true %}
                {% else %}
                <div class='shop'>
                    <a class='shop' href="{{site.baseurl}}{{post.url}}">SHOP</a>
                </div>
                {% endif %}
            </div>
            <div class="col" data-aos="fade-left">
                <img src="{{site.baseurl}}{{post.image}}" class="img-fluid">
            </div>
        </div>
    </div>
{%- endfor -%}