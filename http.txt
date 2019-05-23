# HTTP 

## HTTP là gì?
HTTP (HyperText Transfer Protocol - Giao thức truyền tải siêu văn bản) là một trong các giao thức chuẩn về mạng Internet, được dùng để liên hệ thông tin giữa Máy cung cấp dịch vụ (Web server) và Máy sử dụng dịch vụ (Web client), là giao thức Client/Server dùng cho World Wide Web – WWW

## Sơ đồ hoạt động của HTTP 

<img src="https://images.viblo.asia/retina/7da268f1-718b-465c-87df-700e766df185.png">

HTTP hoạt động dựa trên mô hình Client – Server. Trong mô hình này, các máy tính của người dùng sẽ đóng vai trò làm máy khách (Client). Sau một thao tác nào đó của người dùng, các máy khách sẽ gửi yêu cầu đến máy chủ (Server) và chờ đợi câu trả lời từ những máy chủ này.
# Mô hình TCP/IP 

<img src="https://images.viblo.asia/retina/1596a7ea-09cc-4a36-82ac-48768e0cb24f.png">


Bộ giao thức TCP/IP là một bộ các giao thức truyền thông cài đặt chồng giao thức mà internet và hầu hết các mạng máy tính thương mại đang chạy trên đó. Bộ giao thức này được đặt tên theo hai giao thức chính của nó là TCP (Transmission Control Protocol - Giao thức điều khiển truyền vận) và IP (Internet Protocol - Giao thức Internet).

## Layer 1. Network Access Layer

` Network Access Layer ` xác định chi tiết về về cách thức dữ liệu được gửi qua mạng, bởi các thiết bị phần cứng trực tiếp giao tiếp với môi trường mạng, chẳng hạn như cáp đồng trục, cáp quang hay dây đồng xoắn đôi. Các giao thức bao gồm trong Network Access Layer là Ethernet, Token Ring, FDDI, X.25, Frame Relay ...vv

## Layer 2. Internet Layer

` Internet Layer ` đóng gói dữ liệu vào các gói dữ liệu được biết đến dưới dạng các gói tin thông giao thức Internet Protocol, chứa địa chỉ nguồn và đích (địa chỉ logic hoặc địa chỉ IP) được sử dụng để chuyển tiếp các gói tin giữa các máy chủ và qua các mạng.

## Layer 3. Transport Layer


Mục đích của Transport Layer là cho phép các thiết bị trên máy chủ nguồn và đích đến trao đổi dữ liệu. Transport Layer sẽ xác định mức độ service và trạng thái của kết nối được sử dụng khi vận chuyển dữ liệu. Trong đó có giao thức chính trong lớp Transport là TCP (Transmission Control Protocol). Sử dụng TCP, các ứng dụng trên các máy chủ được nối mạng có thể tạo các "kết nối" với nhau, mà qua đó chúng có thể trao đổi dữ liệu hoặc các gói tin. Giao thức này đảm bảo chuyển giao dữ liệu tới nơi nhận một cách đáng tin cậy và đúng thứ tự.

## Layer 4. Application Layer

Các thực thể của lớp Application cung cấp các ứng dụng cho phép người dùng trao đổi dữ liệu ứng dụng qua mạng

Một số ứng dụng thường gặp của chồng giao thức TCP/IP: FTP (File Transfer Protocol), DNS


