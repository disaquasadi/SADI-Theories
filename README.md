# SADI_MicroService

Load Balancers : https://www.nginx.com/resources/glossary/load-balancing/

      Load balancing refers to efficiently distributing incoming network traffic across a group of backend servers, also known as a server farm or server pool.

      a load balancer performs the following functions:

      Distributes client requests or network load efficiently across multiple servers
      Ensures high availability and reliability by sending requests only to servers that are online
      Provides the flexibility to add or subtract servers as demand dictates

High Availabilities : http://searchdatacenter.techtarget.com/definition/high-availability

    high availability refers to a system or component that is continuously operational for a desirably long length of time, can be measured relative to "100% operational" or "never failing." 



Share Nothing Architecture(sticky sessions) : http://wiki.metawerx.net/wiki/StickySessions

    A method used with Application Load Balancing, to achieve server-affinity.

    A router or load balancer with sticky-session support can assign a single server to a particular user, based on their HTTP session or IP address. The assigned server is remembered by the router for a certain amount of time, ensuring that all future requests for the same session are sent to the same server.

    To be effective, the router must remember the server selection for a time that is longer than the session timeout.

    Advantages
    Reasonably simple to implement for experienced network administrators.
    Reduces the need to implement session-failover, as users are only sent to other servers if one goes offline.
    Load balancer/router is often responsible for detecting offline servers, providing faster request-failover than round robin DNS-based load balancing.

    Disadvantages
    Difficult to set up for network administrators who are new to sticky sessions.
    Problems can be difficult to diagnose. See the sections below for the main issues.
    The load-balancer/router must be load-balanced itself, or it becomes a point of failure that will take down an entire cluster.
    Cannot provide global load-balancing (whereas round-robin DNS can).
    Session-failover is often not implemented, as there is reduced need. If a server goes offline, all users lose their session.

Relational DBMS's problem is the join query. It's extremely difficult to scale ===> Use mongodb or big database.

-session is a special values save in the server(define the usage of the users)

-when session or server died, the load balancers will automatically reroot the request to the new server by saving the sessions into the database

Database Replication : http://searchsqlserver.techtarget.com/definition/database-replication

    Database replication is the frequent electronic copying data from a database in one computer or server to a database in another so that all users share the same level of information. The result is a distributed database in which users can access data relevant to their tasks without interfering with the work of others. The implementation of database replication for the purpose of eliminating data ambiguity or inconsistency among users is known as normalization.

    Database replication can be done in at least three different ways:

    Snapshot replication: Data on one server is simply copied to another server, or to another database on the same server.
    Merging replication: Data from two or more databases is combined into a single database.
    Transactional replication: Users receive full initial copies of the database and then receive periodic updates as data changes.
    A distributed database management system (DDBMS) ensures that changes, additions, and deletions performed on the data at any given location are automatically reflected in the data stored at all the other locations. Therefore, every user always sees data that is consistent with the data seen by all the other users. 

Cluster - the data will be spilt equally amongst the servers so that the server will be able to process more requests ./however if 1 of the server died all things fail. ==> mirror storing(update the info in every server.

Change existing code every-time over the system
