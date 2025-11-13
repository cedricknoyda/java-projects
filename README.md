# Student Enrollment System
Student Enrollment System designed to easily manage student registrations and course details. It allows administrators to efficiently add students, organize the course catalog, and track enrollments. The system is built using object-oriented principles to ensure data is handled reliably and the application is easy to maintain.

## Table of Contents
* [Features](#features)
* [Prerequisites](#prerequisites)
* [Installation](#installation)
* [Usage](#usage)
* [Code Structure](#code-structure)
* [Program Details](#program-details)

  # Usage
  The EnrollmentSystem project is a command-line application that simulates student enrollment. It collects personal and academic data, shows course options based on the chosen program and year level, and displays a detailed enrollment summary. This summary includes a generated student ID and the selected block schedule. The system guides the user through a series of inputs for name, age, program, and block choice. It also includes validation checks for inputs like age and name format to ensure correct data collection.

  ## Features
* **Collection of Student Information:** Gathers Name, Age, and Address.
* **Enrollment Period Selection:** Currently supports enrollment only for the first semester 2025-2026
* **Program and Year Level Choice:** Allows selection between BSIT and BSCS for 1st, 2nd, 3rd, and 4th Year, 1st Semester.
* **Course and Block Display:** Shows the list of courses for the selected program/year and presents detailed block schedules (including F2F-Face-to-Face and OLC-Online Class).
* **Automated ID Generation:** Generates a unique student ID upon enrollment.
* **Summary Display:** Prints a formatted enrollment summary for the student.
* **Formatted Output:** Uses custom helper methods (`printCenteredLine`, `printBoxLine`) to create a neat, boxed CLI interface.

  
