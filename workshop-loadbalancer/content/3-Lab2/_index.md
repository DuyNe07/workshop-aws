---
title: "Lab 2: Create Load balancer"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

Next, after initializing the 2 EC2 Instances template, next create a load balancer.

1. In the left panel, scroll down to **Load Balancing** and select **Load Balancers**
   ![buoc1](/images/3.Lab2/lab-2-1.png?height=300px&width=200px)
2. Select **Create Load Balancer.**
   ![buoc2](/images/3.Lab2/lab-2-2.png?height=300px&width=900px)
3. Here we will see the 3 types of _Load Balancer_ that I mentioned in the introduction. Since my lab is simulating the simplest model, _Application Load Balancer_, we will choose Create in this part.
   ![buoc3](/images/3.Lab2/lab-2-3.png?height=400px&width=400px)
4. In the **Basic configuration** section enter the name `myloadbalaner` and leave the default as IPv4 à Internet-facing
   ![buoc4](/images/3.Lab2/lab-2-4.png?height=360px&width=700px)
5. In the **Network mapping** section, select the 2 _Availability Zones_ of the 2 EC2 Instances we created before (mine are _us-east-1b (use1-az2)_ and _us-east-1c (use1-az2)_)
   ![buoc5](/images/3.Lab2/lab-2-5.png?height=500px&width=600px)

{{% notice info %}}
You can double check by clicking on the _Instances_ section on the left panel and double checking on the Instances list
{{% /notice %}}

6. In the **Security groups** section, delete the default and select the **Security groups** that were created for the 2 EC2 Instances!
   ![buoc6](/images/3.Lab2/lab-2-6.png?height=230px&width=900px)
7. In the **Listeners and routing** section, select Create target group, a new window will open.
   ![buoc7](/images/3.Lab2/lab-2-7.png?height=420px&width=900px)
8. In the **Basic configuration** section, leave the default Instance and name it `myalbTG`
   ![buoc8](/images/3.Lab2/lab-2-8.png?height=450px&width=600px)
9. In the **Health checks** section, enter `index.html` so that the path is `/index.html` and select Next to go to part 2.
   ![buoc9](/images/3.Lab2/lab-2-9.png?height=290px&width=600px)
10. On the **Register targets** page, in the **Available instances** section, select the 2 instances _Web Server 1_ and _Web Server 2_ created in the previous Lab.
    ![buoc10](/images/3.Lab2/lab-2-10.png?height=400px&width=900px)
    Then select Include as pending below and check if 2 instances have been added in the Targets section. If so, select Create target group
    ![buoc11](/images/3.Lab2/lab-2-11.png?height=380px&width=900px)

{{% notice info %}}
**Target Group** is a group of targets that the **Load Balancer** will distribute traffic to. Each target can be an EC2 instance, an ECS container, or a Lambda endpoint.
{{% /notice %}}

11. Return to the **Create Application Load Balancer** tab, select reload in the **Listeners and routing** section, then select the newly created Target groups
    ![buoc12](/images/3.Lab2/lab-2-12.png?height=380px&width=800px)
12. Double check in the **Summary** section and select _Create load balancer_
    ![buoc13](/images/3.Lab2/lab-2-13.png?height=400px&width=600px)
13. Then keep pressing the _reload_ button until **Status** changes to **Active** and it's successful!!! (actually, wait for 1 minute before pressing, don't spam it all the time)
    ![buoc14](/images/3.Lab2/lab-2-14.png?height=300px&width=900px)
