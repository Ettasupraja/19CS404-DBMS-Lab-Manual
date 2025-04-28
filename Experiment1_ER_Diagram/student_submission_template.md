# ER DIAGRAM

## Ex.no:1
## Name: ETTA SUPRAJA
## Register no: 212223220022

## Scenario Chosen:
University 

## ER Diagram:
## University Database:
![Screenshot 2025-04-28 110955 1](https://github.com/user-attachments/assets/12ea772f-3555-4e46-bf17-b9a6fff75b35)

![WhatsApp Image 2025-04-28 at 11 18 03_2c3a94ea](https://github.com/user-attachments/assets/315e419e-4c31-4571-9dc0-cbfaa87127b8)


## Entities and Attributes:

- Department - Dept id, Dept name, Head of Department
- Program - Program id, Program name
- Student - Student id, Date of birth, Email, Name, Phone number
- Course - Credits, Department, Course id, Course name, Course description
- Instructor - Name, Department, Mobile number, Office location, Email, Instructor id

...

## Relationships and Constraints:
Relationship 1: Department - Program
Cardinality: 1 Department → many Programs (1:N)

Participation:

Department: Total

Program: Total

Relationship 2: Program - Student
Cardinality: 1 Program → many Students (1:N)

Participation:

Program: Total

Student: Total

Relationship 3: Student - Course (Enrolled in)
Cardinality: Many Students → Many Courses (M:N)

Participation:

Student: Partial

Course: Partial

Relationship 4: Course - Instructor (Taught by)
Cardinality: 1 Instructor → many Courses (1:N)


Participation:

Instructor: Partial

Course: Partial
...

## Extension (Prerequisite / Billing):
Extension (Prerequisite / Billing):
1. Prerequisite Modeling:
Idea: Some courses may require students to complete other courses first.

Modeling:

Add a "Prerequisite" relationship between Course and Course itself.

It will be a binary relationship like:

One Course (prerequisite) → another Course (dependent).

Cardinality:

0 or 1 prerequisite for a course (Optional, 0:1).

2. Billing Modeling:
Idea: Students pay based on enrolled courses (credits or fixed fees).

Modeling:

Add a Billing entity.

Connect Student ↔ Billing and Course ↔ Billing.

Billing will store:

Billing ID

Amount

Payment Date

Payment Status

Cardinality:

1 Student → Many Billing Records (1:N)

1 Course → Many Billing Records (1:N)



## Design Choices:
Design Choices:
Entities like Department, Program, Student, Course, and Instructor were chosen because they represent real-world objects we need to track separately, each with their own properties (attributes).

Relationships like offers, enrolled by, enrolled in, and taught by were used to properly connect the entities:

Department offers Program: Logical because programs are under departments.

Program enrolled by Student: Students must belong to a program.

Student enrolled in Course: Students register for multiple courses.

Course taught by Instructor: Instructors are responsible for teaching courses.

Assumptions:

Every Program must belong to exactly one Department.

A Student must be enrolled in one Program but can enroll in multiple Courses.

Each Course must belong to a Department.

Instructors are assigned based on department expertise but can teach multiple courses.

Billing and Prerequisites (if added) are optional extensions for real-world system needs.

## Result:
Thus, the ER diagram for the hospital management system was successfully designed, and the entities, relationships, and constraints were clearly represented.
