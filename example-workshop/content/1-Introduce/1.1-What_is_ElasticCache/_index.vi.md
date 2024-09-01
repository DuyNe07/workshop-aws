---
title: "Elasticache là gì"
date: "`r Sys.Date()`"
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

Amazon ElastiCache giúp dễ dàng thiết lập, quản lý và mở rộng môi trường bộ nhớ đệm phân tán trong AWS Cloud. Nó cung cấp bộ nhớ đệm trong bộ nhớ có hiệu suất cao, có thể thay đổi kích thước và tiết kiệm chi phí, đồng thời loại bỏ sự phức tạp liên quan đến việc triển khai và quản lý môi trường bộ nhớ đệm phân tán.

![ElasticCache](/images/1.introduction/011-ElasticCache.png)

ElastiCache hỗ trợ hai công cụ lưu trữ đệm trong bộ nhớ nguồn mở: Redis và Memcached.

-   Redis, viết tắt của Remote Dictionary Server, là một kho lưu trữ cấu trúc dữ liệu nguồn mở, nhanh. Nó thường được sử dụng như một kho lưu trữ dữ liệu trong bộ nhớ phân tán được sử dụng làm cơ sở dữ liệu, bộ nhớ đệm, công cụ phát trực tuyến và môi giới tin nhắn. Redis hỗ trợ nhiều loại cấu trúc dữ liệu trừu tượng khác nhau, chẳng hạn như chuỗi, danh sách, bản đồ, tập hợp, tập hợp được sắp xếp, HyperLogLog, bitmap, luồng và chỉ số không gian.
-   Memcached là một kho lưu trữ dữ liệu trong bộ nhớ trực quan, hiệu suất cao. Nó cung cấp một giải pháp nguồn mở, có khả năng mở rộng, trưởng thành để cung cấp thời gian phản hồi dưới một mili giây, giúp nó hữu ích như một bộ nhớ đệm hoặc một kho lưu trữ phiên không bền.

ElastiCache là dịch vụ lưu trữ đệm trong bộ nhớ được quản lý hoàn toàn, hỗ trợ các trường hợp sử dụng thời gian thực đòi hỏi hiệu suất cực nhanh và thông lượng cao. ElastiCache thường được sử dụng làm bộ nhớ đệm để tăng hiệu suất ứng dụng hoặc cơ sở dữ liệu. Nó cũng có thể đóng vai trò là kho lưu trữ dữ liệu chính cho các trường hợp sử dụng không yêu cầu độ bền, chẳng hạn như kho lưu trữ phiên, bảng xếp hạng trò chơi, phát trực tuyến và giới hạn tốc độ API.

## ElastiCache giải quyết được những vấn đề gì?

Sử dụng ElastiCache, bạn có thể hợp lý hóa cách triển khai, vận hành và mở rộng quy mô trên đám mây. Với cơ sở dữ liệu truyền thống, bạn phải quản lý cơ sở hạ tầng và nâng cấp cơ bản, vá lỗi, quản lý cụm, sao lưu và khối lượng công việc sản xuất. Các dịch vụ cơ sở dữ liệu được quản lý hoàn toàn tự động hóa các tác vụ này. Sau đây là một số cách ElastiCache có thể giúp:

-   Cung cấp các công cụ Redis và Memcached tuân thủ API với bất kỳ ứng dụng nguồn mở nào sử dụng OSS Redis hoặc Memcached
-   Mở rộng tài nguyên tính toán và bộ nhớ của bạn theo chiều dọc hoặc chiều ngang trong vài phút
-   Mở rộng khả năng đọc/ghi của bạn dựa trên nhu cầu kinh doanh thay đổi
-   Cung cấp mức độ bảo mật và hỗ trợ cao cho Amazon Virtual Private Cloud (Amazon VPC), Transport Layer Security (TLS), mã hóa và đủ điều kiện cho nhiều chứng chỉ tuân thủ
-   Cung cấp khả năng giám sát liên tục và chuyển đổi dự phòng tự động

Mục tiêu của ElastiCache là giảm bớt sự phức tạp bổ sung khi quản lý hệ thống lưu trữ đệm trong bộ nhớ của bạn cho các công cụ Redis và Memcached. Các nhà phát triển có thể tiếp tục sử dụng cùng một mã ứng dụng Redis và Memcached, trình điều khiển và công cụ để chạy, quản lý và mở rộng khối lượng công việc của họ trên ElastiCache. Các nhà phát triển và quản trị viên có thể dựa vào các dịch vụ được quản lý để xử lý các công việc nặng nhọc không phân biệt, tập trung vào phát triển ứng dụng để tăng thêm giá trị cho khách hàng của họ.

## ElastiCache được sử dụng như thế nào để xây dựng giải pháp đám mây ?

ElastiCache lưu trữ dữ liệu trong bộ nhớ chính (DRAM) của máy chủ để truy cập nhanh. ElastiCache thường được sử dụng làm bộ nhớ đệm trước cơ sở dữ liệu chính phụ trợ như Amazon Relational Database Service (Amazon RDS). Vì dữ liệu được lưu trữ trong DRAM có thể được truy cập nhanh hơn nhiều so với các hệ thống dựa trên đĩa, ElastiCache có thể mang lại lợi ích đáng kể về hiệu suất khi được đặt trước cơ sở dữ liệu.

ElastiCache là dịch vụ chỉ trong bộ nhớ được thiết kế để cung cấp hiệu suất cực nhanh với cái giá phải trả là độ bền. Nó có thể phục vụ đọc/ghi dữ liệu tạm thời ở độ trễ micro giây, điều này rất mong muốn đối với các ứng dụng thời gian thực.

Sơ đồ sau đây hiển thị một ví dụ về cách khi máy khách gửi yêu cầu đến ứng dụng, trước tiên nó sẽ cố gắng truy xuất dữ liệu tương ứng từ ElastiCache. Nếu yêu cầu thành công, thì được gọi là truy cập bộ nhớ đệm. Nếu không thành công, thì được gọi là bỏ lỡ bộ nhớ đệm. Trong trường hợp lỗi bộ nhớ đệm, yêu cầu được chuyển tiếp đến nguồn dữ liệu thực (RDS MySQL trong trường hợp này) và truy xuất dữ liệu tương ứng. Sau đó, dữ liệu được ghi vào bộ nhớ đệm trước khi gửi phản hồi trở lại máy khách.

_Ví dụ về cách ElastiCache xử lý yêu cầu của khách hàng gửi tới ứng dụng_
![ElasticCache](/images/1.introduction/011-Example.png)
