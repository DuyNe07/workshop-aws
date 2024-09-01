---
title: "Giới thiệu"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 1. </b> "
---

Trong số nhiều cách xử lý dữ liệu trên máy tính, một trong những cách phổ biến nhất là dữ liệu chỉ đọc cần được trình bày nhanh chóng và tới số lượng lớn người dùng, chẳng hạn như nhạc hoặc video được phát trực tuyến trên toàn thế giới. Loại dữ liệu này hiếm khi được cập nhật hoặc xóa nhưng có khối lượng lớn và nhu cầu về nó có thể dao động đáng kể (hãy nghĩ đến một video hoặc bài hát được lan truyền rộng rãi). Do nhu cầu về loại quyền truy cập này ngày càng trở nên phổ biến nên Amazon Web Services (AWS) cung cấp các công cụ để xử lý nó. Các công cụ này chủ yếu là những công cụ có thể truy xuất dữ liệu nhanh chóng và phân phối dữ liệu trên nhiều máy chủ để đáp ứng nhu cầu cao nhất và thấp nhất—đồng thời thực hiện việc đó theo cách tiết kiệm chi phí và chỉ tính phí sử dụng.

Các ứng dụng và trang web thường cung cấp nhiều loại dữ liệu và dịch vụ cho người dùng. Trong phạm vi dữ liệu rộng lớn này, thường có một tập hợp con dữ liệu nhỏ hơn được yêu cầu và truy cập thường xuyên hơn. Đây có thể là dữ liệu trên trang nhất được hiển thị cho mọi khách truy cập (hãy nghĩ đến 10 sản phẩm hàng đầu trong ngày của Amazon) hoặc có thể là một phương tiện truyền thông được phát hành gần đây đang có mức độ phổ biến tăng đột biến (một bài hát mới được phát hành trên Spotify). Các ứng dụng khác chạy các quy trình cực kỳ tốn nhiều bộ nhớ và có thể gặp phải các vấn đề về hiệu suất trên ổ lưu trữ chậm hơn.

Trong bài workshop này, chúng ta sẽ cùng tìm hiểu sâu hơn về Amazon ElastiCache và Elastic Load Balancing?, khám phá cách hoạt động, lợi ích, và cách triển khai dịch vụ này để tối ưu hóa hiệu suất ứng dụng của bạn.

### **Những gì bạn sẽ học**

-   Elasticache là gì ?
-   Elastic Load Balancing là gì?
-   Giá cả
-   Các loại ELB trong AWS
