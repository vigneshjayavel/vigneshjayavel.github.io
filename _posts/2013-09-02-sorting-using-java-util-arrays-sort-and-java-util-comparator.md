---
title: Sorting using java.util.Arrays.sort and java.util.Comparator
author: vigneshjayavel
description: 
post_id: 343
created: 2013/09/02 18:35:25
created_gmt: 2013/09/02 13:05:25
comment_status: open
post_name: sorting-using-java-util-arrays-sort-and-java-util-comparator
status: publish
layout: post
---

## Sorting using java.util.Arrays.sort and java.util.Comparator

When it comes to Sorting an array of primitive types (int, char) or boxed types (Integers, Characters) or custom types(user defined object types), nothing comes in handy as "Arrays.sort()" method which is part of the official JavaSE API. It is a modified "merge sort" implementation that provides worst case running time of O(nlogn) [Source: Stackoverflow.com]. Combined with the java.util.Comparator, Arrays.sort() provides some powerful sorting functionality. The following is a demo about the same. [source language="java"] class MyComparator implements Comparator<Character>{ @Override public int compare(Character o1, Character o2) { // TODO Auto-generated method stub return o1-o2; } } static void customSort(String s){ Character[] ch=new Character[s.length()]; for (int i = 0; i < s.length(); i++) { ch[i]=s.charAt(i); } Arrays.sort(ch, new Comparator<Character>() { @Override public int compare(Character o1, Character o2) { // TODO Auto-generated method stub return o2.compareTo(o1); } }); String res=Arrays.toString(ch); System.out.println(res); } static void customSortStringArray(String[] arr){ Arrays.sort(arr, new Comparator<String>() { @Override public int compare(String o1, String o2) { // TODO Auto-generated method stub return o2.compareTo(o1); } }); System.out.println(Arrays.toString(arr)); } public static class Student{ String name; Integer id; public Student() { // TODO Auto-generated constructor stub } public void setData(String x, Integer y){ name=x;id=y; } public void getData(){ System.out.println(name+" \- "+id); } } static void customSortCustomObjects(Student[] sArr){ for (int i = 0; i < sArr.length; i++) { sArr[i].getData(); } System.out.println("\-------------"); Arrays.sort(sArr,new Comparator<Student>() { @Override public int compare(Student o1, Student o2) { // TODO Auto-generated method stub return o2.id.compareTo(o1.id); } }); for (int i = 0; i < sArr.length; i++) { sArr[i].getData(); } } public static void main(String[] args) { customSort("adbcasba"); customSortStringArray(new String[]{"apple","ball","cat"}); Student[] studArray=new Student[5]; for (int i = 0; i < studArray.length; i++) { studArray[i]=new Student(); studArray[i].setData("Stud"+i, Integer.valueOf((int) (Math.random()*100))); } customSortCustomObjects(studArray); } [/source]