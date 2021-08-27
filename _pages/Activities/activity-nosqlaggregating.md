---
layout: activity
permalink: /Activities/NoSQL/Aggregating
title: "CS377: Database Design - Aggregation with NoSQL"
excerpt: "CS377: Database Design - Aggregation with NoSQL"

info:
  goals: 
    - To define functions to aggregate values in a MongoDB data store
    
  models:
    - model: |
        <script src="https://gist.github.com/javierarilos/015e2ce27cecdea63564.js"></script>
      title: Aggregation Methods
      questions:
        - "Investigate how to limit to two results on a <code>find</code>, but to make those results the second and third documents from the sorted result set."
    - model: |
        <script type="syntaxhighlighter" class="brush: python"><![CDATA[    
        # TODO: create the MongoDB pymongo client 
        # ... with a variable called client
        
        # Compute the average of the $grade field in the collection, in a key called TotalGrade
        collection.aggregate([{$group: {"_id": "_id", "TotalGrade": {$avg: "$grade"}}}}])
        
        # Compute the average grade of each assignment type
        collection.aggregate([{$group: {"_id": "$asmttype", "TotalGrade": {$avg: "$grade"}}}}])
        ]]></script>
      title: Quantitative Aggregation Methods
      questions:
        - "By specifying an <code>_id</code> of <code>_id</code>, each item is individually counted in the average.  Suppose <code>asmttype</code> is a key in your document; what do you think using that key as the <code>_id</code> of the aggregation does to the group?  Try it to find out!"        
        
tags:
  - nosql
  - aggregation
  - programming
  
---

