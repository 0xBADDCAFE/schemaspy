SchemaSpy
=====================================

**Document your database simply and easily**

Do you hate starting on a new project and having to try to figure out someone else's idea of a database? 
Or are you in QA and the developers expect you to understand all the relationships in their schema? If so then this tool's for you.


What is SchemaSpy ?
-------------------

SchemaSpy is a Java-based tool (requires Java 8 or higher) that analyzes the metadata of a schema in a database and generates a visual representation of it in a browser-displayable format. 
It lets you click through the hierarchy of database tables via child and parent table relationships as represented by both HTML links and entity-relationship diagrams. 
It's also designed to help resolve the obtuse errors that a database sometimes gives related to failures due to constraints.

SchemaSpy comes with ABSOLUTELY NO WARRANTY. |br|
SchemaSpy is free software licensed and distributed under LGPL version 3 or later |br|
SchemaSpy can be redistributed under the conditions of LGPL version 3 or later. |br|
http://www.gnu.org/licenses/

If you like SchemaSpy, don't forget to give us a star on |github_link|.

SchemaSpy uses the dot executable from `Graphviz <http://www.graphviz.org/>`_ to generate graphical representations of the table/view relationships. This was initially added for people who see things visually. 
Now the graphical representation of relationships is a fundamental feature of the tool. Graphvis is not required to view the output generated by SchemaSpy, but the dot program should be in your PATH 
(not CLASSPATH) when running SchemaSpy or none of the entity relationship diagrams will be generated (or use the -gv option).

SchemaSpy uses JDBC's database metadata extraction services to gather the majority of its information, but has to make vendor-specific SQL queries to gather some information such as the SQL associated with a view and the details of check constraints. 
The differences between vendors have been isolated to configuration files and are extremely limited. Almost all of the vendor-specific SQL is optional.

Features
--------

* Supports most JDBC compliant dbms (support missing? you can add your own)
* Generates |er_wiki_link| for foreign keys
* Generates |er_wiki_link| for implied relationships (name, type) of a column matches a primary key
* Generates |er_wiki_link| for relationships based on rails naming conventions
* Shows column relationship and actions
* Shows routines (Functions/Stored procedures)
* Shows views and definitions
* Will render |markdown_link| present in comments
* Allows for supplying additional metadata, see :ref:`schemameta`
* Present a set of found anomalies

Sample documentation
--------------------

Browse some `sample documentation <http://schemaspy.org/sample/index.html>`_ generated by SchemaSpy. Note that this was run against an extremely limited schema so it doesn't show the full power of the tool.

SchemaSpy GUI
-------------

SchemaSpy is a command line tool. If you're more comfortable with the point-and-click approach then try out `Joachim Uhl's <http://www.joachim-uhl.de/>`_ `SchemaSpyGUI <http://schemaspygui.sourceforge.net/>`_. 

SchemaSpy was mentioned in one of th  O'Reilly's book |java_power_tools|

.. links external on new tab
.. |github_link| raw:: html

   <a href="https://github.com/schemaspy/schemaspy" target="_blank">Github</a>

.. |java_power_tools| raw:: html

   <a href="http://my.safaribooksonline.com/9780596527938/I_book_d1e1d1e112?portal=oreilly#X2ludGVybmFsX0h0bWxWaWV3P3htbGlkPTk3ODA1OTY1Mjc5MzglMkZjaDEyJnF1ZXJ5PQ==" target="_blank">Java Power Tools</a>

.. |br| raw:: html

   <br />

.. |markdown_link| raw:: html

   <a href="https://daringfireball.net/projects/markdown/" target="_blank">markdown</a>

.. |er_wiki_link| raw:: html

   <a href="https://en.wikipedia.org/wiki/Entity%E2%80%93relationship_model" target="_blank">ER diagram</a>
