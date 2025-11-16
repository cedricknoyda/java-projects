# Student Enrollment System
![Student Enrollment System Background](https://raw.githubusercontent.com/cedricknoyda/image-/main/Screenshot%202025-11-13%20210808.png)
<br/>
<br/>

## Description/Overview
<br/>
The Student Enrollment System is a console-based program that simplifies the student enrollment process for the "Batangas State University , College of Informatics and Computing Sciences." It collects essential student information such as name, age, and address. It also helps students choose their academic program (BSIT or BSCS) and year level, and assigns them to a proper class block with a set schedule. The key features include validating student data like name and age, showing course lists and block schedules specific to each program (including face-to-face and online classes), and generating a unique Student ID after successful registration. This system addresses the issues of manual and error-prone enrollment by offering a structured, interactive, and automated way to register students, giving them their complete class schedule and enrollment summary right away.
<br/>
<br/>



## OOP Concepts Applied
- **CLASSES and OBJECTS**
    - Classes
        - The ```Student```acts as a guide for making personal student records.It defines the attributes such as ```name```,```age```,```program```,and ```studentID```, and the methods (behavior) like ```displayDetails()```.
        - The ```EnrollmentSystem``` class serves as the main application container. It holds the core logic, utility methods (```printCenteredLine```,``` displayCourses```), and the main execution point (```main```).
    - Objects
        - In the ```main``` method, a new student object```newStudent```, is created using the ``Student`` class's constructor: ```Student newStudent = new Student(...)```.
        - This object holds all the specific data gathered during the enrollment process for that student.
        - The ```studentRoster``` array, defined as private static ```Student[] studentRoster = new Student[50];```, is an array designed to hold up to 50 **Student objects**.
<br>

- **ENCAPSULATION** - Encapsulation involves grouping data and the methods that work on that data within a class. It also controls how external entities can access that data.
   - Attributes like a student's ```name```, ```age```, and ```studentID``` are contained within the ```Student``` class
   - The program provides specific methods to interact with this data:
        - Getters (like ```getProgram()``` in the ```Student``` class) allow code to read a value.
        - Setters (like ```setBlock()``` in the ```Student``` class) allow code to write or modify a value in a controlled way.

- **INHERITANCE** 
- **POLYMORPHISM**
- **ABSTRACTION** - Abstraction shows only the essential information while hiding the complicated implementation details.
   - Methods like ```displayCourses()``` hide the vast ```if/else``` logic that determines which specific courses to list based on the program (BSIT/BSCS) and year level.The calling code just needs to know the method name and the required parameters, which are ```program``` and ```yearLevel```.
   - The ```Student.displayDetails()``` This method offers a straightforward interface to print the student's complete enrollment summary. It removes the need for multiple calls to format and print each line.
