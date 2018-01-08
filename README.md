# SADI_MicroService

Load Balancers 

High Availabilities

Share Nothing Architecture(sticky sessions) 

Relational DBMS's problem is the join query. It's extremely difficult to scale ===> Use mongodb or big database.

-session is a special values save in the server(define the usage of the users)

-when session or server died, the load balancers will automatically reroot the request to the new server by saving the sessions into the database

Replication

Cluster- the data will be spilt equally amongst the servers so that the server will be able to process more requests ./however if 1 of the server died all things fail. ==> mirror storing(update the info in every server.

Change existing code every-time over the system
