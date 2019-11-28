---
layout: layouts/post.njk
title: 'Number([undefined]) -> 0, Number([undefined,undefined]) -> NaN'
date: 2019-11-28T17:45:04.747Z
tags:
  - js
---
`Number([undefined])` is `0` because JS engine will coerce it which means
there will be some abstract operations inside engine and what it does is , it will call `toPrimitive(hint)`, here argument `hint` means what will be the expected type or what the value should be coerced to.
In JS if we try to stringify empty array then it will return empty array removing the brackets and if an array has value undefined/null then 
