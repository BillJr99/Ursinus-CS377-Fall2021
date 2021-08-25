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
        f = file("somepath.txt", "a+") # a+ for append to the end, w for overwrite
        
        f.write("This is a test")
        
        data = f.read() # can provide the number of bytes
        
        lines = data.split("\n")
        words = data.split()
        
        f.close()
        ]]></script> 
      title: Basic File Reading
      questions:
        - "Modify this program to read a comma separated value, and for each row, print every column individually via a loop (so that they print without the commas!)."
      embed: |
        <iframe height="400px" width="100%" src="https://repl.it/@BillJr99/PythonFileIO?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe> 
tags:
  - files  
---

