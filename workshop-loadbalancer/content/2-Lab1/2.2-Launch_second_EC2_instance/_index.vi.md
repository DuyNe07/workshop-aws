---
title: "Launch a second EC2 instance"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 2.2. </b> "
---

Để mô phỏng một mô hình Load Balance thì cần 2 EC2 để có thể cân bằng tải, vì thế chúng ta sẽ tạo 2 EC2 instance

#### Khởi tạo 1 EC2 instance dựa trên khung mẫu EC2 vừa tạo

1. Chọn phần **Instances** trong thanh bên trái
   ![buoc1](/images/2.Lab1/lab-22/lab-22-1.png?height=300px&width=800px)
2. Từ menu **Action**, chọn _Images and templates_, sau đó chọn _Launch more like this_ thì trang _Launch an instance_ sẽ mở ra.
   ![buoc2](/images/2.Lab1/lab-22/lab-22-2.png?height=230px&width=800px)
3. Đổi tên thành `Web service 2`
   ![buoc3](/images/2.Lab1/lab-22/lab-22-3.png?height=380px&width=460px)
4. Chú ý ở phần **Network setting** hãy chọn _Subnet_ ở 1 nơi khác
   ![buoc4](/images/2.Lab1/lab-22/lab-22-4.png?height=450px&width=460px)
   Vì mình đã chọn từ đầu là khởi tạo từ 1 mẫu **Intances** khác nên nó sẽ chung _security group_ với EC2 đã tạo trước đó

{{% notice note %}}
Hãy nhớ **Availability Zone** để sử dụng cho phần sau: `us-east-1c`
{{% /notice %}}

5. Tương tự thay nội dung ở phần User data thành như sau:
    ```
    #!/bin/bash
     yum update -y
     yum -y install httpd
     systemctl enable httpd
     systemctl start httpd
     echo '<html><h1>Hello World! This is server 2.</h1></html>' > /var/www/html/index.html
    ```
    ![buoc5](/images/2.Lab1/lab-22/lab-22-5.png?height=400px&width=600px)
6. Khởi chạy instance
   ![buoc6](/images/2.Lab1/lab-22/lab-22-6.png?height=300px&width=900px)

#### Truy cập trang web trên phiên bản EC2 thứ hai

![buoc7](/images/2.Lab1/lab-22/lab-22-7.png?height=200px&width=600px)
