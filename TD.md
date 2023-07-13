Tech Design Guide

Problem
=======
What problem are we working on solving? Could be a summary from the product spec.

Functional Requirements
=======================
1) Identify main business objects and their relationships.
Do business objects contain media? (Images, audio, files)
Which objects can be mutated and which can't? Deleted?
2) What are the use cases? This about access patterns "Given user id 123, return all orders".
Create a table of main use cases, edge cases and behaviors that are not explicit in the product spec. Make sure to run them by product and seek agreement.
It is crucial that this captures the bulk if not all of the behaviors to be supported as this will be used by QA as well as their starting point for a testing plan.



Non Functional Requirements
===========================
1) Performance: Which access patterns require good performance?
2) Availability: Eg 99% availability
3) Security: Is there a workflow that requires a special handling?

Data types, API and Scale
=========================
1) What data types does the system need to store?
2) What does the API look like?
3) What volume of requests do we need to support?
