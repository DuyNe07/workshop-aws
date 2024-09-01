---
title: "What is ElasticCache"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

Amazon ElastiCache makes it easy to set up, manage, and scale a distributed caching environment in the AWS Cloud. It provides a high-performance, scalable, and cost-effective in-memory cache, while eliminating the complexity associated with deploying and managing a distributed caching environment.

![ElasticCache](/images/1.introduction/011-ElasticCache.png)

ElastiCache supports two open-source in-memory caching engines: Redis and Memcached.

-   Redis, short for Remote Dictionary Server, is a fast, open-source data structure store. It is commonly used as a distributed in-memory data store that is used as a database, cache, streaming engine, and message broker. Redis supports a variety of abstract data structures, such as strings, lists, maps, sets, sorted sets, HyperLogLog, bitmaps, streams, and spatial indices.
-   Memcached is an intuitive, high-performance in-memory data store. It provides a mature, scalable, open-source solution for delivering sub-millisecond response times, making it useful as a cache or a non-durable session store.

ElastiCache is a fully managed in-memory caching service that supports real-time use cases that require extremely fast performance and high throughput. ElastiCache is often used as a cache to increase application or database performance. It can also serve as the primary data store for use cases that do not require durability, such as session stores, gaming leaderboards, streaming, and API rate limiting.

## What problems does ElastiCache solve?

Using ElastiCache, you can streamline how you deploy, operate, and scale in the cloud. With traditional databases, you have to manage the infrastructure and underlying upgrades, patching, cluster management, backups, and production workloads. Fully managed database services automate these tasks. Here are some ways ElastiCache can help:

-   Provide API-compliant Redis and Memcached engines with any open source application that uses OSS Redis or Memcached
-   Scale your compute and memory resources vertically or horizontally in minutes
-   Scale your read/write capacity based on changing business needs
-   Provide high levels of security and support for Amazon Virtual Private Cloud (Amazon VPC), Transport Layer Security (TLS), encryption, and qualify for multiple compliance certifications
-   Provide continuous monitoring and automatic failover

The goal of ElastiCache is to reduce the additional complexity of managing your in-memory caching system for Redis and Memcached engines. Developers can continue to use the same Redis and Memcached application code, drivers, and tools to run, manage, and scale their workloads on ElastiCache. Developers and administrators can rely on managed services to handle the heavy lifting, focusing on application development to add value to their customers.

## How is ElastiCache used to build cloud solutions?

ElastiCache stores data in the server's main memory (DRAM) for fast access. ElastiCache is often used as a cache in front of a backend primary database such as Amazon Relational Database Service (Amazon RDS). Since data stored in DRAM can be accessed much faster than disk-based systems, ElastiCache can provide significant performance benefits when placed in front of the database.

ElastiCache is an in-memory only service designed to provide blazing fast performance at the expense of durability. It can serve temporary data reads/writes at microsecond latency, which is desirable for real-time applications.

The following diagram shows an example of how when a client sends a request to an application, it first tries to retrieve the corresponding data from ElastiCache. If the request is successful, it is called a cache hit. If it is unsuccessful, it is called a cache miss. In case of a cache miss, the request is forwarded to the real data source (RDS MySQL in this case) and the corresponding data is retrieved. The data is then written to the cache before the response is sent back to the client.

_Example of how ElastiCache handles client requests to the application_
![ElasticCache](/images/1.introduction/011-Example.png)
