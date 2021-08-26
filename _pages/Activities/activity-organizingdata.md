---
layout: activity
permalink: /Activities/OrganizingData
title: "CS377: Database Design - Data Organization: Fields, Records, and Keys"
excerpt: "CS377: Database Design - Data Organization: Fields, Records, and Keys"

info:
  goals: 
    - To define a record, field, and key in a database system
    - To explain the importance and challenges of internal consistency
    
  models:
    - model: |
        <img alt="Ham Radio Logbook Showing Two Records with Slighly Different Field Values" src="../images/logbook.png">
      title: "Records, Fields, and Keys"
      questions:
        - "What records do you see in the data?  What fields?"
        - "What should happen if a particular field does not have a value?"
        - "Two records are sometimes linked together; what do you think this means in this application?"
        - "The two records are somewhat different; how, and what should be done about this?"
        - "What field(s) are most likely to be unique throughout the table?  These are referred to as a <strong>key</strong>, but a single serial number is often used instead to guarantee uniqueness."
    - model: |
        <img alt="An Example Gradebook" src="https://s3.amazonaws.com/kb-media.populi.co/course_gradebook_editing_grades.png">
      title: "Internal Consistency"
      questions:
        - "Which fields should a user be able to update?  Which ones should a user not update directly, and why?"
        
tags:
  - records
  - fields
  - keys  
---

