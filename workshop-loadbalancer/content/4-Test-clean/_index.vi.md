---
title: "Test and clean"
date: "`r Sys.Date()`"
weight: 4
chapter: false
pre: " <b> 4. </b> "
---

#### Chạy thử Load balancer

1. Mở phần Load balancer và chọn Details Load balancer vừa mới tạo
   ![Hinh1](/images/4.Test-clean/4-1.png?height=450px&width=800px)
2. Sao chép DNS name và mở vào 1 tab mới
   ![Hinh2](/images/4.Test-clean/4-2.png?height=120px&width=600px)
3. F5 vài lần nó sẽ luân chuyển giữa EC1 và EC2 đã tạo ở trước đó
   ![Hinh3](/images/4.Test-clean/4-3.png?height=100px&width=600px)

### Dọn dẹp tài nguyên

Sau khi chạy xong bạn nhớ tắt 2 máy EC2 đã tạo đi nhé để tránh lãng phí free tier cho các Lab sau nãy nữa.

Chọn vào 2 phần EC2 và chọn **Instance state** sau đó chọn **Terminate instance** là thành công nhé !!!
