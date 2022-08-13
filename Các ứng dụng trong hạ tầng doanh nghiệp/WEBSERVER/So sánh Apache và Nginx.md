*Đây là so sánh cách đây 2 năm về trước*
![image](https://user-images.githubusercontent.com/105496635/184299155-1785150b-c699-4d45-8ecc-76a3d6e934dc.png)

## So sánh về Nginx và Apache 
### 1. Hiệu suất:
#### 1.1 Web tĩnh
![image](https://user-images.githubusercontent.com/105496635/184299787-fd3296fa-2530-4500-8d49-7b30ee675377.png)

Nginx có khả năng kết nối gấp 2,5 lần thử nghiệm chuẩn tới 1000 kết nối đòng thời

#### 1.2 Web động

![image](https://user-images.githubusercontent.com/105496635/184300133-e3b053f7-16be-4966-ac92-b9da55a7e7e9.png)

Nếu bạn đã có một trang web động bằng WordPress, Joomla, Drupal, ... bạn có thể cân nhắc sử dụng NGINX hoặc Apache. Nội dung tĩnh trong các tình huống này ít hơn rất nhiều so với nội dung động.

### 1.2 Hệ điều hành hỗ trợ

![image](https://user-images.githubusercontent.com/105496635/184300449-c71448a4-8708-443c-b644-0b052f50f74b.png)

- Apache hoạt động trên tất cả hệ điều hành Linux và hỗ trợ đầy đủ cho Microsoft Windows 
- Nginx cũng chạy trên tất cả hệ thống trong số chúng và cũng hỗ trợ Window nhưng hiệu xuất không bằng

### 1.3 Bảo mật

Nginx và Apache rất cói trọng việc bảo mật. Không có hệ thống nào mạnh mẽ mà lại không có những biện pháp tấn công ddos

### 1.4 Hỗ trợ tài liệu

![image](https://user-images.githubusercontent.com/105496635/184301961-e9d21770-6995-4ff8-b102-8aafc7106e52.png)

Apache sở hữu mạng lưới hỗ trợ cộng đồng lớn thông qua mailing lists, IRC và Stack Overflow. Ngoài ra, còn có tùy chọn hỗ trợ bên thứ ba từ OpenLogic.

Tương tự, Nginx cũng có hỗ trợ thông qua mailing lists, IRC và Stack Overflow. Nginx còn có một sản phẩm có tên Nginx + có hỗ trợ riêng của Google bao gồm nhiều tính năng hơn.

Cả Nginx và Apache đều cung cấp tài liệu, bao gồm hầu hết mọi chủ đề và tính năng cần thiết. Tài liệu này bao gồm release notes, user guides, tutorials... Nginx thậm chí có wiki riêng!

### 1.5 Tính linh hoạt

Một máy chủ web phải đủ linh hoạt để cho phép các tùy chỉnh. Apache làm điều đó khá tốt, thông qua việc sử dụng các công cụ .htaccess mà Nginx không hỗ trợ. Nó cho phép phân cấp nhiệm vụ admin. Admin bên thứ ba và admin cấp hai có thể bị ngăn truy cập vào máy chủ chính. Hơn nữa, Apache hỗ trợ hơn 60 mô-đun, giúp nó có khả năng mở rộng cao. Đó là lý do tại sao Apache phổ biến hơn với các nhà cung cấp dịch vụ hosting chia sẻ.
