---
title: DOM Elements
desc: "This example was taken from the official website at <https://mithril.js.org/index.html#dom-elements>."
date: 2021-10-16
tags: [basics, official, m.render]
level: beginner
version: 2.0.4
author: mithril
layout: layouts/example.html
---

## HTML

~~~html
<!doctype html>
<html lang=en>
<head>
  <meta charset=utf-8>
  <title>DOM Elements</title>
</head>
<body>
</body>
</html>
~~~

## JavaScript

~~~js
let root = document.body
m.render(root, [
  m("main", [
    m("h1", {class: "title"}, "My first app"),
    m("button", "A button"),
  ])
])
~~~
