---
layout: post
tags:
- javascript
- css
author_path: _authors/victor-de-leon.md
main_category: coding
language: en
title: Scroll Behavior not working on Safari
abstract: Instructions about how to fix scroll behavior not working on safari
img_url: "/uploads/code.png"
date: 2021-09-07 06:00:00 +0000

---
I was developing a card scroller and everything was fine until I tested it in safari.

Initially I just used the css property  `scroll-behavior: smooth;` and it worked fine in chrome but when I tested in safari it didn't work.

The reason is that `scroll-behavior: smooth;` is not supported in Safari yet.

The solution was to import the Polyfill with npm, in my case I was working with angular2+.

    npm install smoothscroll-polyfill
    npm install @types/smoothscroll-polyfill

Then in the component where I intended to use it 

    import * as smoothscroll from 'smoothscroll-polyfill';
    
     constructor() {
     	smoothscroll.polyfill();
     }
      
     