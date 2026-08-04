---
title: "Event 3"
date: 2026-05-11
weight: 1
chapter: false
pre: " <b> 4.3. </b> "
---

# Bài thu hoạch: AWS AI Hackathon Project Showcase

## Mục Đích Của Sự Kiện

* Giới thiệu các dự án AI Agent được phát triển trong khuôn khổ AWS AI Hackathon.
* Chia sẻ cách ứng dụng AWS và Trí tuệ nhân tạo để giải quyết các bài toán thực tế của doanh nghiệp.
* Giúp sinh viên hiểu rõ hơn về quy trình thiết kế, xây dựng và triển khai các hệ thống AI trên nền tảng AWS.
* Giới thiệu các dịch vụ AWS hiện đại như Amazon Bedrock, AWS Lambda, Amplify và các dịch vụ Cloud Native khác.
* Tạo cơ hội học hỏi kinh nghiệm thực tế từ các đội thi và truyền cảm hứng cho sinh viên theo đuổi lĩnh vực Cloud Computing và AI Engineering.

## Danh Sách Diễn Giả

### Team One

* Trần Đông
* Đoàn Trung
* Mạnh Việt

### Team Two

* Hoàng Hiếu
* Quốc Hào
* Minh Quân
* Công Minh
* Trí Khiêm
* Tuấn Lực

### Team Three

* Phạm Tiến Thuận Phát
* Huỳnh Hoàng Long
* Lê Minh Nghĩa
* Trần Đại Vĩ
* Nguyễn An

### Team 3KA

* Huỳnh An Khương
* Nguyễn Quốc Huy
* Ngô Quang Khôi
* Hoàng Lê Thành Đức
* Đặng Nguyễn Phước Lộc
* Đặng Trường Hưng

### Team Four – Six Pillars Team

* Bùi Hoàng Việt
* Nguyễn Lâm Anh
* Nguyễn Văn Linh
* Nguyễn Cảnh Nguyên
* Nguyễn Minh Nhật
* Trần Phương Huyền

## Nội Dung Nổi Bật

### AI-Powered Conversational Ordering

Team One trình bày giải pháp AI Agent hỗ trợ khách hàng đặt món ăn trực tiếp thông qua các ứng dụng nhắn tin như Zalo và WhatsApp.

Một số nội dung nổi bật:

* Xây dựng hệ thống đặt hàng đa kênh (Multi-channel) bằng kiến trúc Channel Adapter.
* Cho phép khách hàng đặt món ngay trong cuộc trò chuyện mà không cần cài đặt thêm ứng dụng hoặc tạo tài khoản mới.
* Quy trình xử lý gồm các bước: Input → Normalize → Agent Core → Response.
* Xây dựng Dashboard để quản lý lịch sử hội thoại và hỗ trợ giám sát hoạt động của AI Agent.
* Thiết kế kiến trúc linh hoạt giúp dễ dàng mở rộng sang các nền tảng hoặc mô hình kinh doanh khác.

### AI Agent for Enterprise Strategy Intelligence

Team Two giới thiệu hệ thống AI Agent hỗ trợ thu thập và phân tích dữ liệu chiến lược của doanh nghiệp từ nhiều nguồn khác nhau.

Một số nội dung nổi bật:

* Tự động tổng hợp dữ liệu từ báo cáo tài chính, tài liệu doanh nghiệp và nhiều nguồn thông tin khác.
* Hiển thị kết quả trên Dashboard trực quan phục vụ đội ngũ quản trị và phân tích rủi ro.
* Xây dựng giao diện bằng React và triển khai trên AWS Amplify.
* Sử dụng AWS Lambda để điều phối các AI Sub-agent thông qua mô hình Agent-to-Agent (A2A).
* Amazon Bedrock được sử dụng để quản lý ngữ cảnh (Session Memory) cho AI Agent.

### Solution Architect Professional Native App

Team Three trình bày ứng dụng AI hỗ trợ các Solution Architect trong quá trình thiết kế hệ thống.

Các nội dung nổi bật:

* Phân tích yêu cầu của khách hàng bằng ngôn ngữ tự nhiên.
* Tự động sinh sơ đồ kiến trúc trên Draw.io.
* Hỗ trợ dự toán chi phí triển khai hạ tầng.
* Sinh mã Infrastructure as Code (CloudFormation hoặc Terraform).
* Nhấn mạnh vai trò của AI Engineering trong việc quản lý workflow, context và memory để tạo ra giải pháp phù hợp với yêu cầu doanh nghiệp.

### Hackathon Journey

Team 3KA chia sẻ hành trình tham gia AWS AI Hackathon và những bài học rút ra trong quá trình thực hiện dự án.

Một số nội dung nổi bật:

