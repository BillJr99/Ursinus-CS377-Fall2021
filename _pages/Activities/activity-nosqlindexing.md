---
layout: activity
permalink: /Activities/NoSQL/Indexing
title: "CS377: Database Design - Indexing a Denormalized NoSQL Datastore"
excerpt: "CS377: Database Design - Indexing a Denormalized NoSQL Datastore"

info:
  goals: 
    - To create an index in a NoSQL database
    
  models:
    - model: |
        <script type="syntaxhighlighter" class="brush: python"><![CDATA[    
        # TODO: obtain the collection as usual
        # ... in a variable called collection
        
        collection.ensureIndex({airport: 1})
        
        # you can have more than one index 
        # ... depending on the values you intend to query together!
        collection.ensureIndex({student: 1, grade -1})
        ]]></script>
      title: Indexes in NoSQL databases
      questions:
        - "Look up which sort order is specified by <code>1</code> and which by <code>-1</code>."
        - "Insert many records with a loop into a MongoDB database, and query it with and without an index.  What speedup do you observe for varying numbers of <code>N</code> documents in your collection?  You can use the <code>.explain()</code> method on the cursor returned by your call to <code>find()</code> to obtain information about the time required to execute the query, as well as whether an index (<code>BtreeCursor</code>) was used or not (<code>BasicCursor</code>)."
        
tags:
  - nosql
  - normalization
  
---

