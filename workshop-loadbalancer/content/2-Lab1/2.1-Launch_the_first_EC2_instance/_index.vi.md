---
title: "Launch the first EC2 instance"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 2.1. </b> "
---

#### Đầu tiên hãy tạo 1 EC2 instance

1. Trong hộp tìm kiếm bên phải Dịch vụ, hãy tìm kiếm và chọn EC2 để mở bảng điều khiển EC2
   ![buoc1](/images/2.Lab1/lab-21/lab-21-1.png?height=350px&width=500px)
2. Chọn nút Khởi chạy phiên bản ở giữa trang, sau đó chọn Khởi chạy phiên bản từ menu thả xuống.
   ![buoc2](/images/2.Lab1/lab-21/lab-21-2.png?height=300px&width=500px)
3. Tiếp theo hãy nhập tên và lựa chọn Application and OS Images là Amazon Linux để sử dụng free tier
   ![buoc3](/images/2.Lab1/lab-21/lab-21-3.png?height=550px&width=480px)
4. Chọn Instance type là t2.micro (free tier) và key pair là vockey
   ![buoc4](/images/2.Lab1/lab-21/lab-21-4.png?height=380px&width=500px)
5. Trong phần _Network settings_, chọn Chỉnh sửa.

    - Ở mục **Subnet**, chọn mạng con hiện có trong **Availability Zone us-east-1a**.
    - Đối với **Security group name** hãy nhập **Web Server security group**
    - Đối với **Description** hãy nhập **Security group for my web server**
    - Trong phần **Inbound security groups rules**, chọn **Remove** để xóa quy tắc mặc định.
    - Chọn **Add security group rule** để định cấu hình quy tắc mới như bên dưới
        - _Type_ : HTTP
        - _Source type_ : Anywhere
          ![buoc51](/images/2.Lab1/lab-21/lab-21-5.png?height=550px&width=480px)
          ![buoc52](/images/2.Lab1/lab-21/lab-21-6.png?height=450px&width=480px)

{{% notice info %}}
Sau khi ở bước này nó sẽ tạo ra 1 Security group mới, nếu bạn muốn lựa chọn security theo ý muốn của mình thì hãy chọn exisiting security group nhé !
{{% /notice %}}

1. Trong bảng _Configure storage_ thì hãy giữ nguyên cấu hình lưu trữ mặc định.
2. Cấu hình phần Advance details để chèn mẫu 1 script mẫu để có thể test thử EC2

    - Mở rộng phần Advance details
    - Kéo xuống cuối ở phần User data và nhập đoạn cript cli mẫu như dưới

    ```
        #!/bin/bash
        yum update -y
        yum -y install httpd
        systemctl enable httpd
        systemctl start httpd
        echo '<html><h1>Hello World! This is server 1.</h1></html>' > /var/www/html/index.html
    ```

    Tập lệnh này thực hiện các thao tác sau:

    - Cập nhật máy chủ
    - Cài đặt máy chủ web Apache (httpd)
    - Cấu hình máy chủ web để tự động khởi động khi khởi động
    - Khởi động máy chủ web
    - Tạo trang web đơn giản

    ![buoc7](/images/2.Lab1/lab-21/lab-21-7.png?height=350px&width=480px)

3. Kiểm tra kỹ lại 1 lần nữa và chọn Launch instance ở phần Summary
   ![buoc8](/images/2.Lab1/lab-21/lab-21-8.png?height=500px&width=240px)
4. Tiếp theo sau khi Lauch log Succeeded toàn bộ hãy chọn Instances
   ![buoc9](/images/2.Lab1/lab-21/lab-21-9.png?height=350px&width=480px)
5. Hãy đợi 1 lúc và chờ cho trạng thái của nó là sẵn sàng tất cả
   ![buoc10](/images/2.Lab1/lab-21/lab-21-10.png?height=400px&width=900px)

#### Truy cập trang web của phiên bản EC2 của bạn

Sao chép chuỗi Ipv4 và truy cập: `http://<ip của bạn>`
![buoc11](/images/2.Lab1/lab-21/lab-21-11.png?height=200px&width=600px)
