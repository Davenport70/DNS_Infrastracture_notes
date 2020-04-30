# Load Balancer

## What is a load balancer?

A load balancer is a device that acts as a reverse proxy and distributes network or application traffic across a number of servers. Load balancers are used to increase capacity (concurrent users) and reliability of applications. They improve the overall performance of applications by decreasing the burden on servers associated with managing and maintaining application and network sessions, as well as by performing application-specific tasks.

## What does a load balancer do ?

A load balancer acts as the “traffic cop” sitting in front of your servers and routing client requests across all servers capable of fulfilling those requests in a manner that maximizes speed and capacity utilization and ensures that no one server is overworked, which could degrade performance. If a single server goes down, the load balancer redirects traffic to the remaining online servers. When a new server is added to the server group, the load balancer automatically starts to send requests to it.

## Benefits of Load Balancing

- Reasonably simple to implement for experienced network administrators.
- Reduces the need to implement session-failover, as users are only sent to other servers if one goes offline.
- Load balancer/router is often responsible for detecting offline servers, providing faster request-failover than round-robin DNS-based load balancing.

## Terraform Load Balancing
```
resource "aws_lb" "example" {
  name               = "example"
  load_balancer_type = "network"

  subnet_mapping {
    subnet_id     = "${aws_subnet.example1.id}"
    allocation_id = "${aws_eip.example1.id}"
  }

  subnet_mapping {
    subnet_id     = "${aws_subnet.example2.id}"
    allocation_id = "${aws_eip.example2.id}"
  }
}
```

**Author**

**Zack Davenport** - *Junior DevOps Engineer* - Davenport70
