---
title: "Types of ELBs"
date: "`r Sys.Date()`"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

Lưu lượng truy cập lớn có thể tắt ứng dụng và trang web nếu máy chủ không thể xử lý tải. Đây là lý do tại sao AWS có ELB, có thể phát hiện khi có quá nhiều yêu cầu và tự động chuyển hướng lưu lượng truy cập sang máy chủ mới để duy trì tốc độ và độ ổn định. Có ba loại ELB trong AWS.

-   **Cân bằng tải ứng dụng**: Cân bằng tải ứng dụng phù hợp nhất để cân bằng tải lưu lượng Giao thức truyền siêu văn bản (HTTP) và HTTP an toàn (HTTPS), đồng thời cung cấp định tuyến yêu cầu nâng cao nhắm mục tiêu phân phối các kiến trúc ứng dụng hiện đại, bao gồm cả vi dịch vụ và bộ chứa. Hoạt động ở cấp độ yêu cầu riêng lẻ (Lớp 7), Cân bằng tải ứng dụng định tuyến lưu lượng truy cập đến các mục tiêu trong Amazon Virtual Private Cloud (Amazon VPC) dựa trên nội dung của yêu cầu.
    Cân bằng tải ứng dụng được thực hiện dựa trên nội dung của bộ định vị tài nguyên thống nhất (URL). Ví dụ: nếu URL kết thúc bằng /main, yêu cầu sẽ được chuyển đến một phiên bản; nếu URL kết thúc bằng blog/, nó sẽ được định tuyến đến một phiên bản khác nếu công việc định nghĩa Cân bằng tải ứng dụng đã được thực hiện trước để thực hiện điều này.
-   **Trình cân bằng tải mạng:** Trình cân bằng tải mạng phù hợp nhất để cân bằng tải lưu lượng Giao thức điều khiển truyền dẫn (TCP), Giao thức gói dữ liệu người dùng (UDP) và Bảo mật lớp truyền tải (TLS) khi cần hiệu suất cực cao. Hoạt động ở cấp độ kết nối (Lớp 4), Network Load Balancer định tuyến lưu lượng truy cập đến các mục tiêu trong Amazon VPC và có khả năng xử lý hàng triệu yêu cầu mỗi giây trong khi vẫn duy trì độ trễ cực thấp. Network Load Balancer cũng được tối ưu hóa để xử lý các dạng lưu lượng truy cập đột ngột và không ổn định.

    Do tốc độ tăng lên có thể đạt được ở lớp kết nối, nên loại cân bằng tải Network Load Balancer được ưa chuộng hơn khi cố gắng tránh lưu lượng mạng cao hơn. Ví dụ: để tránh sự chậm trễ khi sự quan tâm đến một trang web lan truyền rộng rãi, bạn nên chọn sử dụng cân bằng Network Load Balancer.

-   **Cân bằng tải cổ điển**: Cân bằng tải cổ điển cung cấp khả năng cân bằng tải cơ bản trên nhiều phiên bản EC2 và hoạt động ở cấp độ yêu cầu và kết nối. Cân bằng tải cổ điển dành cho các ứng dụng được xây dựng trong mạng EC2-Classic.
