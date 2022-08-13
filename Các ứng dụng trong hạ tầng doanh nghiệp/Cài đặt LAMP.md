# LAMP

- LAMP là viết tắt của Linux, Apache, MySQL và PHP (cũng có thể là Python, Perl nhưng bài này chỉ nói về Php), mỗi trong số đó là các gói phần mềm riêng lẻ được kết hợp để tạo thành một giải pháp máy chủ web linh hoạt. Các thành phần này, được sắp xếp theo các lớp hỗ trợ lẫn nhau, tạo thành các stack phần mềm

## I. Stack của LAMP

### 1. LAMP Stack là một bộ sofmware mã ngườn mở được sử dụng để phát triển ứng dụng web

![image](https://user-images.githubusercontent.com/105496635/184464022-08d4f413-0cfb-4e43-9a22-76fc83a85c92.png)

- Linux: là lớp đầu tiên trong stack. Hệ điều hành này là cơ sở nền tảng cho các lớp phần mềm khác.
- Apache đóng vai trò một HTTP server dùng để xử lý các yêu cầu gửi tới máy chủ.
- Mysql là cơ sở dữ liệu để lưu trữ mọi thông tin trên website.
- PHP sau đó sẽ xử lý các nhiệm vụ cần thiết hoặc kết nối với CSDL MySQL để lấy thông tin cần thiết sau đó trả về cho Apache. Apache cuối cùng sẽ trả kết quả nhận được về cho máy khách đã gửi yêu cầu tới.

### 2. Ưu điểm của LAMP stack
- LAMP stack gồm  4 thành phần, tất cả đều ví dụ Free and Open- Soucre Software (FOSS). VÌ chúng miễn phí dowload nên thu hút nhiều người sử dụng để tránh phải trả số tiền lớn khi phát triển web của họ
- Vì là FOSS, nên mã nguồn mở của somfware  đuọcư chia sẻ và có sẵn để mọi người thực hiện
- LAM stack được xem là một nền an toàn, vì nếu có lỗi phát sinh thì họ sẽ góp ý để khắc phục sớm nhất
- Điều khiến nó hấp dẫn là bạn có thể điều chỉnh stack và hoán đổi các thành phần Software mà nguồn mở khác để phù hợp với nhu cầu mình
 
### 3. LAMP Stack thay thế
Các lựa chọn thay thế nguồn mở:
- LEMP (Linux, NGINX, MySQL / MariaDB, PHP / Perl / Python)
- LAPP (Linux, Apache, PostgreSQL, PHP)
- LEAP (Linux, Eucalyptus, AppScale, Python)
- LLMP (Linux, Lighttpd, MySQL / MariaDB, PHP / Perl / Python)

Các lựa chọn thay thế không phải nguồn mở gồm:
- WAMP (Windows, Apache, MySQL / MariaDB, PHP / Perl / Python)
- WIMP (Windows, Dịch vụ thông tin Internet, MySQL / MariaDB, PHP / Perl / Python)
- MAMP (Mac OS x, Apache, MySQL / MariaDB, PHP / Perl / Python)

### 4. Cơ chế hoạt động các thành phần trong LAMP

#### 4.1 Sự hoạt động của Linux trong LAMP

Linux cũng đóng vai trò là một hệ điều hành.  Trong LAMP, Linux có vai trò là hệ điều hành mã nguồn mở, được cung cấp hoàn toàn miễn phí. Khi bạn tìm thấy một vài chương trình trong LAMP mà không thấy Linux như Suse, Redhat, Ubuntu,... thì đừng lo, Linux của bạn không hề thiếu vì những chương trình này chính là phiên bản
khác của Linux.

#### 4.2 Apache được hoạt đọng như thế nào
Apache nắm giữ vai trò là một phần mềm server web phổ biến nhất hiện nay Apache có thế mạnh về độ nhanh chóng khi truy cập và cực kỳ an toàn. Người dùng có thể tùy chỉnh nó để phục vụ cho mục đích hỗ trợ ngôn ngữ web như CGI, PHP, SSL, ASP

 #### 4.3 MySql 
 Đây là một mã nguồn mở vô cùng phổ biến, có lợi thế lớn từ độ hiệu suất cũng như mức độ uy tín cao, đem đến cho người dùng có thể dễ dàng sử dụng. MySQL đặc biệt tốt khi ứng dụng trên web, đây là một lý do quan trọng khiến cho nó trở nên đặc biệt hiệu quả trong LAMP.

#### 4.4  PHP hoạt động trong LAMP như thế nào?
PHP là ngôn ngữ kịch bản trong máy chủ và cũng được cập nhật một cách thường xuyên những kỹ thuật mới thông qua cơ chế vay mượn những tính năng tốt nhất từ các ngôn ngữ lập trình.


