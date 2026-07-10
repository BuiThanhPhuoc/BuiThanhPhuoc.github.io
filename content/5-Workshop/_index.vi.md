---
title: "Voice-Driven Construction Management System"
date: 2026-07-04
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

{{% notice note %}}
📌 **Info:** Bài viết tổng hợp dự án **Voice-Driven Construction Management System (VDCMS)** - hệ thống quản lý công trình tích hợp báo cáo bằng giọng nói và triển khai theo định hướng AWS.
{{% /notice %}}

# Voice-Driven Construction Management System

## Tổng quan

**Voice-Driven Construction Management System (VDCMS)** là hệ thống quản lý công trình được xây dựng để hỗ trợ quá trình quản lý dự án, giao việc, theo dõi tiến độ và ghi nhận báo cáo hiện trường. Điểm nổi bật của hệ thống là hỗ trợ kỹ sư tạo báo cáo bằng giọng nói, sau đó chuyển nội dung ghi âm thành văn bản để giảm thao tác nhập liệu thủ công.

Dự án được triển khai theo mô hình web application gồm frontend React/Vite, backend Node.js/Express, cơ sở dữ liệu MySQL và Socket.IO cho các chức năng thời gian thực. Khi đưa lên AWS, hệ thống được ánh xạ vào kiến trúc có CloudFront, S3, WAF, ALB, EC2, RDS MySQL, SQS, Transcribe, SES, Cognito, Secrets Manager, Systems Manager, CloudWatch và VPC.

## Mục tiêu của dự án

Mục tiêu chính của VDCMS là xây dựng một hệ thống quản lý công trình có thể sử dụng trong môi trường thực tế hơn so với một ứng dụng CRUD cơ bản. Hệ thống cần hỗ trợ phân quyền theo vai trò, quản lý dự án, giao việc, báo cáo tiến độ, quản lý tài liệu, xử lý sự cố, chat nội bộ và luồng báo cáo bằng giọng nói.

Thông qua dự án này, tôi có thể thực hành nhiều phần quan trọng trong quá trình phát triển phần mềm như phân tích yêu cầu, thiết kế database, xây dựng backend/frontend, xử lý xác thực, triển khai cloud, kiểm thử end-to-end và rà soát bảo mật cơ bản.

## Vai trò người dùng

Hệ thống gồm ba vai trò chính:

- **Admin:** quản trị người dùng, toàn bộ dự án, báo cáo, tài liệu và giám sát hoạt động trong hệ thống.
- **Manager:** quản lý các dự án được phân công, giao việc cho kỹ sư, theo dõi tiến độ, duyệt yêu cầu và xem báo cáo theo dự án.
- **Engineer:** xem công việc được giao, cập nhật checklist, gửi báo cáo tiến độ, ghi âm báo cáo, gửi yêu cầu gia hạn và báo cáo sự cố hiện trường.

Việc tách vai trò giúp hệ thống kiểm soát quyền truy cập rõ ràng hơn. Mỗi người dùng chỉ được thao tác trong phạm vi phù hợp với trách nhiệm của mình, ví dụ Manager chỉ làm việc trên dự án thuộc quyền quản lý và Engineer chỉ thao tác trên công việc được giao.

## Chức năng chính

Các chức năng chính của hệ thống bao gồm quản lý tài khoản, quản lý dự án, giao việc, theo dõi deadline, báo cáo tiến độ, checklist nghiệm thu, quản lý tài liệu, chat nội bộ, thông báo, xử lý sự cố và báo cáo bằng giọng nói.

Ở phía Engineer, hệ thống tập trung vào trải nghiệm sử dụng tại hiện trường. Người dùng có thể xem danh sách công việc, cập nhật trạng thái, gửi báo cáo kèm nội dung ghi âm, lưu nháp cục bộ và bổ sung hình ảnh hoặc thông tin liên quan đến sự cố. Ở phía Manager và Admin, hệ thống hỗ trợ theo dõi tiến độ, xem báo cáo, kiểm tra yêu cầu chờ duyệt và quản lý dữ liệu theo dự án.

## Kiến trúc kỹ thuật

