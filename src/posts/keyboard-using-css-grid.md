---
layout: layouts/post.njk
title: Keyboard using CSS Grid
date: 2020-02-04T16:42:58.287Z
tags:
  - css
  - grid
---
**CSS GRID**

Last week I was learning about the CSS grid which I always ignored but always wanted to learn about it. Though I do a lot of frontends, it is mostly focused with JS/React and I do very fewer design things like slicing out PSD, A HTML from UI but when I work on my pet projects I have to do all the things on my own and I find it quite hard to make layout accurate to my thinking because of margin, padding, floating and clearing: both;

I came to know CSS GRID is good to do layouts, aligning and positioning.



I made a simple Virtual keyboard to learn CSS GRID so I will be noting some key points here so I can revision it in the future.



URL to Virtual Keyboard:<https://elegant-albattani-c325d7.netlify.com/>

Github:<https://github.com/samundrak/virtual-keyboard>



![](https://lh3.googleusercontent.com/7Qg4M-UmvtInkcjIb1LPnTH5LdgacqjWJdH4wemfuARkXIRSRIbl3G4zNM3QnYjhcKRMbNa7s2quopD4HF6H7d3FSbQIXvTKXAntTp00FZtEa5q4uc8jpw4meODfXRB2xZlhIbvb "Demo")

Demo



I have taken inspiration from the image below, i.e how the layout of the keyboard will be in skeleton

![](https://lh6.googleusercontent.com/sJhVnSuFwyNRPZnJ00xFzBEqkFG59kkIth2rpcHOPztl9okZbx5VIYUFAuy2ehS6l6YK3EhofFm55kUKMLJVeBC5f1gllpKuZerUCGN15z0W3k0KvKnqeuu9IpY0j47LvrJJtjJo)



So we will have four grid areas which will be Function, Alphanumeric, Control Pad, Arrow Pad, Numpad. Grid areas
