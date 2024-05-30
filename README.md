# Course-connect

  

This project is a proposed solution to Sigma Phi Delta - Beta Nu academic network.
Members will have a the ability to search for course numbers or professors and see
which other members have taken that course or professor. This is an alternative
solution to the academic bank.

  

## Table of Contents

  

- [Usage](#usage)

- [Logic](#logic)

- [Contact](#contact)

## Usage
Find others who have taken courses or professors you want to take. Simply look up a course number ex. CSC 202 and find any member who has taken that class. Alternatively, search for a professor name and see who has taken them ex. John Clements.

  

## Logic

  

This software is designed to be used as a database interface. The data base will have three tables:

- [members]
- [courses]
- [professors] 

**Courses Table**
This table contains courses available in the 2026 Cal Poly catalog. PRIMARY_KEY(subject, course-number)
ex.
| subject | course-number |  course-name |
| ----------- | ----------- |  ----------- |
| CSC | 202 |  Data Structures|
| EE | 211 | Circuits I | 

**Professors Table**
This table contains first and last names of professors.
PRIMARY_KEY(firstname, lastname)
ex.
| firstname | lastname |  
| ----------- | ----------- |  
| John | Fox |  
| John | Clements |

**Members Table**
This table is the main data source of the database, combining data from all three tables. 
PRIMARY_KEY(firstname, lastname) 
FOREIGN_KEY(prof_firstname, prof_lastname) REFERENCES professors(firstname, lastname)
FOREIGN_KEY(course-subj, course-num) REFERENCES courses(subject, course-number)

## Contact
For questions on use or website issues contact Ethan Trantalis.



  


