---
layout: activity
permalink: /Activities/FileIO
title: "CS377: Database Design - File I/O"
excerpt: "CS377: Database Design - File I/O"

info:
  goals: 
    - To read files for processing
    
  models:
    - model: |
        <script type="syntaxhighlighter" class="brush: python"><![CDATA[        
        f = file("somepath.txt", "w") # w+ for overwrite
        
        f.write("This is a test")
        
        data = f.read() # can provide the number of bytes
        
        lines = data.split("\n")
        words = data.split()
        
        f.close()
        ]]></script> 
      title: Basic File Reading
      questions:
        - "Modify this program to read a comma separated value, and for each row, print every column individually via a loop (so that they print without the commas!)."
        
tags:
  - files  
---

