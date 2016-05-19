---
layout: page
title: Contents
---
Welcome to the contents page. Below is every post on this site, shown in a hierarchical alphabetical order.

{% for collection in site.collections %}

  {% if collection.label != 'posts' %}

            {% assign sortedPosts = collection.docs| sort: 'url' %}
            {% for post in sortedPosts %}    

            {% assign listclass = 'post' %}
            {% assign spliturl = post.url | split: '/' %}
            {% if spliturl.size == 4 %}
                {% assign listclass = 'subpost' %}
            {% elsif  spliturl.size == 5 %}
                {% assign listclass = 'subsubpost' %}
            {% elsif  spliturl.size == 6 %}
                {% assign listclass = 'subsubsubpost' %}    
            {% endif %}   
                        - {{post.title}}                        
              {% endfor %}
     {% endif %}
{% endfor %}