---
title: "Worklog Tuần 4"
date: 2026-05-18
weight: 1
chapter: false
pre: " <b> 1.4. </b> "
---

### Mục tiêu tuần 4:

* Tìm hiểu dịch vụ lưu trữ đối tượng Amazon S3 và các thành phần liên quan.
* Tìm hiểu các giải pháp lưu trữ dữ liệu, sao lưu và phục hồi trên AWS.
* Tìm hiểu các phương pháp tối ưu chi phí lưu trữ và chiến lược Disaster Recovery.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                                                                                                                 | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                     |
| --- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------------------ |
| 2   | - Tìm hiểu Amazon Simple Storage Service (S3): <br>  + Bucket <br>  + Object <br>  + Object Key <br>  + Multipart Upload <br>  + Event Notification <br>  + Access Point <br> - **Thực hành:** <br>  + Tạo S3 Bucket <br>  + Upload dữ liệu lên Amazon S3                                                                                                                                                 | 08/06/2026   | 08/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| 3   | - Tìm hiểu các lớp lưu trữ của Amazon S3: <br>  + S3 Standard <br>  + S3 Standard-IA <br>  + S3 Intelligent-Tiering <br>  + S3 One Zone-IA <br>  + Glacier <br>  + Deep Archive <br> - Tìm hiểu Lifecycle Policy và cơ chế quản lý vòng đời dữ liệu                                                                                                                                                       | 09/06/2026   | 09/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| 4   | - Tìm hiểu Static Website Hosting trên Amazon S3 <br> - Tìm hiểu CORS (Cross-Origin Resource Sharing) <br> - Tìm hiểu cơ chế kiểm soát truy cập: <br>  + ACL <br>  + Bucket Policy <br>  + IAM Policy <br> - Tìm hiểu VPC Endpoint và S3 Versioning                                                                                                                                                       | 10/06/2026   | 10/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| 5   | - Tìm hiểu các giải pháp lưu trữ và di chuyển dữ liệu: <br>  + Snowball <br>  + Snowball Edge <br>  + Snowmobile <br> - Tìm hiểu AWS Storage Gateway: <br>  + File Gateway <br>  + Volume Gateway <br>  + Tape Gateway <br> - **Thực hành:** <br>  + Tạo Storage Gateway <br>  + Cấu hình File Sharing                                                                                                    | 11/06/2026   | 11/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| 6   | - Tìm hiểu Disaster Recovery trên AWS: <br>  + RTO (Recovery Time Objective) <br>  + RPO (Recovery Point Objective) <br>  + Backup & Restore <br>  + Pilot Light <br>  + Low Capacity Active <br>  + Full Capacity Active <br> - Tìm hiểu AWS Backup: <br>  + Backup Plan <br>  + Notification <br>  + Backup Monitoring <br> - **Thực hành:** <br>  + Tạo Backup Plan <br>  + Kiểm tra hoạt động sao lưu | 12/06/2026   | 12/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |

### Kết quả đạt được tuần 4:

* Hiểu được kiến trúc lưu trữ đối tượng của Amazon S3 và cách tổ chức dữ liệu bằng Bucket và Object.

* Nắm được các tính năng quan trọng của Amazon S3:

  * Object Key
  * Multipart Upload
  * Event Notification
  * Access Point

* Hiểu được các lớp lưu trữ của Amazon S3:

  * S3 Standard
  * S3 Standard-IA
  * S3 Intelligent-Tiering
  * S3 One Zone-IA
  * Glacier
  * Deep Archive

* Hiểu được cơ chế Lifecycle Policy và cách tối ưu chi phí lưu trữ dữ liệu.

* Nắm được cách triển khai Static Website Hosting trên Amazon S3.

* Hiểu được cơ chế hoạt động của CORS và các trường hợp sử dụng trong ứng dụng web.

* Hiểu được các phương pháp kiểm soát truy cập dữ liệu trên Amazon S3:

  * ACL
  * Bucket Policy
  * IAM Policy

* Hiểu được vai trò của VPC Endpoint trong việc truy cập Amazon S3 thông qua mạng nội bộ AWS.

* Nắm được cơ chế Versioning và khả năng khôi phục dữ liệu khi bị xóa hoặc ghi đè ngoài ý muốn.

* Hiểu được các giải pháp di chuyển dữ liệu quy mô lớn:

  * Snowball
  * Snowball Edge
  * Snowmobile

* Hiểu được kiến trúc lưu trữ Hybrid thông qua AWS Storage Gateway:

  * File Gateway
  * Volume Gateway
  * Tape Gateway

* Hiểu được các khái niệm quan trọng trong Disaster Recovery:

  * Recovery Time Objective (RTO)
  * Recovery Point Objective (RPO)

* Nắm được các chiến lược khôi phục sau thảm họa trên AWS:

  * Backup & Restore
  * Pilot Light
  * Low Capacity Active
  * Full Capacity Active

* Hiểu được cách quản lý và giám sát các tác vụ sao lưu bằng AWS Backup.

* Hoàn thành các bài thực hành về:

  * Tạo S3 Bucket
  * Upload dữ liệu lên Amazon S3
  * Host Static Website trên S3
  * Tạo Storage Gateway
  * Tạo Backup Plan
  * Kiểm tra hoạt động sao lưu

* Có khả năng lựa chọn giải pháp lưu trữ, sao lưu và phục hồi dữ liệu phù hợp với từng nhu cầu triển khai trên AWS.

