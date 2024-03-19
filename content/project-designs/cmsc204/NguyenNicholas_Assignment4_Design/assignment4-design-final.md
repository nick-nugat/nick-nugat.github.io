---
aliases: "202403121810"
type: design
language: java
date: 2024-03-12
created: 2024-03-16T17:59
updated: 2024-03-18T20:19
---
# Final Assignment 4 Design

- Nicholas Nguyen
- [CMSC204 GitHub Repository](https://github.com/nick-nugat/CMSC204)

___
## GitHub screenshot
![[assignment4-github-screenshot.png]]

## Learning experience


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

	class Comparable{ <<interface>> }
	class CourseDBElement { 
	    - ID: String
	    - CRN: int
	    - credits: int
	    - roomNum: String
	    - instructorName: String
		  
	    + compareTo(o: Object) int
	}
	
	class CourseDBStructureInterface{ <<interface>> }
	class CourseDBStructure{
		 - LOAD_FACTOR: double
		 - hashTable: LinkedList~CourseDBElement~[]
		 - tableLength: int
		 - COURSE_AS_STRING: String
		   
		 + CourseDBStructure(n: int)
		 + CourseDBStructure(testing: String, hashTableSize: int)
		 + add(element: CourseDBElement) void
		 + get(CRN: int) CourseDBElement
		 + showAll() ArrayList~String~
		 + getTableSize() int
	 }

	class CourseDBManagerInterface{ <<interface>> }
	class CourseDBManager{
		 - structure: CourseDBStructure
		 
		 + CourseDBManager()
		 + add(ID: String, CRN: int, credits: int, roomNum: String, instructor: String) void
		 + get(CRN: int) CourseDBElement
		 + readFile(input: File) void
		 + showAll() ArrayList~String~
	 }
```

## Pseudocode
- `CourseDBElement`
	- blueprint for a course with attributes for the course id, crn number, room number, and instructor name
	- getters and setters for each attribute
- `CourseDBStructure`
	- represents a hash table with buckets
	- each hash code is based on the crn since unique to every course
- `CourseDBManager`
	- data manager class that allows users to read courses from a text file
	- uses `CourseDBStructure` quite a bit
		- calls some of its methods
	- can be used to enter data manually