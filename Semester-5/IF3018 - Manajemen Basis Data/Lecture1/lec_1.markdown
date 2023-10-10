## Lecture 1

### DBMS
* *Software* used to manage and organized large volume of data
* A DBMS serves as an interface between user and apps to manipulate the data within the database. Purpose of database system: 
-> To remove data redudancy and inconsistency.
-> Difficulty in accessing data.
-> Data isolation
-> Integrity problems

### Transactation Management
* Transactation is a collection of opearation that performs a single logical function in a database.
* Transactation management component ensure that databases remain in a consistent state despite system failures and transsactation errors.
* Concurranct-control manager control the interaction among the concurrenct
    transactation, to ensure the consistency of the databases.

### The Log
* Log records chained together by transactation id, so it's easy to undo
    a specific transactation (e.g. to resolve a deadlock)
* Log is often duplexed and archived on "stable" storage.
* All log related activites (an in fact, all concurrency control related
    activities, such as lock / unlock, dealing with deadlocks, etc. ) are
    handled transparently by DBMS.

### Database Users
* Users are differentiated by the way they expect to interact with the system
* Application programmers – interact with system through DML calls
* Sophisticated users – form requests in a database query language
* Specialized users – write specialized database applications that do not fit into the traditional data processing framework
* Naïve users – invoke one of the permanent application programs that have been written previously

### Database Administrator
* Coordinates all the activiteis of the databases system; the database admin
    has a good understanding of the enterprise's information resources and
    needs. Database admins task include:
-> Schema definition
-> Storage structure and access method definition
-> Schema and physical organization modification
-> Granting user authority to access the database
-> Specifying integrity constraints
-> Acting as liaison with users
-> Monitoring performance and responding to changes in requirements
