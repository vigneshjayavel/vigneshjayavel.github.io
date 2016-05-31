---
title: Java - Swapping two numbers using a custom wrapper class
author: vigneshjayavel
description: 
post_id: 371
created: 2013/10/14 22:59:39
created_gmt: 2013/10/14 17:29:39
comment_status: open
post_name: java-swapping-two-numbers-using-a-custom-wrapper-class
status: publish
layout: post
---

## [Java] Swapping two numbers using a custom wrapper class

Java is technically pass by value where the values for non-primitive data are actually references to those data.So essentially the parameters are passed as "values" during the function calls. Your modification of the value inside a function to which it is passed will not reflect back to the called function. So you cannot swap two numbers simply by passing references of those two numbers to a swap() function. The following code will not swap even though we use a wrapper class "Integer". [source lang="java"] static void swapper(Integer a,Integer b){ Integer t=a; a=b; b=t; } public static void main(String[] args) { Integer a,b; a=10;b=20; swapper(a,b); System.out.println(a+","+b); } [/source] The above code is expected to work but technically Java does a shallow copy (just swapping/changing the reference of the objects that are passed as parameters) here which does not work. We need to perform a deep copy to achieve our goal.We can write our own wrapper class and try deep cloning (i.e. copying the members/fields of one object to another thereby modifying the overall object without touching its "reference" part.) [source lang="java"] static class MyInteger{ int data; } static void swapper(MyInteger a,MyInteger b){ int t=a.data; a.data=b.data; b.data=t; } public static void main(String[] args) { MyInteger a=new MyInteger(); MyInteger b=new MyInteger(); a.data=10;b.data=20; swapper(a,b); System.out.println("a.data = "+a.data+",b.data = "+b.data); } [/source] The swap() method thus performs a deep clone of the objects that are passed as a reference to it. To recap the concept, the following code does a shallow copy and it does not work. [source language="java"] static void swapper(MyInteger a,MyInteger b){ MyInteger t=a; a=b; b=t; } [/source]