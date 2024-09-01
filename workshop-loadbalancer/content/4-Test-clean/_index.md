---
title: "Test and clean"
date: "`r Sys.Date()`"
weight: 4
chapter: false
pre: " <b> 4. </b> "
---

#### Test run Load balancer

1. Open the Load balancer section and select Details of the newly created Load balancer
   ![Hinh1](/images/4.Test-clean/4-1.png?height=450px&width=800px)
2. Copy the DNS name and open it in a new tab
   ![Hinh2](/images/4.Test-clean/4-2.png?height=120px&width=600px)
3. F5 several times it will rotate between EC1 and EC2 created previously
   ![Hinh3](/images/4.Test-clean/4-3.png?height=100px&width=600px)

### Clean up resources

After running, remember to turn off the 2 EC2 machines you created to avoid wasting free tier for the Labs later.

Select the 2 EC2 sections and select **Instance state** then select **Terminate instance** and you're done!!!
