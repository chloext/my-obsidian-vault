
###### 2024-10-25 12:36
###### Status:
###### Tags: [[System Design]] 

# Types of Data Systems

- _[[databases]]_: Store data so the application or other applications can find it again later (NoSQL, Graph Database)
- _[[caches]]_: Remember result of an expensive operation to speed up reads  (Memcached, [[LRU Cache]])
- _[[search indexes]]_: Allow user to search data by keyword or filter it in various ways
- _[[stream processing]]_: Send message to another process, to be handled asynchronously ([[asynchronous]])
- _[[batch processing]]_: Crunching large amount of accumulated data periodically

![[1_fyf4FbgKcQ8r1YRSZ3ek9Q 1.webp]]
![[1__WvcpX-pF9qyDuET0nBFqA.webp]]

# Reference
- [[Designing Data-Intensive Applications]] chapter 1 p3
- https://medium.com/plumbersofdatascience/stream-vs-batch-processing-explained-acfcdce4ce6