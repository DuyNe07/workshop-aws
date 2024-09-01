---
title: "Pricing"
date: "`r Sys.Date()`"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

Elastic Load Balancing cung cấp bốn loại cân bằng tải, tất cả đều có độ khả dụng cao, tự động điều chỉnh quy mô và hỗ trợ bảo mật mạnh mẽ cho các ứng dụng của bạn: Application Load Balancer, Network Load Balancer, Gateway Load Balancer và Classic Load Balancer. Bạn chỉ phải trả cho những gì mình sử dụng với các dịch vụ này.

#### Application Load Balancer

Bạn phải trả phí cho mỗi giờ hoặc thời gian không tròn một giờ mà Application Load Balancer đang hoạt động và số Đơn vị công suất Load Balancer (LCU) được sử dụng mỗi giờ.

#### Network Load Balancer

Bạn phải trả phí cho mỗi giờ hoặc thời gian không tròn một giờ mà Network Load Balancer đang hoạt động và số Đơn vị công suất Network Load Balancer (NLCU) được Network Load Balancer sử dụng mỗi giờ.

#### Gateway Load Balancer

Bạn phải trả phí cho mỗi giờ hoặc thời gian không tròn một giờ mà Gateway Load Balancer đang hoạt động và số Đơn vị công suất Gateway Load Balancer (GLCU) được Gateway Load Balancer sử dụng mỗi giờ. Gateway Load Balancer sử dụng Điểm cuối Gateway Load Balancer (GWLBE). Đây là loại Điểm cuối VPC mới với sức mạnh của công nghệ AWS PrivateLink, giúp đơn giản hóa phương thức các ứng dụng trao đổi lưu lượng truy cập một cách bảo mật nhờ GWLB trên các biên VPC. GWLBE có mức định giá và tính phí riêng biệt.

#### Classic Load Balancer

Bạn phải trả phí cho mỗi giờ hoặc thời gian không tròn một giờ mà Bộ cân bằng tải cổ điển hoạt động và cho mỗi GB dữ liệu được truyền qua bộ cân bằng tải của bạn.

#### Free Tier của AWS

Sau khi mình tìm hiểu thì ELB có trong chương trình free tier của AWS cho các tài khoản mới. Khi đăng ký, khách hàng AWS mới sẽ nhận được 750 giờ sử dụng chung mỗi tháng cho Classic Load Balancer và Application Load Balancer; 15 GB xử lý dữ liệu cho Classic Load Balancer và 15 LCU cho Application Load Balancer.

{{% notice note %}}
Để biết thêm nhiều chi tiết hơn về chi phí của ELB truy cập: [Phân bổ lưu lượng truy cập mạng và ứng dụng - Giá của Elastic Load Balancing - AWS (amazon.com)](https://aws.amazon.com/vi/elasticloadbalancing/pricing/)
{{% /notice %}}
