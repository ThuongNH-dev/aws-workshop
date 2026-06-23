---
title: "Blog 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---

# AWS WAF GIÚP SCALE TO WIN CHỐNG DDoS NHƯ THẾ NÀO?

Trong mùa bầu cử Tổng thống Mỹ năm 2024, Scale to Win đã phải đối mặt với nhiều cuộc tấn công DDoS có lưu lượng rất lớn. Để bảo vệ hệ thống, họ đã sử dụng Amazon CloudFront kết hợp với AWS WAF nhằm lọc và chặn lưu lượng độc hại trước khi truy cập vào hạ tầng bên trong.

## Những điểm nổi bật

* Sử dụng Amazon CloudFront và AWS WAF để lọc traffic ngay tại edge location.
* Cấu hình Application Load Balancer chỉ nhận request hợp lệ từ CloudFront.
* Sử dụng secret header để ngăn attacker truy cập trực tiếp vào ALB.
* Tách biệt traffic người dùng và traffic machine-to-machine để áp dụng chính sách bảo vệ phù hợp.
* Kết hợp Rate Limiting và CAPTCHA nhằm hạn chế các cuộc tấn công tự động.
* AWS WAF Bot Control hỗ trợ phát hiện hành vi tái sử dụng CAPTCHA token từ botnet.

![Blog Photo](/images/3-Blog/blog2-img.jpg)

## Kết quả đạt được

* Giảm đáng kể tác động của các cuộc tấn công DDoS.
* Ngăn chặn việc bypass CloudFront để tấn công trực tiếp vào hệ thống.
* Tăng cường khả năng bảo vệ ứng dụng trước lưu lượng độc hại.
* Duy trì khả năng phục vụ người dùng hợp lệ trong thời gian diễn ra tấn công.

## Điều bản thân rút ra

Theo em, bài viết cho thấy việc chống DDoS không chỉ đơn thuần là tăng tài nguyên hệ thống mà còn cần xây dựng kiến trúc bảo mật nhiều lớp. Việc kết hợp CloudFront, AWS WAF và các cơ chế kiểm soát traffic phù hợp giúp hệ thống an toàn và ổn định hơn trước các cuộc tấn công quy mô lớn.

## Tài liệu tham khảo

[Bài viết - Xem tại đây](https://www.facebook.com/groups/awsstudygroupfcj/permalink/2180420536056240/)
