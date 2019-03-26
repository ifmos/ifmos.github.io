---
layout: post
date: 2019-03-26 15:08:59 +0800
title: class-and-prototype
categories:
  - front-end
tags:
  - class
  - prototype
  - javascript
---

<script>
// 继承
function Parent (name) {
  this.name = name
}

function Child (name) {
  Parent.call(this, name)
}

Child.prototype = Object.create(Parent.prototype, {
  constructor: {
    value: Child,
    enumerable: false,
    writable: true,
    configurable: true
  }
})

console.log(new Child('Mos'))
</script>
