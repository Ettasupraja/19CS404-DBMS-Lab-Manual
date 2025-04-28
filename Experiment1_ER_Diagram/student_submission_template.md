# ER DIAGRAM

## Ex.no:1
## Name: ETTA SUPRAJA
## Register no: 212223220022

## Scenario Chosen:
University 

## ER Diagram:
## University Database:
![Screenshot 2025-04-27 223343](https://github.com/user-attachments/assets/9e9cb47a-1cf3-4c2a-b7ef-215ee642138e)



## Entities and Attributes:

### DEPARTMENT:

ID

NAME

### PROGRAM:

ID

NAME

DEPT_ID

### STUDENT:

ID

NAME

PHONE_NO

EMAIL

DATE_OF_BIRTH

### PROGRAM_ID

FACULTY:

ID

NAME

EMAIL

PHONE_NO

### COURSE:

ID

NAME

CREDIT

PROGRAM_ID

### PRE REQUEST (seems to represent prerequisites for courses):

COURSE_ID

PREREQ_COURSE_ID

### ENROLLMENT:

ID

ENROLLMENT_DATE

COURSE_ID

STUDENT_ID

### Relationships and Constraints:

OFFER (DEPARTMENT —> PROGRAM)

1 Department offers many Programs

(1, M)

CONSIST (PROGRAM —> COURSE)

1 Program consists of many Courses

(1, M)

HAVE (COURSE —> PRE REQUEST)

1 Course has many Prerequisites

(1, M)

TEACHER (COURSE —> FACULTY)

1 Course is taught by 1 Faculty

(M, 1)

ENROLL (PROGRAM —> STUDENT)

1 Program enrolls many Students

(1, M)

ENROLL (STUDENT <—> ENROLLMENT <—> COURSE)

Many Students enroll in many Courses (through ENROLLMENT)

(M, M)

## Extension (Prerequisite / Billing):
- Explain how you modeled prerequisites or billing.

## Design Choices:
Brief explanation of why you chose certain entities, relationships, and assumptions.

## Result:
Thus, the ER diagram for the hospital management system was successfully designed, and the entities, relationships, and constraints were clearly represented.
