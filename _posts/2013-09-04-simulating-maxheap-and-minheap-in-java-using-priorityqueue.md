---
title: Simulating maxheap and minheap in Java using PriorityQueue
author: vigneshjayavel
description: 
post_id: 366
created: 2013/09/04 00:01:24
created_gmt: 2013/09/03 18:31:24
comment_status: open
post_name: simulating-maxheap-and-minheap-in-java-using-priorityqueue
status: publish
layout: post
---

## Simulating maxheap and minheap in Java using PriorityQueue

Heap is a very useful data structure. PriorityQueue class in JavaSE API can be used to implement heaps easily and efficiently. The following snippet demonstrates how PriorityQueue can be used in simulating both MaxHeap and MinHeap. [source language="java"] static void testHeapUsingPriorityQueue(){ //create a new object and add a custom comparator that provides the "MinHeap" behaviour. PriorityQueue<Integer> minheap=new PriorityQueue<Integer>(1,new Comparator<Integer>() { @Override public int compare(Integer o1, Integer o2) { return o1-o2; } }); //add elements minheap.addAll(Arrays.asList(new Integer[]{8,9,1,2,3,4,5,})); System.out.println("Minheap---------------------"); System.out.println(Arrays.toString(minheap.toArray())); for (Iterator iterator = minheap.iterator(); iterator.hasNext();) { System.out.println("Min : "+minheap.element()); System.out.println("Removing " \+ minheap.element()); minheap.remove(); } //create a new object and add a custom comparator that provides the "MaxHeap" behaviour. PriorityQueue<Integer> maxheap=new PriorityQueue<Integer>(1,new Comparator<Integer>() { @Override public int compare(Integer o1, Integer o2) { return o2-o1; } }); System.out.println("Maxheap---------------------"); //add elements maxheap.addAll(Arrays.asList(new Integer[]{8,9,1,2,3,4,5,})); System.out.println(Arrays.toString(maxheap.toArray())); for (Iterator iterator = maxheap.iterator(); iterator.hasNext();) { System.out.println("Max : "+maxheap.element()); System.out.println("Removing " \+ maxheap.element()); maxheap.remove(); } } [/source]