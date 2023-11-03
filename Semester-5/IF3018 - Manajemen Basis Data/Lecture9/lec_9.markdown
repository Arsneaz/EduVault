## Transcation Processing

### Definition of Transaction
+ _Sequence of operations_ that form a single unit of work.
+ A _transaction_ T, transforms one consistent database state into another consistent database state (confirming the transition state).
+ This whole transaction is either be succeed or the effect must be undone (`rollabck`)

<p align="center">Example of Transation</p>

![image](https://github.com/Arsneaz/EduVault/assets/96061442/49de4a45-3c5e-45ee-b979-7f557ad6b93c)

### Transaction States 
+ Active: This phase is on initial state; a transaction is in this state
+ Partially Commited: After the last statement has been executed
+ Commited: After successfull completion
+ Failed: After discovery that a normal exec is no longer possible (such that bad input, system error)
+ Aborted: Sending a rollback

![image](https://github.com/Arsneaz/EduVault/assets/96061442/f956ddf6-96fe-4e4d-b068-911fcb21f681)

### Transaction Processing System
+ Transaction execution is controlled by TP (Transaction Processing) Monitor
    + TP monitor and DBMS guarantee the special properties of transaction

### Challeges in Transaction Processing
+ Reliability - system should rarely fail
+ Availability - system must be up all the time
+ Response time - within 1-2 seconds
+ Throughput - thousands of transactions/second
+ Scalability - start small, ramp up to Internet-scale
+ Security – for confidentiality and high finance
+ Configurability - for above requirements + low cost
+ Atomicity - no partial results
+ Durability - a transaction is a legal contract
+ Distribution - of users and data

### Single-User System
![image](https://github.com/Arsneaz/EduVault/assets/96061442/27f5f7c4-3cdb-43e0-9470-f5cad71c80fa)
The user module which are consistent in layer (`presentation service` and `application services` layer) to connect into the DBMS
+ Presentation Service - display forms, handles flow of information
+ Application Services - implements user request, interact with DBMS
+ ACID properties

### Two-Tiered Models of TPS
![image](https://github.com/Arsneaz/EduVault/assets/96061442/d365e34d-22e7-41d5-9ecb-ae279d65e95f)
Simplified the layer just only several layer being takes care of the server application.
![image](https://github.com/Arsneaz/EduVault/assets/96061442/67206a5f-6e5f-4413-adab-13a57766e94b)

### Transaction Processing Summary
Kemampuan untuk transaksi itu dilakukan di dalam basis data untuk mencapai persistance dengan konfigurasi
+ Lingkungan dari aplikasi service

### ACID Properties
- Atomicity - all or nothing
- Consistency - Preserve Database integrity
- Isolation - Execute as if they were run alone
- Durability - results aren't loss by a failure (by a rollback)


