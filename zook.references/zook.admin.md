I. ZooKeeper Concepts And Basics

1. Introduction
  
            The ZooKeeper Mission
            How the World Survived without ZooKeeper
            What ZooKeeper Doesn’t Do
            The Apache Project
            Building Distributed Systems with ZooKeeper
            Example: Master–Worker Application
            Master Failures
            Worker Failures
            Communication Failures
            Summary of Tasks
            Why Is Distributed Coordination Hard?
            ZooKeeper Is a Success, with Caveats

2. Getting To Grips With ZooKeeper
  
            ZooKeeper Basics
            API Overview
            Different Modes for Znodes
            Watches and Notifications
            Versions
            ZooKeeper Architecture
            ZooKeeper Quorums
            Sessions
            Getting Started with ZooKeeper
            First ZooKeeper Session
            States and the Lifetime of a Session
            ZooKeeper with Quorums
            Implementing a Primitive: Locks with ZooKeeper
            Implementation of a Master–Worker Example
            The Master Role
            Workers, Tasks, and Assignments
            The Worker Role
            The Client Role
            Takeaway Messages

II. Programming With ZooKeeper
  
3. Getting Started With The ZooKeeper API
  
            Setting the ZooKeeper CLASSPATH
            Creating a ZooKeeper Session
            Implementing a Watcher
            Running the Watcher Example
            Getting Mastership
            Getting Mastership Asynchronously
            Setting Up Metadata
            Registering Workers
            Queuing Tasks
            The Admin Client
            Takeaway Messages

4. Dealing With State Change
  
            One-Time Triggers
            Wait, Can I Miss Events with One-Time Triggers?
            Getting More Concrete: How to Set Watches
            A Common Pattern
            The Master–Worker Example
            Mastership Changes
            Master Waits for Changes to the List of Workers
            Master Waits for New Tasks to Assign
            Worker Waits for New Task Assignments
            Client Waits for Task Execution Result
            An Alternative Way: Multiop
            Watches as a Replacement for Explicit Cache Management
            Ordering Guarantees
            Order of Writes
            Order of Reads
            Order of Notifications
            The Herd Effect and the Scalability of Watches
            Takeaway Messages

5. Dealing With Failure
  
            Recoverable Failures
            The Exists Watch and the Disconnected Event
            Unrecoverable Failures
            Leader Election and External Resources
            Takeaway Messages

6. ZooKeeper Caveat Emptor
  
            Using ACLs
            Built-In Authentication Schemes
            SASL and Kerberos
            Adding New Schemes
            Session Recovery
            Version Is Reset When Znode Is Re-Created
            The sync Call
            Ordering Guarantees
            Order in the Presence of Connection Loss
            Order with the Synchronous API and Multiple Threads
            Order When Mixing Synchronous and Asynchronous Calls
            Data and Child Limits
            Embedding the ZooKeeper Server
            Takeaway Messages

7. The C Client
  
            Setting Up the Development Environment
            Starting a Session
            Bootstrapping the Master
            Taking Leadership
            Assigning Tasks
            Single-Threaded versus Multithreaded Clients
            Takeaway Messages

8. Curator: A High-Level API For ZooKeeper
  
            The Curator Client
            Fluent API
            Listeners
            State Changes in Curator
            A Couple of Edge Cases
            Recipes
            Leader Latch
            Leader Selector
            Children Cache
            Takeaway Messages

III. Administering ZooKeeper
  

9. ZooKeeper Internals
  
            Requests, Transactions, and Identifiers
            Leader Elections
            Zab: Broadcasting State Updates
            Observers
            The Skeleton of a Server
            Standalone Servers
            Leader Servers
            Follower and Observer Servers
            Local Storage
            Logs and Disk Use
            Snapshots
            Servers and Sessions
            Servers and Watches
            Clients
            Serialization
            Takeaway Messages

10. Running ZooKeeper
  
            Configuring a ZooKeeper Server
            Basic Configuration
            Storage Configuration
            Network Configuration
            Cluster Configuration
            Authentication and Authorization Options
            Unsafe Options
            Logging
            Dedicating Resources
            Configuring a ZooKeeper Ensemble
            The Majority Rules
            Configurable Quorums
            Observers
            Reconfiguration
            Managing Client Connect Strings
            Quotas
            Multitenancy
            File System Layout and Formats
            Transaction Logs
            Snapshots
            Epoch Files
            Using Stored ZooKeeper Data
            Four-Letter Words
            Monitoring with JMX
            Connecting Remotely
            Tools
            Takeaway Messages