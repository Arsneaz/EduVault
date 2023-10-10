### Lecture 2

### Database Tuning
* *Database tuning* adalah kegiatan untuk meningkatkan performa database sehingga bisa berjalan lebih cepat.
Definisi "lebih cepat" biasanya membuat hasil output yang lebih besar, meskipun membuat response-time yang lebih lambat.

* Definisi performa lebih tentang mengenai waktu.
sistem yang lebh cepat meningkakat tujuan bisnis lebih baik lagi. Peningkatan performa biasanya mengartikan segala sesatu berjalan lebih cepat.

### How does one affects performace
-> Hardware
-> Operating system settings
-> Database server parameter settings
-> Database design (schema, indexing)
-> Indexes on Database tables
-> SQL statement

* Issue related on database performace
Pada akhirnya performa yang tinggi membutuhkan dana yang lebih tinggi untuk membuat *hardware* yang cepat.
Faktor untuk mempercepat pengaksesan infromasi
-> cache (size of objcts)
-> Jenis akses (table scan / indexes)
-> Contention between processes
-> Indirect processes

### Bottlenecks Identifying
* Performance of most systems usually limited by performace of few components (E.g. 80% dari sebuah program memakan waktu 20% dan 20% dari program memakan waktu 80%)
* Bottlenecks biasanya di hardware (CPU) atau di dalam sebuah software
* Removing one bottlenecks often exposes another

### Identifying Bottlenecks
* Transactions request a sequence of services.
* With concurrent transactions, it may have to wait for a request service while other transactions are being served.

### Database performace tuning
* DBMS Installation
-> Setiing installation parameters
* Memory Usage (set cache levels)
* Input / outpug contention
* CPU Usage
-> Monitor CPU load
* Application tunning 
-> Modification of SQL code in apps

### Tuning of Hardware
* Typical disk supports about 100 random I/O operations / sec.
* Number of I/O soperations per transaction can be reduced by keeping more data in memory.

* Remember 5-minute rule: If a page that is randomly accessed is used more freq. than once in 5 minutes, then it should be kept in memory
* For sequentially accessed data, there' a 1-minute rule: sequentially accesssed data that is accessed once or more in a minute should be kept in memory

### Schema Tuning the Database
* Vertcally partition relations to isolate the data that is accesed more often (E.g split account into two branch such as **[account-number, branch-name] and [account-number, balance]** )
* Or just improve performace by storing a **denormalized relation**

### Index tuning
* Create appropriate indicies to speed up the queries

### Materialized Views (view sementara)
Later.... This is a new things for me lmao

### Tuning of transactions

### Performance Simulation
* Performance simulation using queueing model, useful to predict bottlenecks, even  

### Performance Benchmarks
* Suites of task used to quantify the performance of software systems.
* Important in compring database systems become more standards and compliant.
* Commonly used performance measures
-> Throughtput (transaction per time TPS)
-> Response time (delay from submission of transaction)
-> Availability (mean time to failure)

* Beware when computing average throughput of different transaction types
-> E.g supposed a system runs transaction type A at 99 tps, and type B at 1 tps.
 There some this stuff in the future later...

### Database Application Classses
* Online Transaction Processsing (OLTP)
Req. high concurrency and cleaver techniques to speed commit processing
* Decision support applications
Including **online analytical processing (OLAP)** aplication

### Benchmarks Suites
Transaction Processing Council (TPC) benchmarks suites are widely used.
This TPC stuff, I dont even know mate lmao...

### Summary
At the end, there are few options for performance tuning such as
* Hardware (all related on physical component such as memory, processor, storage)
* Skema database (Fragmentasi, denormalisasi)
* Transaksi (Konkurensi, Serializability)
* File (The method accessing data such as: Index, sequential, Hash, B-Tree)