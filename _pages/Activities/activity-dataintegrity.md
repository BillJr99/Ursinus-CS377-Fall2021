---
layout: activity
permalink: /Activities/DataIntegrity
title: "CS377: Database Design - Data Integrity"
excerpt: "CS377: Database Design - Data Integrity"

info:
  goals: 
    - To differentiate between domain and integrity constraints
    
  models:
    - model: |
        <script type="syntaxhighlighter" class="brush: sql"><![CDATA[        
        -- Employees Table
        CREATE TABLE EMPLOYEE (
            ID INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT, 
            FirstName TEXT NOT NULL, 
            LastName TEXT NOT NULL, 
            Age INTEGER,
            SMOKER INTEGER DEFAULT 0
        );
        
        -- Spouse Table
        CREATE TABLE SPOUSE (
            ID INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT, 
            EmployeeID INTEGER NOT NULL,
            FirstName TEXT NOT NULL, 
            LastName TEXT NOT NULL, 
            Age INTEGER,
            SMOKER INTEGER DEFAULT 0,
            FOREIGN KEY(EmployeeID) REFERENCES EMPLOYEES(ID)
        );

        -- Child Table
        CREATE TABLE CHILD (
            ID INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT, 
            EmployeeID INTEGER NOT NULL,
            FirstName TEXT NOT NULL, 
            LastName TEXT NOT NULL, 
            Age INTEGER,
            SMOKER INTEGER DEFAULT 0,
            FOREIGN KEY(EmployeeID) REFERENCES EMPLOYEES(ID)
        );        
        ]]></script>
      title: Domain and Integrity Constraints
      questions:
        - "The <strong>domain</strong> of the <code>SMOKER</code> attribute is all positive integers, but it is really intended to be <code>0</code> or <code>1</code>.  This is an <code>integrity constraint</code> since it cannot be restricted syntactically by the domain (although some SQL engines do support boolean data types!).  What other integrity constraints do you see in this table?"
        - "Describe a potential <strong>referential integrity</strong> violation that could occur within this database if records can be deleted from the <code>EMPLOYEE</code> table without checking the <code>SPOUSE</code> table first."
        - "What should be done in the <code>EMPLOYEE</code> table if an entry is deleted in the <code>SPOUSE</code> table?"
        - "Draw this schema, and indicate the cardinality of each relationship (1:1, 1:many, optional)."
        - "What inefficiency exists within this table?  Could someone be a spouse of one person and a child of another?  Re-design this schema to eliminate redundant data storage."
        - "What do you think a <a href=&quot;https://www.w3schools.com/sql/sql_check.asp&quot;>CHECK Constraint</a> does?"
        
tags:
  - integrity
  
---