Frontend được xây dựng bằng **React/Vite**, sử dụng React Router cho điều hướng và thiết kế giao diện riêng cho từng vai trò. Backend được xây dựng bằng **Node.js/Express**, kết nối **MySQL** để lưu dữ liệu nghiệp vụ và sử dụng **Socket.IO** cho các chức năng real-time như chat hoặc thông báo.

Khi triển khai trên AWS, frontend có thể được build và lưu trữ trên **Amazon S3**, sau đó phân phối qua **Amazon CloudFront**. Request từ người dùng đi qua **AWS WAF** và **Application Load Balancer** trước khi đến backend chạy trên **Amazon EC2** trong private subnet. Dữ liệu chính được lưu trong **Amazon RDS MySQL**, file và ghi âm được lưu private trên **Amazon S3**.

## Luồng xử lý giọng nói

Luồng báo cáo bằng giọng nói là phần quan trọng nhất của dự án. Engineer có thể ghi âm báo cáo tiến độ, sau đó hệ thống lưu file ghi âm vào S3 và tạo tác vụ xử lý trong database. Tác vụ này được đưa vào **Amazon SQS** để xử lý bất đồng bộ, giúp backend không phải chờ quá lâu khi người dùng gửi báo cáo.

Worker chạy trên EC2 nhận message từ SQS, gọi **Amazon Transcribe** để chuyển giọng nói tiếng Việt hoặc tiếng Anh thành văn bản, sau đó cập nhật kết quả về hệ thống. Nếu xử lý lỗi, message có thể được đưa vào Dead-Letter Queue để kiểm tra và xử lý lại. Cách làm này giúp luồng chuyển giọng nói thành văn bản ổn định hơn và phù hợp với môi trường production.

## Bảo mật và vận hành

VDCMS áp dụng nhiều điểm bảo mật cơ bản như phân quyền theo vai trò, lưu access token trong cookie HttpOnly, xoay vòng refresh token, thu hồi phiên đăng nhập khi đổi mật khẩu hoặc đăng xuất, giới hạn loại file upload và không trả secret ra frontend.

Ở tầng AWS, hệ thống định hướng đặt RDS trong private subnet, lưu file S3 ở chế độ private, sử dụng URL ký tạm thời cho media, dùng WAF để giảm rủi ro request bất thường, dùng Secrets Manager để quản lý thông tin nhạy cảm và Systems Manager để vận hành EC2 mà không cần mở SSH trực tiếp.

## Kết quả đạt được

Trong quá trình thực hiện, tôi đã phân tích yêu cầu nghiệp vụ, thiết kế database, xây dựng backend/frontend, hoàn thiện các luồng theo vai trò Admin, Manager và Engineer, đồng thời triển khai kiến trúc AWS cho hệ thống. Tôi cũng đã kiểm thử luồng end-to-end qua CloudFront, xử lý các lỗi liên quan đến WAF, S3 permission, Transcribe và xác nhận được khả năng chuyển giọng nói tiếng Việt thành văn bản.

Dự án giúp tôi hiểu rõ hơn cách kết hợp giữa phát triển ứng dụng web và triển khai cloud. Ngoài việc viết code, tôi học thêm được cách thiết kế kiến trúc, phân quyền, xử lý file, dùng hàng đợi cho tác vụ bất đồng bộ, cấu hình dịch vụ AWS và dọn dẹp tài nguyên sau khi kiểm thử để tránh phát sinh chi phí.

## Kết luận

Voice-Driven Construction Management System là dự án giúp tôi kết nối kiến thức lập trình web với các dịch vụ AWS trong một bài toán gần với thực tế. Hệ thống không chỉ quản lý dự án và công việc, mà còn hỗ trợ báo cáo hiện trường bằng giọng nói, giúp quá trình nhập liệu thuận tiện hơn. Qua dự án này, tôi có thêm kinh nghiệm về React, Express, MySQL, Socket.IO, AWS deployment, xử lý bất đồng bộ và bảo mật hệ thống. Đây là nền tảng quan trọng để tôi tiếp tục phát triển các project cloud có tính ứng dụng cao hơn trong tương lai.
