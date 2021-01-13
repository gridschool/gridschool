---
layout: post
tags:
- javascript
author_path: _authors/victor-de-leon.md
main_category: coding
language: en
title: How to Sort an Array in Javascript
abstract: Explore the different ways to sort Arrays in Javascript
img_url: "/uploads/javascript-logo.png"
date: 2021-01-13 07:00:00 +0000

---
## How to sort an Array in javascript

#### To sort an array in ascending order:

        const list = [1,6,3,8,3,2]
        const sortedList = list
          .slice()
          .sort((a, b) => a.upvotes - b.upvotes);

#### To sort an array in descending order:

        const list = [1,6,3,8,3,2]
        const sortedList = list
          .slice()
          .sort((a, b) => b.upvotes - a.upvotes);