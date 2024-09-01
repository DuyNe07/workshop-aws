---
title: "What is Elastic Load Balancing"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

Other applications run extremely memory-intensive processes and may experience performance issues on slower storage.

For this type of highly requested or memory-intensive data, a data caching service like ElastiCache can help ensure that data can be accessed and processed extremely quickly. It works by storing data in ultra-fast memory, but temporarily, faster than disk storage. The trade-off is that fast storage has less storage capacity and does not store data permanently.

Many companies use ElastiCache to build real-time applications, accelerate e-commerce, and cache their websites. Use cases: real-time transactions, chat, BI and analytics, session stores, gaming leaderboards, and caching.

Heavy traffic can take down applications and websites if the server cannot handle the load. This is why AWS has ELB, which can detect when there are too many requests and automatically redirect traffic to new servers to maintain speed and stability.

Elastic Load Balancing automatically distributes your incoming traffic across multiple targets, such as EC2 instances, containers, and IP addresses, in one or more Availability Zones. It monitors the health of registered targets and routes traffic only to healthy targets. Elastic Load Balancing automatically adjusts your load balancer capacity in response to changes in incoming traffic.

# Benefits of Load Balancing

Elastic Load Balancing automatically distributes incoming application traffic across multiple targets, such as Amazon Elastic Computing Cloud (Amazon EC2) instances, containers, IP addresses, and AWS Lambda functions.

If traffic to a website suddenly spikes, that traffic can be routed to other EC2 instances (or other instance types such as Lambda instances) that have been pre-set up for this purpose. This load balancing prevents a single server from being overloaded by increased traffic.

### Key benefits of ELB:

1. **Increased availability:**

-   **Traffic distribution:** ELB distributes traffic to multiple instances, reducing the risk of one instance failing. If an instance fails, ELB automatically redirects requests to the remaining instances.

-   **Resilience:** ELB continuously monitors the health of instances and automatically removes inactive ones and adds new ones as needed.

2. **Improved performance:**

-   **Load distribution:** ELB helps distribute workload evenly across instances, preventing one instance from becoming overloaded.

-   **Reduce Response Time:** By distributing traffic, ELB helps reduce application response time, providing a better user experience.

3. **Increase Scalability:**

-   **Automatic Scaling:** ELB can automatically adjust the size of the instance cluster to meet the changing needs of the application. As traffic increases, ELB will automatically add new instances to the cluster and vice versa.

4. **Security:**

-   **SSL/TLS Connection:** ELB supports SSL/TLS connection to secure data transmitted between users and applications.

-   **Certificate Management:** ELB helps you easily manage SSL/TLS certificates.

5. **Advanced Features:**

-   **Path-Based Load Balancing:** ELB can distribute traffic based on URL paths, helping to optimize the use of resources.
-   **Cookie-based load balancing:** ELB can maintain user sessions using cookies, ensuring that requests from a particular user are always sent to the same instance.

-   **Integration with other AWS services:** ELB can easily integrate with other AWS services such as Auto Scaling, CloudWatch, and Route 53.