* Những khó khăn khi phát triển sản phẩm trong thời gian rất ngắn.
* Quá trình học và áp dụng các công nghệ AWS khi nhiều thành viên chưa có nhiều kinh nghiệm.
* Tầm quan trọng của tinh thần làm việc nhóm và sự phối hợp giữa các thành viên.
* Giá trị của việc học hỏi và trải nghiệm thực tế lớn hơn việc đạt giải thưởng.
* Khuyến khích sinh viên chủ động học tập và không ngại thử thách bản thân.

### Adaptive AML Workflow Engine

Six Pillars Team giới thiệu hệ thống AI hỗ trợ quy trình phát hiện và xử lý các giao dịch có dấu hiệu rửa tiền.

Các nội dung nổi bật:

* Sử dụng Machine Learning để đánh giá mức độ nghi ngờ của các giao dịch.
* AI Agent tự động thu thập dữ liệu và điều tra các giao dịch bất thường.
* Đưa ra các quyết định hỗ trợ như Hold, Dismiss hoặc Escalate.
* Sử dụng Amazon Bedrock Agent để điều phối các AI Sub-agent.
* Áp dụng cơ chế kiểm chứng chéo giữa các AI Agent kết hợp với Guardrails nhằm giảm hiện tượng Hallucination.
* Bảo vệ dữ liệu bằng các dịch vụ AWS IAM, AWS KMS và AWS Secrets Manager.

## Những Gì Học Được

### Kiến Thức Kỹ Thuật

* Hiểu cách xây dựng AI Agent hoạt động trên nhiều nền tảng giao tiếp khác nhau.
* Biết cách phối hợp nhiều AI Agent thông qua mô hình Agent-to-Agent.
* Hiểu vai trò của Amazon Bedrock trong việc quản lý ngữ cảnh và điều phối AI Workflow.
* Học được tầm quan trọng của AI Engineering, bao gồm quản lý workflow, context và memory.
* Hiểu thêm về cách ứng dụng AI và AWS trong các lĩnh vực như thương mại điện tử, phân tích chiến lược doanh nghiệp, thiết kế kiến trúc hệ thống và phòng chống rửa tiền.

### Kỹ Năng Và Tư Duy

* Nhận thấy việc giải quyết bài toán thực tế quan trọng hơn việc chỉ sử dụng các mô hình AI mạnh.
* Hiểu được tầm quan trọng của việc thiết kế kiến trúc hệ thống có khả năng mở rộng và dễ bảo trì.
* Nhận thức rõ vai trò của làm việc nhóm và giao tiếp hiệu quả trong quá trình phát triển phần mềm.
* Có thêm động lực để tiếp tục nghiên cứu AI Engineering và các dịch vụ AWS.

## Ứng Dụng Vào Công Việc Và Học Tập

* Tìm hiểu và thực hành Amazon Bedrock để xây dựng AI Agent.
* Nghiên cứu AWS Lambda và mô hình Serverless để phát triển các ứng dụng AI.
* Tìm hiểu thêm về Multi-Agent System và AI Workflow.
* Áp dụng các nguyên tắc thiết kế kiến trúc Cloud vào các dự án học tập và cá nhân.
* Tiếp tục nâng cao kiến thức về AWS và AI Engineering nhằm phục vụ định hướng nghề nghiệp trong tương lai.

## Trải Nghiệm Trong Event

Sự kiện mang đến nhiều dự án AI sáng tạo được xây dựng trên nền tảng AWS nhằm giải quyết các bài toán thực tế trong nhiều lĩnh vực khác nhau. Mỗi đội thi đều trình bày một hướng tiếp cận riêng, từ hệ thống đặt món ăn thông minh, nền tảng phân tích dữ liệu doanh nghiệp, công cụ hỗ trợ Solution Architect cho đến hệ thống phát hiện giao dịch rửa tiền bằng AI.

Điều em ấn tượng nhất là các nhóm không chỉ tập trung vào việc sử dụng các mô hình AI mà còn chú trọng đến cách thiết kế workflow, quản lý context, tối ưu kiến trúc hệ thống và đảm bảo tính bảo mật khi triển khai trên AWS. Những chia sẻ thực tế từ các đội thi giúp em hiểu rõ hơn về AI Engineering cũng như cách áp dụng các dịch vụ AWS vào việc xây dựng các giải pháp có tính ứng dụng cao.

#### Một số hình ảnh khi tham gia sự kiện

![Hình ảnh sự kiện](/images/4-Event/event-3-pic.JPG)

> Tổng thể, AWS AI Hackathon Project Showcase là một sự kiện bổ ích giúp em mở rộng kiến thức về AI Engineering, Amazon Bedrock và các dịch vụ AWS hiện đại. Bên cạnh những kiến thức kỹ thuật, em còn học được nhiều kinh nghiệm về tư duy giải quyết vấn đề, thiết kế kiến trúc hệ thống và làm việc nhóm thông qua các dự án thực tế.

