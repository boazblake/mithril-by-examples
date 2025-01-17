---
title: Counter from 7GUIs
date: 2021-10-18
tags: [7guis, m.mount]
level: beginner
version: 2.0.4
author: narayand16
layout: layouts/example.html
---

Challenge: Understanding the basic ideas of a language/toolkit.

The task is to build a frame containing a label or read-only textfield T and a button B. Initially, the value in T is “0” and each click of B increases the value in T by one.

See <https://eugenkiss.github.io/7guis/tasks#counter>.

## HTML

~~~html
<!doctype html>
<html lang=en>
<head>
  <meta charset=utf-8>
  <title>Counter</title>
</head>
<body>
</body>
</html>
~~~

## JavaScript

~~~js
let root = document.body
let count = 0

let Counter = {
  view: function() {
    return m("main", [
      m("input[readonly=true]", {
        value: count
      }),
      m("button", {
        onclick: function() {count++}
      }, "Count")
    ])
  }
}

m.mount(root, Counter)

~~~
