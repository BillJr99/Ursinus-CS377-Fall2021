---
layout: activity
permalink: /Activities/Modeling/Normalization
title: "CS377: Database Design - Data Modeling and Normalization"
excerpt: "CS377: Database Design - Data Modeling and Normalization"

info:
  goals: 
    - To model database dependencies using a formal notation
    - To normalize database schemas at varying degrees (first, second, and third normal forms)
    
  models:
    - model: |
        <span>\(SSN \longrightarrow Name\)</span>
        <br>
        <span>\(SSN, PhoneNumber \longrightarrow Name, PhoneNumber\)</span>
        <br>
        <span>\(SSN \longrightarrow Name\)</span>, <span>\(Name \longrightarrow Address\)</span>
      title: "Determinant / Dependent Relationships"
      questions:
        - "What is the <strong>determinant</strong> attribute and the <strong>dependent</strong> attribute above?  In other words, if you know the determinant, you can look up the dependent value?"
        - "What determinant / dependent relationships can you find from the data schema in the <a href=\"./ERModel\">ER Modeling Activity</a>?"
        - "Is a primary key a determinant or a dependent?  How about records with a foreign key?"
        - "Describe, in your own words, the axiom of augmentation from the second rule above."
        - "<code>Phone Number</code> should not be part of the primary key; how can we break up this relationship to create a normalized schema?"
        - "Describe the axiom of transitivity, proving that <span>\(SSN \longrightarrow Address\)</span>, in the third relationship above."

        
tags:
  - normalization
  - modeling
  
---

