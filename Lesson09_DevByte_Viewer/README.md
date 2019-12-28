##	﻿Lesson 09: DevByte Viewer - Tripi&#x0107; Nenad

**Contents:**

 - Caching Data
 - Cache invalidation
 - Local SQL Database - Room Database
 - DAOs
 - Repositories
 - WorkManager
 - Pre-fetchin


## Key takeaways - What was new for me?



### Caching data
Always show data from the database and making sure the server saves before updating the offline cache is the key to implementing a successful offline cache!




### suspend (annotation)
This tells kotlin that this method is coroutine friendly!
```
suspend fun refreshVideos() {  
    withContext(Dispatchers.IO){  
  
 }}
```




### [Worker](https://developer.android.com/reference/androidx/work/Worker)
A class that performs work synchronously on a background thread provided by WorkManager.

```
override suspend fun doWork(): Payload {  
    val database = getDatabase(applicationContext)  
    val repository = VideosRepository(database)  
  
    return try {  
        repository.refreshVideos()  
        return Payload(Result.SUCCESS)  
    } catch (exception: HttpException) {  
        Payload(Result.RETRY)  
    }  
  
}
```




## User-Interface
![alt text](screenshots/devbyte-homescreen.png)


