---
layout: activity
permalink: /Activities/TextAndFileManagement
title: "CS377: Database Design - Text and File Management"
excerpt: "CS377: Database Design - Text and File Management"

info:
  goals: 
    - To represent models
    
  models:
    - model: |
        <a title="Gringer, Public domain, via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File:CousinTree_kinship.svg"><img width="512" alt="CousinTree kinship" src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d7/CousinTree_kinship.svg/512px-CousinTree_kinship.svg.png"></a>
        <br>
        <iframe src="https://en.wikipedia.org/wiki/GEDCOM#Example" width="100%"></iframe>
      title: "A Flat File Structure: GEDCOM"
      questions:
        - "The GEDCOM file format defines ancestral history.  What do you think each of the line headings mean?  If you aren't sure, write one down and skip it for now; we'll check the <a href=\"https://gedcom.io/specifications/FamilySearchGEDCOMv7.html\">specifications</a> later!"
        - "What do you think the numbers mean at the beginning of each line?"
        - "What is a &quot;record&quot; in this format?  How many different types of records can you find, and how many records of each type are there?"
        - "Draw a diagram representing the family depicted by this example."
        - "Could you represent this data in a more friendly way by making &quot;tables&quot; or spreadsheets?  Try representing the basic information in Microsoft Excel, using the <a href=\"https://support.microsoft.com/en-us/office/vlookup-function-0bbc8083-26fe-4963-8ab8-93a18ad188a1\"><code>VLOOKUP</code> function</a> to refer to data across tables."
    - model: |
        <iframe src="https://api.weatherusa.net/v1/forecast?q=40.1915,-75.4559&daily=0&units=e&maxtime=7d" width="100%"></iframe>
      title: Javascript Object Notation (JSON)
      questions:
        - "This JSON result was returned from a web request to <a href=\"https://api.weatherusa.net/v1/forecast?q=40.1915,-75.4559&daily=0&units=e&maxtime=7d\">https://api.weatherusa.net/v1/forecast?q=40.1915,-75.4559&daily=0&units=e&maxtime=7d</a>, which obtains the 7-day forecast at Ursinus College given the College's latitude and longitude GPS coordinates.  Use a <a href=\"https://jsonformatter.org/json-pretty-print\">JSON Pretty Printer</a> to better format the JSON for reading."
        - What do the curly braces represent?
        - What does the square bracket represent?
      embed: |
        <iframe height="400px" width="100%" src="https://repl.it/@BillJr99/PythonWeatherClient?lite=true" scrolling="no" frameborder="no" allowtransparency="true" allowfullscreen="true" sandbox="allow-forms allow-pointer-lock allow-popups allow-same-origin allow-scripts allow-modals"></iframe>  
    - model: |
        <div align="left">
        <pre>
        <code>
        {
            "response": {
                "version": "0.1",
                "termsofService": "http://www.wunderground.com/weather/api/d/terms.html",
                "features": {
                    "conditions": 1
                }
            },
            "current_observation": {
                "image": {
                    "url": "http://icons-ak.wxug.com/graphics/wu2/logo_130x80.png",
                    "title": "Weather Underground",
                    "link": "http://www.wunderground.com"
                },
                "display_location": {
                    "city": "Philadelphia",
                    "state": "PA",
                    "zip": "19104",
                    "latitude": "39.96150970",
                    "longitude": "-75.19716644",
                    "elevation": "41.00000000"
                },
                "observation_location": {
                    "full": "University City - West Philadelphia, Philadelphia, Pennsylvania",
                    "city": "University City - West Philadelphia, Philadelphia",
                    "state": "Pennsylvania",
                    "latitude": "39.950554",
                    "longitude": "-75.211868",
                    "elevation": "70 ft"
                },
              "temp_f": 76.5,      
            }
        }
        </code>
        <pre>
        </div>
      title: A Sample JSON Response
      questions:
        - "What is the path to <code>longitude</code>?"
        - "What is the path to <code>temp_f</code>?"
        
tags:
  - files  
---

