## Design Components

#### **How would you go from something super arbitrary(single server stack) to something that can scale to millions of concurrent users at the same time**
<br>
<img width="420" src="https://user-images.githubusercontent.com/77434770/192516427-2d12593b-73b7-4c5e-b0f1-df74f3699993.png" alt="Design"/>

#### Database Inclusion
<br>
<img width="420" src="https://user-images.githubusercontent.com/77434770/192515986-884801e3-128e-4c0f-be8d-d453ce5c1a32.png" alt="Database Design"/>

#### Database strategies
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

### Sharding

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

### Load Balancer
They balance incoming traffic to your application; and then distributes that traffic accross multiple servers. So that none of them are being overloaded or under utilized. 

**The why**
 * Improves reliability and scalability of your application
 * Allows replication
 
  
 ####Setting up Load Balancers
 1. Round Robin
  * Simplest type of routing
  * Can result to uneven traffic
 2. Least Connections
  * This setting routes based on number of clients connections to the server
  * Useful for chat applications
 3. Least Response time
  * Communicates with servers based on how quickly the servers respond
 4. IP Hash 
  * example; shopping cart

L4 vs L7
 
 
 H/W Load Balancers eg Citrix
 S/W Load Balancers eg Nginx, HAproxy

Examples : Nginx, 
<img width="520" src="https://user-images.githubusercontent.com/77434770/192547253-66e14dc5-6650-484c-ab66-b1f6648e7209.png" alt="Database Design"/>

### Availability zones
### High Availability


ELB, HAProxy

### CDN
Is a service on cloud to offload images or common assets

### Reference

[DNS](https://www.cloudflare.com/en-gb/learning/dns/what-is-dns/)
