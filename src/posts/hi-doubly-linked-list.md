---
layout: layouts/post.njk
title: HI Doubly Linked List
metaTitle: doubly linked list
metaDesc: 'algorithm, doubly linked list'
date: 2019-06-20T16:17:23.536Z
tags:
  - test
---
While learning data structure I always used to think that when will I use this thing in my real life projects but recently while working in a project, I feel that here I can use a data structure and that gonna be Doubly Linked List.

## What is Doubly Linked List?

It’s a List data structure where you can traverse on both sides as you can go to the next node or to the previous node.

| This is what I understand about DLL, for more please search in Wikipedia.

## Image Editor

The project I am working is like an image editor where you can add / edit /crop/scale image and many more. So, now there is a new requirement to add feature Undo/Redo where a user can go back to history and also can move forward from history. I have to save every event’s state somewhere so when a user will press CTRL + Z or CTRL + SHIFT +Z our app has to do Undo or Redo respectively.

## Array

In first I thought of adding all the state in the array where I will push every state and whenever I have to do undo i will just pop it from array but after some thinking I thought this will be expensive as pop, slice, shift will rearrange the whole item every time I will call this method. Also, I have to keep track Array index so that I can return the exact state while undoing like if I want an item from last then I have to do is `A[currentIndex-1]`.To solve this problem I thought of some data structure and DLL was the perfect thing which will fit this requirement.

## Hello! DLL

So, whenever a user will press CTRL+Z I will call tail of our DLL and will store this node somewhere as `currentNode` so that whenever another CTRL+Z will occur we will call `currentNode.previous()` and if a user will do redo then we will call `currentNode.next()`. I just need to keep track of `currentNode`, which is the current state in an image editor and if a user will do some changes in the middle of rollback or undo then I will just create a new state and will assign it to the previous node.
