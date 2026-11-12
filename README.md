# Lab 2 - Conceptual Modeling using Draw.io
This lab will meet the following course objectives:
1. Determine appropriate entity structure for relational databases

2. Apply the correct terminology to an ER Model

3. Design an ER model

## Instructions
In this lab, you will practice writing business rules that describe the relationships between entities. Using the school ER diagram below, write and recreate a conceptual ER diagram that illustrates the relationships shown.

![alt text](https://instructorc.github.io/site/home/images/school_ERD.PNG)

You will record your relationships within this README file.  When writing down the relationships, follow the bullet points below.
- Entity names are uppercase and bolded
- The connecting verb is underlined
- Bidirectionality of the relationship is represented


Once you complete the README.md file, create an ER Diagram based on the relationships you identified. Create the ER Diagram using a free web-based tool called draw.io.  The shapes you will use to create your ER diagram can be found under the "Entity Relation" tab.  Instructions on how to use draw.io are in the assignment resources section below.

## Requirements

### Deliverable 1 (5 Points)
All relationships are identified, including the relationships that are formed when identifying the new **associative entities**


### Deliverable 2 (5 Points)
Update the ReadMe.md file to reflect the relationships. The relationships adhere to the following bullet points below.
- Entity names are uppercase and bolded
- The connecting verb is <ins>underlined</ins>

- Bi-direction of the relationship is represented


### Deliverable 3 (5 Points)
A conceptual Entity Relationship Diagram(ERD) is created to reflect all entities and relationships identified in the write-up

## Submission Guidelines

For this lab, submit 2 items to the repository.  The two items that you will need to submit are listed below: 
1. The README.MD file that identifies the various Entities and briefly describes each entity, including possible attributes, relationships, and assumptions. 
   1. When identifying relationships, be sure to bold and uppercase the entity name, underline the verb, and make sure relationships are bidirectional. 
   2. When identifying assumptions, make sure to formulate assumptions based on what is represented in the school ERD with either a Yes or No. 
   3. You can override this README.md file that contains the instructions or extend this README.md file by listing your requirements below the lab Resources section.

2. The draw.io XML file that contains your ER Diagram.  You will also need to take a snippet of the ER Diagram and add it as an image in your README file.

Once you complete both items above, submit the link to your repository for lab 2 before the due date and time listed.  


## Lab Resources
- [Mark-down Syntax Cheat Sheet](https://enterprise.github.com/downloads/en/markdown-cheatsheet.pdf)
- [Make a ReadMe file Web-based Editor](https://www.makeareadme.com/)
- [Draw.io Web-based diagramming tool](https://app.diagrams.net/)
- [Creating Entity Relationship Diagrams using Draw.io](https://www.youtube.com/watch?v=lAtCySGDD48)




---

# Lab 2 - School Database ER Model

## 1. Entities and Attributes

### STUDENT
Represents a student enrolled at the school.

Attributes:
- student_id (Primary Key)
- student_name
- student_address

### SEAT
Represents a seat assigned to a student.

Attributes:
- seat_no (Primary Key)
- seat_position

### INSTRUCTOR
Represents an instructor who teaches courses.

Attributes:
- instructor_no (Primary Key)
- instructor_name
- instructor_faculty

### COURSE
Represents a course offered by the school.

Attributes:
- course_name (Primary Key component)
- course_number (Primary Key component)

### SECTION
Represents a section of a course.

Attributes:
- section_number (Primary Key)

### PROFESSOR
Represents a professor who teaches sections.

Attributes:
- professor_id (Primary Key)
- professor_name
- professor_faculty



## 2. Entity Relationships

### STUDENT and SEAT
- A **STUDENT** <u>fills</u> exactly one **SEAT**.
- A **SEAT** <u>is filled by</u> exactly one **STUDENT**.
- Cardinality: One-to-One (1:1).

### STUDENT and COURSE
- A **STUDENT** <u>takes</u> one or more **COURSES**.
- A **COURSE** <u>is taken by</u> one or more **STUDENTS**.
- Cardinality: Many-to-Many (M:N).

### INSTRUCTOR and COURSE
- An **INSTRUCTOR** <u>teaches</u> one or more **COURSES**.
- A **COURSE** <u>is taught by</u> exactly one **INSTRUCTOR**.
- Cardinality: One-to-Many (1:M).

### COURSE and SECTION
- A **COURSE** <u>has</u> one or more **SECTIONS**.
- A **SECTION** <u>belongs to</u> one or more **COURSES**.
- Cardinality: Many-to-Many (M:N).

### PROFESSOR and SECTION
- A **PROFESSOR** <u>teaches</u> zero or more **SECTIONS**.
- A **SECTION** <u>is taught by</u> exactly one **PROFESSOR**.
- Cardinality: One-to-Many (1:M).



## 3. Assumptions

1. Can a **STUDENT** fill more than one **SEAT**?
   - **No.** Each student fills exactly one seat.

2. Can a **SEAT** be assigned to multiple **STUDENTS**?
   - **No.** Each seat is filled by exactly one student.

3. Can a **STUDENT** take multiple **COURSES**?
   - **Yes.** A student takes one or more courses.

4. Can a **COURSE** have multiple **STUDENTS**?
   - **Yes.** A course can be taken by multiple students.

5. Can an **INSTRUCTOR** teach multiple **COURSES**?
   - **Yes.** An instructor teaches one or more courses.

6. Can a **COURSE** be taught by multiple **INSTRUCTORS**?
   - **No.** Each course is taught by exactly one instructor.

7. Can a **COURSE** have multiple **SECTIONS**?
   - **Yes.** A course has one or more sections.

8. Can a **SECTION** belong to multiple **COURSES**?
   - **Yes.** The reference diagram shows a many-to-many relationship.

9. Can a **PROFESSOR** teach zero **SECTIONS**?
   - **No.** The reference diagram requires each professor to teach at least one section.

10. Can a **PROFESSOR** teach multiple **SECTIONS**?
    - **Yes.** A professor can teach multiple sections.

11. Can a **SECTION** exist without a **PROFESSOR**?
    - **No.** Each section is taught by exactly one professor.
