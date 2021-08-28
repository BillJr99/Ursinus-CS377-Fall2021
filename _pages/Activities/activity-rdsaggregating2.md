---
layout: activity
permalink: /Activities/RDS/Aggregating2
title: "CS377: Database Design - Aggregation in Relational Databases"
excerpt: "CS377: Database Design - Aggregation in Relational Databases"

info:
  prev: ./Aggregating
  goals: 
    - To explain the use of primary and foreign keys in database systems
    - To aggregate records across multiple tables with referential keys
    - To express basic queries in the programmatic language SQL (Structured Query Language)
  additional_reading:
    - link: https://comptoolsres.github.io/Database_Introduction.html
      title: Database Introduction
    - link: https://www.sqlite.org/lang_aggfunc.html
      title: Sqlite Aggregating Functions
      
  models:
    - model: |
        <script type="syntaxhighlighter" class="brush: sql"><![CDATA[        
        -- Students Table
        CREATE TABLE STUDENTS (
            ID INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT, 
            FirstName TEXT NOT NULL, 
            LastName TEXT NOT NULL, 
            Age INTEGER
        );

        INSERT INTO STUDENTS (FirstName, LastName, Age) VALUES ("Alex", "Smith", 20);
        INSERT INTO STUDENTS (FirstName, LastName, Age) VALUES ("Lee", "Jones", 21);
        INSERT INTO STUDENTS (FirstName, LastName, Age) VALUES ("Brian", "McMullen", 18);
        INSERT INTO STUDENTS (FirstName, LastName, Age) VALUES ("Samantha", "Johnson", 22);
        INSERT INTO STUDENTS (FirstName, LastName, Age) VALUES ("Lee", "Jones", 24);

        -- Courses Table
        CREATE TABLE COURSES (
          ID INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT, 
          CourseNum TEXT NOT NULL, 
          CourseName TEXT NOT NULL
        );

        INSERT INTO COURSES (CourseNum, CourseName) VALUES ("CS377", "Database Design");
        INSERT INTO COURSES (CourseNum, CourseName) VALUES ("CS173", "Intro to Computer Science");
        INSERT INTO COURSES (CourseNum, CourseName) VALUES ("CS174", "Object Oriented Programming");
        INSERT INTO COURSES (CourseNum, CourseName) VALUES ("CS275", "Software Engineering");

        -- Try it out
        SELECT * FROM STUDENTS;
        SELECT * FROM COURSES;

        -- Link the Tables Together with Primary and Foreign Keys
        CREATE TABLE ENROLLMENTS (
          ID INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT, 
          StudentID INTEGER NOT NULL, 
          CourseID INTEGER NOT NULL, 
          FOREIGN KEY(StudentID) REFERENCES STUDENTS(ID), 
          FOREIGN KEY(CourseID) REFERENCES COURSES(ID)
        );

        INSERT INTO ENROLLMENTS(StudentID, CourseID) VALUES (1, 1);
        INSERT INTO ENROLLMENTS(StudentID, CourseID) VALUES (2, 1);
        INSERT INTO ENROLLMENTS(StudentID, CourseID) VALUES (3, 2);

        SELECT * FROM ENROLLMENTS;        
        ]]></script>
      title: The Structured Query Language (SQL)
      questions:
        - "Which statements create tables, and which statements insert records into tables?"
        - "What is unique about the ID columns?  What does <code>AUTOINCREMENT</code> mean?"
        - "What are the values of the <code>STUDENTS</code> and <code>COURSES</code> tables?"
    - model: |
        <script type="syntaxhighlighter" class="brush: sql"><![CDATA[        
        -- These use the table created by the statements above...
        -- You can paste that code together to run everything at once
        -- Join
        SELECT * FROM ENROLLMENTS 
          INNER JOIN STUDENTS
            ON STUDENTS.ID = ENROLLMENTS.StudentID
          INNER JOIN COURSES
            ON COURSES.ID = ENROLLMENTS.CourseID;

        -- Aggregation
        SELECT 
          COUNT(ENROLLMENTS.ID) AS NumStudents, 
          AVG(STUDENTS.Age) AS AvgAge 
        FROM ENROLLMENTS
          INNER JOIN STUDENTS
            ON STUDENTS.ID = ENROLLMENTS.StudentID
          INNER JOIN COURSES
            ON COURSES.ID = ENROLLMENTS.CourseID
        WHERE COURSES.CourseNum = "CS377";
        
        -- Group and Sort
        SELECT 
          COUNT(ENROLLMENTS.ID) AS NumStudents, 
          AVG(STUDENTS.Age) AS AvgAge,
          CourseNum
        FROM ENROLLMENTS
          INNER JOIN STUDENTS
            ON STUDENTS.ID = ENROLLMENTS.StudentID
          INNER JOIN COURSES
            ON COURSES.ID = ENROLLMENTS.CourseID
        GROUP BY CourseNum
        ORDER BY NumStudents DESC;        
        ]]></script>
      title: "Aggregating, Joining, Grouping, and Sorting with SQL"
      embed: |
        <iframe height="400px" width="100%" src="https://repl.it/@BillJr99/Sql-AggregationExample?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>       
      questions:
        - "What is being used to create <strong>aggregated</strong> calculated columns, like the average of a column?"
        - "What clause is used to give a column a custom name?"
        - "How do you think you sort by the average age of the students in each class in ascending order?"
        - "What do you think the <code>INNER JOIN</code> keyword does, and what do you think the resulting table looks like?"
        - "Modify the SQL code example below to incorporate the revisions that the class has recommended."
        
tags:
  - tables
  - aggregation
  - keys
  - rds
  - sql
  
---

