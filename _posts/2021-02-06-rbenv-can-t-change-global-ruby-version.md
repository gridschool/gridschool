---
layout: post
tags:
- ruby
- mac
author_path: _authors/victor-de-leon.md
main_category: coding
language: en
title: rbenv can't change global ruby version
abstract: If you installed a ruby version in your mac using rbenv you may encounter
  with this issue.
img_url: "/uploads/ruby-logo.png"
date: 2021-02-06 07:00:00 +0000

---
### Problem

I installed a ruby version using **rbenv** and it keeps returning the Mac OS X default ruby version.

### Solution

You need to add the following lines to your `~/.bash_profile.`

    export PATH="$HOME/.rbenv/bin:$PATH"
    eval "$(rbenv init -)"