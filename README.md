# THEORIES

MOCK EXAM THEORY QUESTION ANSWERS 
1/Would you use Hibernate in your project? What are other alternatives you consider?
      
      Yes, 
      Alternatives
      -Node js 
      -.NET
      -Spring JDBC Template
      -Sormula
       More can be find in (https://dzone.com/articles/jpa-hibernate-alternatives)

2/- If you start a new project for online shopping, will you select Java technology stack? Why? https://www.thinslices.com/blog/choose-technology-stack() | | (http://www.smashstack.com/articles/why-your-developer-cares-about-technology-stacks-and-why-you-should-too/)

      Yes, Becasue java technology stack will enable the us to manage and monitor the transportation of data that went from         the users to the shop's databases. Furthermore, java stacks will provide the shop the needed security measures to             prevent unauthorised access to the database or lost of data. 
      
      Also, when implement the correct technology stack. it will be better for the shop in multiple perpective such as               maintainabilites and flexibilities in the future, when the shop scales itself.

3/Will you use microservices in your next project ? Why ? (https://blog.digitalfoundry.com/are-microservices-right-for-your-next-project/)

      Yes, Because:
      Containing the work:

      What trips up most large enterprise organizations is not competency, it’s the process. Microservices allow you to contain a prioritized project to a set team, and not disrupt other teams as you get it done.

      Embracing new technology without the risk:

      Leverage the latest and greatest tools and technology to build your new service without the headache of making it work with the entirety of your legacy back-end architecture. Microservice development is technology agnostic, which means you can push your boundaries on your contained project, without hanging up the whole system.

      Scaling Up:

      Architecting a microservice allows your team to independently deploy and respond to increased volume quickly. As many companies on the cutting edge of technology have realized, you will inevitably experience the need to scale up specific areas of your product. Netflix, Uber, and Amazon are just a few that take advantage of microservices to continue providing a stable product while scaling up specific features.

4/Discuss some strategies to scale your database systems (https://www.clustrix.com/bettersql/scale-vs-scale/)

      Sharding: The conventional wisdom of how to scale your database past the single-instance has been database sharding, or partitioning your data across multiple servers. However, this method is costly and require talent engineers to apply this method to current database

      NoSQL: The alternative way to relational database is to use NoSQL database such as MongoDB. With NoSQL database, there is no headache to scale up database system anymore like relational database.  


-----------------------------**************************-----------------------------------************************---------------------

MicroService: 

      Microservices - also known as the microservice architecture - is an architectural style that structures an application as a             collection of loosely coupled services, which implement business capabilities. The microservice architecture enables the                 continuous delivery/deployment of large, complex applications. It also enables an organization to evolve its technology stack.
      
      SPLIT A BIG COMPLEX OPERATION INTO SMALL OPERATIONS which operate seperately.

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
