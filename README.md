# NonFunctionalTesting-JMeter
## Mô tả dự án
Bài tập này nhằm đánh giá hiệu suất của một trang web thương mại điện tử bằng công cụ Apache JMeter. Các kiểm thử bao gồm:
- Kiểm thử hiệu suất với 50 người dùng truy cập đồng thời trong 5 phút.
- Kiểm thử tải với số lượng người dùng tăng dần từ 10 → 50.
- Kiểm thử khả năng chịu tải bằng cách tiếp tục tăng lên 100 người dùng để xác định giới hạn của hệ thống.
## Thiết lập dự án
### Cài đặt Apache Jmeter
- Truy cập trang chủ: https://jmeter.apache.org/
- Tải phiên bản mới nhất của Apache JMeter.
- Cài đặt Java (JDK 8 hoặc cao hơn).
- Giải nén JMeter và chạy jmeter.bat (Windows).
### Cấu hình môi trường
- Thêm đường dẫn của thư mục bin vào PATH.
- Kiểm tra JMeter đã hoạt động bằng cách chạy lệnh:
```bash
jmeter -v
```
## Kiểm thử hiệu suất
- Kịch bản kiểm thử: 
  - Mô phỏng 50 người dùng đồng thời truy cập trang web.
  - Thời gian chạy kiểm thử: 5 phút.
  - Loại request: HTTP Request đến trang chủ của website.
  - Thu thập các chỉ số: Thời gian phản hồi trung bình, Throughput, và tỷ lệ lỗi.
- Kết quả: 

## Kiểm thử tải
- Kịch bản kiểm thử: 
  - Chạy kiểm thử với số lượng người dùng tăng dần từ 10 → 50.
  - Loại request: HTTP Request đến trang chủ của website.
  - 
- Kết quả:
  
## Kiểm thử khả năng chịu tải
- Kịch bản kiểm thử: 
  - Tiếp tục tăng số lượng người dùng từ 50 → 100 → 150
  - Loại request: HTTP Request đến trang chủ của website.
  - Quan sát thời điểm hệ thống bắt đầu giảm hiệu suất đáng kể
- Kết quả:
  
## Kết quả kiểm thử

## Một số câu hỏi thảo luận
1. Tại sao kiểm thử phi chức năng lại quan trọng trong phần mềm?
Kiểm thử phi chức năng quan trọng vì giúp đánh giá:
  - Tốc độ, tính ổn định và khả năng mở rộng của hệ thống.
  - Đảm bảo ứng dụng có thể đáp ứng số lượng người dùng lớn mà không bị sập.
  - Giúp phát hiện bottleneck và tối ưu hiệu suất hệ thống.
2. Các thông số quan trọng cần theo dõi trong kiểm thử hiệu suất là gì?
- Thời gian phản hồi trung bình (Average Response Time): Thời gian server phản hồi sau mỗi request.
- Tỷ lệ lỗi (Error Rate %): Phần trăm request bị lỗi.
- Throughput (Requests per Second): Số request hệ thống xử lý mỗi giây.
- CPU, RAM, Database Performance: Đánh giá mức độ sử dụng tài nguyên hệ thống.
3. Nếu hệ thống không đáp ứng yêu cầu hiệu suất, bạn sẽ đề xuất giải pháp gì?
- Tối ưu truy vấn database (sử dụng index, cache, connection pooling).
- Tối ưu backend (giảm tải API, sử dụng load balancing, microservices).
- Dùng CDN để giảm tải server.
- Tăng tài nguyên phần cứng (CPU, RAM, server scaling).
