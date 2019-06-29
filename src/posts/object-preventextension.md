---
layout: layouts/post.njk
title: Object.preventExtension
metaTitle: 'object.preventExtension, javascript, immutable'
metaDesc: 'object.preventExtension, javascript, immutable'
date: 2019-06-24T16:42:58.173Z
tags:
  - object.preventExtension
  - javascript
  - immutable
---

This methods helps us to prevent adding new properties
to the object. Though it will not throw error in normal
case but will throw error if it is used in 'use strict'.
Changing value of already added property is fine and it won't
throw any error.

```js
const object = {
  a: 1
};
Object.preventExtensions(object);

console.log(object); // {a:1}
object.a = 2; // valid
object.b = 2; // invalid as it doesn't allow to add new properties
object.method = function() {}; // still invalid
console.log(object); // {a:2}
```

Using `preventExtension` for the object instansiated from class will still prevent the object from having new properties but new property can be added to the class and that can be access with
object which was used for `preventExtension`.

```js
class Test {
  constructor() {
    this.a = 2;
  }
}
const test1 = new Test();
console.log(test1); // { a: 2 }
Test.prototype.b = 3;
console.log(test1); // { a: 2 }, property b is added to proto
Object.preventExtensions(test1);

test1.c = 4; // invalid as it is locked for extension
console.log(test1.c); // undefined

Test.prototype.c = 4;
console.log(test1.c); // outputs 4, as it is accessed from proto
```
