---
layout: activity
permalink: /Activities/NoSQL/DataModels
title: "CS377: Database Design - NoSQL Data Models"
excerpt: "CS377: Database Design - NoSQL Data Models"

info:
  goals: 
    - "To distinguish between four types of NoSQL database models: document, key-value, columnar, and graph"
  additional_reading:
    - title: "Types of NoSQL Databases"
      link: "https://www.mongodb.com/scale/types-of-nosql-databases"
    - title: "Setting up Redis"
      link: "https://dev.to/ramko9999/host-and-use-redis-for-free-51if"
      
  models:
    - model: |
        <a title="JuliaL0313, CC BY-SA 4.0 &lt;https://creativecommons.org/licenses/by-sa/4.0&gt;, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Database-document.png"><img width="256" alt="Database-document" src="https://upload.wikimedia.org/wikipedia/commons/e/ec/Database-document.png"></a>
      title: Document Database
      questions:
        - "What does this model remind you of, that you have seen before?"
        - "What types of applications are best suited to this model?"
    - model: |
        <a title="Clescop, CC BY-SA 4.0 &lt;https://creativecommons.org/licenses/by-sa/4.0&gt;, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:KeyValue.PNG"><img width="256" alt="KeyValue" src="https://upload.wikimedia.org/wikipedia/commons/5/5b/KeyValue.PNG"></a>
      title: Key-Value Database
      questions:
        - "How does this model relate to a normalized relational database?"
        - "How is this model similar to a document model?  How is it different?"
        - "What types of applications are best suited to this model?"
    - model: |
        <a title="Scifipete, CC BY-SA 3.0 &lt;https://creativecommons.org/licenses/by-sa/3.0&gt;, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:Oracle_Table_in_a_Tablespace.jpg"><img width="512" alt="Oracle Table in a Tablespace" src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2c/Oracle_Table_in_a_Tablespace.jpg/512px-Oracle_Table_in_a_Tablespace.jpg"></a>
      title: Columnar Database
      questions:
        - "What does this model remind you of, that you have seen before?"
        - "What types of applications are best suited to this model?"
    - model: |
        <a title="Originally uploaded by Ahzf (Transferred by Obersachse), CC0, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:GraphDatabase_PropertyGraph.png"><img width="512" alt="GraphDatabase PropertyGraph" src="https://upload.wikimedia.org/wikipedia/commons/3/3a/GraphDatabase_PropertyGraph.png"></a>
        <br>
        <p><a href="https://commons.wikimedia.org/wiki/File:Rdf-graph3.png#/media/File:Rdf-graph3.png"><img src="https://upload.wikimedia.org/wikipedia/commons/f/fd/Rdf-graph3.png" alt="Rdf-graph3.png"></a><br>Public Domain, <a href="https://commons.wikimedia.org/w/index.php?curid=17096">Link</a></p>
      title: Graph Database
      embed: <iframe height="400px" width="100%" src="https://repl.it/@BillJr99/PythonRedisExample?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe> 
      questions:
        - "What types of applications are best suited to this model?"
        - "Using <a href=\"https://www.redislabs.com\">redis</a>, set up a graph database of the groups in class, and print out each group.  Here is the <a href=\"https://github.com/RedisGraph/redisgraph-py\">Redis for Python API Documentation for reference</a>."
        
tags:
  - nosql
  - modeling
  
---

