---
layout: activity
permalink: /Activities/WebServices
title: "CS377: Database Design - RESTful Web Services to Map to CRUD Functionality"
excerpt: "CS377: Database Design - RESTful Web Services to Map to CRUD Functionality"

info:
  goals: 
    - To integrate a Flask web service with a NoSQL database
  additional_reading:
    - title: "Flask RESTful Web Services"
      link: "https://blog.miguelgrinberg.com/post/designing-a-restful-api-with-python-and-flask"
    - title: "Authentication with Flask"
      link: "https://blog.miguelgrinberg.com/post/restful-authentication-with-flask"
    
  models:
    - model: |
        <a title="Santiago Paredes, CC BY 3.0 &lt;https://creativecommons.org/licenses/by/3.0&gt;, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:SQLyHTTP.JPG"><img width="512" alt="SQLyHTTP" src="https://upload.wikimedia.org/wikipedia/commons/1/15/SQLyHTTP.JPG"></a>
      title: Creating a RESTful Web Service in Python with Flask
      embed: <iframe height="400px" width="100%" src="https://repl.it/@BillJr99/PythonMongoDBExample?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>  
      questions:
        - "The URL bindings to each function look similar from function to function; what differentiates them and what actions each function takes?"
        - "What HTTP <strong>methods</strong> (or verbs) do you see in this program?  To what part of the CRUD model does each correspond?"
        - "What happens if you request a person ID that doesn't exist?"
        - "Investigate what it means to be a <strong>RESTful</strong> web service?"
        - "How would you modify this example to incorporate a NoSQL database backend?  How about a relational database backend?"
        
tags:
  - nosql
  - restful
  - programming
  
---

