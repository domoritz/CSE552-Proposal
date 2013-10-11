# CSE552 Proposal - Profiling and Visualizing Query Execution in Distributed Database System


## Background
* Database system need to transform user's high level queries, eg. SQL, Datalog into physical query plan for the execution of the query
* Physical query plan is the actual exectution map of a database system. Usually it can be viewed as a DAG which consisted by basic operators, such as JOIN, GROUP BY, SCAN, APPLY and relational tables (if the data).
* In distributed database system, the introduction of SHUFFLE operator and data partitioning will make query plan more complicated.

## Objective

* Profile the execution of a physical query plan of distributed database
* Visually present the profiling of the physical query plan execution 
* Use the Visualization to analyze and improve the physical plan

## Platform

* Use Myria, the under developing big data management system

## Question we want to answer with our visualization

* The implicit dependencies between operators
* What is the bottleneck of the execution? Improving which part could best boost the performance?
* How good is the load balancing. If it is skewed, how bad it can affect the performance?
