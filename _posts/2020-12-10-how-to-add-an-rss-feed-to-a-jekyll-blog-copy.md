---
layout: post
title: How to add an RSS feed to a Jekyll blog
abstract: test this is a test test test.
img_url: "/uploads/obi-onyeador-ueqvutrs224-unsplash.jpg"
date: 2020-12-10T07:00:00.000+00:00
main_category: coding
categories: "jekyll rss "
featured: true
tags:
  - jekyll
  - rss
  - coding
author_path: _authors/victor-de-leon.md
---

Add his line to your site's Gemfile:

    gem 'jekyll-feed'

And then add this line to your site’s `_config.yml`:

    plugins:
    	-jekyll-feed
