---
title: "Ứng dụng phân tán"
date: "2025-4-29"
updated: "2025-10-29"
categories:
  - "sveltekit"
  - "markdown"
  - "Ứng dụng phân tán" 
coverImage: "/images/jefferson-santos-fCEJGBzAkrU-unsplash.jpg"
coverWidth: 16
coverHeight: 9
excerpt: Định nghĩa về ứng dụng phân tán.
---

## Hệ thống phân tán là gì?

Hệ thống phân tán (Distributed System) là tập hợp các máy tính độc lập được kết nối qua mạng, phối hợp với nhau để đạt được một mục tiêu chung. Mỗi nút trong hệ thống có thể hoạt động độc lập nhưng được lập trình để phối hợp và chia sẻ tài nguyên, dữ liệu hoặc xử lý. Người dùng thường không nhận thấy rằng các thành phần của hệ thống được phân tán trên nhiều máy khác nhau.  
(*Nguồn: Wikipedia, Fiahub*)

## Các ứng dụng của hệ thống phân tán

Hệ thống phân tán được ứng dụng rộng rãi trong nhiều lĩnh vực:

- **Ngân hàng điện tử**: Xử lý giao dịch tài chính phân tán.
- **Thương mại điện tử**: Quản lý đơn hàng và thanh toán trên nhiều máy chủ.
- **Trò chơi trực tuyến nhiều người chơi (MMOGs)**: Đồng bộ trạng thái trò chơi giữa các máy chủ.
- **Hệ thống đặt vé máy bay**: Quản lý chỗ ngồi và thanh toán theo thời gian thực.
- **Mạng xã hội**: Lưu trữ và phân phối nội dung người dùng.
- **Hệ thống tệp phân tán**: Chia sẻ và lưu trữ tệp trên nhiều nút mạng.

## Các khái niệm chính của hệ thống phân tán

- **Scalability (Khả năng mở rộng)**: Khả năng hệ thống xử lý khối lượng công việc ngày càng tăng bằng cách thêm tài nguyên.
- **Fault Tolerance (Khả năng chịu lỗi)**: Khả năng hệ thống tiếp tục hoạt động ngay cả khi một số thành phần bị lỗi.
- **Availability (Tính sẵn sàng)**: Mức độ hệ thống luôn sẵn sàng phục vụ người dùng.
- **Transparency (Tính trong suốt)**: Người dùng không nhận thấy sự phức tạp của hệ thống phân tán.
- **Concurrency (Tính đồng thời)**: Khả năng xử lý nhiều tác vụ cùng lúc.
- **Parallelism (Tính song song)**: Thực hiện nhiều tác vụ đồng thời để tăng hiệu suất.
- **Openness (Tính mở)**: Khả năng tương tác với các hệ thống và thành phần khác.
- **Vertical Scaling (Mở rộng dọc)**: Tăng khả năng của một nút bằng cách thêm tài nguyên (CPU, RAM).
- **Horizontal Scaling (Mở rộng ngang)**: Thêm nhiều nút vào hệ thống để chia sẻ tải.
- **Load Balancer (Bộ cân bằng tải)**: Phân phối lưu lượng công việc đều giữa các nút.
- **Replication (Sao chép dữ liệu)**: Lưu trữ nhiều bản sao dữ liệu để tăng độ tin cậy và hiệu suất.

## Ví dụ và liên hệ với các thuật ngữ

**Ví dụ**: Một dịch vụ lưu trữ đám mây như *Amazon S3*.

- **Scalability**: Amazon S3 có thể mở rộng để xử lý hàng triệu yêu cầu đồng thời.
- **Fault Tolerance**: Dữ liệu được sao chép trên nhiều vùng để đảm bảo an toàn.
- **Availability**: Dịch vụ luôn sẵn sàng với thời gian hoạt động cao.
- **Transparency**: Người dùng không cần biết dữ liệu được lưu trữ ở đâu.
- **Concurrency**: Hệ thống xử lý nhiều yêu cầu từ người dùng cùng lúc.
- **Parallelism**: Dữ liệu được xử lý song song để tăng tốc độ.
- **Openness**: Amazon S3 hỗ trợ nhiều API và giao thức.
- **Horizontal Scaling**: Thêm nhiều máy chủ để xử lý tải tăng.
- **Load Balancer**: Phân phối yêu cầu đến các máy chủ khác nhau.
- **Replication**: Dữ liệu được sao chép để đảm bảo độ tin cậy.

## Kiến trúc của hệ thống phân tán

Các mô hình kiến trúc phổ biến:

- **Client-Server**: Máy khách gửi yêu cầu đến máy chủ để xử lý.
- **Three-Tier**: Gồm giao diện người dùng, logic ứng dụng và cơ sở dữ liệu.
- **N-Tier**: Mở rộng mô hình Three-Tier với nhiều lớp hơn.
- **Peer-to-Peer (P2P)**: Các nút hoạt động đồng thời như máy khách và máy chủ.
- **Microservices**: Ứng dụng được chia thành các dịch vụ nhỏ, độc lập.
- **Cell-Based Architecture**: Hệ thống được chia thành các "cell" độc lập để tăng khả năng chịu lỗi và mở rộng.

## Ví dụ

**Ví dụ**: Một hệ thống thương mại điện tử sử dụng kiến trúc Microservices.

- **Client-Server**: Người dùng tương tác với giao diện web (client) gửi yêu cầu đến máy chủ.
- **Three-Tier**: Giao diện người dùng, dịch vụ xử lý đơn hàng, và cơ sở dữ liệu.
- **Microservices**: Các dịch vụ như giỏ hàng, thanh toán, và quản lý sản phẩm hoạt động độc lập.
- **Load Balancer**: Phân phối yêu cầu đến các dịch vụ tương ứng.
- **Replication**: Dữ liệu sản phẩm được sao chép để đảm bảo tính sẵn sàng.
