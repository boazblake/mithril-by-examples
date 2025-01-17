---
title: Flight Booker from 7GUIs
date: 2021-10-18
tags: [7guis]
level: beginner
version: 2.0.4
author: ""
layout: layouts/example.html
---

Challenge: Constraints.

The task is to build a frame containing a combobox C with the two options “one-way flight” and “return flight”, two textfields T1 and T2 representing the start and return date, respectively, and a button B for submitting the selected flight. T2 is enabled iff C’s value is “return flight”. When C has the value “return flight” and T2’s date is strictly before T1’s then B is disabled. When a non-disabled textfield T has an ill-formatted date then T is colored red and B is disabled. When clicking B a message is displayed informing the user of his selection (e.g. “You have booked a one-way flight on 04.04.2014.”). Initially, C has the value “one-way flight” and T1 as well as T2 have the same (arbitrary) date (it is implied that T2 is disabled).

See <https://eugenkiss.github.io/7guis/tasks#flight>.

**To be done.**

Do you have time and are you able to implement this example?
Then fork this repo and get ready :-)
