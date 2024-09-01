---
title: "Introduction"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 1. </b> "
---

Among the many ways that computers process data, one of the most common is read-only data that needs to be presented quickly and to a large number of users, such as music or videos that are streamed around the world. This type of data is rarely updated or deleted, but it is large in volume and demand can fluctuate significantly (think of a viral video or song). Because the need for this type of access is becoming more common, Amazon Web Services (AWS) provides tools to handle it. These tools are essentially tools that can retrieve data quickly and distribute it across multiple servers to meet peaks and troughs in demand—and do so in a cost-effective way, charging only for usage.

Applications and websites often provide a wide range of data and services to users. Within this large data set, there is often a smaller subset of data that is requested and accessed more frequently. This could be front-page data that is shown to every visitor (think Amazon’s top 10 products of the day), or it could be a recently released piece of media that is experiencing a spike in popularity (a new song released on Spotify). Other applications run extremely memory-intensive processes and may experience performance issues on slower storage.

In this workshop, we’ll take a deeper look at Amazon ElastiCache and Elastic Load Balancing?, exploring how it works, the benefits, and how to deploy it to optimize your application performance.

# **What you will learn**

-   What is ElasticCache ?
-   What is Elastic Load Balancing ?
-   Pricing
-   Types of ELBs in AWS
