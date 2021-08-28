---
layout: exercise_sql
permalink: /Modules/SQL/Join/Exercise
title: "CS377: Database Design - SQL Joins"
excerpt: "CS377: Database Design - SQL Joins"

info:
  points: 3
  instructions: "Modify the MyFirstStatement.sql file to answer the database questions below."
  goals:
    - To write a SQL Join statement
    
canvasasmtid: "107081"   
canvaspoints: 3
  
processor:  
  correctfeedback: "Correct!!" 
  incorrectfeedback: "Try again"
  submitformlink: false
  feedbackprocess: | 
    var pos = feedbackString;
  correctcheck: |
    pos.toLowerCase().includes("42")
 
files:
  - filename: "MyJoins.sql"
    name: myjoins
    ismain: false
    isreadonly: false
    isvisible: true
    code: | 
        -- TODO: list all people that live in the 19426 zip code
        -- TODO: List the average total household salary of each house, sorted in descending order by salary
        -- TODO: List the average household salary by zip code, in descending order by salary

  - filename: "Main.sql"
    ismain: true
    name: main
    isreadonly: false
    isvisible: true
    code: |
      CREATE TABLE PERSON (
        ID int, 
        FirstName text, 
        LastName text, 
        Age int,
        Salary float
      );

      CREATE TABLE HOUSE (
        ID int, 
        Address text, 
        City text, 
        State text,
        ZIP text
      );

      CREATE TABLE HOUSEHOLDMEMBER (
        ID int, 
        HouseID int,
        PersonID int
      );
     
      INSERT INTO PERSON VALUES (1, "Alex", "Smith", 20, 20000);
      INSERT INTO PERSON VALUES (2, "Susan", "Smith", 22, 30000);

      INSERT INTO PERSON VALUES (3, "Samantha", "Lee", 50, 100000);
      INSERT INTO PERSON VALUES (4, "Alex", "Lee", 49, 110000);
      INSERT INTO PERSON VALUES (5, "Steph", "Lee", 15, 0);

      INSERT INTO PERSON VALUES (6, "Stephen", "Johnson", 29, 40000);

      INSERT INTO HOUSE VALUES (1, "123 Main Street", "Collegeville", "PA", "19426");
      INSERT INTO HOUSE VALUES (2, "234 Main Street", "Collegeville", "PA", "19426");
      INSERT INTO HOUSE VALUES (3, "12 Third Street", "King of Prussia", "PA", "19406");

      INSERT INTO HOUSEHOLDMEMBER VALUES (1, 1, 1);
      INSERT INTO HOUSEHOLDMEMBER VALUES (2, 1, 2);

      INSERT INTO HOUSEHOLDMEMBER VALUES (3, 2, 3);
      INSERT INTO HOUSEHOLDMEMBER VALUES (4, 2, 4);
      INSERT INTO HOUSEHOLDMEMBER VALUES (5, 2, 5);

      INSERT INTO HOUSEHOLDMEMBER VALUES (6, 3, 6);
              
---
