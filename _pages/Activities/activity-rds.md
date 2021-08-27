---
layout: activity
permalink: /Activities/RDS
title: "CS377: Database Design - Relational Database Systems (RDS)"
excerpt: "CS377: Database Design - Relational Database Systems (RDS)"

info:
  goals: 
    - To define the various components of a typical Relational Database System (RDS)
    - To differentiate between the benefits and costs of various indexing structures to improve search performance
    - To select between memory and disk structures for backing a database
    
  models:
    - model: |
        <a title="Scifipete, CC BY-SA 3.0 &lt;https://creativecommons.org/licenses/by-sa/3.0&gt;, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:RDBMS_structure.png"><img width="512" alt="RDBMS structure" src="https://upload.wikimedia.org/wikipedia/commons/5/57/RDBMS_structure.png"></a>
      title: Structure of a Relational Database Management (RDBMS) System
      questions:
        - "Some items are stored in memory as well as on disk; how is this reconciled?"
        - "What would happen to the in-memory data if the database system was shut down prior to writing to disk?  How might this data be recovered?"
    - model: |
        <img src="https://opentextbc.ca/dbdesign01/wp-content/uploads/sites/11/2014/08/MemFormAug2014.jpg" alt="An example database from Database Design 2nd Ed by Watt and Eng">
        <br>
        <a title="Jorge Stolfi, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Hash_table_4_1_1_0_0_1_0_LL.svg"><img width="256" alt="Hash table 4 1 1 0 0 1 0 LL" src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/58/Hash_table_4_1_1_0_0_1_0_LL.svg/256px-Hash_table_4_1_1_0_0_1_0_LL.svg.png"></a>
      title: Indexing
      questions:
        - "What are some strategies you might use to allow a person to look up the location of a record in a database more quickly than by linear search?"
        - "Can you have more than one index on the same table?  What might this mean?"
        - "Given a person's name, how might you use a hash table to quickly identify the row that contains the corresponding record?"
        - "How might you change the hash if you wanted to search by date-of-birth rather than by name?"
        - "If the hash table isn't big enough to hold every possible record hash, what could happen?  What would the drawback be?"
        - "Given that some indices enable <code>O(1)</code> constant time lookups, while others are <code>O(log n)</code> logarithmic time lookup with respect to the number of records <code>n</code>, what might you speculate is the underlying data structure used to create an index?"        
    - model: |
        <a title="Ashish.rana44, CC BY-SA 4.0 &lt;https://creativecommons.org/licenses/by-sa/4.0&gt;, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:CAP_theorem.png"><img width="256" alt="CAP theorem" src="https://upload.wikimedia.org/wikipedia/commons/8/80/CAP_theorem.png"></a>
        <br>
        <table style="border-collapse:collapse;border-spacing:0" class="tg"><thead><tr><th style="background-color:#000000;border-color:inherit;border-style:solid;border-width:1px;color:#ffffff;font-family:Arial, sans-serif;font-size:14px;font-weight:normal;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal">ACID</th><th style="background-color:#000000;border-color:inherit;border-style:solid;border-width:1px;color:#ffffff;font-family:Arial, sans-serif;font-size:14px;font-weight:normal;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal">BASE</th></tr></thead><tbody><tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Atomic</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Basically Available</td></tr><tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Consistent</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Soft State</td></tr><tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Isolated</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Eventual Consistency</td></tr><tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Durable</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal"></td></tr></tbody></table>
      title: "ACID and BASE, and the CAP Theorem"
      questions:
        - "The CAP Theorem specifies the tradeoff between availability, consistency, and partition tolerance.  What do you think these mean?" 
        - "Why do you think it is not possible to achieve all three items in the CAP Theorem?"
        - "How do the ACID and BASE models appear to balance these tradeoffs?"
        
tags:
  - rds
  - indexing  
---

