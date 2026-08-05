---
title: "Worklog Tuần 3"
date: 2026-05-18
weight: 1
chapter: false
pre: " <b> 1.3. </b> "
---

### Mục tiêu tuần 3:

* Tìm hiểu dịch vụ máy chủ ảo Amazon EC2 và các thành phần liên quan.
* Tìm hiểu cơ chế khởi tạo và quản lý EC2 Instance thông qua Amazon Machine Image (AMI).
* Tìm hiểu các giải pháp lưu trữ dành cho EC2 như Elastic Block Store (EBS) và Instance Store.
* Tìm hiểu cơ chế sao lưu dữ liệu, xác thực truy cập và tự động mở rộng hệ thống trên AWS.

### Các công việc cần triển khai trong tuần này:

| Thứ | Công việc                                                                                                                                                                                                                                                                                                           | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                                                     |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ------------------------------------------------------------------ |
| 2   | - Tìm hiểu Amazon Elastic Compute Cloud (EC2) và các khái niệm cơ bản: <br>  + EC2 Instance <br>  + Elasticity <br>  + Instance Type <br>  + CPU / GPU <br>  + Memory <br>  + Network <br>  + Storage                                                                                                               | 01/06/2026   | 01/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| 3   | - Tìm hiểu kiến trúc EC2: <br>  + Hardware Node <br>  + Hypervisor <br>  + Nitro System <br>  + HVM <br>  + Paravirtualization (PV) <br> - Tìm hiểu Amazon Machine Image (AMI): <br>  + Root Volume <br>  + Permission <br>  + Block Device Mapping                                                                 | 02/06/2026   | 02/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| 4   | - Tìm hiểu Snapshot và cơ chế Backup EC2 <br> - Tìm hiểu Key Pair và cơ chế xác thực EC2 <br>  + Public Key <br>  + Private Key <br>  + SSH <br>  + Remote Desktop <br> - **Thực hành:** <br>  + Tạo EC2 Instance <br>  + Tạo Key Pair                                                                              | 03/06/2026   | 03/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| 5   | - Tìm hiểu Elastic Block Store (EBS): <br>  + SSD Volume <br>  + HDD Volume <br>  + EBS Snapshot <br>  + EBS Multi-Attach <br>  + Backup dữ liệu lên Amazon S3 <br> - Tìm hiểu Instance Store: <br>  + NVMe Storage <br>  + Temporary Storage <br> - So sánh EBS và Instance Store                                  | 04/06/2026   | 04/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |
| 6   | - Tìm hiểu User Data và Metadata <br>  + User Data Script <br>  + EC2 Metadata <br> - Tìm hiểu EC2 Auto Scaling <br>  + Scale Out <br>  + Scale In <br>  + Tích hợp Elastic Load Balancer <br> - Tìm hiểu các dịch vụ AWS liên quan: <br>  + Amazon Lightsail <br>  + Amazon EFS <br>  + Amazon FSx <br>  + AWS MGN | 05/06/2026   | 05/06/2026      | https://cloudjourney.awsstudygroup.com/ <br> https://byvn.net/PcQc |

### Kết quả đạt được tuần 3:

* Hiểu được vai trò của Amazon EC2 trong việc triển khai và vận hành ứng dụng trên nền tảng AWS.

* Nắm được các thành phần cấu hình của EC2 Instance:

  * CPU / GPU
  * Memory
  * Network
  * Storage

* Hiểu được kiến trúc hoạt động của EC2:

  * Hardware Node
  * Hypervisor
  * Nitro System
  * HVM
  * Paravirtualization (PV)

* Hiểu được chức năng và cách sử dụng Amazon Machine Image (AMI):

  * Root Volume
  * Permission
  * Block Device Mapping

* Hiểu được cơ chế khởi tạo nhiều EC2 Instance từ một AMI.

* Nắm được cơ chế sao lưu dữ liệu bằng Snapshot và khả năng khôi phục hệ thống từ bản sao lưu.

* Hiểu được cơ chế xác thực và bảo mật khi truy cập EC2 thông qua:

  * Public Key
  * Private Key
  * Key Pair

* Nắm được đặc điểm và cách sử dụng Elastic Block Store (EBS):

  * SSD Volume
  * HDD Volume
  * Snapshot
  * EBS Multi-Attach

* Hiểu được sự khác biệt giữa:

  * Elastic Block Store (EBS)
  * Instance Store

* Hiểu được ưu điểm và hạn chế của từng loại lưu trữ để lựa chọn phù hợp với nhu cầu sử dụng.

* Hiểu được vai trò của User Data trong việc tự động cấu hình EC2 khi khởi tạo.

* Nắm được khái niệm Metadata và các thông tin quản lý liên quan đến EC2 Instance.

* Hiểu được cơ chế tự động mở rộng hệ thống bằng EC2 Auto Scaling:

  * Tự động tăng số lượng EC2 Instance khi tải tăng.
  * Tự động giảm số lượng EC2 Instance khi tải giảm.
  * Tích hợp với Elastic Load Balancer để phân phối lưu lượng truy cập.

* Tìm hiểu thêm một số dịch vụ AWS liên quan:

  * Amazon Lightsail
  * Amazon EFS
  * Amazon FSx
  * AWS Application Migration Service (MGN)

* Hoàn thành các bài thực hành về tạo EC2 Instance, Key Pair và quản lý lưu trữ trên AWS.

* Có khả năng lựa chọn cấu hình EC2, phương thức lưu trữ và giải pháp mở rộng phù hợp cho từng nhu cầu triển khai ứng dụng trên nền tảng AWS.


