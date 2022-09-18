Server architecture:

Single Server architecture
Reverse Proxy Servers: SSL termination (For future https communication)
Forward Proxy Servers

1. Vertical scaling: increasing spec of server(CPU and RAM) 
	- Has an upper limit
2. Horizontal scaling: Increase number of servers, potentially unlimited number of servers
	-Requires load balancing : checking health downstream servers, 
		- hardware or software based	
		- examples: nginx, apache, iis

		Different load sharing algorithms
		- round robin: circulates the requests between evenly 
		- for more information (https://kemptechnologies.com/load-balancer/load-balancing-algorithms-techniques)
