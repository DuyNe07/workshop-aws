---
title: "Lab 1: Create EC2 instance"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

Bây giờ chúng ta sẽ bắt đầu thực hiện bài lab bằng việc tạo mô phỏng Ba máy tính đang truy cập nội dung trên Đám mây AWS. Bộ cân bằng tải sẽ phân chia quyền truy cập này giữa Vùng sẵn sàng A và Vùng sẵn sàng B. Mỗi Vùng sẵn sàng có ba phiên bản EC2, nhưng một phiên bản ở Vùng sẵn sàng A không hoạt động.

![Lab](/images/2.Lab1/020-lab.png?height=400px&width=400px)

Bắt đầu bằng việc khởi tạo 2 EC2 Instances ở 2 vùng khác nhau !
