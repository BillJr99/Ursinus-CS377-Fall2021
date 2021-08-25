---
layout: activity
permalink: /Activities/RelationalModel
title: "CS377: Database Design - Relational Data Model"
excerpt: "CS377: Database Design - Relational Data Model"

info:
  goals: 
    - To express database table relationships through mathematical abstraction
    - To implement database schemas into programming constructs using libraries and database engines
    - To describe the advantages and disadvantages of different database engines
  additional_reading:
    - link: https://pypi.org/project/PyMySQL/
      title: PyMySQL Python Library
    - link: https://docs.python.org/3/library/sqlite3.html
      title: Sqlite3 Python Library
    - link: https://www.tutorialspoint.com/postgresql/postgresql_python.htm
      title: PostgreSQL Python Library
    - link: https://github.com/comptoolsres/Jupyter_content/blob/main/py4e_ch15_databases.ipynb
      title: Databases and SQL
  models:
    - model: |
        <table style="border-collapse:collapse;border-spacing:0" class="tg"><thead><tr><th style="background-color:#000000;border-color:inherit;border-style:solid;border-width:1px;color:#ffffff;font-family:Arial, sans-serif;font-size:14px;font-weight:normal;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal">FirstName</th><th style="background-color:#000000;border-color:inherit;border-style:solid;border-width:1px;color:#ffffff;font-family:Arial, sans-serif;font-size:14px;font-weight:normal;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal">LastName</th><th style="background-color:#000000;border-color:inherit;border-style:solid;border-width:1px;color:#ffffff;font-family:Arial, sans-serif;font-size:14px;font-weight:normal;overflow:hidden;padding:10px 5px;text-align:center;vertical-align:top;word-break:normal">Age</th></tr></thead><tbody><tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Alex</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Smith</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">20</td></tr><tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Lee</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Jones</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">21</td></tr><tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Brian</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">McMullen</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">18</td></tr><tr><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Samantha</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Johnson</td><td style="border-color:inherit;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">22</td></tr><tr><td style="border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Lee</td><td style="border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">Jones</td><td style="border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;overflow:hidden;padding:10px 5px;text-align:left;vertical-align:top;word-break:normal">24</td></tr></tbody></table>
        <br>
        <span>\(FirstName \times LastName \times Age = \{(firstname, lastname, age) : firstname \in \{a-zA-Z\}+, lastname \in \{a-zA-Z\}+, age \in \mathbb{Z}^{+}\}\)</span>
      title: Domains and Relations
      questions:
        - "If the <strong>domain</strong> of the <code>Age</code> field is all positive numbers <code>Age > 0</code>, what is the domain of <code>FirstName</code>?"
        - "Translate the cartesian product formula into your own words describing the nature of the table it defines."
        - "Is it ever appropriate to have the same row in a table more than once?  What is the alternative if such a situation is needed?"
        - "Suppose you wish to track the history and provenance of a record.  For example, if someone changes their name, a record of both names and the dates during which each name was valid would be included.  What tables and fields might you add to do this?"
    - model: |
        <script src="https://gist.github.com/BillJr99/53c92b77f465ba1f7259beeec31f50cb.js"></script>
        <br>
        <script src="https://gist.github.com/BillJr99/138231874d9d1c00bab4d20d1ff4267e.js"></script>
      title: Database Programming and SQL Library Support
      questions:
        - "Sketch the database schema implemented with the two programs (they are the same!)"
        - "What basic aggregation operations can you find in each program?"
        - "Why do you think there are two versions of this program, one for the Sqlite database engine, and one for the MySQL database engine?"
        
tags:
  - relational
  - programming  
---

