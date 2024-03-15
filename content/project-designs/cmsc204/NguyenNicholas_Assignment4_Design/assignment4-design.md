---
aliases: "202403121810"
type: design
language: java
date: 2024-03-12
created: 2024-03-12T18:10
updated: 2024-03-15T16:20
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
	CourseDBStructureInterface <|-- CourseDBStructure: implements
	
	
	class CourseDBElement { 
	    - courseID: String;  
	    - crn: int;  
	    - credits: int;  
	    - roomNumber: String;  
	    - instructorName: String;  
	  
	    + compareTo() int
	}
	
	 class CourseDBManager{
		 + add(id: String, crn: int, credits: int, roomNum: String, instructor: String) void
		 + get(crn: int) CourseDBElement
		 + readFile(input: File) void
		 + showAll() ArrayList<String>
	 }
	
	 class CourseDBStructure{
		 - StrinLOAD_FACTOR$
	 }


```

## Pseudocode