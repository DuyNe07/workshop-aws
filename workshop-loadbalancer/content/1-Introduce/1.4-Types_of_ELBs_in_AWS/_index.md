---
title: "Types of ELBs"
date: "`r Sys.Date()`"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

Heavy traffic can shut down applications and websites if the server cannot handle the load. This is why AWS has ELBs, which can detect when there are too many requests and automatically redirect traffic to new servers to maintain speed and stability. There are three types of ELBs in AWS.

-   **Application Load Balancers**: Application Load Balancers are best suited for load balancing Hypertext Transfer Protocol (HTTP) and Secure HTTP (HTTPS) traffic, and provide advanced request routing targeted at delivering modern application architectures, including microservices and containers. Operating at the individual request level (Layer 7), Application Load Balancers route traffic to targets in the Amazon Virtual Private Cloud (Amazon VPC) based on the content of the request.
    Application Load Balancing is performed based on the content of a Uniform Resource Locator (URL). For example, if the URL ends in /main, the request will be routed to one instance; if the URL ends in blog/, it will be routed to another instance if the Application Load Balancer definition work has been done beforehand to do so.
-   **Network Load Balancer:** The Network Load Balancer is best suited for load balancing Transmission Control Protocol (TCP), User Datagram Protocol (UDP), and Transport Layer Security (TLS) traffic when extreme performance is required. Operating at the connection level (Layer 4), the Network Load Balancer routes traffic to targets within the Amazon VPC and is capable of handling millions of requests per second while maintaining extremely low latency. The Network Load Balancer is also optimized to handle bursty and unstable traffic patterns.

    Because of the increased speed that can be achieved at the connection layer, the Network Load Balancer load balancer type is preferred when trying to avoid higher network traffic. For example, to avoid delays when interest in a site spreads widely, you should choose to use Network Load Balancer.

-   **Classic Load Balancer**: Classic Load Balancer provides basic load balancing across multiple EC2 instances and operates at the request and connection level. Classic Load Balancer is for applications built on the EC2-Classic network.
