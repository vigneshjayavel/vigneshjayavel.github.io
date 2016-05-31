---
title: Custom Search for an Array of Custom Objects using java.util.Arrays.binarySearch and java.util.Comparator
author: vigneshjayavel
description: 
post_id: 361
created: 2013/09/02 19:41:40
created_gmt: 2013/09/02 14:11:40
comment_status: open
post_name: custom-search-for-an-array-of-custom-objects-using-java-util-arrays-binarysearch-and-java-util-comparator
status: publish
layout: post
---

## Custom Search for an Array of Custom Objects using java.util.Arrays.binarySearch and java.util.Comparator

As a follow up to my previous post discussing on performing sorting usig JavaSE APIs, here is another post on searching through an array of custom(user-defined) objects in O(logn) time (worst case). 
{% highlight java %} 
public static class Student{ 	
	String name; 
	Integer id; 
	public Student(String string, int i) { 
		// TODO Auto-generated constructor stub 
		name=string;
		id=i; 
	} 
	public Student() { 
		// TODO Auto-generated constructor stub 
	} 
	public void setData(String x, Integer y){ 
		name=x;
		id=y; 
	} 
	public void getData(){ 
		System.out.println(name+" \- "+id); 
	} 
} 


public static void customBinarySearch(Student[] arr, String key){ 
	
	//Comparator that works based on "name" property of a Student object 
	Comparator<Student> studentNameComparator=new Comparator<Student>() { 
		@Override 
		public int compare(Student o1, Student o2) { 
			// TODO Auto-generated method stub 
			return o1.name.compareTo(o2.name); 
		} 
	}; 

	//Comparator that works based on "name" property of a Student object 
	Comparator<Student> studentIdComparator=new Comparator<Student>() { 
		@Override 
		public int compare(Student o1, Student o2) { 
			// TODO Auto-generated method stub 
			return o1.id.compareTo(o2.id); 
		} 
	}; 

	for (Student student : arr) { 
		student.getData(); 
	} 

	//binary search requires the array to be sorted 
	//we sort using student name AScending order 
	Arrays.sort(arr, studentNameComparator); 
	//Searching for a Student obj based on "name" 
	System.out.println(Arrays.binarySearch(arr, new Student("Stud2",2),studentNameComparator)); 
	//Searching for a Student obj based on "id" 
	System.out.println(Arrays.binarySearch(arr, new Student("Stud2",2),studentIdComparator)); } 
{% endhighlight %}