---
layout: exercise_sql
permalink: /Modules/SQL/Aggregation/Exercise
title: "CS377: Database Design - SQL Aggregation"
excerpt: "CS377: Database Design - SQL Aggregation"

info:
  points: 3
  instructions: "Modify the Aggregation.sql file to answer the database questions below."
  goals:
    - To write a SQL statement performing an aggregated query
    
canvasasmtid: "107081"   
canvaspoints: 3
  
processor:  
  correctfeedback: "Correct!!" 
  incorrectfeedback: "Try again"
  submitformlink: false
  feedbackprocess: | 
    var pos = feedbackString;
  correctcheck: |
    pos.toLowerCase().includes(String.raw``.toLowerCase())
 
files:
  - filename: "Aggregation.sql"
    name: aggregation
    ismain: false
    isreadonly: false
    isvisible: true
    code: | 
        -- TODO: How many grocery items are there?  Call the column NumGrocery.
        -- TODO: How many of each item is there (use only one query!)?  Call the column NumItems, and sort in increasing order by the number of items.
        -- TODO: What is the average cost of produce items? Call the column AvgCost.
        -- TODO: What is the average cost of each type of item (use only one query!)?  Call the column AvgCost and sort in decreasing order by the average cost.

  - filename: "Main.sql"
    ismain: true
    name: main
    isreadonly: true
    isvisible: true
    code: |
      CREATE TABLE INVENTORY (
        ID int, 
        ProductType text,
        ProductName text, 
        Price float,
        Quantity int
      );
     
      INSERT INTO INVENTORY VALUES (1, "Produce", "Banana", 0.33, 5);             
      INSERT INTO INVENTORY VALUES (1, "Household", "Bleach", 2.50, 10);
      INSERT INTO INVENTORY VALUES (1, "Grocery", "Milk", 2.50, 3);
      INSERT INTO INVENTORY VALUES (1, "Grocery", "Orange Juice", 3.99, 4);
      INSERT INTO INVENTORY VALUES (1, "Produce", "Apple", 0.5, 10);
      INSERT INTO INVENTORY VALUES (1, "Household", "Legal Pad", 1.00, 10);
      
---
