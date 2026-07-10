---
title: "Workshop"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# Truy cập Amazon S3 an toàn trong mô hình hybrid bằng VPC Endpoint

#### Tổng quan

Workshop này tập trung vào cách truy cập **Amazon S3** theo đường riêng tư từ workload trên AWS và môi trường on-premises mô phỏng thông qua **VPC Endpoint**. Bài lab giúp làm rõ vì sao private connectivity quan trọng khi workload cần truy cập dịch vụ AWS mà không đưa traffic đi qua public internet.

**AWS PrivateLink** cung cấp kết nối riêng tư giữa VPC, các dịch vụ AWS được hỗ trợ và mạng on-premises. Trong workshop này, hai mô hình endpoint được sử dụng:

* **Gateway VPC Endpoint:** Dùng để truy cập Amazon S3 riêng tư từ tài nguyên trong VPC thông qua cấu hình route table.
* **Interface VPC Endpoint:** Dùng để truy cập riêng tư thông qua endpoint network interface và DNS resolution, phù hợp với các tình huống nâng cao hoặc hybrid connectivity.

Thông qua bài lab, tôi đã thực hành triển khai môi trường, tạo endpoint, kiểm thử truy cập S3, rà endpoint policy, kiểm tra hành vi DNS và dọn dẹp tài nguyên sau khi hoàn tất.

#### Nội dung

1. [Tổng quan về workshop](5.1-Workshop-overview/)
2. [Chuẩn bị](5.2-Prerequiste/)
3. [Truy cập S3 từ VPC](5.3-S3-vpc/)
4. [Truy cập S3 từ môi trường on-premises mô phỏng](5.4-S3-onprem/)
5. [VPC Endpoint Policies (Bonus)](5.5-Policy/)
6. [Dọn dẹp tài nguyên](5.6-Cleanup/)
