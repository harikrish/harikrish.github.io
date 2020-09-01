---
layout: post
title:  "MVC (Model View Controller) Design Pattern"
date:   2020-03-24 06:35:48 -0700
categories: [Programming, JavaScript]
---

Design patterns are important to write maintainable and reusable code. A pattern is a reusable solution that can be applied to commonly occurring problems in software design

MVC is composed of three components:

Model is where the application’s data objects are stored. The model doesn’t know anything about views and controllers. When a model changes, typically it will notify its observers that a change has occurred.

View is what's presented to the users and how users interact with the app. The view is made with HTML, CSS, JavaScript and often templates. 

The controller is the decision maker and the glue between the model and view. The controller updates the view when the model changes. It also adds event listeners to the view and updates the model when the user manipulates the view.

Resources
- https://developer.chrome.com/apps/app_frameworks