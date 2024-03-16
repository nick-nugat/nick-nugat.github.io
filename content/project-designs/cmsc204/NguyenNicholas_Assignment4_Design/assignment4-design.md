---
aliases: "202403121810"
type: design
language: java
date: 2024-03-12
created: 2024-03-12T18:10
updated: 2024-03-15T20:12
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
	    - ID: String;  
	    - CRN: int;  
	    - credits: int;  
	    - roomNum: String;  
	    - instructorName: String;  
		  
	    + compareTo(o: Object) int
	}
	
	 class CourseDBManager{
		 - structure: CourseDBStructure
		 
		 + CourseDBManager()
		 + add(ID: String, CRN: int, credits: int, roomNum: String, instructor: String) void
		 + get(CRN: int) CourseDBElement
		 + readFile(input: File) void
		 + showAll() ArrayList<String>
	 }
	
	 class CourseDBStructure{
		 - LOAD_FACTOR: double
		 - hashTable: LinkedList<CourseDBElement>[]
		 - tableLength: int
		 - COURSE_AS_STRING: String
		   
		 + CourseDBStructure(n: int)
		 + CourseDBStructure(testing: String, hashTableSize: int)
		 + add(element: CourseDBElement) void
		 + get(CRN: int) CourseDBElement
		 + showAll() ArrayList<String>
		 + getTableSize() int
		 %%helper methods%%
		 - isPrime(n: int) boolean$ 
		 - getNextPrime(n: int) int$
	 }


```

## Pseudocode