CSE552 Proposal - Profiling and Visualizing Query Execution in Distributed Database System
==========================================================================================


## Background
* Database system need to transform user's high level queries, eg. SQL, Datalog into physical query plan for the execution of the query
* Physical query plan is the actual exectution map of a database system. Usually it can be viewed as a DAG which consisted by basic operators, such as JOIN, GROUP BY, SCAN, APPLY and relational tables (if the data).
* In distributed database system, the introduction of SHUFFLE operator and data partitioning will make query plan more complicated.

## Objective

* Profile the execution of a physical query plan of distributed database
* Visually present the profiling of the physical query plan execution 
* Use the Visualization to analyze and improve the physical plan

## Platform

* Use Myria, the under development distributed big data management system
* Visualization as web aplication with front and backend. 

## Question we want to answer with our visualization

* The implicit dependencies between operators
* What is the bottleneck of the execution? Improving which part could best boost the performance?
* How good is the load balancing? If it is skewed, how bad it can affect the performance?
* Is an execution IO/ Network or CPU bound?

## Tasks

* Log events of operators.
* Collect the logs on one node.
* Evaluate the logs and write summaries to local database.
* Visualize query execution on a web page.
* Analyze the query execution and find patterns that suggest a problem. Visualize the problem or give a desciption. 

## Visualization

* Gantt chart which also shows the hierarchy of the operators and possibly where an operator is executed.


## Quantitative output

* There will not be a measurable output.
* We hope to answer questions about the Myria query execution and develop physical optimization rules based on the observations. 



## TODO


### Visualization 

#### QF

* start, end, duration
* percentages of states on hover over name

### Data (TBD)

#### Routes

* `/query/id-2/qf=1&worker=1` specific data for one worker and one qf
* `/query/ID/working?qf=4` aggregated per worker, working/ not working for root
