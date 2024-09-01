---
title: "Preparing VPC and EC2"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 2.1 </b> "
---

In this step, we will need to create a VPC with 2 public / private subnets. Then create 1 EC2 Instance Linux located in the public subnet, 1 EC2 Instance Windows located in the private subnet.

The architecture overview after you complete this step will be as follows:

![VPC](/images/arc-01.png)

To learn how to create EC2 instances and VPCs with public/private subnets, you can refer to the lab:

-   [About Amazon EC2](https://000004.awsstudygroup.com/en/)
-   [Works with Amazon VPC](https://000003.awsstudygroup.com/en/)

### Content

-   [Create EC2 instance for load balancing](content/2-Create_EC2_instance_for_load_balancing/)
-   [Initialize Load Balancer](content/3-Initialize_load_balancer/)
-   [Test and clean up](content/4-Test_clean_up)
