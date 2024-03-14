---
aliases: "202403121810"
type: design
language: java
date: 2024-03-12
created: 2024-03-12T18:10
updated: 2024-03-14T13:12
---
# [[assignment4-design]]
> Nicholas Nguyen
___


## UML diagram
```mermaid
---
title: Course Database
---
classDiagram

direction BT

Comparable <|-- CourseDBElement: implements
CourseDBManagerInterface <|-- CourseDBManager: implements

class CourseDBElement { 
    - courseID: String;  
    - crn: int;  
    - credits: int;  
    - roomNumber: String;  
    - instructorName: String;  
  
    + compareTo() int
}
 class CourseDBManagerInterface{
	 add(String id, int crn, int credits, String roomNum, String instructor)
 }


```

## Pseudocode