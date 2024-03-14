---
aliases: "202403121810"
type: design
language: java
date: 2024-03-12
created: 2024-03-12T18:10
updated: 2024-03-14T12:57
---
# [[assignment4-design]]
> Nicholas Nguyen
___


## UML diagram
```mermaid
classDiagram

direction BT

class CourseDBElement implements Comparable { 
    
    - String courseID;  
    private int crn;  
    private int credits;  
    private String roomNumber;  
    private String instructorName;  
  
    + int compareTo()
    
}

```

## Pseudocode