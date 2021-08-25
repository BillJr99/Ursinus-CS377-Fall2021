---
layout: assignment
permalink: /Labs/FileIO
title: "CS377: Intro to Computer Science - File I/O"
excerpt: "CS377: Intro to Computer Science - File I/O"

info:
  coursenum: CS377
  points: 100
  goals:
    - To use file I/O to read and process records in a flat file format
  rubric:
    - weight: 60
      description: Algorithm Implementation
      preemerging: The algorithm fails on the test inputs due to major issues, or the program fails to compile and/or run
      beginning: The algorithm fails on the test inputs due to one or more minor issues
      progressing: The algorithm is implemented to solve the problem correctly according to given test inputs, but would fail if executed in a general case due to a minor issue or omission in the algorithm design or implementation
      proficient: A reasonable algorithm is implemented to solve the problem which correctly solves the problem according to the given test inputs, and would be reasonably expected to solve the problem in the general case
    - weight: 30
      description: Code Quality and Documentation
      preemerging: Code commenting and structure are absent, or code structure departs significantly from best practice, and/or the code departs significantly from the style guide
      beginning: Code commenting and structure is limited in ways that reduce the readability of the program, and/or there are minor departures from the style guide
      progressing: Code documentation is present that re-states the explicit code definitions, and/or code is written that mostly adheres to the style guide
      proficient: Code is documented at non-trivial points in a manner that enhances the readability of the program, and code is written according to the style guide
    - weight: 10
      description: Writeup and Submission
      preemerging: An incomplete submission is provided
      beginning: The program is submitted, but not according to the directions in one or more ways (for example, because it is lacking a readme writeup or missing answers to written questions)
      progressing: The program is submitted according to the directions with a minor omission or correction needed, including a readme writeup describing the solution and answering nearly all questions posed in the instructions
      proficient: The program is submitted according to the directions, including a readme writeup describing the solution and answering all questions posed in the instructions
  readings:
    - rtitle: "Text and File Management Activity"
      rlink: "../Activities/TextAndFileManagement" 
    - rtitle: "File I/O Activity"
      rlink: "../Activities/FileIO"    
      
tags:
  - introduction
  
---

In this lab, you will create a class to represent a data model of some type (your movie collection, people you work with, *etc*).  This can be anything you'd like, but each class should have at least three fields in it.  Your class should have a method that returns a `dict` structure whose keys are the name of the field and whose values are the corresponding values of that object (you can use the `.__dict__` attribute of your object to return this dictionary automatically, or you may create the `dict` structure yourself).

Create a second class that writes a `dict` structure to a comma-separated value.  The first line of this file (and only the first line) should be the header row, containing the columns of the data within.  The desired filename should be a parameter.  For safety, if the file already exists, append to it by opening the file in `'a'` mode.  If the parameter is not a dict, your program should fail gracefully (in other words, it should continue execution beyond the point of the error, and not simply quit!).

In your `main` function, instantiate at least three of these objects and write them to a file that you specify with a parameter.

### Unit Testing
Explore the [Unit Testing](https://docs.python.org/3/library/unittest.html) framework that Python provides to automatically test your lab.  Create a test class at least three test cases that write to a file.  You can read the file and inspect its contents as your test validation.

## Exporting your Project for Submission

When you're done, write a README for your project, and save all your files, before exporting your project to ZIP.  In your README, answer any bolded questions presented on this page.  