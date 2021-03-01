---
layout: post
tags:
- macos
- git
author_path: _authors/victor-de-leon.md
main_category: coding
language: en
title: 'How to fix ''xcrun: error: invalid active developer path'''
abstract: It happens when you update your macOS or some other dependencies.
img_url: "/uploads/code.png"
date: 2021-03-01 07:00:00 +0000

---
Sometimes when you update your macOS or other dependencies you get the **xcrun: error: invalid active developer path** error.

One scenario could be if you type the **git** command on your terminal.

The reason of this error is that you no longer accept the terms of use of this tools so you are unable to use them anymore.

To fix this the easiest way is to install them again so it gets the right path.

Just execute the following command:

    $ xcode-select --install

After that you should get a window asking you to install **xcode-select.**

Once you click install it will download and install **xcode-select** which should fix the error.