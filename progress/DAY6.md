Caching

For a web service receiving multiple requests to the same object:
Client—>server—> database to obtain (image)
Client—>server—> cache —>>database( optimized architecture)

Hit and miss
Hit- requested information available in the cache
Miss - requested information is not available in the cache, we go to the database and update the cache with the information

Benefits
- speed up the request
- reduce load on the database


Constraints
 Size: main memory is limited, we can only store much

Caching could be either in memory on a single machine in memory cache or distributed cache:  
Distributed cache takes advantage of several machine memory to fully accommodate the data.

We need an eviction strategy : a way to utilize the space available for caching:  retire items from the cache 
Using a specified criteria.

General procedure for adding items to the cache:
1. We check if cache is full, 
	if its not: 
		apply strategy in ranking the item
	else:
		evict an item according to the strategy: then add new item


1. Least Recently Used.
- Every time an item is accessed we take to the back of the queue
- Removal/ eviction of an item is done at the back of the queue which signifies the item that is oldest in terms of access

2. Least Frequently Used 
 - Every time an item is accessed we increase its popularity
- Incase of a removal/ eviction we remove the item with the least popularity
