---
title: Reference operator in c++
author: vigneshjayavel
description: 
post_id: 121
created: 2013/03/21 12:53:16
created_gmt: 2013/03/21 12:53:16
comment_status: open
post_name: reference-operator-in-c
status: publish
layout: post
---

## Reference operator in c++

whenever a caller function needs a data to be modified by the callee function, it is customary that the caller sends the callee a pointer that points to that data. for instance, lets say funCallee(int *x){ x=10; } funCaller(){ int x=0; funCallee(&x); } the above snippet solves the purpose..The same can be achieved through a built in data-type called reference data-type in c++. funCallee(int &x){ x=10; } funCaller(){ int x=0; funCallee(x); } Here, the compiler takes care of the parameter passing nuances. It automatically recognizes that funCallee requires a reference to an integer data and automatically passess the reference from the caller. This can be very handy in pointer manipulations like insertAtHead(node *&list,int data){ //create newnode node *newnode; newnode=(node*)malloc(sizeof(node)); newnode->data=data; //make connections newnode->next=list; list=newnode; } main(){ node *list; insertAtHead(list,data); } Without the usage of & operator, we would have coded like this insertAtHead(node **list,int data){ //create newnode node *newnode; newnode=(node*)malloc(sizeof(node)); newnode->data=data; //make connections newnode->next=*list; *list=newnode; } main(){ node *list; insertAtHead(&list,data); } So, we need to explicitly pass a pointer to a pointer. This can be tricky at times. Reference type in c++ can be used in scenario like this.The flexibility that the '&'operator brings is thus evident.