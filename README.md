# completablefuture-demo

* Future was introduced in JDK 5
* CompletableFuture is an implementation of Future Interface
* There were some restrictions in Future which CompletableFuture resolves
* It cannot be manually completed.
* Multiple futures cannot be chained together.
* We cannot combine multiple futures together.
* No proper Exception Handling mechanism.

* Normal java application runs on main thread, whereas whenever we create new thread pool from ExecutorService and run, than it would run in a seperate thread and not main thread.
Thread.getcurrentThread.getName()

### runAsync() vs supplyAsync()
If we want to run some background tasks asynchronously and donot want to return anything from that task, then use CompletableFuture.runAsync() method. It takes a runnable object and returns CompletableFuture<Void>
1. CompletableFuture.runAsync(Runnable)
2. CompletableFuture.runAsync(Runnable, Executor) //difference is if we wont provide Executor the thread will be of type fork join, whereas if we give executor, the thread will be from the thread pool we create.

If we want to run some background tasks asynchronously and want to return anything from that task, then use CompletableFuture.supplyAsync() method. It takes a Supplier<T> object and returns CompletableFuture<T>, where T is the type of value obtained by calling the given supplier. 
1. CompletableFuture.supplyAsync(Runnable)
2. CompletableFuture.supplyAsync(Runnable, Executor)

### void vs Void ???
### Supplier vs Consumer
### theApply vs thenApplyAsync