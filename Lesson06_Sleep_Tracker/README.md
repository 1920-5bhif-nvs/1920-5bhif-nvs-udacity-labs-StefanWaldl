##	﻿Lesson 06: Sleep tracker - Tripi&#x0107; Nenad

**Contents:**

 - Persistence
 - Room Database
 - Test room databases
 - DAO
 - Multithreading & Coroutines
 - SQLite
 - Synchronized


## Key takeaways - What was new for me?



### Room Database
Room provides an abstraction layer over SQLite to allow fluent database access while harnessing the full power of SQLite. Apps that handle non-trivial amounts of structured data can benefit greatly from persisting that data locally. The most common use case is to cache relevant pieces of data. That way, when the device cannot access the network, the user can still browse that content while they are offline. Any user-initiated content changes are then synced to the server after the device is back online.




### DAO
Marks the class as a Data Access Object. Data Access Objects are the main classes where you define your database interactions. They can include a variety of query methods. The class marked with `@Dao` should either be an interface or an abstract class. At compile time, Room will generate an implementation of this class when it is referenced by a Database.




### Coroutines
Coroutines handle long-running tasks elegantly and efficiently. Kotlin coroutines convert callback based code to sequential code. Coroutines are asynchronus, non-blocking and sequential. Non-blocking means that the system is not blocking the UI- or Main-Thread.




### @Volatile
Helps that the INSTANCE is always up to date and the same to all execution threads. All changes are immediately visible to any other threads.




### Synchronized-Block
Only one executing thread can acces the block which makes sure that the DB is initialized once.

## User-Interface
![alt text](screenshots/sleep_quality_tracker_start.png)
![alt text](screenshots/sleep_quality_tracker_quality.png)
![alt text](screenshots/sleep_quality_tracker_stop.png)









