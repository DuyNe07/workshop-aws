---
title: "Pricing"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

Elastic Load Balancing offers four load balancers, all of which provide high availability, auto-scaling, and robust security for your applications: Application Load Balancer, Network Load Balancer, Gateway Load Balancer, and Classic Load Balancer. You pay only for what you use with these services.

#### Application Load Balancer

You are charged for each hour or partial hour that the Application Load Balancer is running and the number of Load Balancer Capacity Units (LCUs) used per hour.

#### Network Load Balancer

You are charged for each hour or partial hour that the Network Load Balancer is running and the number of Network Load Balancer Capacity Units (NLCUs) used per hour.

#### Gateway Load Balancer

You are charged for each hour or partial hour that the Gateway Load Balancer is running and the number of Gateway Load Balancer Capacity Units (GLCUs) used by the Gateway Load Balancer per hour. The Gateway Load Balancer uses Gateway Load Balancer Endpoints (GWLBEs). These are new VPC Endpoint types powered by AWS PrivateLink technology that simplify how applications securely exchange traffic using GWLB across VPC edges. GWLBEs are priced and billed separately.

#### Classic Load Balancer

You are charged for each hour or partial hour that the Classic Load Balancer is running and for each GB of data transferred through your load balancer.

#### AWS Free Trier

After I researched, ELBs are included in AWS's free trier program for new accounts. Upon sign-up, new AWS customers receive 750 shared hours per month for Classic Load Balancer and Application Load Balancer; 15 GB of data processing for Classic Load Balancer and 15 LCUs for Application Load Balancer.

{{% notice note %}}
For more details on the cost of ELB visit [Network and Application Traffic Distribution - Elastic Load Balancing Pricing - AWS (amazon.com)](https://aws.amazon.com/vi/elasticloadbalancing/pricing/)
{{% /notice %}}
