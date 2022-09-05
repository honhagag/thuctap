# Các giao thức

![image](https://user-images.githubusercontent.com/105496635/188404762-435d5fa5-b9a2-49d4-9123-5d0edaaf13a3.png)

## Có 4 loại giao thức chính mà quản trị Load Balancer có thể tạo quy định chuyển tiếp:
- HTTP: HTTP: dựa trên cơ chế HTTP chuẩn, HTTP Balancing đưa ra yêu cầu tác vụ. Load Balancer đặt X-Forwarded-For, X-Forwarded-Proto và tiêu đề X-Forwarded-Port cung cấp các thông tin backends về những yêu cầu ban đầu.

- HTTPS: các chức năng tương tự HTTP Balancing. HTTPS Balancing được bổ sung mã hóa và nó được xử lý bằng 2 cách: passthrough SSL duy trì mã hóa tất cả con đường đến backend hoặc: chấm dứt SSL, đặt gánh nặng giải mã vào load balancer và gửi lưu lượng được mã hóa đến backend.

- TCP: trong một số trường hợp khi ứng dụng web giao thức HTTP hoặc HTTPS, TCP sẽ là một giải pháp để cân bằng lưu lượng truy cập vào một cụm cơ sở dữ liệu . TCP sẽ giúp làn truyền lưu lượng trên máy chủ
- UDP: trong thời gian gần đây, Load BaLancer đã bổ sung thê, hỗ trợ cho cân bằng tải giao thức internet lõi như DNS và syslogd sử dụng UDp

Các quy tắc chuyển tiếp sẽ xác định loại hình thức và cồng vào Load Balancer để di chuyển đếnc các giao thức. Cổng Load Balancer lúc này được sử dụng để định tuyến lưu lượng trên backend








