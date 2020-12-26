---
layout: post
tags:
  - coding
  - jekyll
author_path: _authors/victor-de-leon.md
main_category: coding
language: en
title: Connect to local Jekyll server from a mobile device
abstract:
  Instructions to connect to a local Jekyll development server from a mobile
  device (Using a Mac).
img_url: "/uploads/html-rich-text.webp"
date: 2020-12-26 07:00:00 +0000
---

1. In your Terminal run:

   jekyll serve --host=0.0.0.0

2. Then open **Network Preferences** and copy the IP Address of the wifi that you are connected to.
3. Paste that IP Address in your browser and add the port your Jekyll app is running at, it looks like this:

   http://**0.0.0.0:4000** (The 0.0.0.0 should be your IP Address).

And that's it!
