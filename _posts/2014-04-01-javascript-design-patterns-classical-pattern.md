---
title: JavaScript Design Patterns - Classical Pattern
author: vigneshjayavel
description: 
post_id: 468
created: 2014/04/01 17:22:01
created_gmt: 2014/04/01 11:52:01
comment_status: open
post_name: javascript-design-patterns-classical-pattern
status: publish
layout: post
---

## JavaScript Design Patterns - Classical Pattern

Unlike the Prototype pattern, the "Classical" pattern is easy to read for somebody from a class-based language background. It provides you with most of the features of a real O-O model. Here we make use of a 3rd party library called Base.js (A base class for JS inheritance, [download it here](http://dean.edwards.name/base/Base.js)) that provides Classical pattern implementation off the shelf. So, we need not write the required "core" from scratch. Features of the classical pattern: 

  * Inheritance.
  * Removes the need to redefine constructors in the child class. (You can call the base class constructor from the child class just like the way you do in a class-based language)
  * Cleaner than Prototype pattern.
  * Can support multiple inheritance (I guess Base.js allows that)
IMO classical pattern is a syntactic sugar on top of prototype pattern. Lets look at how our Tooltip is getting done using Classical pattern. 
Your html is this. 
{% gist vigneshjayavel/9910804 %} 
Your JS is this. 
{% gist vigneshjayavel/9911765 %}