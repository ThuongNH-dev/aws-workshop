---
title: "Worklog Tuần 2"
date: 2026-05-29
weight: 1
chapter: false
pre: " <b> 1.2. </b> "
---

### Mục tiêu tuần 2:

* Tìm hiểu kiến trúc mạng trên AWS thông qua Amazon VPC.
* Thực hành cấu hình các thành phần mạng cơ bản như Subnet, Route Table, Internet Gateway, NAT Gateway và Security Group.
* Tìm hiểu các phương thức kết nối mạng và dịch vụ cân bằng tải trên AWS.

### Các công việc cần triển khai trong tuần này:
| Thứ | Công việc                                                                                                                                                                                   | Ngày bắt đầu | Ngày hoàn thành | Nguồn tài liệu                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ------------ | ----------------------------------------- |
| 2   | - Tìm hiểu Amazon VPC và các khái niệm cơ bản:        <br>&emsp; + VPC  <br>&emsp; + CIDR Block <br>&emsp; + Available Zone  <br>&emsp; + Subnet <br> - Tìm hiểu Public Subnet và Private Subnet                                                                                      | 25/05/2026   | 25/05/2026      |<https://cloudjourney.awsstudygroup.com/> <br> <https://byvn.net/PcQc> | 
| 3   | - Tìm hiểu cơ chế định tuyến trong VPC: <br>&emsp; + Route Table <br>&emsp; + Internet Gateway <br>&emsp; + NAT Gateway <br> - **Thực hành:**    <br>&emsp; + Tạo VPC    <br>&emsp; + Tạo Public Subnet và Private Subnet  <br>&emsp; + Cấu hình Route Table                                | 26/05/2026   | 26/05/2026      | <https://cloudjourney.awsstudygroup.com/> <br> <https://byvn.net/PcQc>|
| 4   | - Tìm hiểu các thành phần mạng trong VPC:  <br>&emsp; + Elastic Network Interface (ENI)   <br>&emsp; + Elastic IP Address (EIP) <br>&emsp; + VPC Endpoint <br> - Tìm hiểu bảo mật mạng với Security Group và NACL <br> - **Thực hành:** <br>&emsp; + Cấu hình Security Group <br>&emsp; + Cấu hình Network ACL | 27/05/2026    | 27/05/2026       | <https://cloudjourney.awsstudygroup.com/> <br> <https://byvn.net/PcQc> |
| 5   | - Tìm hiểu VPC Flow Logs và giám sát lưu lượng mạng <br> - Tìm hiểu các phương thức kết nối mạng: <br>&emsp; + VPC Peering <br>&emsp; + Transit Gateway <br>&emsp; + Site-to-Site VPN <br>&emsp; + Client VPN  <br>&emsp; + Direct Connect           | 28/05/2026   | 28/05/2026      | <https://cloudjourney.awsstudygroup.com/> <br> <https://byvn.net/PcQc> |
| 6   | - Tìm hiểu Elastic Load Balancing (ELB) <br> - Phân biệt các loại Load Balancer: <br>&emsp; + Application Load Balancer (ALB) <br>&emsp; + Network Load Balancer (NLB) <br>&emsp; + Classic Load Balancer (CLB) <br>&emsp; + Gateway Load Balancer (GWLB) <br> - **Thực hành:** <br>&emsp; + Triển khai và kiểm thử Load Balancer                                                                                        | 29/05/2026   | 29/05/2026      | <https://cloudjourney.awsstudygroup.com/> <br> <https://byvn.net/PcQc> |


### Kết quả đạt được tuần 2:

* Hiểu được kiến trúc mạng cơ bản trên AWS và vai trò của Amazon VPC trong việc xây dựng môi trường mạng riêng biệt trên nền tảng đám mây.
* Nắm được các thành phần chính trong Amazon VPC:
  * VPC
  * Subnet
  * Route Table
  * Internet Gateway
  * NAT Gateway
  * VPC Endpoint

* Hiểu được cách thiết kế và triển khai Public Subnet và Private Subnet trong hệ thống mạng AWS.

* Hiểu cơ chế định tuyến và kết nối mạng trong AWS:
  * Route Table
  * Internet Gateway
  * NAT Gateway
  * Elastic Network Interface
  * Elastic IP Address

* Hiểu được các cơ chế bảo mật mạng trên AWS:
  * Security Group
  * Network Access Control List
  * VPC Flow Logs

* Nắm được các phương thức kết nối giữa các hệ thống mạng:
  * VPC Peering
  * AWS Transit Gateway
  * Site-to-Site VPN
  * Client VPN
  * AWS Direct Connect

* Tìm hiểu về Elastic Load Balancing và vai trò của cân bằng tải trong hệ thống
* Nắm được đặc điểm của các loại Load Balancer:
  * Application Load Balancer
  * Network Load Balancer
  * Classic Load Balancer
  * Gateway Load Balancer

* Hoàn thành các bài thực hành về VPC, Subnet, Route Table, Security Group, NACL và Load Balancer.
* Có khả năng xây dựng và quản lý một kiến trúc mạng AWS cơ bản đáp ứng yêu cầu kết nối, bảo mật và khả năng mở rộng.



