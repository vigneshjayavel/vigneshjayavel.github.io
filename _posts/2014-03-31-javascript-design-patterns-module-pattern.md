---
title: JavaScript Design Patterns - Module Pattern
author: vigneshjayavel
description: 
post_id: 420
created: 2014/03/31 17:44:54
created_gmt: 2014/03/31 12:14:54
comment_status: open
post_name: javascript-design-patterns-module-pattern
status: publish
layout: post
---

## JavaScript Design Patterns - Module Pattern

Design patterns help you organize your application in a maintainable and scalable way. Choosing a suitable design pattern for your application is a crucial decision and is mastered by experience. You can appreciate design patterns only when you code your way out inside a complex application code-base. 

Module pattern is a famous JavaScript design pattern that has the following features.

  * Private variables (those that cannot be over-written or accessed outside of the object)
  * Single Object instance (you cannot have more than a single instance of the module that you are creating)
  * No inheritance (you get only a anonymous object that has public functions and variables. The module itself is abstracted out (since it contains private members) and it returns an object (this object has access to the private members inside the module, thanks to closure).

The following is a demo of the module pattern

What we are doing is we creating a JS tooltip using module pattern. The user hovers-in/out over a div and the div's content changes. 

Create a html page that hosts this 

{% gist vigneshjayavel/9890632 %}

Your JS code should be as follows

{% gist vigneshjayavel/9890614 %}