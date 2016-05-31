---
title: JavaScript Design Patterns - Prototype Pattern
author: vigneshjayavel
description: 
post_id: 457
created: 2014/04/01 15:03:26
created_gmt: 2014/04/01 09:33:26
comment_status: open
post_name: javascript-design-patterns-prototype-pattern
status: publish
layout: post
---

## JavaScript Design Patterns - Prototype Pattern

Prototype pattern allows you to mimic the class based inheritance model offered by modern O-O languages. Anyways there are limitations to that. The following are the features offered by prototype pattern.

  * Normal functions can act as constructors to instantiate objects. (This is achieved through the "new" keyword);
  * Provides a means for inheritance. (Using an object's prototype).

Lets try to build the tooltip using Prototype pattern. Firstly we create a simple tooltip with the core functionalities. Later on we move on to extend the simple tooltip to override it to make a special tooltip that showcases "fading" behavior.

Our html should be like this. (Of course we need jQuery for the DOM manipulation stuffs..)

{ gist vigneshjayavel/9910804 }

Our JS should be like this.

{ gist vigneshjayavel/9910794 }