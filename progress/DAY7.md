## Design Components

#### **How would you go from something super arbitrary(single server stack) to something that can scale to millions of concurrent users at the same time**
<br>
<img width="420" src="https://user-images.githubusercontent.com/77434770/192516427-2d12593b-73b7-4c5e-b0f1-df74f3699993.png" alt="Design"/>

#### Database Inclusion
<br>
<img width="420" src="https://user-images.githubusercontent.com/77434770/192515986-884801e3-128e-4c0f-be8d-d453ce5c1a32.png" alt="Database Design"/>

#### Scaling the database as a separate entity from the server
<br>
**ACID**
A-Atomicity
C-Correctness
I-Isolation (database mutation)
D-Durable (databases should be reliable and durable)

NoSQL
SQL
Other

### Manager Worker Model 
* duplicates data down to other databases
<img height="150" src="https://user-images.githubusercontent.com/77434770/192758988-f89a129f-5cdf-4de7-b384-cc43399d588d.png" alt="Manager Worker Model"/>

Circular Manager Worker Model



#### How do we start to scale
* Vertical Scaling - Scaling a single server server instance; be it Memory, CPU, Disc 
Making a single server more powerful if you're scaling up, or less powerful if you're scaling it down
  * Pros 
   - It's cheap 
  * Cons
* Horizontal Scaling

> Server read/ write to each db instances(replication) - If one db we have two dbs to failover

### Load Balancer
<img width="520" src="https://user-images.githubusercontent.com/77434770/192547253-66e14dc5-6650-484c-ab66-b1f6648e7209.png" alt="Database Design"/>

### CDN
Is a service on cloud to offload images or common assets

### Reference

[DNS](https://www.cloudflare.com/en-gb/learning/dns/what-is-dns/)
