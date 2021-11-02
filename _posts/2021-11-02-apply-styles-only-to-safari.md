---
layout: post
tags:
- css
- coding
- safari
author_path: _authors/victor-de-leon.md
main_category: coding
language: en
title: Apply styles only to safari
abstract: Use this hack to apply styles only to safari
img_url: "/uploads/code.png"
date: 2021-11-02 07:00:00 +0000

---
Sometimes you need to apply specific styles to Safari, in order to accomplish that you can use this hack:

    @media not all and (min-resolution:.001dpcm) { 
         @supports (-webkit-appearance:none) {
              ...Your Css specific to safari code here
         }
    }