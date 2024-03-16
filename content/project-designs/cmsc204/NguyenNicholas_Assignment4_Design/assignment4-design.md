---
aliases: "202403121810"
type: design
language: java
date: 2024-03-12
created: 2024-03-12T18:10
updated: 2024-03-15T20:33
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
	CourseDBStructureInterface <|-- CourseDBStructure: implements
	CourseDBManagerInterface <|-- CourseDBManager: implements
	
	
	class CourseDBElement { 
	    - ID: String
	    - CRN: int
	    - credits: int
	    - roomNum: String
	    - instructorName: String
		  
	    + compareTo(o: Object) int
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
	 }

	class CourseDBManager{
		 - structure: CourseDBStructure
		 
		 + CourseDBManager()
		 + add(ID: String, CRN: int, credits: int, roomNum: String, instructor: String) void
		 + get(CRN: int) CourseDBElement
		 + readFile(input: File) void
		 + showAll() ArrayList<String>
	 }
```

## Pseudocode
- `CourseDBElement`
	- blueprint for a course with attributes for the course id, crn number, room number, and instructor name
- `CourseDBStructure`
	- represents a hash table with buckets
	- each hash code is based on the crn since unique to every course
- `CourseDBManager`
	- data manager class that allows users to read courses from a text file
	- can be used to enter data manually