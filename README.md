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

- **INHERITANCE** - Inheritance involves creating a superclass. Specialized subclasses then take on its shared attributes and behaviors.
   - Superclass:
        - A base class, like ```AcademicPerson``` (or a similar name), is created. It contains attributes that are common to all university members, such as ```name```, ```age```, and ```address```.
    - Subclasses:
        -  Include classes such as ```Student```, ```Faculty```, and ```Administrator``` (or the other two subclasses you added), which extend the ```AcademicPerson``` superclass. They inherit common attributes and add their unique properties. For instance, the ```Student`` class adds ```studentID```, ```program```, and ```block```. This creates a clear "is-a" relationship; a **Student is an AcademicPerson**.
          
- **POLYMORPHISM** - Polymorphism, which means "many forms," allows a common method to work differently depending on the specific type of the object.
    - Overridden Method: A method, such as ```getDetailsSummary()``` or ```displayRole()```, is defined in the superclass (```AcademicPerson```).
    - Dynamic Behavior: This method is overridden in each subclass (```Student```, ```Faculty```, etc.) to provide role-specific output.
        - The ```Student``` version might print: "Enrolled in BSIT - 1st Year 1st Sem."
        - The ```Faculty``` version might print: "Teaching in the Computer Science Department."
    - When a collection of ```AcademicPerson``` references is processed, calling the common method runs the right, specialized version for each object at runtime. This shows dynamic polymorphism.
  
- **ABSTRACTION** - Abstraction shows only the essential information while hiding the complicated implementation details.
   - Methods like ```displayCourses()``` hide the vast ```if/else``` logic that determines which specific courses to list based on the program (BSIT/BSCS) and year level.The calling code just needs to know the method name and the required parameters, which are ```program``` and ```yearLevel```.
   - The ```Student.displayDetails()``` This method offers a straightforward interface to print the student's complete enrollment summary. It removes the need for multiple calls to format and print each line.

## PROGRAM STRUCTURE

The project is built using two main parts, which are the main classes in the Java program. First, is the **EnrollmentSystem** class. This class is the main part of the program because it has the main method, which is where the program starts running. It handles everything the user sees, like asking for information like the name, age, and program, and displaying the course lists and the final summary. This class also makes sure the user enters the right data by including special checks (exception handling) and keeps track of all the enrolled students using an array, showing how it manages multiple objects.
Second, there is the **Student** class. This class is like a blueprint for creating an actual student. Every time a new student enrolls, the EnrollmentSystem creates a new Student object to hold their information, like their generated ID, age, and chosen block. The Student class keeps the student's data safe inside it by using methods to set and get the details, which is an example of encapsulation. The main class calls a method in the Student class to print out the final enrollment summary.

## HOW TO RUN THE PROGRAM
To start, the user needs to use the command like command prompt or terminal and have java installed. First, they must compile the source code. The user should go to the folder where they saved the Java files (**EnrollmentSystem.java** and **Student.java**) and use the Java compiler command **“javac EnrollmentSystem.java”** Once the code is compiled successfully, the user can run the program. They should use the Java execution command to start the main class **“java EnrollmentSystem”** The program will then greet the user and start asking for their details right away.
