---
title: Hidden features of C - printf() and scanf() functions
author: vigneshjayavel
description: 
post_id: 338
created: 2013/07/15 22:54:00
created_gmt: 2013/07/15 17:24:00
comment_status: open
post_name: hidden-features-of-c-printf-and-scanf-functions
status: publish
layout: post
---

## Hidden features of C - printf() and scanf() functions

Did you know that printf() and scanf() function calls return values? Please read further to know about the hidden features of these most widely used functions! [code language="cpp"] printf("Hello!"); //returns integer value 6 i.e the no. of characters printf() prints on screen int i=10; printf("%d",i); //this would return 2 //scanf() behaves differently compared to printf() scanf("%d",&i); //say the input is 10. This would return 1, as only one variable is assigned an input char str[100]; scanf("%d %s",&i,&str); //this would return 2, as 2 variables are assigned [/code]