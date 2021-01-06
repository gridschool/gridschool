---
layout: post
tags:
- node.js
- node
- javascript
author_path: _authors/victor-de-leon.md
main_category: coding
language: en
title: Command line Args in Node.js
abstract: An explanation of how Node.js Command Line Args work
img_url: "/uploads/node-js_logo.svg"
date: 2021-01-06 07:00:00 +0000

---
### Instructions

*  Create a file named **`app.js`**
*  Add the following code 

    console.log(process.argv)
    
    if (command === 'add') {
    	console.log('Adding Note');
    } else if (command === 'remove') {
    	console.log('Reomoving Note') 
    }

* Run the next command in your Terminal `node app.js add` 
  * It should return 'Adding Note'
* 