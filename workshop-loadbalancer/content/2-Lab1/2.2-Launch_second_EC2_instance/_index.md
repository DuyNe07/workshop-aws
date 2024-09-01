---
title: "Launch a second EC2 instance"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 2.2. </b> "
---

To simulate a Load Balance model, we need 2 EC2s to be able to balance the load, so we will create 2 EC2 instances

#### Initialize 1 EC2 instance based on the EC2 template just created

1. Select the **Instances** section in the left sidebar
   ![buoc1](/images/2.Lab1/lab-12/lab-12-1.png?height=300px&width=800px)
2. From the **Action** menu, select _Images and templates_, then select _Launch more like this_ and the _Launch an instance_ page will open.
   ![buoc2](/images/2.Lab1/lab-12/lab-12-2.png?height=230px&width=800px)
3. Rename to `Web service 2`
   ![buoc3](/images/2.Lab1/lab-12/lab-12-3.png?height=380px&width=460px)
4. Note in the **Network setting** section, select _Subnet_ in another place.
   ![buoc4](/images/2.Lab1/lab-12/lab-12-4.png?height=450px&width=460px)
   Because I chose from the beginning to initialize from a different **Intances** template, it will share the same _security group_ as the previously created EC2.

{{% notice note %}}
Remember **Availability Zone** to use for the following: `us-east-1c`
{{% /notice %}}

5. Similarly, change the content in the User data section to the following:
    ```
    #!/bin/bash
     yum update -y
     yum -y install httpd
     systemctl enable httpd
     systemctl start httpd
     echo '<html><h1>Hello World! This is server 2.</h1></html>' > /var/www/html/index.html
    ```
    ![buoc5](/images/2.Lab1/lab-12/lab-12-5.png?height=400px&width=600px)
6. Launch instance
   ![buoc6](/images/2.Lab1/lab-12/lab-12-6.png?height=300px&width=900px)

#### Access the website on the second EC2 instance

![buoc7](/images/2.Lab1/lab-12/lab-12-7.png?height=200px&width=600px)
