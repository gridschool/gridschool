---
layout: post
tags:
- coding
- javascript
author_path: _authors/victor-de-leon.md
main_category: coding
title: Javascript post
abstract: a test post to filter javascript
img_url: "/uploads/jekyll-github-pages.webp"
date: 2020-12-21T07:00:00.000+00:00

---
this is a javascript post

    console.log('hello world');

more code here:

    <div class="featured-container">
        {% for post in site.posts %}
            {% for tag in post.tags %}
                {% if page.name == tag and forloop.index <= 2 %}
                    {% include post-item.html %}
                {% endif %}
            {% endfor %}
        {% endfor %}
        {% include ad-medium.html %}
    </div>

![alt text of the pic](/uploads/jekyll-github-pages.webp "a picture")

# how does it look

## good?