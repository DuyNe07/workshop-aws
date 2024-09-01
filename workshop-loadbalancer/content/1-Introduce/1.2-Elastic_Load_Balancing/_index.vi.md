---
title: "Elastic Load Balancing"
date: "`r Sys.Date()`"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

Các ứng dụng khác chạy các quy trình cực kỳ tốn nhiều bộ nhớ và có thể gặp phải các vấn đề về hiệu suất trên ổ lưu trữ chậm hơn.

Đối với loại dữ liệu được yêu cầu nhiều hoặc sử dụng nhiều bộ nhớ này, dịch vụ lưu vào bộ nhớ đệm dữ liệu như ElastiCache có thể giúp đảm bảo rằng dữ liệu có thể được truy cập và xử lý cực kỳ nhanh chóng. Nó hoạt động bằng cách lưu trữ dữ liệu trong bộ nhớ cực nhanh nhưng tạm thời nhanh hơn bộ nhớ trên đĩa. Sự đánh đổi là bộ nhớ nhanh có ít dung lượng lưu trữ hơn và không lưu trữ dữ liệu vĩnh viễn.

Nhiều công ty sử dụng ElastiCache để xây dựng ứng dụng thời gian thực, tăng tốc thương mại điện tử và lưu vào bộ nhớ đệm trang web của họ. Các trường hợp sử dụng: giao dịch theo thời gian thực, trò chuyện, BI và phân tích, cửa hàng phiên, bảng xếp hạng trò chơi và bộ đệm.

Lưu lượng truy cập lớn có thể tắt ứng dụng và trang web nếu máy chủ không thể xử lý tải. Đây là lý do tại sao AWS có ELB, có thể phát hiện khi có quá nhiều yêu cầu và tự động chuyển hướng lưu lượng truy cập sang máy chủ mới để duy trì tốc độ và độ ổn định.

Elastic Load Balancing tự động phân phối lưu lượng truy cập đến của bạn trên nhiều mục tiêu, chẳng hạn như các phiên bản EC2, vùng chứa và địa chỉ IP, trong một hoặc nhiều Vùng khả dụng. Nó theo dõi tình trạng của các mục tiêu đã đăng ký và chỉ định tuyến lưu lượng truy cập đến các mục tiêu lành mạnh. Elastic Load Balancing tự động điều chỉnh dung lượng bộ cân bằng tải của bạn để phản hồi các thay đổi trong lưu lượng truy cập đến.

#### Lợi ích của Load Balancing

Cân bằng tải đàn hồi tự động phân phối lưu lượng truy cập ứng dụng đến trên nhiều mục tiêu, chẳng hạn như phiên bản, bộ chứa, địa chỉ IP và chức năng AWS Lambda của Amazon Elastic Computing Cloud (Amazon EC2).

Nếu lưu lượng truy cập vào một trang web đột ngột tăng đột biến, lưu lượng truy cập đó có thể được chuyển đến các phiên bản EC2 khác (hoặc các loại phiên bản khác như phiên bản Lambda) đã được thiết lập trước cho mục đích này. Cân bằng tải này tránh cho một máy chủ bị quá tải do lưu lượng truy cập tăng lên.

### Những lợi ích chính của ELB:

1. **Tăng khả năng sẵn sàng:**

-   **Phân tán lưu lượng:** ELB phân tán lưu lượng truy cập đến nhiều instance, giúp giảm thiểu rủi ro khi một instance gặp sự cố. Nếu một instance bị lỗi, ELB sẽ tự động chuyển hướng các yêu cầu đến các instance còn lại.
-   **Khả năng phục hồi:** ELB liên tục giám sát tình trạng của các instance và tự động loại bỏ những instance không hoạt động và thêm các instance mới vào khi cần thiết.

2. **Cải thiện hiệu suất:**

-   **Phân bổ tải:** ELB giúp phân bổ tải làm việc đồng đều cho các instance, ngăn chặn tình trạng quá tải trên một instance.
-   **Giảm thời gian phản hồi:** Bằng cách phân tán lưu lượng, ELB giúp giảm thiểu thời gian phản hồi của ứng dụng, mang lại trải nghiệm tốt hơn cho người dùng.

3. **Tăng khả năng mở rộng:**

-   **Điều chỉnh quy mô tự động:** ELB có thể tự động điều chỉnh quy mô của cụm instance để đáp ứng nhu cầu thay đổi của ứng dụng. Khi lưu lượng tăng, ELB sẽ tự động thêm các instance mới vào cụm và ngược lại.

4. **Bảo mật:**

-   **Kết nối SSL/TLS:** ELB hỗ trợ kết nối SSL/TLS để bảo mật dữ liệu truyền đi giữa người dùng và ứng dụng.
-   **Quản lý chứng chỉ:** ELB giúp bạn dễ dàng quản lý các chứng chỉ SSL/TLS.

5. **Tính năng nâng cao:**

-   **Cân bằng tải dựa trên đường dẫn:** ELB có thể phân phối lưu lượng dựa trên đường dẫn URL, giúp tối ưu hóa việc sử dụng các tài nguyên.
-   **Cân bằng tải dựa trên cookie:** ELB có thể duy trì session của người dùng bằng cách sử dụng cookie, giúp đảm bảo rằng các yêu cầu của một người dùng cụ thể luôn được gửi đến cùng một instance.
-   **Tích hợp với các dịch vụ AWS khác:** ELB có thể dễ dàng tích hợp với các dịch vụ AWS khác như Auto Scaling, CloudWatch, và Route 53.
