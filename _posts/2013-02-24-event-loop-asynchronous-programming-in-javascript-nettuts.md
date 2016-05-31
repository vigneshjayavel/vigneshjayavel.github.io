---
title: Event Loop - Asynchronous Programming in JavaScript (#nettuts)
author: vigneshjayavel
description: 
post_id: 110
created: 2013/02/24 11:05:23
created_gmt: 2013/02/24 11:05:23
comment_status: open
post_name: event-loop-asynchronous-programming-in-javascript-nettuts
status: publish
layout: post
---

## Event Loop - Asynchronous Programming in JavaScript (#nettuts)

The **Event Loop** is a queue of callback functions. When an async function executes, the callback function is pushed into the queue. The JavaScript engine doesn’t start processing the event loop until the code after an async function has executed. This means that JavaScript code is not multi-threaded even though it appears to be so. The event loop is a first-in-first-out (FIFO) queue, meaning that callbacks execute in the order they were added onto the queue.