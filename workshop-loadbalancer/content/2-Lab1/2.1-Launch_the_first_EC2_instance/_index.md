---
title: "Launch the first EC2 instance"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 2.1. </b> "
---

#### Đầu tiên hãy tạo 1 EC2 instance

1. In the search box to the right of Services, search for and select EC2 to open the EC2 console
   ![buoc1](/images/2.Lab1/lab-21/lab-21-1.png?height=350px&width=500px)
2. Select the Launch Instance button in the middle of the page, then select Launch Instance from the drop-down menu.
   ![buoc2](/images/2.Lab1/lab-21/lab-21-2.png?height=300px&width=500px)
3. Next, enter a name and select Application and OS Images as Amazon Linux to use the free tier.
   ![buoc3](/images/2.Lab1/lab-21/lab-21-3.png?height=550px&width=480px)
4. Select Instance type as t2.micro (free tier) and key pair as vockey8
   ![buoc4](/images/2.Lab1/lab-21/lab-21-4.png?height=380px&width=500px)
5. In the _Network settings_ section, select Edit.

    - Under **Subnet**, select the existing subnet in **Availability Zone us-east-1a**.

    - For **Security group name** enter **Web Server security group**
    - For **Description** enter **Security group for my web server**
    - In the **Inbound security groups rules** section, select **Remove** to delete the default rule.
    - Select **Add security group rule** to configure a new rule as shown below
        - _Type_ : HTTP
        - _Source type_ : Anywhere
          ![buoc51](/images/2.Lab1/lab-21/lab-21-5.png?height=550px&width=480px)
          ![buoc52](/images/2.Lab1/lab-21/lab-21-6.png?height=450px&width=480px)

{{% notice info %}}
After this step, it will create a new Security group. If you want to choose security according to your wishes, choose exiting security group!
{{% /notice %}}

1. In the _Configure storage_ table, keep the default storage configuration.
2. Configure the Advance details section to insert a sample script to test EC2

    - Expand the Advance details section
    - Scroll down to the bottom of the User data section and enter the sample cli script as below

    ```
        #!/bin/bash
        yum update -y
        yum -y install httpd
        systemctl enable httpd
        systemctl start httpd
        echo '<html><h1>Hello World! This is server 1.</h1></html>' > /var/www/html/index.html
    ```

    This script does the following:

    - Update the server
    - Install the Apache web server (httpd)
    - Configure the web server to start automatically on boot
    - Start the web server
    - Create a simple web page

    ![buoc7](/images/2.Lab1/lab-21/lab-21-7.png?height=350px&width=480px)

3. Double check again and select Launch instance in Summary section.
   ![buoc8](/images/2.Lab1/lab-21/lab-21-8.png?height=500px&width=240px)
4. Next after Lauch log Succeeded all select Instances
   ![buoc9](/images/2.Lab1/lab-21/lab-21-9.png?height=350px&width=480px)
5. Please wait a moment and wait for its status to be ready all
   ![buoc10](/images/2.Lab1/lab-21/lab-21-10.png?height=400px&width=900px)

#### Visit your EC2 instance's website

Copy Ipv4 string and access: `http://<ip của bạn>`
![buoc11](/images/2.Lab1/lab-21/lab-21-11.png?height=200px&width=600px)
