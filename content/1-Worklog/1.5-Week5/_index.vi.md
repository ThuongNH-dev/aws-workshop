---
title: "Worklog Tuần 5"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.5. </b> "
---
### Mục tiêu tuần 5:

* Tìm hiểu mô hình trách nhiệm chia sẻ trong AWS Security.
* Tìm hiểu dịch vụ AWS Identity and Access Management (IAM).
* Thực hành quản lý người dùng, nhóm và phân quyền trong AWS.
* Tìm hiểu các cơ chế xác thực, phân quyền và quản lý khóa mã hóa trên AWS.
* Tìm hiểu các dịch vụ hỗ trợ quản trị tập trung và bảo mật trên AWS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                 | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                     |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------------------ |
| 2   | - Tìm hiểu Shared Responsibility Model trên AWS <br> - Tìm hiểu AWS IAM: <br>  + Root Account <br>  + IAM User <br>  + IAM Group <br>  + IAM Policy <br>  + IAM Role <br> - **Thực hành:** <br>  + Tạo IAM Group và IAM User <br>  + Tạo IAM Role <br>  + Assume Role                     | 15/06/2026   | 15/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| 3   | - Tìm hiểu cơ chế phân quyền trong IAM <br> - Tìm hiểu IAM Condition: <br>  + Giới hạn theo IP Address <br>  + Giới hạn theo thời gian truy cập <br> - **Thực hành:** <br>  + Tạo User quản trị EC2 <br>  + Tạo User quản trị RDS <br>  + Tạo Group quản trị <br>  + Cấu hình Switch Role | 16/06/2026   | 16/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| 4   | - Tìm hiểu Permission Boundary <br> - Tìm hiểu nguyên tắc Least Privilege <br> - **Thực hành:** <br>  + Tạo Policy giới hạn quyền <br>  + Tạo IAM User bị giới hạn quyền <br>  + Kiểm tra User bị giới hạn quyền                                                                          | 17/06/2026   | 17/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| 5   | - Tìm hiểu Access Key và AWS CLI Authentication <br> - Tìm hiểu IAM Role trên Amazon EC2 <br> - Tìm hiểu Amazon Cognito: <br>  + User Pool <br>  + Identity Pool <br> - **Thực hành:** <br>  + Sử dụng Access Key <br>  + Gán IAM Role cho EC2                                            | 18/06/2026   | 18/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| 6   | - Tìm hiểu AWS Organizations <br> - Tìm hiểu Service Control Policy (SCP) <br> - Tìm hiểu AWS Identity Center (SSO) <br> - Tìm hiểu AWS KMS và Customer Managed Key (CMK) <br> - Tìm hiểu AWS Security Hub và các tiêu chuẩn bảo mật AWS                                                  | 19/06/2026   | 19/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |

### Kết quả đạt được tuần 5:

* Hiểu được mô hình Shared Responsibility Model của AWS và phạm vi trách nhiệm giữa AWS với khách hàng.

* Hiểu được kiến trúc và cơ chế quản lý truy cập của AWS IAM.

* Nắm được các thành phần quan trọng của IAM:

  * Root Account
  * IAM User
  * IAM Group
  * IAM Policy
  * IAM Role

* Hiểu được nguyên tắc phân quyền tối thiểu (Least Privilege Principle).

* Hiểu được cơ chế Explicit Deny và thứ tự ưu tiên của IAM Policy.

* Nắm được cách sử dụng IAM Condition để kiểm soát quyền truy cập:

  * Giới hạn theo địa chỉ IP
  * Giới hạn theo thời gian truy cập

* Hiểu được cơ chế Assume Role và Switch Role trong AWS.

* Hiểu được mục đích và cách sử dụng Permission Boundary để giới hạn quyền tối đa của IAM User.

* Hiểu được cơ chế xác thực bằng Access Key và các rủi ro bảo mật liên quan.

* Hiểu được lợi ích của việc sử dụng IAM Role trên EC2 thay cho Access Key.

* Hiểu được chức năng của Amazon Cognito:

  * User Pool
  * Identity Pool

* Hiểu được cách quản lý nhiều AWS Account bằng AWS Organizations.

* Hiểu được vai trò của Service Control Policy (SCP) trong quản trị tập trung.

* Hiểu được cơ chế Single Sign-On thông qua AWS Identity Center.

* Hiểu được cách quản lý khóa mã hóa bằng AWS KMS và Customer Managed Key (CMK).

* Hiểu được chức năng giám sát và đánh giá bảo mật của AWS Security Hub.

* Hoàn thành các bài thực hành về:

  * Tạo IAM User và IAM Group
  * Tạo IAM Role và Assume Role
  * Tạo User quản trị EC2 và RDS
  * Cấu hình IAM Condition
  * Cấu hình Switch Role
  * Tạo Permission Boundary
  * Sử dụng Access Key
  * Gán IAM Role cho EC2

* Có khả năng thiết kế và triển khai mô hình quản lý danh tính và phân quyền phù hợp trên AWS.



