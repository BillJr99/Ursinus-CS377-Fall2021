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
  - filename: "MyFirstStatement.sql"
    name: myfirststatement
    ismain: false
    isreadonly: false
    isvisible: true
    code: | 
        -- TODO: list all people that live in the 19426 zip code
        -- TODO: List the average total household salary of each house, sorted in descending order by salary
        -- TODO: List the average household salary by zip code, in descending order by salary

  - filename: "Setup.sql"
    ismain: true
    name: main
    isreadonly: true
    isvisible: true
    code: |
      CREATE TABLE PERSON (
        ID INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT, 
        FirstName TEXT NOT NULL, 
        LastName TEXT NOT NULL, 
        Age INTEGER,
        Salary REAL
      );

      CREATE TABLE HOUSE (
        ID INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT, 
        Address TEXT NOT NULL, 
        City TEXT NOT NULL, 
        State TEXT NOT NULL,
        ZIP TEXT NOT NULL
      );

      CREATE TABLE HOUSEHOLDMEMBER (
        ID INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT, 
        HouseID INTEGER NOT NULL,
        PersonID INTEGER NOT NULL,
        FOREIGN KEY(HouseID) REFERENCES HOUSE(ID),
        FOREIGN KEY(PersonID) REFERENCES PERSON(ID)
      );
     
      INSERT INTO PERSON (FirstName, LastName, Age, Salary) VALUES ("Alex", "Smith", 20, 20000);
      INSERT INTO PERSON (FirstName, LastName, Age, Salary) VALUES ("Susan", "Smith", 22, 30000);

      INSERT INTO PERSON (FirstName, LastName, Age, Salary) VALUES ("Samantha", "Lee", 50, 100000);
      INSERT INTO PERSON (FirstName, LastName, Age, Salary) VALUES ("Alex", "Lee", 49, 110000);
      INSERT INTO PERSON (FirstName, LastName, Age) VALUES ("Steph", "Lee", 15);

      INSERT INTO PERSON (FirstName, LastName, Age, Salary) VALUES ("Stephen", "Johnson", 29, 40000);

      INSERT INTO HOUSE (Address, City, State, ZIP) VALUES ("123 Main Street", "Collegeville", "PA", "19426");
      INSERT INTO HOUSE (Address, City, State, ZIP) VALUES ("234 Main Street", "Collegeville", "PA", "19426");
      INSERT INTO HOUSE (Address, City, State, ZIP) VALUES ("12 Third Street", "King of Prussia", "PA", "19406");

      INSERT INTO HOUSEHOLDMEMBER(HouseID, PersonID) VALUES(1, 1);
      INSERT INTO HOUSEHOLDMEMBER(HouseID, PersonID) VALUES(1, 2);

      INSERT INTO HOUSEHOLDMEMBER(HouseID, PersonID) VALUES(2, 3);
      INSERT INTO HOUSEHOLDMEMBER(HouseID, PersonID) VALUES(2, 4);
      INSERT INTO HOUSEHOLDMEMBER(HouseID, PersonID) VALUES(2, 5);

      INSERT INTO HOUSEHOLDMEMBER(HouseID, PersonID) VALUES(3, 6);
        
---
