---
title: Function pointers - 101 in C++
author: vigneshjayavel
description: 
post_id: 334
created: 2013/07/15 18:46:16
created_gmt: 2013/07/15 13:16:16
comment_status: open
post_name: function-pointers-101-in-c
status: publish
layout: post
---

## Function pointers - 101 in C++

[code language="cpp"] #include<iostream> using namespace std; void fun1(){ cout<<endl<<"fun1"; } int fun2(int data){ cout<<endl<<"fun2..data : "<<data; } int fun3(){ cout<<endl<<"fun3"; } int fun4(){ cout<<endl<<"fun4"; } int main(int argc, char *argv[]) { //pointer to a function that has no args //here, "void" is the return type of the function, fPtr1 is the function pointer void (*fPtr1)(); //fPtr1 now points to fun1 fPtr1=&fun1; //calling fun1() using pointer fPtr1(); //pointer to a function that has a single "int" argument and "int" return type int (*fPtr2)(int); fPtr2=&fun2; fPtr2(10); //array of pointers to functions //here, fPtrArr is an array of pointers of length 2 int (*fPtrArr[2])(); fPtrArr[0]=&fun3; fPtrArr[1]=&fun4; //calling fun3() and fun4() using array of pointers to functions fPtrArr[0](); fPtrArr[1](); return 0; } [/code]