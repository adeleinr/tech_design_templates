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
2) What does the API look like (what are the access patterns to these objects)?
3) What volume of requests do we need to support? Read Heavy or Write Heavy?

Design
======
1) Data storage solutions to support above requirements
- Relational vs. Non-Relational. Do you need ACID compliance or not?
- Blob storage for media
b) What entities are we storing?
3) Architecture. Eg Microservice architecture: Connecting our API to the storage layer
- Caching
- Load balancing, CDNs for caching images/videos, files
- Queuing systems/ Async Messaging to support Push Notifications?
- Scaling: Do we need to plan for vertical vs horiozontal scaling both for servers and/or DBs?

Resources
=========
1) A great overall chat on how pieces of a system design go together, granted it is all in the context of google products but it is useful for engineers new to system design.
2) Anutline for system design in the context of an interview but I find it very helpful while outlining what is needed in a tech design. https://interviewing.io/guides/system-design-interview/part-three#part-3-intro
