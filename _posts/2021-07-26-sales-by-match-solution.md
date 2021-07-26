---
layout: post
tags:
- challenges
- javascript
- coding
author_path: _authors/victor-de-leon.md
main_category: coding
language: en
title: Sales by Match (Solution)
abstract: Solution of the sales by match hackerrank challenge.
img_url: "/uploads/code.png"
date: 2021-07-26 06:00:00 +0000

---
    let n = 9; // Number of items on ar
    let ar = [10,20,20,10,10,30,50,10,20]; // Array of random numbers, (will refer to each number as type)
    
    let pairTypes = []; // Array variable to store pair types
    let pairTypesObj = []; // Array variable to store objects by type
    let pairs = 0; // Variable to accumulate number of pairs
    
    function sockMerchant(n, ar) {
        for (let i = 0; i < n; i++) { // Iterates over ar
            if (!pairTypes.includes(ar[i])) { // Checks if pairType has been pushed to the pairTypes array
                pairTypes.push(ar[i]); // Pushes to pairTypes array
                pairTypesObj.push({type: ar[i], count:0}); // Creates pair type object with the count property
            }
        }
        for (let i = 0; i < n; i++) { 
            for (let j = 0; j < pairTypesObj.length; j++) { // Iterates over the objects pairTypesObj
              if (ar[i] == pairTypesObj[j].type) { // Check If current Type in the array is equal to the pair types object
                pairTypesObj[j].count++; // If so increment the count property by one
                if (pairTypesObj[j].count == 2) { // Check If the pair type object count property is equal to 2 
                  pairs++; // If so then increment pairs by one
                }
              }
              if (pairTypesObj[j].count == 2) {  // Check if pairTypesObj is equal to 2
                pairTypesObj[j].count = 0; // If so then reset it to 0 so it doesn't add aditional pairs
              }
            }
        }
        return pairs;
    }
    
    console.log(sockMerchant(n, ar));
    
    