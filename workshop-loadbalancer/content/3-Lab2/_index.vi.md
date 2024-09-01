---
title: "Lab 2: Tạo Load balancer"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

Tiếp theo khi đã khởi tạo mẫu 2 EC2 Instances thì tiếp theo tạo 1 load balancer

1. Ở phần panel bên trái kéo xuống phần **Load Balancing** chọn **Load Balancers**
   ![buoc1](/images/3.Lab2/lab-2-1.png?height=300px&width=200px)
2. Chọn **Create Load Balancer.**
   ![buoc2](/images/3.Lab2/lab-2-2.png?height=300px&width=900px)
3. Ở đây chúng ta sẽ thấy được 3 loại _Load Balancer_ mà mình đã nói tới ở phần giới thiệu. Vì bài lab của mình đang mô phỏng mô hình đơn giản nhất là _Application Load Balancer_ nên chúng ta sẽ chọn Create ở phần này
   ![buoc3](/images/3.Lab2/lab-2-3.png?height=400px&width=400px)
4. Ở phần **Basic configuration** hãy nhập tên `myloadbalaner` và để mặc định là IPv4 à Internet-facing
   ![buoc4](/images/3.Lab2/lab-2-4.png?height=360px&width=700px)
5. Ở phần **Network mapping**, hãy chọn 2 _Availability Zones_ của 2 EC2 Instances mà chúng ta đã tạo ở trước (của mình là _us-east-1b (use1-az2)_ và _us-east-1c (use1-az2)_)
   ![buoc5](/images/3.Lab2/lab-2-5.png?height=500px&width=600px)

{{% notice info %}}
Bạn có thể kiểm tra lại bằng cách nhấp vào phần _Instances_ ở thanh panel bên trái và kiểm tra lại trên list Instances
{{% /notice %}}

6. Ở phần **Security groups** hãy xóa defaut và chọn vào **Security groups** mà đã tạo cho 2 EC2 Instances nhé !
   ![buoc6](/images/3.Lab2/lab-2-6.png?height=230px&width=900px)
7. Ở phần **Listeners and routing**, hãy chọn Create target group, lúc này 1 cửa sổ mới sẽ được mở ra
   ![buoc7](/images/3.Lab2/lab-2-7.png?height=420px&width=900px)
8. Ở phần **Basic configuration** hãy để mặc định Instance và đặt tên là `myalbTG`
   ![buoc8](/images/3.Lab2/lab-2-8.png?height=450px&width=600px)
9. Ở phần **Health checks** hãy nhập `index.html` để đường dẫn là `/index.html` và chọn Next sang phần 2
   ![buoc9](/images/3.Lab2/lab-2-9.png?height=290px&width=600px)
10. Ở trang **Register targets**, ở phần **Available instances** hãy chọn 2 instances _Web Server 1_ và _Web Server 2_ đã tạo ở Lab trước
    ![buoc10](/images/3.Lab2/lab-2-10.png?height=400px&width=900px)
    Sau đó hãy chọn Include as pending below và kiểm tra xem 2 instaces đã được thêm ở mục Targets hay chưa. Nếu có rồi thì chọn Create target group
    ![buoc11](/images/3.Lab2/lab-2-11.png?height=380px&width=900px)

{{% notice info %}}
**Target Group** là một nhóm các mục tiêu (targets) mà **Load Balancer** sẽ phân phối lưu lượng đến. Mỗi target có thể là một instance EC2, một container trong ECS hoặc một endpoint của Lambda.
{{% /notice %}}

11. Trở về tab **Create Application Load Balancer**, hãy chọn reload ở phần **Listeners and routing**, sau đó hãy chọn vào Target groups vừa mới tạo
    ![buoc12](/images/3.Lab2/lab-2-12.png?height=380px&width=800px)
12. Kiểm tra lại lần nữa ở phần **Summary** và chọn _Create load balancer_
    ![buoc13](/images/3.Lab2/lab-2-13.png?height=400px&width=600px)
13. Sau đó hãy liên tục nhấn nút _reload_ đến khi **Status** chuyển sang **Active** là thành công gòi !!! (thật ra là để 1p rồi hãy nhấn chứ đừng spam quài nhen)
    ![buoc14](/images/3.Lab2/lab-2-14.png?height=300px&width=900px)
