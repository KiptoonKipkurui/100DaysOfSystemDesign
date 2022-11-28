## Design Patterns
**System design** defines the architecture and product design by building scalable, reliable and maintainable systems

## Basics Concepts
<br>

- <a href="#servers">Web Servers</a>
- <a href="#databaseinclusion">Database Inclusion</a>
  * [Database strategies]()
    * [Master-slave Replication]()
    * [Circular Manager Worker Model]()
- <a href="#sharding">Sharding</a>
  * [Sharding Strategies]()
- <a href="#loadbalancers">Load Balancers</a>
- <a href="#caching">Caching</a>
    * [Implementing Cache]()
    * [Cache Eviction Policies]()
    * [Updating Cache]()
- <a href="#cdn">CDN</a>

---


 **How would you go from something super arbitrary(single server stack) to something that can scale to millions of concurrent users at the same time**
<br>

## **[Day 1]()**

## <b id="servers">Web Servers</b>

<img width="420" src="https://user-images.githubusercontent.com/77434770/192516427-2d12593b-73b7-4c5e-b0f1-df74f3699993.png" alt="Design"/>

## <b id="databaseinclusion">Database Inclusion</b>

<img width="420" src="https://user-images.githubusercontent.com/77434770/192515986-884801e3-128e-4c0f-be8d-d453ce5c1a32.png" alt="Database Design"/>

<br>

## **[Day 2]()**

### <b id="servers">Database strategies</b>
Scaling the database as a separate entity from the server
<br>

**ACID**
* A-Atomicity
* C-Correctness
* I-Isolation (database mutation)
* D-Durable (databases should be reliable and durable)

DB Types
- NoSQL
- SQL
- Other

### Master-slave Replication
Read & Write

Redundancy

### Manager Worker Model 
* duplicates data down to other databases
<img height="150" src="https://user-images.githubusercontent.com/77434770/192760696-7d52459b-263a-4fff-b6b3-d14a146df527.png" alt="Manager Worker Model"/>

### Circular Manager Worker Model
- Eventual Consistency
- Low Latency
<img height="150" src="https://user-images.githubusercontent.com/77434770/192763294-5ec2b113-9745-41ab-b726-958574b13368.png" />

---

## **[Day 3]()**

## <b id="sharding">Sharding</b>
The process of splitting data into small chunks or shards

**Why**
* Data may be too large to fit in a single machine. This provides horizontal database scaling.
* Distributed processing to speed up computations

**Ways to achieve sharding**
1. Application Level sharding
 - Database clients picks relevant shard for read/writing data
2. Database level sharding
 - Router/ config present in database not with client

**Sharding Strategies**
1. Hashing
2. Ranges

**Databases with sharding support**
1. Cassandra
2. HBase

Concepts
- Hotspotting - uneven distribution of data
- Redistribution of data
- Network Partition

**Federation**
**Sharding**
**Denormalization**
**SQL Tuning**


### Data Centers

### SAAS

#### How do we start to scale
* Vertical Scaling - Scaling a single server server instance; be it Memory, CPU, Disc 
Making a single server more powerful if you're scaling up, or less powerful if you're scaling it down
  * Pros 
   - It's cheap 
  * Cons
* Horizontal Scaling

> Server read/ write to each db instances(replication) - If one db we have two dbs to failover

---

## **[Day 4]()**

## <b id="loadbalancers">Load Balancers</b>
They balance incoming traffic to your application; and then distributes that traffic accross multiple servers. So that none of them are being overloaded or under utilized. 

**The why**
 * Improves reliability and scalability of your application
 * Allows replication
 
  
 #### Setting up Load Balancers
 1. Round Robin
  * Simplest type of routing
  * Can result to uneven traffic
 2. Least Connections
  * This setting routes based on number of clients connections to the server
  * Useful for chat applications
 3. Least Response time
  * Communicates with servers based on how quickly the servers respond
 4. Source IP Hash 
  * example; shopping cart
 5. Weighted least connection
  *
 7. 

L4 vs L7
 
 
 H/W Load Balancers eg Citrix
 S/W Load Balancers eg Nginx, HAproxy

Examples : Nginx, 
<img width="520" src="https://user-images.githubusercontent.com/77434770/192547253-66e14dc5-6650-484c-ab66-b1f6648e7209.png" alt="Database Design"/>

### Availability zones
### High Availability


ELB, HAProxy

---

## **[Day 5]()**

## <b id="caching">Caching</b>

- in memory database, limitation in size/ number elements that you can store
- relieves the database from pressure
- makes serving of information faster 
   - Example: Redis, MemCache

 **Implementing Cache**
 
 //redis
 //memcached
 
 //Different patterns -implementing cache
 // Database Queries
 // Caching objects

 **Eviction Policies** - These are algorithms that help deciding which element to evict when the cache is full
1. **LRU** - Least Recently Used
2. **LFU** - Least Frequently Used
3. **MRU** - Most Recently Used
4. **FIFO** - First In First Out

 **Updating Cache**
1. Cache Aside
2. Write through
3. Write Behind
4. Refresh Ahead

  * **1. Cache Aside**


---

## **[Day 6]()**

## <b id="cdn">CDN</b>
Is a service on cloud to offload images or common assets
Content Delivery Network Brings data closer to consumers to improve overall experience for [more information refer to](https://www.cloudflare.com/en-gb/learning/cdn/what-is-a-cdn/)

### Reference

1. [DNS](https://www.cloudflare.com/en-gb/learning/dns/what-is-dns/)
