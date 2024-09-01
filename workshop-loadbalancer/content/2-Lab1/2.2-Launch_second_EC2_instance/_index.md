---
title: "Launch a second EC2 instance"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 2.2. </b> "
---

Now we will start the lab by creating a simulation of Three computers accessing content in the AWS Cloud. A load balancer will split this access between Availability Zone A and Availability Zone B. Each Availability Zone has three EC2 instances, but one instance in Availability Zone A is down.

![Lab](/images/2.Lab1/021-lab.png?height=400px&width=400px)

Start by creating 2 EC2 Instances in 2 different regions !
