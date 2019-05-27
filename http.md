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


# DHCP 
` DHCP ` là giao thức cấp phát ip một cách tự động cùng với các cấu hình liên quan như subnet mask và gateưay và cung cấp database trung tâm để theo dõi tất cả máy tính trong hệ thống mạng tránh việc trùng lặp ip như cài đặt ip thủ công.


## Mô hình làm việc của DHCP 
<img src="https://techvccloud.mediacdn.vn/2018/10/9/photo-1-1539053199157968494441.png" >

Khi 1 thiết bị được bật và kết nối tới một mạng có máy chủ DHCP, thiết bị sẽ gửi yêu cầu tới máy chủ, và yêu cầu đó được gọi là yêu cầu DHCPDISCOVER.

Sau khi gói DISCOVER đến máy chủ DHCP, máy chủ sẽ tìm cách giữ lấy một địa chỉ IP mà thiết bị có thể sử dụng, và sau đó cung cấp cho client địa chỉ với một gói DHCPOFFER.

Sau khi cung cấp địa chỉ IP đã chọn, thiết bị sẽ phản hồi lại máy chủ DHCP với một gói DHCPREQUEST để chấp nhận yêu cầu, máy chủ sau đó sẽ gửi ACK để xác nhận thiết bị đã có địa chỉ IP cụ thể và xác định khoảng thời gian thiết bị có thể sử dụng địa chỉ đó trước khi nhận một địa chỉ mới.

# Subnet mask 
` Subnet mask ` gíup chia nhỏ mạng thành các mạng con và kết nối với nhau qua router.

# IP 
` Internet protocol ` là giao hướng gói dữ liệu sử dụng bởi các máy chủ nguồn và đích để truyền dữ liệu liên mạng chuyển mạch gói 

# DNS 
` Domain Name System ` là hệ thống thiết lập tương ứng giữ địa chỉ ip và tên miền giúp người đọc dễ nhớ hơn là những chữ số IP .


## Mô hình hoạt động của DNS 
<img scr="https://whitehat.vn/image/xenforo_image/1490892963Cac%20buoc%20truy%20van.png">
 
Giả sử máy tính muốn truy cập vào trang whitehat.vn 

Trước hết chương trình trên máy người sử dụng gửi yêu cầu tìm kiếm địa chỉ IP ứng với tên miền whitehat.vn tới máy chủ quản lý tên miền (name server) cục bộ thuộc mạng của nó.Máy chủ tên miền cục bộ này kiểm tra trong cơ sở dữ liệu của nó có chứa cơ sở dữ liệu chuyển đổi từ tên miền sang địa chỉ IP của tên miền mà người sử dụng yêu cầu không. Trong trường hợp máy chủ tên miền cục bộ có cơ sở dữ liệu này, nó sẽ gửi trả lại địa chỉ IP của máy có tên miền nói trên.Trong trường hợp máy chủ tên miền cục bộ không có cơ sở dữ liệu về tên miền này nó sẽ hỏi lên các máy chủ tên miền ở mức cao nhất ( máy chủ tên miền làm việc ở mức ROOT). Máy chủ tên miền ở mức ROOT này sẽ chỉ cho máy chủ tên miền cục bộ địa chỉ của máy chủ tên miền quản lý các tên miền có đuôi .VN.Máy chủ tên miền cục bộ gửi yêu cầu đến máy chủ quản lý tên miền có đuôi (.VN) tìm tên miền whitehat.vn. Máy chủ tên miền quản lý các tên miền.VN sẽ gửi lại địa chỉ của máy chủ quản lý tên miền whitehat.vnMáy chủ tên miền cục bộ sẽ hỏi máy chủ quản lý tên miền vnn.vn này địa chỉ IP của tên miền whitehat.vn. Do máy chủ quản lý tên miền vnn.vn có cơ sở dữ liệu về tên miền whitehat.vn nên địa chỉ IP của tên miền này sẽ được gửi trả lại cho máy chủ tên miền cục bộ. Máy chủ tên miền cục bộ chuyển thông tin tìm được đến máy của người sử dụng. Người sử dụng dùng địa chỉ IP này để kết nối đến server chứa trang web có địa chỉ whitehat.vn



# TCP - UDP 

| TCP | UDP |
|-----|-----|
| TCP có quá trình kiểm tra lỗi khi truyền tin nên độ tin cậy cao và không bị mất dữ liệu nhưng bị giới hạn thời gian chuyển gói tin vì khi bên chuyển nhận được xác nhận đã nhận gói tin thì mới tiếp tục chuyển tiếp | UDP không có quá trình kiểm tra lỗi khi truyền tin nên độ tin cậy là k có và không thể kiểm soát lỗi trong quá trình truyền tin nhưng bù lại được thời gian chuyển gói tin vì không cần xác nhận gói tin đã được nhận nên việc gửi gói tin theo UDP được gửi một cách liên tục |

